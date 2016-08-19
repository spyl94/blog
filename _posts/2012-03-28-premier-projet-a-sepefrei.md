---
id: 160
title: Premier projet à SEPEFREI
date: 2012-03-28T22:06:49+00:00
author: spyl94
layout: post
guid: http://blog.spyl.net/?p=160
permalink: /2012/03/premier-projet-a-sepefrei/
categories:
  - Geek
  - MyLife
---
<p style="text-align: justify;">
  <a href="http://blog.spyl.net/wp-content/uploads/2012/03/responsive_design.png"><img class="aligncenter size-full wp-image-166" title="responsive_design" src="http://blog.spyl.net/wp-content/uploads/2012/03/responsive_design.png" alt="" width="400" height="300" srcset="http://blog.spyl.net/wp-content/uploads/2012/03/responsive_design-300x225.png 300w, http://blog.spyl.net/wp-content/uploads/2012/03/responsive_design.png 400w" sizes="(max-width: 400px) 100vw, 400px" /></a>
</p>

<p style="text-align: justify;">
  Dès le lendemain de mon inscription à l’entreprise de l’école, j’étais déjà mis sur une étude: réaliser le design responsive d&rsquo;un site internet, dont je ne peux vous révéler le nom.
</p>

<p style="text-align: justify;">
  La première chose à comprendre est la façon dont se déroule un projet du point de vue du développeur, à la SEP :
</p>

<p style="text-align: justify;">
  J’ai en tout premier reçu la proposition commerciale (compter une 20aines de slides) incluant cahier des charges, planning, technologies… puis après avoir validé le projet la convention complète. SEPEFREI a mis en place une équipe constituée de 1 développeur (moi) et d’un chef de projet ou Maître d’œuvre (MO) en M1 à l’EFREI (4ème année).
</p>

<p style="text-align: justify;">
  Voici, la description de ce que j’ai effectué:
</p>

<p style="text-align: justify;">
  <span style="text-decoration: underline;">Avenant :</span> Mise en page en 2 colonnes (5 jours)
</p>

<p style="text-align: justify;">
  Avant de commencer le projet, le client souhaitait pouvoir sur sa page d’accueil afficher plusieurs articles, avec une colonne. Le premier problème était que le site étant géré par un prestataire externe qui ne me fournissait pas les sources, je ne pouvais pas modifier la requête affichant les articles. Mon MO (maître d’œuvre, si vous suivez :P) a donc discuté avec celui-ci et finalement je dois simplement lui envoyer la structure HTML/CSS, celui-ci s’occupera d’adapter la requête et de m’envoyer une version du site pour travailler. J’ai cependant dû télécharger le site au complet puisque les modèles ne m’ont été envoyés qu’à la fin de la semaine. La réalisation des colonnes étant quelque chose d’assez basique, ce ne fut pas bien long, c&rsquo;est pourquoi j’ai préféré ajouter le CSS directement en JavaScript, ce qui évitera au prestataire d’avoir à s’adapter à ma structure.
</p>

<p style="text-align: justify;">
  <span style="text-decoration: underline;">Étape 0 :</span> Phase d’analyse (5 jours) <em>Analyse des besoins du client et conception d’une solution technique adaptée.</em>
</p>

<p style="text-align: justify;">
  Première véritable étape du projet et première question: comment réaliser un design pour mobile? Je savais qu’il était possible en CSS d’afficher un design différent en fonction de la largeur de l’écran grâce aux <em>Media Queries</em> mais également que l’on pouvait réaliser une application complète à l’aide de jQuery Mobile (par exemple…). J’ai finalement opté pour la première solution qui semblait être plus libre à la créativité et ce qui correspondait le plus aux besoins du client. Après un rapide tour sur le site, les éléments problématiques étaient facilement identifiables: le Menu qui était trop conséquent pour être laissé tel quel sur un mobile, l’onglet de connexion inutilisable, un calendrier trop large et quelques autres éléments pas vraiment adaptés aux mobiles: Animation Flash, carrousel d’articles, images de présentation…
</p>

<p style="text-align: justify;">
  J’ai finalement commencé à coder afin dans un premier temps d’éviter les dépassements en largeur du site, tout en plaçant les éléments sur la même colonne et en limitant la taille de tout ce qui pouvait être gênant et en cachant les éléments facultatifs et contraignants. Le dernier jour, il était temps de rencontrer en chair et en os mon MO pour discuter du projet. Je suis arrivé avec la première version du site, ce qui l’a un peu surprit puis nous avons discuté du design, pour choisir la version suivante:
</p>

<p style="text-align: justify;">
  Ajouter un bouton à gauche façon application Facebook, qui fait slider la page et apparaitre le menu. Un autre bouton à droite pour l’onglet de connexion et le logo au centre. J’avais de quoi m’occuper pour le week-end… ^^
</p>

<p style="text-align: justify;">
  <span style="text-decoration: underline;">Étape 1 :</span> Interface design (10 jours)<em> Conversion de 5 pages du site internet en version mobile.</em>
</p>

<p style="text-align: justify;">
  J’ai commencé par analyser le carrousel d’articles qui n’était vraiment pas adapté pour les petites résolutions, ne souhaitant pas toucher au JavaScript réalisé par le prestataire, j’ai bidouillé le CSS afin de l’adapter aussi bien que possible. Puis j’ai réalisé la barre de navigation dans le header avec les 2 boutons et le logo, simplement en adaptant le CSS et en créant le bouton menu en JS puisqu’il n’existait pas auparavant.
</p>

<p style="text-align: justify;">
  Ensuite il a fallu adapter le Menu pour le rendre utilisable sur mobile, encore une fois uniquement en CSS ainsi que d’adapter pour mobile l’onglet de connexion. 5 jours se sont écoulés et je devais montrer cette première version au client. Celui était globalement satisfait cependant il restait de nombreuses retouches graphiques à effectuer, couleurs à améliorer, padding à ajouter pour les textes, ainsi qu’un bouton sur la page d’accueil pour accéder directement aux nouveautés.
</p>

<p style="text-align: justify;">
  Je me suis en premier attaqué à l’animation « Menu Facebook », pas évidente à réaliser au premier coup d’œil, cela m’a pris pas mal de temps, jQuery ayant heureusement bien facilité la chose. Puis j’ai ajouté le bouton « Nouveauté » en utilisant le fameux plugin scrollTo, afin d’avoir une petite animation. Les retours du client ont été positifs et il ne restait que des retouches mineures de design à effectuer, jusqu’à ce que celui-ci soit pleinement satisfait.
</p>

<p style="text-align: justify;">
  <span style="text-decoration: underline;">Étape 2 :</span> Phase de conversion<em> (10 jours) SEPEFREI convertira toutes les pages du site internet.</em>
</p>

<p style="text-align: justify;">
  Je suis actuellement dans cette phase qui consiste à convertir toutes les pages du site, celles-ci utilisant les mêmes fichiers CSS, cela ne devrait pas poser de problème. Je vous donnerais des nouvelles lorsque cela sera terminé, ainsi qu’un article un peu plus technique dans lequel je vous présenterais des morceaux de code afin d’expliquer la réalisation d’une adaptation mobile.
</p>

<p style="text-align: justify;">
  À très bientôt pour la suite du projet !
</p>