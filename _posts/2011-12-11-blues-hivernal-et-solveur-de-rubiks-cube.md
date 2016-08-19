---
id: 127
title: 'Blues hivernal et solveur de rubik&rsquo;s cube'
date: 2011-12-11T00:40:55+00:00
author: spyl94
layout: post
guid: http://blog.spyl.net/?p=127
permalink: /2011/12/blues-hivernal-et-solveur-de-rubiks-cube/
categories:
  - Efrei
  - MyLife
---
J&rsquo;ai eu ce matin ma soutenance de Structures de Données, sur ce fameux projet nous demandant de concevoir un solveur de rubik&rsquo;s cube. C&rsquo;est notre seul projet de programmation du semestre c&rsquo;est pourquoi j&rsquo;y ai consacré un temps assez conséquent. Il est marrant de constater que comme à chaque projet, lors de la lecture du sujet je me dis toujours que je n&rsquo;arriverais jamais à aller jusqu&rsquo;au bout pour finalement penser, le jour du rendu que j&rsquo;aurais pu bien mieux faire.

Le prof nous a accueilli certains de notre capacité à le surprendre. Je lui explique notre algorithme de résolution: générer la première face en brute force (par arborescence) puis résoudre le reste du cube à l&rsquo;aide des algorithmes manuels utilisés habituellement pour résoudre le cube. Première conclusion nous appartenons au groupe visiblement restreint qui résout le cube. D&rsquo;autre part, nous avons cherché la performance en allant plus loin qu&rsquo;un algorithme de résolution manuel en utilisant l&rsquo;arborescence.

Nous lançons notre programme, il semble apprécier l&rsquo;interface et nous lui montrons la résolution du cube avec le mélange proposé dans le sujet, la résolution s&rsquo;effectue comme prévu 104 rotations ce qui est vraisemblablement un score équivalent à celui du meilleur groupe. Il nous demande si nous résolvons tous les cas du cube, d&rsquo;après mes tests sur une centaine de cas oui. Je confirme en ajoutant que celui-ci a été programmé pour ne pas planter et afficher un message d’erreur dans le cas où la résolution échouerait. Autre aspect positif, l&rsquo;utilisation du C++ orienté objet ce qui n&rsquo;est appris à l&rsquo;école que lors du prochain semestre.

Il nous demande alors d&rsquo;expliquer le fonctionnement des rotations dont les structures de données (liste chainée de liste chainées circulaires) étaient imposées par le sujet. Une fois l&rsquo;explication faite, nous devions justifier l’intérêt d&rsquo;un tel dispositif (dynamique) comparé à l&rsquo;utilisation de tableaux statiques par exemple. Je lui explique ce que j&rsquo;en ai pensé, puis pour prouver le tout lui montre ma fonction qui crée cette liste à partir d&rsquo;un nombre indéterminé de paramètres ce qui a semblé lui plaire. Il nous explique ensuite jusqu’où nous aurions pu aller en utilisant d&rsquo;autres permutations et obtenir ainsi un véritable avantage de l&rsquo;aspect dynamique.

Après ce bref échange, il nous situe entre 16 et 18 en fonction du rapport et de la qualité du code. Côté code justement je me suis bien amusé à tester des trucs jamais utilisés auparavant comme les pointeurs de fonction, fonctions à nombre indéterminé de paramètres&#8230; qui apportent une meilleure fluidité de syntaxe. C&rsquo;est ce que je trouve de passionnant à la programmation toujours et encore apprendre de sorte à trouver horrible un code écrit il y a 3 mois, car on sait très bien qu&rsquo;on pourrait le faire d&rsquo;une façon bien meilleure aujourd&rsquo;hui. Nous allons visiblement entrer en compétition avec d&rsquo;autres groupes durant les vacances en résolvant des mélanges particuliers.

En attendant d&rsquo;avoir trouvé le temps de terminer mon site de projets, vous pouvez retrouver l&rsquo;intégralité des sources sur mon github. Cette soutenance nous a motivé mon binôme et moi à continuer à travailler sur le projet nous allons essayer d&rsquo;améliorer la performance qui est loin d&rsquo;être top.

Ces derniers temps j&rsquo;ai eu une vraie baisse de motivation, le semestre actuel est vraiment horrible la seule matière qui me plait correspond au pavé que j&rsquo;ai écrit au-dessus&#8230; Du coup j&rsquo;ai de grandes chances de devoir rattraper quelques matières en avril, même si je vais tenter de me rattraper en travaillant un peu durant ces vacances. Parler des cours n&rsquo;est pas ce qui me branche le plus alors je ne vais pas vous embêter plus longtemps avec ça !

J&rsquo;ai hâte d&rsquo;être en vacances de me détendre, prendre du temps pour moi et jouer de la musique. À très bientôt&#8230;