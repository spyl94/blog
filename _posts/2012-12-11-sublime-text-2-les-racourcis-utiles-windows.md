---
id: 362
title: 'Sublime Text 2 &#8211; Les racourcis utiles (Windows)'
date: 2012-12-11T14:43:29+00:00
author: spyl94
layout: post
guid: http://blog.spyl.net/?p=362
permalink: /2012/12/sublime-text-2-les-racourcis-utiles-windows/
categories:
  - Sublime Text 2
tags:
  - clavier
  - racourcis
  - sublime text 2
  - windows
---
## Préambule

<p style="text-align: justify;">
  L&rsquo;un des nombreux avantages de Sublime Text 2 est son nombre impressionnant de <strong>raccourcis clavier </strong>et de fonctionnalités permettant de<strong> gagner en productivité</strong>, ce qui vous empêchera tout simplement d&rsquo;envisager de vous tourner vers un autre éditeur !
</p>

<p style="text-align: justify;">
  J&rsquo;ai regroupé dans une fiche, l&rsquo;ensemble des raccourcis que j&rsquo;ai trouvé: <a href="https://github.com/spyl94/st2shortcuts">https://github.com/spyl94/st2shortcuts</a>
</p>

<p style="text-align: justify;">
  Je vous recommande de l&rsquo;ajouter à vos favoris, afin de pouvoir y jeter un œil lorsqu&rsquo;en codant vous serez en train de vous demander:
</p>

<p style="text-align: justify;">
  <em>Je viens de faire 5 fois la même chose, c&rsquo;est un peu rébarbatif, il n&rsquo;y a pas un raccourci pour le faire ?</em>
</p>

<p style="text-align: justify;">
  C&rsquo;est sans conteste la meilleure façon d&rsquo;apprendre un raccourci !
</p>

<p style="text-align: justify;">
  Avant de commencer, prenez en compte la notation <strong>Ctrl+KB</strong> qui signifie enfoncer les touches <strong>Ctrl</strong> et <strong>K</strong> simultanément puis relâcher <strong>K</strong>, enfoncer <strong>B</strong> tout en maintenant la touche <strong>Ctrl</strong> enfoncée. (Testez directement sur ST2, ça deviendra tout de suite plus clair 😉 )
</p>

<p style="text-align: justify;">
  Contrairement à la fiche qui sert de mémo, la suite de cet article est là pour vous amener en douceur à découvrir les principaux raccourcis, vous êtes prêt ? En avant !
</p>

## Général

<p style="text-align: justify;">
  L&rsquo;une des actions que l&rsquo;on effectue le plus souvent est d&rsquo;ouvrir l&rsquo;invite de commande <strong>Ctrl+Shift+P</strong>, pour changer la syntaxe d&rsquo;un fichier par exemple on écrit dans la commande &laquo;&nbsp;<strong>ss</strong>&nbsp;&raquo; pour <strong>S</strong>et <strong>S</strong>yntax puis le nom du langage par exemple <strong>html</strong>, on presse enter et voilà la nouvelle syntaxe est chargée ! Pour installer un nouveau package on tape &laquo;&nbsp;<strong>install</strong>&nbsp;&raquo; pour lancer Package Control. Cela ne fonctionne pas ? Vous n&rsquo;avez pas encore installé Package Control ? Dans ce cas, allez vite lire mon article pour débuter sur Sublime Text 2 !
</p>

<p style="text-align: justify;">
  En entrant &laquo;&nbsp;<strong>Toggle</strong>&nbsp;&raquo; dans la commande vous pourrez faire apparaitre/disparaitre des éléments comme le Menu, la Mini Map, les onglets, mais aussi la barre latérale (<strong>Side Bar</strong>) pour cette dernière il existe un raccourci sans passer par la commande: <strong>Ctrl+KB</strong>.
</p>

<p style="text-align: justify;">
  J&rsquo;imagine que certains d&rsquo;entrevous ont l&rsquo;habitude de coder en plein écran, le raccourci est habituel il suffit de presser <strong>F11</strong> pour entrer ou sortir de ce mode. ST2 propose un autre mode appelé « sans distraction » encore plus léger en pressant <strong>Shift+F11</strong>.
</p>

<p style="text-align: justify;">
  Le dernier raccourci de cette partie permet d&rsquo;afficher la console python le raccourci par défaut est <strong>Ctrl+`</strong> cependant si vous utilisez comme moi un clavier Azerty vous aurez un peu de mal à l&rsquo;utiliser ! Celui-ci n&rsquo;est pas forcément très utile cependant nous allons en profiter pour étudier la façon dont ST2 gère les raccourcis. Dans le menu préférences, vous trouverez 2 fichiers &laquo;&nbsp;<strong>Key Bindings &#8211; Default</strong>&nbsp;&raquo; et &laquo;&nbsp;<strong>Key Bindings &#8211; User</strong>&laquo;&nbsp;. C&rsquo;est dans le premier fichier que ST2 gère la configuration par défaut, vous y trouverez l&rsquo;ensemble des raccourcis, mais il faut l&rsquo;avouer, ce n’est pas très digeste ! N&rsquo;essayez surtout pas d&rsquo;y toucher en effet toutes les modifications seront supprimées au prochain lancement du logiciel&#8230; Rassurez-vous le fichier &laquo;&nbsp;Key Bindings &#8211; User&nbsp;&raquo; est justement fait pour y placer <strong>nos modifications</strong> !
</p>

<p style="text-align: justify;">
  Voici la méthodologie à effectuer pour ajouter une modification, recherchons (<strong>Ctrl+F</strong>) dans le fichier Default le raccourci que l&rsquo;on souhaite modifier en tapant &laquo;&nbsp;<strong>ctrl+&rsquo;</strong>&nbsp;&raquo; ou bien son nom &laquo;&nbsp;<strong>console</strong>&laquo;&nbsp;, vous devriez obtenir ça :
</p>

<pre class="toolbar:2 show-title:false lang:default decode:true">{ "keys": ["ctrl+'"], "command": "show_panel", "args": {"panel": "console", "toggle": true} },</pre>

<p style="text-align: justify;">
  Placez votre curseur n&rsquo;importe où sur cette ligne et pressez <strong>Ctrl+C</strong> pour la copier, avec ST2 sans sélection, c&rsquo;est la ligne entière qui est copiée par défaut, pratique ! Collez là entre les crochets du fichier &laquo;&nbsp;Key Bindings &#8211; User&nbsp;&raquo; et supprimez la virgule à la fin de la ligne. Nous allons remplacer le raccourci <strong>Ctrl+&rsquo;</strong> par <strong>Ctrl+,</strong> pour cela toujours dans User, modifiez la partie <strong>&laquo;&nbsp;keys&nbsp;&raquo;: [&laquo;&nbsp;ctrl+'&nbsp;&raquo;]</strong> par <strong>&laquo;&nbsp;keys&nbsp;&raquo;: [&laquo;&nbsp;ctrl+,&nbsp;&raquo;]</strong>, on sauvegarde et c&rsquo;est tout, vous pouvez essayer pas besoin de relancer ST2 !
</p>

<p style="text-align: justify;">
  Les différents packages que vous allez installer proposeront également le système de fichiers Key Bindings &#8211; Default et User, c&rsquo;est donc important de bien le maîtriser ! Pour plus d&rsquo;infos sur le format utilisé par ces fichiers: <a title="JSON" href="http://fr.wikipedia.org/wiki/JavaScript_Object_Notation">JavaScript_Object_Notation (JSON)</a>.
</p>