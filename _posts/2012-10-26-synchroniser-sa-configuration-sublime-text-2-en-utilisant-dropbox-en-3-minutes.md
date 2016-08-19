---
id: 310
title: Synchroniser sa configuration Sublime Text 2 avec Dropbox en 3 minutes
date: 2012-10-26T09:13:38+00:00
author: spyl94
layout: post
guid: http://blog.spyl.net/?p=310
permalink: /2012/10/synchroniser-sa-configuration-sublime-text-2-en-utilisant-dropbox-en-3-minutes/
categories:
  - Sublime Text 2
  - 'Tips &amp; Tricks'
tags:
  - dropbox
  - odinateurs
  - plusieurs
  - sublime text 2
  - synchroniser
---
<p style="text-align: justify;">
  Cela fais quelques temps déjà que j&rsquo;ai totalement adopté <strong>Sublime Text 2</strong> dont je vous parlais dans un précédent <a href="http://blog.spyl.net/2012/07/optez-pour-sublime-text-2/">article</a>. Il est d&rsquo;ailleurs recommandé comme éditeur dans la nouvelle documentation de <a href="http://twitter.github.com/bootstrap/getting-started.html">Twitter Bootstrap</a>&#8230; Etant donné le nombre de Packages supplémentaires que j&rsquo;ai installé depuis, il fallait que je trouve un moyen de les <strong>synchroniser entre mes ordinateurs</strong>&#8230; Et c&rsquo;est vraiment simple et rapide !
</p>

<p style="text-align: justify;">
  Je vais montrer un exemple avec Dropbox mais cette astuce fonctionne assurément avec d&rsquo;autres services de stockage comme Drive, etc&#8230;Voici la procédure pour Windows, pour les autres OS c&rsquo;est facilement adaptable.
</p>

<li style="text-align: justify;">
  Commencez par créer un dossier dans votre Dropbox, afin de stocker votre configuration. Pour ma part j&rsquo;ai choisi :<br /> <blockquote>
    <p>
      {Chemin vers Dropbox}/appdata/Sublime Text 2
    </p>
  </blockquote>
</li>

<li style="text-align: justify;">
  Ensuite il faut trouver le dossier dans lequel Sublime Text 2 enregistre votre configuration, pour cela faites: Preferences/Browse Packages. A priori, c&rsquo;est le suivant:<br /> <blockquote>
    <p>
      C:\Users\{username}\AppData\Roaming\Sublime Text 2\Packages
    </p>
  </blockquote>
  
  <p>
    Pour éviter tout problème, commencez par <strong>fermer</strong> complètement Sublime Text 2.<br /> <strong>Remontez d&rsquo;un dossier</strong> et Coupez (Ctrl + X) les dossiers suivants: <strong>Packages</strong>, <strong>Installed Packages</strong>, <strong>Pristine Packages</strong>. Collez les dans le dossier de votre Dropbox créé à l&rsquo;étape 1.</li> 
    
    <li style="text-align: justify;">
      Il est temps de créer des <strong>liens symboliques</strong>, pour cela ouvrez la commande Windows en administrateur. Si vous n&rsquo;êtes pas habitué à utiliser la console: recherchez cmd.exe, clique droit, &laquo;&nbsp;Exécuter en tant qu’administrateur.&nbsp;&raquo;. Déplacez vous (en utilisant <strong>cd</strong>) dans le dossier de configuration vu à l&rsquo;étape précédente:<br /> <blockquote>
        <p>
          C:\Users\{username}\AppData\Roaming\Sublime Text 2
        </p>
      </blockquote>
      
      <p>
        Pour finir nous allons créer les liens symboliques en tapant les commandes suivantes, <strong>pensez à modifier le chemin vers votre Dropbox</strong>.
      </p>
      
      <blockquote>
        <p>
          mklink /D &laquo;&nbsp;Installed Packages&nbsp;&raquo; &laquo;&nbsp;C:\{Chemin vers Dropbox}\appdata\Sublime Text 2\Installed Packages&nbsp;&raquo;<br /> mklink /D &laquo;&nbsp;Packages&nbsp;&raquo; &laquo;&nbsp;C:\{Chemin vers Dropbox}\appdata\Sublime Text 2\Packages&nbsp;&raquo;<br /> mklink /D &laquo;&nbsp;Pristine Packages&nbsp;&raquo; &laquo;&nbsp;C:\{Chemin vers Dropbox}\appdata\Sublime Text 2\Pristine Packages&nbsp;&raquo;
        </p>
      </blockquote>
    </li></ol> 
    
    <p style="text-align: justify;">
      Et voilà, c&rsquo;est tout&#8230; Il suffit de créer ces liens symboliques vers votre dossier Dropbox sur chacun des ordinateurs que vous utilisez !
    </p>