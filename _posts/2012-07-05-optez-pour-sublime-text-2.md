---
id: 215
title: Optez pour Sublime Text 2 !
date: 2012-07-05T21:56:31+00:00
author: spyl94
layout: post
guid: http://blog.spyl.net/?p=215
permalink: /2012/07/optez-pour-sublime-text-2/
categories:
  - Geek
  - Sublime Text 2
tags:
  - débuter
  - optez
  - sublime text 2
---
Difficile de ne pas entendre parler de cet éditeur lorsque l&rsquo;on travaille dans le **web**, c&rsquo;est ce qui m&rsquo;a décidé à l&rsquo;essayer&#8230;et croyez moi c&rsquo;est vraiment un éditeur qui vous permettra d&rsquo;améliorer votre quotidien ! (Une fois maîtrisé bien entendu&#8230; Rassurez-vous tout va bien se passer !)

Plutôt que de déballer une à une toutes les fonctionnalités que j&rsquo;ai découvertes, je vous propose avant tout de jeter un coup d’œil à la démo disponible au site officiel [sublimetext.com](http://www.sublimetext.com/). Votre futur éditeur favori est disponible sur toutes les plateformes habituelles, cependant il n&rsquo;est **ni open source ni gratuit,** mais heureusement, il est possible de l&rsquo;essayer et de l&rsquo;**évaluer gratuitement** pour une **durée indéterminée**.

L&rsquo;interface est classique, mais cependant soignée, ce qui est agréable devant le nombre d&rsquo;heures que l&rsquo;on va passer à coder en utilisant la bête ! Découvrons notre premier raccourci bien pratique _Ctrl + P_, afin d&rsquo;**ouvrir un fichier**, en tapant (plus ou moins bien) son nom.

En dehors des raccourcis classiques que l&rsquo;on retrouve chez tous les éditeurs, Sublime Text 2 se démarque par l&rsquo;utilisation d&rsquo;une **invite de commande** (_Ctrl + Shift + P_) qui va nous permettre d’accélérer toutes les actions pour lesquelles on passe habituellement par des menus.

Commençons par quelques astuces qui vont changer votre vie&#8230; (enfin peut-être juste votre façon de coder :-P)

  * **La sélection multiple**, qui permet d&rsquo;avoir un curseur sur plusieurs lignes ainsi d&rsquo;en modifier plusieurs à la fois, pratique pour modifier une liste, par exemple. Pour l&rsquo;activer, plusieurs solutions _Ctrl + Clic_ sur les différentes lignes ou bien sélectionnez en plusieurs puis faites _Ctrl + Shift + L_. Ou bien pour modifier du contenu identique, sélectionnez une occurrence puis faites _Ctrl + D_ pour sélectionner les suivantes une à une ou bien _Alt+F3_ pour **toutes les occurrences** d&rsquo;un seul coup, super pratique !

&nbsp;

  * **Diviser l&rsquo;écran** en plusieurs parties _Alt + Shift + NombreDeParties_, exemple _Alt + Shift + 2_ pour diviser l&rsquo;éditeur en 2 fichiers !

<div id="attachment_390" style="width: 635px" class="wp-caption aligncenter">
  <a href="http://blog.spyl.net/wp-content/uploads/2012/07/Sans-titre1.png"><img class="size-large wp-image-390" title="split" src="http://blog.spyl.net/wp-content/uploads/2012/07/Sans-titre1-1024x624.png" alt="Séparer l'écran en 2 parties" width="625" height="380" srcset="http://blog.spyl.net/wp-content/uploads/2012/07/Sans-titre1-300x182.png 300w, http://blog.spyl.net/wp-content/uploads/2012/07/Sans-titre1-1024x624.png 1024w, http://blog.spyl.net/wp-content/uploads/2012/07/Sans-titre1.png 1483w" sizes="(max-width: 625px) 100vw, 625px" /></a>
  
  <p class="wp-caption-text">
    Séparer l&rsquo;écran en 2 parties
  </p>
</div>

  * On a pas encore vu toute la magie de _Ctrl + P_ puisqu&rsquo;il nous permet de positionner le curseur à une certaine ligne en tapant &laquo;&nbsp;**:NuméroDeLaLigne**&nbsp;&raquo; ou bien positionner le curseur devant un mot en utilisant &laquo;&nbsp;**#LeMot**&laquo;&nbsp;.

  * **Beaucoup d&rsquo;autres** qu&rsquo;il serait bien long de détailler ici&#8230; Faites un tour sur la [doc](http://docs.sublimetext.info/en/latest/index.html) ou le [site](http://www.sublimetext.com/) !

Avant de commencer à coder, la première chose à faire est d&rsquo;installer **Package Control**, afin par la suite d&rsquo;installer tous les Packages dont vous aurez besoin directement depuis l&rsquo;invite de commande, exactement comme un gestionnaire de paquet pour les habitués à Linux ! Pour cela, faites un tour par [ici](http://wbond.net/sublime_packages/package_control/installation) et copier-coller le code directement dans la **console** (View / Show Console ou _Ctrl+\`_)&#8230; Bah quoi vous vous attendiez à plus compliqué ? Ceux qui sont un peu curieux auront tout de suite remarqué l&rsquo;utilisation du langage **Python** !

Désormais après avoir redémarré Sublime Text 2, pour installer un nouveau Package, il vous suffira de taper **Install Package** dans la commande !

Voici une liste de quelques Packages dont vous ne pourrez bientôt plus vous passer :

  * <del><strong>Zen Coding</strong></del> **emmet-sublime**, afin d&rsquo;éviter d&rsquo;avoir à toujours écrire les mêmes lignes de code, vous connaissez certainement déjà la syntaxe via d&rsquo;autres éditeurs, sinon je vous invite à la découvrir sur [docs.emmet.io](http://docs.emmet.io/)
  * **Nettuts+ Fetch**, pour récupérer directement des fichiers comme jquery ou des dossiers WordPress, Symfony&#8230;
  * **Alignement**, pour un code propre avec une simple combinaison de touches.
  * **Prefixr Plugin**, afin d&rsquo;ajouter automatiquement les différents préfixes CSS3.
  * **Sublime Linter**, pour détecter les erreurs, on en fait tous !
  * **SublimeCodeIntel**, une auto complétion que j’apprécie puisque basée sur mon ancien éditeur Open Komodo !
  * **SFTP**, que serait un éditeur sans un FTP intégré ?
  * **Beaucoup d&rsquo;autres&#8230;** N&rsquo;hésitez pas à partager vos trouvailles en commentaires !
  * **Créez votre propre plugin**,  il est possible de créer ces propres Packages (et de les partager ! ) en python, consultez la doc pour plus d&rsquo;infos.

Enfin, pour configurer vos Packages: **Préférences** &#8211; **Package Settings**, chaque Package présente un fichier **Settings &#8211; Default** et un **Settings &#8211; User**, référez-vous au fichier **Default** pour la configuration par défaut mais ne le modifiez pas puisque tout sera perdu au redémarrage du logiciel ! Pour effectuer des modifications, copiez les lignes dans le fichier **User** puis modifiez-les. Vous pouvez bien entendu y accéder par la commande, cela va devenir un réflexe !

<pre class="lang:default decode:true" title="Preferences / Settings - User ">{
	"color_scheme": "Packages/Theme - Nil/Tubnil.tmTheme",
	"font_size": 13,
	"ignored_packages":
	[
		"Vintage"
	],
	"project_defaults":
	{
		"check_time": true,
		"download_on_open": false,
		"ignore": null,
		"passive": true,
		"password": "jesaispas",
		"path": "/efrei/",
		"port": 21,
		"private_key": null,
		"private_key_pass": null,
		"timeout": 30,
		"tls": false,
		"upload_on_save": true,
		"username": "kikoo"
	}
}</pre>

Ces fichiers sont sous forme de [JSON](http://fr.wikipedia.org/wiki/JavaScript_Object_Notation), bref c&rsquo;est parfait pour les geeks !

J&rsquo;espère que ce rapide survol de Sublime Text 2 vous a donné envie de l&rsquo;essayer, en tout cas pour moi il est adopté ! Vous devriez être capable d&rsquo;utiliser la bête maintenant 😉

Pour continuer votre apprentissage, attaquez-vous aux [Difficile de ne pas entendre parler de cet éditeur lorsque l&rsquo;on travaille dans le **web**, c&rsquo;est ce qui m&rsquo;a décidé à l&rsquo;essayer&#8230;et croyez moi c&rsquo;est vraiment un éditeur qui vous permettra d&rsquo;améliorer votre quotidien ! (Une fois maîtrisé bien entendu&#8230; Rassurez-vous tout va bien se passer !)

Plutôt que de déballer une à une toutes les fonctionnalités que j&rsquo;ai découvertes, je vous propose avant tout de jeter un coup d’œil à la démo disponible au site officiel [sublimetext.com](http://www.sublimetext.com/). Votre futur éditeur favori est disponible sur toutes les plateformes habituelles, cependant il n&rsquo;est **ni open source ni gratuit,** mais heureusement, il est possible de l&rsquo;essayer et de l&rsquo;**évaluer gratuitement** pour une **durée indéterminée**.

L&rsquo;interface est classique, mais cependant soignée, ce qui est agréable devant le nombre d&rsquo;heures que l&rsquo;on va passer à coder en utilisant la bête ! Découvrons notre premier raccourci bien pratique _Ctrl + P_, afin d&rsquo;**ouvrir un fichier**, en tapant (plus ou moins bien) son nom.

En dehors des raccourcis classiques que l&rsquo;on retrouve chez tous les éditeurs, Sublime Text 2 se démarque par l&rsquo;utilisation d&rsquo;une **invite de commande** (_Ctrl + Shift + P_) qui va nous permettre d’accélérer toutes les actions pour lesquelles on passe habituellement par des menus.

Commençons par quelques astuces qui vont changer votre vie&#8230; (enfin peut-être juste votre façon de coder :-P)

  * **La sélection multiple**, qui permet d&rsquo;avoir un curseur sur plusieurs lignes ainsi d&rsquo;en modifier plusieurs à la fois, pratique pour modifier une liste, par exemple. Pour l&rsquo;activer, plusieurs solutions _Ctrl + Clic_ sur les différentes lignes ou bien sélectionnez en plusieurs puis faites _Ctrl + Shift + L_. Ou bien pour modifier du contenu identique, sélectionnez une occurrence puis faites _Ctrl + D_ pour sélectionner les suivantes une à une ou bien _Alt+F3_ pour **toutes les occurrences** d&rsquo;un seul coup, super pratique !

&nbsp;

  * **Diviser l&rsquo;écran** en plusieurs parties _Alt + Shift + NombreDeParties_, exemple _Alt + Shift + 2_ pour diviser l&rsquo;éditeur en 2 fichiers !

<div id="attachment_390" style="width: 635px" class="wp-caption aligncenter">
  <a href="http://blog.spyl.net/wp-content/uploads/2012/07/Sans-titre1.png"><img class="size-large wp-image-390" title="split" src="http://blog.spyl.net/wp-content/uploads/2012/07/Sans-titre1-1024x624.png" alt="Séparer l'écran en 2 parties" width="625" height="380" srcset="http://blog.spyl.net/wp-content/uploads/2012/07/Sans-titre1-300x182.png 300w, http://blog.spyl.net/wp-content/uploads/2012/07/Sans-titre1-1024x624.png 1024w, http://blog.spyl.net/wp-content/uploads/2012/07/Sans-titre1.png 1483w" sizes="(max-width: 625px) 100vw, 625px" /></a>
  
  <p class="wp-caption-text">
    Séparer l&rsquo;écran en 2 parties
  </p>
</div>

  * On a pas encore vu toute la magie de _Ctrl + P_ puisqu&rsquo;il nous permet de positionner le curseur à une certaine ligne en tapant &laquo;&nbsp;**:NuméroDeLaLigne**&nbsp;&raquo; ou bien positionner le curseur devant un mot en utilisant &laquo;&nbsp;**#LeMot**&laquo;&nbsp;.

  * **Beaucoup d&rsquo;autres** qu&rsquo;il serait bien long de détailler ici&#8230; Faites un tour sur la [doc](http://docs.sublimetext.info/en/latest/index.html) ou le [site](http://www.sublimetext.com/) !

Avant de commencer à coder, la première chose à faire est d&rsquo;installer **Package Control**, afin par la suite d&rsquo;installer tous les Packages dont vous aurez besoin directement depuis l&rsquo;invite de commande, exactement comme un gestionnaire de paquet pour les habitués à Linux ! Pour cela, faites un tour par [ici](http://wbond.net/sublime_packages/package_control/installation) et copier-coller le code directement dans la **console** (View / Show Console ou _Ctrl+\`_)&#8230; Bah quoi vous vous attendiez à plus compliqué ? Ceux qui sont un peu curieux auront tout de suite remarqué l&rsquo;utilisation du langage **Python** !

Désormais après avoir redémarré Sublime Text 2, pour installer un nouveau Package, il vous suffira de taper **Install Package** dans la commande !

Voici une liste de quelques Packages dont vous ne pourrez bientôt plus vous passer :

  * <del><strong>Zen Coding</strong></del> **emmet-sublime**, afin d&rsquo;éviter d&rsquo;avoir à toujours écrire les mêmes lignes de code, vous connaissez certainement déjà la syntaxe via d&rsquo;autres éditeurs, sinon je vous invite à la découvrir sur [docs.emmet.io](http://docs.emmet.io/)
  * **Nettuts+ Fetch**, pour récupérer directement des fichiers comme jquery ou des dossiers WordPress, Symfony&#8230;
  * **Alignement**, pour un code propre avec une simple combinaison de touches.
  * **Prefixr Plugin**, afin d&rsquo;ajouter automatiquement les différents préfixes CSS3.
  * **Sublime Linter**, pour détecter les erreurs, on en fait tous !
  * **SublimeCodeIntel**, une auto complétion que j’apprécie puisque basée sur mon ancien éditeur Open Komodo !
  * **SFTP**, que serait un éditeur sans un FTP intégré ?
  * **Beaucoup d&rsquo;autres&#8230;** N&rsquo;hésitez pas à partager vos trouvailles en commentaires !
  * **Créez votre propre plugin**,  il est possible de créer ces propres Packages (et de les partager ! ) en python, consultez la doc pour plus d&rsquo;infos.

Enfin, pour configurer vos Packages: **Préférences** &#8211; **Package Settings**, chaque Package présente un fichier **Settings &#8211; Default** et un **Settings &#8211; User**, référez-vous au fichier **Default** pour la configuration par défaut mais ne le modifiez pas puisque tout sera perdu au redémarrage du logiciel ! Pour effectuer des modifications, copiez les lignes dans le fichier **User** puis modifiez-les. Vous pouvez bien entendu y accéder par la commande, cela va devenir un réflexe !

<pre class="lang:default decode:true" title="Preferences / Settings - User ">{
	"color_scheme": "Packages/Theme - Nil/Tubnil.tmTheme",
	"font_size": 13,
	"ignored_packages":
	[
		"Vintage"
	],
	"project_defaults":
	{
		"check_time": true,
		"download_on_open": false,
		"ignore": null,
		"passive": true,
		"password": "jesaispas",
		"path": "/efrei/",
		"port": 21,
		"private_key": null,
		"private_key_pass": null,
		"timeout": 30,
		"tls": false,
		"upload_on_save": true,
		"username": "kikoo"
	}
}</pre>

Ces fichiers sont sous forme de [JSON](http://fr.wikipedia.org/wiki/JavaScript_Object_Notation), bref c&rsquo;est parfait pour les geeks !

J&rsquo;espère que ce rapide survol de Sublime Text 2 vous a donné envie de l&rsquo;essayer, en tout cas pour moi il est adopté ! Vous devriez être capable d&rsquo;utiliser la bête maintenant 😉

Pour continuer votre apprentissage, attaquez-vous aux](http://blog.spyl.net/2012/12/sublime-text-2-les-racourcis-utiles-windows/) !

_Note : sur Mac OS la touche Ctrl est à remplacer par cmd. Pour certains raccourcis plus complexes, il vous faudra consulter la doc._