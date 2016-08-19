---
id: 276
title: Vérifier simplement en JavaScript si une Media Queries CSS a été exécutée.
date: 2012-10-12T13:21:58+00:00
author: spyl94
layout: post
guid: http://blog.spyl.net/?p=276
permalink: /2012/10/verifier-simplement-en-javascript-si-une-media-queries-css-a-ete-executee/
categories:
  - 'Tips &amp; Tricks'
tags:
  - Javascript
  - Media Queries
---
Lorsque je travaillais sur un projet de responsive design, je cherchais un moyen de savoir si une Media Queries avait été exécuté sans pour autant avoir à la dupliquer en JavaScript. Il existe un moyen tout simple:

<pre class="lang:css decode:true">@media (min-width: 45em) {
    body:after {
        content: 'widescreen';
        display: none;
        }
    }</pre>

Ce code en lui-même ne fait pas grand-chose mais nous allons pouvoir l&rsquo;utiliser pour vérifier la Media Queries a bien été exécutée en JavaScript:

<pre class="lang:js decode:true">var size = window.getComputedStyle(document.body,':after').getPropertyValue('content');
if (size == 'widescreen') {
    // c'est good !
}</pre>

C&rsquo;est tout pour cette astuce qui vous sera très certainement utile un jour.

[Merci à Jeremy Keith et ses lecteurs !](http://adactio.com/journal/5429/)