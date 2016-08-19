---
id: 574
title: 'L&rsquo;importance de la revue de code'
date: 2015-01-12T22:21:14+00:00
author: spyl94
layout: post
guid: http://blog.spyl.net/?p=574
permalink: /2015/01/limportance-de-la-revue-de-code/
categories:
  - Non classé
---
<p style="text-align: justify;">
  <span style="color: #000000;">Les bons développeurs sont flemmards, c&rsquo;est un fait connu. Après avoir développé une fonctionnalité il est courant de vouloir s&rsquo;en débarrasser le plus vite possible en la fusionnant avec la branche principale du projet. Malheureusement, un tel comportement apporte de nombreux problèmes à la longue : bugs, parties du code incompréhensibles, doublons, choix d&rsquo;implémentations douteux, tests oubliés qui font que votre projet acquiert de la dette technique et devient de plus en plus difficile à maintenir et à faire évoluer.</span>
</p>

<p style="text-align: justify;">
  <span style="color: #000000;">C&rsquo;est pourquoi avant de fusionner votre travail, il est important de vérifier qu&rsquo;il est <strong>vraiment</strong> terminé, pour cela vous devez compter sur votre équipe !</span>
</p>

<p style="text-align: justify;">
  <span style="color: #000000;">En principe, lorsque vous partagez votre travail avec les autres développeurs vous faites une Pull-Request. Des plateformes comme Github ou Gitlab (entre autre) permettent à votre équipe de voir tous les ajouts et changements que vous avez fait au sein de votre branche, mais également de commenter chacune des lignes de code&#8230; C&rsquo;est l&rsquo;endroit idéal pour faire votre revue de code, en anglais <strong>Code Review (CR) </strong>!</span>
</p>

<p style="text-align: justify;">
  <span style="color: #000000;">Bon alors, qui relit le code ? En principe, si vous êtes une équipe : tous les développeurs ! En général, je pense que l&rsquo;accord d&rsquo;un développeur expérimenté suffit pour les petites tâches ou la correction d&rsquo;un bug simple, pour tout le reste, il est préférable d&rsquo;attendre l&rsquo;avis d&rsquo;au moins deux ou trois développeurs. Il est important de vérifier absolument tout, même un code court et simple, ainsi on n&rsquo;oublie rien, la CR doit devenir une habitude intégrée dans votre workflow de développement et pas une exception.</span>
</p>

<p style="text-align: justify;">
  <span style="color: #000000;">Pour indiquer à l&rsquo;équipe que votre Pull Request attend une CR, je recommande d&rsquo;y ajouter un label « Needs CR ». Tous les développeurs peuvent ensuite consacrer un peu de temps de leur journée, (après chaque pause par exemple) à faire les différentes relectures de code.</span>
</p>

<span style="color: #000000;">Vous vous demandez ce qu&rsquo;on peut vérifier ? Personnellement je suis la check-list suivante :</span>

### <span style="color: #000000;"><strong>Le code</strong></span>

<span style="color: #000000;">&#8211; Est-ce que ça fonctionne ? La logique est-elle correcte, et est-ce bien ce qu&rsquo;on attendait ?</span>

<span style="color: #000000;">&#8211; Est-il facile à comprendre ? (Correctement structuré, le choix des noms est bon, &#8230;)</span>

<span style="color: #000000;">&#8211; Y a-t-il des parties redondantes ou en double ?</span>

<span style="color: #000000;">&#8211; Est-il suffisamment modulaire, réutilisable,  évite-t-il les variables globales ?</span>

<span style="color: #000000;">&#8211; Du code peut-il être remplacé par des fonctions issues des librairies ?</span>

<span style="color: #000000;">&#8211; Est-il optimisé ?</span>

<span style="color: #000000;">&#8211; Est-il propre ? (Ne comporte pas  de code commenté, de logs superflus, de fonctions de debug oubliées&#8230;)</span>

<span style="color: #000000;">&#8211; Respect-il les conventions de codage ? (Pour automatiser cette étape, je conseille d&rsquo;utiliser des linters comme jshint, phpcs)</span>

<h3 class="tw-data-text vk_txt tw-ta tw-text-small " dir="ltr" data-placeholder="Traduction">
  <span style="color: #000000;"><strong>Documentation</strong></span>
</h3>

<p class="tw-data-text vk_txt tw-ta tw-text-small " dir="ltr" data-placeholder="Traduction">
  <span style="color: #000000;">&#8211; L&rsquo;API est-elle commentée ?</span>
</p>

<p class="tw-data-text vk_txt tw-ta tw-text-small " dir="ltr" data-placeholder="Traduction">
  <span style="color: #000000;">&#8211; Les éventuels comportements inhabituels sont-ils commentés ?</span>
</p>

<p class="tw-data-text vk_txt tw-ta tw-text-small " dir="ltr" data-placeholder="Traduction">
  <span style="color: #000000;">&#8211; Y a-t-il du code incomplet ? Si oui, est-il indiqué par un marqueur approprié comme « TODO » ?</span>
</p>

### <span style="color: #000000;"><strong>Tests</strong></span>

<p class="tw-data-text vk_txt tw-ta tw-text-small " dir="ltr" data-placeholder="Traduction">
  <span style="color: #000000;">&#8211; Les tests existent-ils et couvrent-ils suffisamment les fonctionnalités ? (Evidemment, il faut commencer par vérifier que les tests passent !)</span>
</p>

<p class="tw-data-text vk_txt tw-ta tw-text-small " dir="ltr" data-placeholder="Traduction">
  <span style="color: #000000;">&#8211; Les tests unitaires sont compréhensibles et vérifient suffisamment le code ?</span>
</p>

<p class="tw-data-text vk_txt tw-ta tw-text-small " dir="ltr" data-placeholder="Traduction">
  <span style="color: #000000;">Si vous avez répondu  « Oui » à toutes ces questions alors vous pouvez valider la Code Review !</span>
</p>

<h2 id="tw-target-text" class="tw-data-text vk_txt tw-ta tw-text-small " dir="ltr" data-placeholder="Traduction">
  <span style="color: #000000;"><strong>Quelques bénéfices :</strong></span>
</h2>

<p class="tw-data-text vk_txt tw-ta tw-text-small " dir="ltr" style="text-align: justify;" data-placeholder="Traduction">
  <span style="color: #000000;"><del>« Mais qui a bien pu ajouter cette classe chelou ??? »</del></span>
</p>

<p class="tw-data-text vk_txt tw-ta tw-text-small " dir="ltr" style="text-align: justify;" data-placeholder="Traduction">
  <span style="color: #000000;">En adoptant la revue du code au sein de votre équipe, la qualité du code de vos développements va être améliorée et chacun fera plus attention à ce qu&rsquo;il écrit pour éviter de se prendre des non-validations ! De plus chacun sera plus au courant des évolutions et des ajouts au sein du projet en lisant le code des copains.</span>
</p>

<p class="tw-data-text vk_txt tw-ta tw-text-small " dir="ltr" style="text-align: justify;" data-placeholder="Traduction">
  <span style="color: #000000;"><del>« Ça sert à quoi ce truc-là RabbitMQ ??? »</del></span>
</p>

<p style="text-align: justify;">
  <span style="color: #000000;">La meilleure façon d&rsquo;apprendre à coder c&rsquo;est de lire du code, ainsi chacun est susceptible d&rsquo;apprendre des choses à chaque CR. Pour les nouveaux membres cela facilite grandement l&rsquo;intégration dans l&rsquo;équipe et la compréhension des projets.</span>
</p>

<p style="text-align: justify;">
  <span style="color: #000000;"><del>« Hey Jean-Mimi comment on fait une boucle for ??? »</del></span>
</p>

<p style="text-align: justify;">
  <span style="color: #000000;">Les commentaires sont archivés, vous pouvez ainsi retourner regarder les commentaires écris par un copain développeur sur n&rsquo;importe quelle CR pour répondre à un problème sans avoir à le déranger !</span>
</p>

<p style="text-align: justify;">
  <span style="color: #000000;"><del>« Le stagiaire a encore tout fait bugger&#8230; »</del></span>
</p>

<p style="text-align: justify;">
  <span style="color: #000000;">Tout le monde est responsable du code qui a été fusionné, il n&rsquo;y a plus de coupable de bugs, enfin tout le monde l&rsquo;est !</span>
</p>

<h2 style="text-align: justify;">
  <span style="color: #000000;"><strong>A garder en tête</strong></span>
</h2>

<p style="text-align: justify;">
  <span style="color: #000000;">Le but n&rsquo;est pas de juger l&rsquo;autre, mais d&rsquo;aider chacun à écrire le meilleur code possible pour conserver ensemble l&rsquo;intégrité du projet. S&rsquo;améliorer doit être un objectif partagé par tous au sein de l&rsquo;équipe, sans quoi les CRs n&rsquo;auront pas l’effet escompté.</span>
</p>

<p id="tw-target-text" class="tw-data-text vk_txt tw-ta tw-text-small " dir="ltr" style="color: #212121; text-align: justify;" data-placeholder="Traduction">
  <span style="color: #000000;">Les CRs doivent être faites rapidement pour éviter la frustration, les retours sont plus simples à corriger pour la personne qui a soumis le code quand celui-ci est encore frais dans sa tête.</span>
</p>

<h2 class="tw-data-text vk_txt tw-ta tw-text-small " dir="ltr" style="color: #212121; text-align: justify;" data-placeholder="Traduction">
  <span style="color: #000000;"><strong>Et ensuite ?</strong></span>
</h2>

<p class="tw-data-text vk_txt tw-ta tw-text-small " dir="ltr" style="color: #212121; text-align: justify;" data-placeholder="Traduction">
  <span style="color: #000000;">La revue code c&rsquo;est une chose, mais je vous encourage à faire également une UX Review et une QA Review avant de vraiment pouvoir considérer une tâche « terminée ».</span>
</p>

<p style="text-align: justify;">
  <span style="color: #000000;">Cet article a été inspiré par la lecture de <span style="color: #ff6600;"><a href="http://matthewmachuga.com/blog/2015/code-review-processes.html"><span style="color: #ff6600;">celui-ci</span></a> </span>et <span style="color: #ff6600;"><a href="http://blog.fogcreek.com/increase-defect-detection-with-our-code-review-checklist-example/"><span style="color: #ff6600;">celui-là</span></a></span>. Des idées à rajouter dans la liste, ou un avis à donner ? N&rsquo;hésitez pas à commenter !</span>
</p>