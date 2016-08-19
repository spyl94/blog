---
id: 537
title: Déploiement continu pour votre startup
date: 2014-09-24T21:28:39+00:00
author: spyl94
layout: post
guid: http://blog.spyl.net/?p=537
permalink: /2014/09/deploiement-continu-pour-votre-startup/
categories:
  - Non classé
---
<span style="color: #000000;">Ou comment mettre en production votre projet à chaque modifications !</span>

<span style="color: #000000;">Une suite d&rsquo;articles ayant pour thème DevOps pour accélérer le développement de votre produit.</span>

<span style="color: #000000;"><em>Bon en fait, pour le moment c&rsquo;est surtout un plan ! Si vous avez envie de lire la suite, faites-le moi savoir ça me motivera à continuer ! 😉</em></span> <span style="color: #000000;"><strong> </strong></span>

<span style="color: #000000;"><strong>Pourquoi ?</strong></span>

<span style="color: #000000;">Vous êtes une lean startup,  vous avez besoin d&rsquo;aller vite et de vous adapter.</span>

<span style="color: #000000;">Ainsi, vous cherchez à réduire les temps entre les déploiements en production le plus possible, votre objectif : <strong>avoir une application facile à faire évoluer et dont les évolutions soient directement visibles par vos utilisateurs.</strong></span>

<span style="color: #000000;">La méthodologie que je vais décrire va vous permettre tout ça mais également :</span>

  * <span style="color: #000000;">Accélérer les déploiements pour éviter de faire perdre du temps à vos développeurs et diminuer le risque de déploiements ratés.</span>
  * <span style="color: #000000;">Réduire le temps de résolution des problèmes.</span>
  * <span style="color: #000000;">Permettre à tous le monde de déployer (Oui, même au junior qui vient d&rsquo;arriver !).</span>

<span style="color: #000000;"><strong>Comment ?</strong></span>

<span style="color: #000000;"><em>Intégration continue, un socle indispensable</em></span>

<span style="color: #000000;">L’exécution des tests dans un environnement d’intégration permet de vérifier le bon fonctionnement de l&rsquo;ensemble de votre produit.</span>

<p style="color: #6d6f71;">
  <span style="color: #000000;"><em>Déploiement automatisé, une nécessité</em></span>
</p>

<p style="color: #6d6f71;">
  <span style="color: #000000;">Une fois les tests passés avec succès, il ne reste qu&rsquo;à mettre en ligne les changements !</span>
</p>

<p style="color: #6d6f71;">
  <span style="color: #000000;"><strong>Le plan </strong></span>
</p>

<span style="color: #000000;">Maintenant nous allons le mettre en plusieurs étapes :</span>

<span style="color: #000000;"><strong>Etape 0 : Agilité et Git-Workflow</strong></span>

<span style="color: #000000;">Scrum, Github workflow</span>

<span style="color: #000000;"><strong>Etape 1 : Mettre en place votre environnement de développement</strong></span> <span style="color: #000000;">Objectif : permettre à n&rsquo;importe quel développeur de travailler sur votre projet en moins d&rsquo;une heure.</span>

> <span style="color: #000000;">Everyone gets a shiny new virtual machine with a working development version of the site, along with their LDAP credentials, github write access, and laptop.</span>

<span style="color: #000000;">Environnement de développement sous Linux ou Mac OS, éviter Windows.</span>

<span style="color: #000000;">Isolé & normalisé entre tous les développeurs : Vagrant ou Docker.</span>

<span style="color: #000000;">Plus peur d&rsquo;installer une librairie sans casser votre ordi, facile de revenir en arrière.</span>

<span style="color: #000000;">Provisionning : faire un template par un Ops expérimenté ou utiliser Puphpet</span>

<span style="color: #000000;"><strong>Etape 2 : Découpez votre projet en plusieurs applications</strong></span>

Par la suite nous utiliserons une application backend utilisant le framework Symfony et une application frontend basée sur Angular.js.

<span style="color: #000000;"><strong>Etape 3 : Testez votre application Symfony avec Behat et PhpSpec (Behavior Driven Development)</strong></span>

<span style="color: #000000;"><strong>Etape 4 : Testez votre application Angular.js avec Protractor et Cucumber.js (Behavior Driven Development)</strong></span>

<span style="color: #000000;"><strong>Etape 5 : Utiliser Travis-CI, la plateforme d’intégration continue</strong></span>

<span style="color: #000000;">http://chez-syl.fr/2014/04/debuter-avec-travis-ci-la-plateforme-dintegration-continue/</span>

<span style="color: #000000;"><strong>Etape 6 : Déployer votre projet Symfony automatiquement en production</strong></span>

<span style="color: #000000;">Easy to Deploy on Day One</span>

<span style="color: #000000;">Quick recovery : ne plus avoir peur de l&rsquo;erreur humaine</span>

<span style="color: #000000;"><strong>Etape 7 : Et après ? Allez plus loin avec vos applications</strong></span>

<span style="color: #000000;">NewRelic et AppDynamics permettent la détection des problèmes de performance et des erreurs 500 cachées.</span>

<span style="color: #000000;">Des backups automatisés : http://www.r1soft.com/ backup</span>

<span style="color: #000000;">Tests de montés en charge ?</span>