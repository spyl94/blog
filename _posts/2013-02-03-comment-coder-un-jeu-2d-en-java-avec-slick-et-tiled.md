---
id: 407
title: Comment coder un jeu 2d en Java avec Slick et Tiled ?
date: 2013-02-03T16:00:01+00:00
author: spyl94
layout: post
guid: http://blog.spyl.net/?p=407
permalink: /2013/02/comment-coder-un-jeu-2d-en-java-avec-slick-et-tiled/
categories:
  - Non classé
---
Je vais prendre pour exemple [Drasus](https://github.com/spyl94/drasus), jeu réalisé comme projet du cours de programmation Java à l&rsquo;Efrei. Celui-ci ne peut se jouer qu&rsquo;en multijoueur en réseau, cependant s&rsquo;il n&rsquo;y a pas d&rsquo;autres joueurs présents sur le serveur du jeu, vous pouvez toujours le tester en lançant deux fois le client. Pour plus d&rsquo;information referez-vous au [wiki de drasus](https://github.com/spyl94/drasus/wiki). Le jeu étant open source, vous pouvez vous tout à fait lire ou réutiliser le code.

Commencez par importer Slick à votre projet comme indiqué sur le [wiki de slick](http://www.slick2d.org/wiki/index.php/Main_Page) ainsi qu&rsquo;à lire les quelques exemples de code afin de comprendre son fonctionnement. Nous allons utiliser une architecture  MVC pour Model, View, Controller, que je vous invite à utiliser en séparant votre code dans différents packages.

<pre class="lang:java decode:true">import org.newdawn.slick.AppGameContainer;
import org.newdawn.slick.SlickException;	

//...

try {
	app = new AppGameContainer(new ViewController());
	app.setShowFPS(false);
	app.setDisplayMode(1280, 704, false);
	app.start();
} catch (SlickException e) {
	e.printStackTrace();
}</pre>

La classe ViewController va contenir les différents états de notre jeu, afin de différencier le menu, le jeu en lui-même, les statistiques de fin, etc.

<pre class="lang:java decode:true" title="ViewController">package controller;

import org.newdawn.slick.GameContainer;
import org.newdawn.slick.SlickException;
import org.newdawn.slick.state.StateBasedGame;

import view.GamePlayState;
import view.LoseState;
import view.MainMenuState;
import view.VictoryState;

public class ViewController extends StateBasedGame {

    public static final int MAINMENUSTATE = 0;
    public static final int GAMEPLAYSTATE = 1;
    public static final int VICTORYSTATE = 2;
    public static final int LOSESTATE = 3;

    public ViewController() {
		super("Drasus"); // Texte affiché comme titre de la fenêtre
    }

    @Override
    public void initStatesList(GameContainer gameContainer)
	throws SlickException {
		// Le premier ajouté à la liste est le premier à être lancé
		this.addState(new MainMenuState(MAINMENUSTATE));
		this.addState(new GamePlayState(GAMEPLAYSTATE));
		this.addState(new VictoryState(VICTORYSTATE));
		this.addState(new LoseState(LOSESTATE));
    }
}</pre>

Voici un exemple simplifié de menu :

<pre class="lang:java decode:true" title="MainMenuState">package view;

import org.newdawn.slick.GameContainer;
import org.newdawn.slick.Image;
import org.newdawn.slick.Input;
import org.newdawn.slick.SlickException;
import org.newdawn.slick.state.BasicGameState;
import org.newdawn.slick.state.StateBasedGame;

import controller.MainController;
import controller.ViewController;

public class MainMenuState extends BasicGameState {

	private int stateID = -1;
	private MainController main;

	private Image background = null;
	private Image startGame = null;
	private int mouseX = 0;
	private int mouseY = 0;
	private boolean insideStartGame = false;

	public MainMenuState(int stateID) {
		this.stateID = stateID;
	}

	@Override
	public int getID() {
		return stateID;
	}

	/**
	* Send the position of the mouse when it clicked.
	*
	* @param gc
	* gc is the game container created by slick
	*/
	private void getPosClicked(GameContainer gc) {
		Input input = gc.getInput();
		if (input.isMousePressed(0)) {
			mouseX = input.getMouseX();
			mouseY = input.getMouseY();
		}
	}

	@Override
	public void init(GameContainer gc, StateBasedGame sbg)
	throws SlickException {
		background = new Image("res/menu/drasus.png");
		startGame = new Image("res/menu/jouer.png");
	}

	@Override
	public void render(GameContainer arg0, StateBasedGame arg1, Graphics arg2)
	throws SlickException {
		background.draw(0, 0);
		startGame.draw(530, 500);
	}

	@Override
	public void update(GameContainer gc, StateBasedGame sbg, int delta)
	throws SlickException {
		getPosClicked(gc);

		if (insideStartGame)
			sbg.enterState(ViewController.GAMEPLAYSTATE);

		if ((mouseX &gt; 530 && mouseX &lt; startGame.getWidth() + 530)
		&& (mouseY &gt;= 500 && mouseY &lt;= startGame.getHeight() + 500)) {
			insideStartGame = true;
		}
	}
}</pre>

Avant de créer notre GamePlayState nous allons voir comment récupérer notre TiledMap avec Slick :

<pre class="lang:default decode:true" title="TiledMap">TiledMap map = new TiledMap("res/testMap.tmx");</pre>

C&rsquo;est très simple ! Cependant il nous reste à récupérer les propriétés des Tiles que nous avons ajouté dans Tiled. Pour cela commençons par créer une classe Tile qui contiendra les coordonnées de la case sur la carte ainsi qu&rsquo;un booléen blocked pour savoir si le Tile est bloqué ou non et une énumération Field afin de récupérer le type du terrain.

<pre class="lang:default decode:true" title="La class Tile qui représente une case du jeu">package view;

public class Tile {

    public enum FIELD {
        DEFAULT, GRASS, FOREST, MOUNTAIN, BRIDGE, FORT
    }

    // let public for easier use
    public final int x;
    public final int y;

    private FIELD field;
    private boolean blocked;

    public Tile(int x, int y, boolean block, FIELD field) {
        this.x = x;
        this.y = y;
        this.blocked = block;
        this.field = field;
    }

    @Override
    public boolean equals(Object o) {
        if (this == o) return true;
        if (!(o instanceof Tile)) return false;
        Tile t = (Tile) o;
        return this.x == t.x && this.y == t.y;
    }

    /**
    * Returns the field of the Tile.
    *
    * @return the field.
    */
    public FIELD getField() {
        return field;
    }

    /**
    * Returns is the Tile is blocked or not.
    *
    * @return true if blocked false otherwise
    */
    public boolean isBlocked() {
        return blocked;
    }

}</pre>

Pour Drasus nous n&rsquo;utilisons qu&rsquo;une seule couche de Tiles, nous allons donc représenter notre carte du jeu par un simple vector de Tile, voici comment récupérer nos différents Tile et ainsi la carte du jeu :

<pre class="lang:java decode:true">package view;

//import ...

import view.Tile.FIELD;
import controller.ViewController;

public class GamePlayState extends BasicGameState {

	private TiledMap grassMap;
	private Vector&lt;Tile&gt; tiles;
	private int stateID;

	public GamePlayState(int stateID) {
		this.stateID = stateID;
		tiles = new Vector&lt;Tile&gt;();
	}

	@Override
	public int getID() {
		return stateID;
	}

	@Override
	public void init(GameContainer gc, StateBasedGame sbg)
	throws SlickException {
		grassMap = new TiledMap("res/drasus.tmx");

		for (int xAxis = 0; xAxis &lt; grassMap.getWidth(); xAxis++) {
			for (int yAxis = 0; yAxis &lt; grassMap.getHeight(); yAxis++) {
				int tileID = grassMap.getTileId(xAxis, yAxis, 0);
				boolean block = false;

				String value = grassMap.getTileProperty(tileID, "blocked","false");
				if ("true".equals(value)) block = true;

				value = grassMap.getTileProperty(tileID, "field", "default");
				switch (value) {
					case "default":
					tiles.addElement(new Tile(xAxis, yAxis, block, FIELD.DEFAULT));
					break;
					case "grass":
					tiles.addElement(new Tile(xAxis, yAxis, block, FIELD.GRASS));
					break;
					case "forest":
					tiles.addElement(new Tile(xAxis, yAxis, block, FIELD.FOREST));
					break;
					case "mountain":
					tiles.addElement(new Tile(xAxis, yAxis, block, FIELD.MOUNTAIN));
					break;
					case "fort":
					tiles.addElement(new Tile(xAxis, yAxis, block, FIELD.FORT));
					break;
					case "bridge":
					tiles.addElement(new Tile(xAxis, yAxis, block, FIELD.BRIDGE));
					break;
					default:
					break;
				}
			}
		}
	}

	// ...
}</pre>

Pour afficher la carte, ajoutez simplement :

<pre class="lang:java decode:true">@Override
public void render(GameContainer gc, StateBasedGame sbg, Graphics arg2)
throws SlickException {
	grassMap.render(0, 0);
}</pre>

Pour que notre jeu <span style="color: #000000;">fonctionne, </span>il faut ensuite le décomposer en plusieurs états, pour cela utilisons une énumération d&rsquo;états :

<pre class="lang:java decode:true">private enum STATES {
		START_GAME, NEW_UNIT, START_TURN, PLAY_TURN, END_TURN, SELECTING_UNIT, PAUSE_GAME, GAME_OVER
	}
	private STATES currentState = null;

	// Le jeu commence à l'état START_GAME
	public GamePlayState(int stateID) {
		this.stateID = stateID;
		currentState = STATES.START_GAME;
		tiles = new Vector&lt;Tile&gt;();
	}

	// Exemple d'utilisation dans drasus...
	@Override
	public void update(GameContainer gc, StateBasedGame sbg, int delta)
	throws SlickException {
		switch (currentState) {
			case START_GAME:
				startGame();
				currentState = STATES.NEW_UNIT;
				break;
			case NEW_UNIT:
				newUnit(gc, sbg, delta);
				break;
			case START_TURN:
				initTurn(sbg);
				currentState = STATES.PLAY_TURN;
			case PLAY_TURN:
				playTurn(gc, sbg, delta);
				break;
			case SELECTING_UNIT:
				selectingUnit(gc, sbg, delta);
				break;
			case END_TURN:
				endTurn();
				break;
			case GAME_OVER:
				sbg.enterState(ViewController.MAINMENUSTATE);
				break;
		}

	}</pre>

Vous avez désormais toutes les clés en main pour réaliser le jeu que vous souhaitez&#8230;
  
Voici en bonus une fonction permettant de récupérer le Tile sur lequel un utilisateur a cliqué :

<pre class="lang:java decode:true">/**
* Returns the tile the user clicked on.
* 
* @param gc
*            GameContainer of slick
* @return the tile the user clicked on
*/
private Tile getTileClicked(GameContainer gc) {
	Input input = gc.getInput();
	if (input.isMousePressed(Input.MOUSE_LEFT_BUTTON)) {
		int x = input.getMouseX() / grassMap.getTileWidth();
		int y = input.getMouseY() / grassMap.getTileHeight();

		for (Tile t : tiles) {
			if (t.x == x && t.y == y)
				return t;
		}
	}
	return null;
}</pre>