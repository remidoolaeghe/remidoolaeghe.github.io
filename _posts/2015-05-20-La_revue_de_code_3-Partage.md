---
layout: post
title: La revue de code - Partie 3
subtitle: Ou comment partager ses compétences
category: lachezlesclaviers
tags: agile revue-de-code
feature-image: 2015-05-20-La_revue_de_code_0-feature-image.jpg
---

Dans cet univers alternatif où *Dave Lawper* a effectué sa **revue de code** avec *Deb Lopez*, un phénomène s'est produit. Ils se sont rapprochés l'un de l'autre, ont échangé, et se sont <del>embrassés</del> mieux compris.

*Dave Lawper* n'est pas le seul à avoir appris de cette **revue de code**. A sa façon, *Deb Lopez* également en a retiré *quelque chose*.

> *Deb Lopez* aussi ? Elle ne s'est pas juste contentée de taper sur les doigts de *Dave Lawper* ?

Là réside un nouvel effet de la **revue de code**. Lorsque deux développeurs (ou plus, mais c'est une autre histoire) en effectuent une, ils échangent. Ils parlent. Ils discutent. Ils partagent. La **revue de code** est donc un **partage de compétence bidirectionnel** qui se découpe en plusieurs avantages.

#### Partage des nouveautés applicatives
Posons-nous un instant la question : pourquoi *Dave Lawper* s'est-il ce soir-là retrouvé seul face à un code obscur que personne ne connaissait ? 

Peut-être est-ce une lib écrite dans les années 90 que personne n'a retouché depuis. Mais les probabilités sont faibles. Si ce code n'a pas été retouché depuis 15 ans, c'est probablement qu'il est stable.

La véritable hypothèse qui fonctionne dans 90% des cas, c'est que cette lib a été écrite par un seul développeur qui est ensuite parti sans jamais avoir effectué la moindre **revue de code**, ou à défaut de formation du reste de l'équipe pour prendre sa suite. Chacun a pensé comme une autruche, imaginant que personne n'aurait à y retoucher, tout en croisant méchamment les doigts. Et pas de bol, on a découvert un bug.

Peut-être aussi que c'est une lib assez ancienne, truffée de bugs, que des développeurs successifs ont chacun leur tour corrigé à leur manière, sans jamais faire part de leur solution à quiconque d'autre.

Chaque développeur se retrouve alors à poil pour corriger le problème qu'il rencontre, et il se garde bien de partager ce qu'il a fait. A quoi cela servirait-il ? Personne n'y comprendrait rien de toute façon. Pire, il ne saurait peut-être même pas expliquer ce qu'il a fait. C'est en bidouillant qu'il a fini par faire tomber en marche le bousin, par miracle.

Si quelqu'un dans l'équipe de *Dave Lawper* avait eu connaissance de la lib, ou au moins de la partie pouvant intéresser *Dave*, le fix aurait été bien moins douloureux. Il aurait pu comprendre ce qu'il faisait, et produire un code plus en adéquation avec la philosophie de la lib en question.

> Que se serait-il passé avec une **revue de code** ?

*Dave Lawper* aurait pu partager son correctif avec *Deb Lopez* et lui expliquer ce qu'il avait produit, continuant ainsi la grande chaîne de partage, permettant au code de continuer de rester connu par au moins quelqu'un dans l'équipe. Il aurait ainsi pu répandre sa connaissance, mais aussi expliquer les nouveautés ou les changements de comportement possibles.

Plus généralement, la **revue de code** améliore la diffusion de la connaissance du code existant, mais également du changement, de la nouveauté ou de la suppression d'une fonctionnalité. De ce fait, l'application est globalement mieux connue par l'ensemble de l'équipe. Chaque développeur ne connaîtra pas l'ensemble de l'application, mais la part de connaissance de chacun sera bien plus étendue. Et surtout, l'intersection des connaissances de chaque développeur n'aura aucune chance d'être nulle. Donc chaque portion de code sera connue par plusieurs développeurs. Mieux connaître une application, c'est mieux savoir la faire vivre et évoluer.

#### Partage des technos

Ce lundi, la matinée a été une catastrophe. L'absence de **revue de code** a fait perdre une demi-journée de travail à l'ensemble de l'équipe de développement, qui est finalement parvenue à stabiliser un correctif qui fonctionne *a priori*. *Dave Lawper* a donc pu reprendre la tâche sur laquelle il travaillait, et qu'il avait dû interrompre pour se focaliser sur cette fichue lib.

*Dave Lawper* a pu boucler la partie **back-end** de son développement en cours. Tout semble maintenant marcher du feu de dieu. Hélas, il se retrouve bloqué. Le client, ce n'est vraiment pas son fort. Depuis son arrivée dans l'équipe, il a toujours su se débrouiller pour refiler le boulot côté client à quelqu'un d'autre. Cette fois-ci, il allait devoir jouer profil bas, vu le temps qu'il a fait perdre à tout le monde.

A contrecoeur, et persuadé qu'il ne biterait rien au code client, il s'y plonge tant bien que mal. Il parcourt les fichiers, et les lignes. Des expressions bizarres et une syntaxe étrange le déroutent, au point qu'il ne parvient même pas à comprendre quoi que ce soit de son après-midi. Il finit par rentrer chez lui, dépité.

Le lendemain, au **daily meeting**, il déclare timidement n'avoir pas du tout avancé sur sa tâche, sans être capable de se justifier correctement. La journée à venir s'annonçait tout aussi peu glorieuse pour le pauvre *Dave Lawper*.

Que s'est-il donc passé dans l'équipe pour que notre pauvre **Dave Lawper** soit à ce point coincé ? La réponse est simple : absence de **revue de code**.

> Que se serait-il passé avec une **revue de code** ?

Des mois durant, depuis son arrivée dans l'équipe, *Dave Lawper* aurait été impliqué dans des **revues du code front-end**. Il aurait été obligé de sortir de sa zone de confort **back-end** pour comprendre quelque chose à ce qu'il révisait. *Dave Lawper* n'aurait certes rien apporté directement en terme de **qualité de code** de par ses remarques, mais davantage par les questions qu'il aurait été obligé de poser pour y comprendre quelque chose. Le développeur révisé, *Deb Lopez*, aurait pu se rendre compte des erreurs faites dans son code qui le rendait difficile à comprendre. En parallèle, *Dave Lawper* aurait été jeté dans le grand bain avec les brassards, et aurait pu ingurgiter des nouvelles connaissances sur les technos dont il ignorait tout.

Plus généralement, la **revue de code** permet de mener une initiation à des technos utilisés sur un projet, mais non connues par l'ensemble de l'équipe. La **revue de code** sert de tutorial ou de cours par la pratique lorsque le **réviseur** a une connaissance moins vaste que le **révisé** sur un sujet en particulier.

#### Partage des techniques

Le mardi, alors que *Dave Lawper* a passé une bonne partie de la matinée à naviguer vaguement dans des sources toutes plus obscures les unes que les autres pour son oeil novice, il se résoud à tirer le signal de détresse.

Il s'adresse à *Deb Lopez*, qui connait extrêmement bien le code **front-end** et ses technos. De bonne grâce, elle accepte de lui consacrer son après-midi, pour lui expliquer l'architecture et les technos utilisées.

Ravi, au terme de 4 heures de formation épuisantes, *Dave Lawper* rentre chez lui. Motivé, il arrive le lendemain avant le reste de son équipe pour mettre en pratique ses nouvelles connaissances.

La tâche n'est pas évidente pour lui, mais il sait qu'il ne doit pas échouer. Les frasques de début de semaine n'ont pas amélioré sa réputation, et il fallait que la fin de semaine marque un tournant. *Dave Lawper* parvient donc à pondre un code qui marche miraculeusement, bien appuyé par le code **back-end** qu'il a lui-même produit.

Le vendredi matin, après deux jours de dur labeur, il annonce que sa fonctionnalité est bouclée. Sceptique, *Deb Lopez* propose de "jeter un coup d'oeil" à ce qu'il a fait. Sans le savoir, elle veut faire une **revue de code**. La catastrophe lui apparait alors dans toute sa splendeur. Certes, le code fonctionne, mais *Dave Lawper* a tellement tordu le code pour le plier à sa volonté et à sa vision que c'en est devenu imbitable. Tout le code est bon à jeter.

Que s'est-il passé ? *Deb Lopez* a fourni à *Dave Lawper* une formation sur les technos du code **front-end**. Ce qu'elle a en revanche oublié, c'est que *Dave Lawper* n'avait aucune connaissance de la technique pour écrire ce type de code. Il a certes compris comment fonctionnait la techno, mais il n'avait pas acquis le réflexe salvateur de savoir quelle réponse apporter à quelle problématique. En conséquence, il a fait "comme il a pu". 

> Que se serait-il passé avec des **revues de code** ?

Outre le fait que *Dave Lawper* aurait connu les technos utilisées dans le code **front-end**, il aurait été plongé depuis longtemps déjà dans les techniques employées pour répondre aux problématiques déjà rencontrées dans le passé.

Plus généralement, la **revue de code** apporte, dans ce genre de cas de figure, des cas d'école formidables. Lorsqu'un développeur effectue une **revue de code**, il peut montrer quelle solution il a apportée à une certaine problématique. Son **réviseur** pourrait ne pas connaître cette technique de base. A cette occasion, il peut s'en imprégner sur un exemple très concret, sur une base de code qu'il connait par ailleurs bien. Il lui sera d'autant plus facile d'en extrapoler la substance et de se l'approprier.

#### Partage des outils

*Dave Lawper* est dépité. Il a passé un temps fou à écrire ce code, et tout est bon pour partir à la poubelle. Même dans son super **IDE** qui fait tout, même le café, il n'arrivait pas à obtenir des outils intéressants pour lui faire gagner du temps.

La **complétion de code** ne marchait pas terriblement bien, et il devait sans arrêt recourir à sa fonction recherche pour effectuer des actions que son **IDE** habituel savait faire en un claquement de doigt. Ces deux jours de développement ont été une vraie purge pour lui, et voilà que le résultat n'en valait même pas la chandelle.

> Que se serait-il passé avec des **revues de code** ?

*Dave Lawper* aurait eu l'habitude de voir *Deb Lopez* lui montrer son code baignant dans leurs outils naturels. Plutôt que de voir son **IDE** chéri sur le poste de sa collègue, *Dave Lawper* aurait vu de formidables alternatives qui auraient été de vraies purges pour un code **back-end**. Dans un contexte de code **front-end**, elles devenaient un bonheur à utiliser et un formidable gain de productivité. 

Qui plus est, *Dave Lawper* aurait vu *Deb Lopez* les utiliser, et aurait donc vu de ses yeux les capacités de ces outils, et aurait donc été capable de les utiliser à leur plein rendement par lui-même, lorsqu'il aurait plongé les mains dans le cambouis.

Plus généralement, la **revue de code** permet aux développeurs de partager leurs outils, ouvrant ainsi de nouveaux horizons au reste de l'équipe. Ils peuvent également se donner des conseils, voire des trucs et astuces pour gagner du temps ou pour utiliser telle fonctionnalité que l'un d'entre eux ne connaissait pas.

#### Bilan du partage

La **revue de code** est un formidable réseau social "en local". Les développeurs d'une équipe sont invités beaucoup plus régulièrement à se côtoyer d'une part, mais également à partager leur monde avec leurs semblables. Ils ouvriront leur horizon vers des nouveautés, et gagneront en compétence technique ainsi qu'en sociabilité. Le temps du développeur utilisant les techniques sioux apprises des anciens shamans est révolu. L'équipe peut converger vers une meilleure compréhension et utilisation des outils et technologies au sein d'un projet.

[Je veux lire la suite]({% post_url 2015-05-20-La_revue_de_code_4-Cohesion %}) !

[Ramène-moi au sommaire]({% post_url 2015-05-20-La_revue_de_code_0-Intro %}) !