---
layout: post
title: La revue de code - Partie 2
subtitle: Ou comment chasser les mauvaises pratiques
category: lachezlesclaviers
feature-image: 2015-05-20-La_revue_de_code_0-feature-image.jpg
---

Le correctif de *Dave Lawper* se situait au fin fond d'une librairie historique, écrite en **C**. Or, *Dave Lawper* a un background très orienté nouvelles technologies. **Java**, **Groovy**, **Scala**, il connait bien. Tout ce qui date d'avant les années 90, beaucoup moins. Les pointeurs du **C**, il en a entendu parler. Ca ressemble même plutôt aux références en **Java**, après tout. Mais les pointeurs de pointeurs, ça l'a toujours laissé perplexe. Et pas de chance, la librairie en question en était truffée.

*Dave Lawper* n'est pas la dernière des andouilles. Il sait se servir d'un debugger, même en **C**. Il a dégainé le meilleur qu'il connaisse, et il a suivi la piste du bug. Il a même su diagnostiquer le problème. Même si les profondeurs du **C** resteront toujours un mystère pour lui, il est capable d'écrire du code, dont la syntaxe lui rappelle furieusement celle de **Java**. Après deux ou trois tentatives au hasard, le compilateur finit par lui indiquer que son code est correct, d'un point de vue lexical. Et si le résultat n'est pas le bon, il suffit d'ajuster le code. *Dave Lawper* réussit donc au final à converger vers un code *qui marche*.

Rappelez-vous, c'était vendredi soir. Bien trop heureux de pouvoir quitter les locaux de sa boîte avant 22 heures, il n'avait pas cherché plus loin. *Dave Lawper* n'attendait pas mieux de son correctif. Il *marchait*, après tout. Peu importe le moyen employé. Ce qu'il avait écrit était compréhensible de son point de vue, et même pas forcément moche.

Mais lorsque *Deb Lopez*, développeuse aux multiples talents dont celui d'être vétéran dans les langages bas niveau,  est enfin tombée sur le correctif produit par *Dave Lawper* le lundi matin, elle laissa sur le carreaux plusieurs touffes de cheveux violemment arrachées. Un charnier. Une horreur sans nom. Un cow-boy des pointeurs était passé par là, et le résultat n'était pas joli joli. Et ça, *Deb Lopez* l'a vu au premier coup d'oeil. Des déréférencement utilisés à grand coups d'adresses mémoire et des pointeurs tous azimuts, massacrés sauvagement. Elle avait devant les yeux une usine de fabrication de pointeurs nuls et d'erreurs de segmentation. Un vrai massacre. L'horreur. L'apocalypse. De quoi tuer sur le coup [Dennis Ritchie](https://fr.wikipedia.org/wiki/Dennis_Ritchie) une seconde fois. 

*Deb Lopez* aurait pu sauter à la gorge de *Dave Lawper*. Encore une bonne raison de créer une tension entre les deux développeurs, à cause d'une simple incompréhension, venant de deux mondes très différents.

> Et s'il avaient fait ensemble une **revue de code** ?

Je vois que vous suivez. Et ça, ça me fait plaisir.

Oui, et s'il avaient fait une **revue de code** ensemble ? La situation aurait été très différente. Imaginez donc.

*Dave Lawper a bouclé son correctif. Il est 21h53, un vendredi soir. Il ne voit plus personne dans les locaux. *
*"Qu'à cela ne tienne, j'attendrai lundi matin pour ma livraison, après ma revue de code", pense-t-il.*
*Après un week-end reposant, il arrive à 10h le lundi matin. Son correctif n'est pas livré. Après tout, il n'y avait pas d'urgence. Il salue ses collègues, sereins de travailler en toute quiétude. Dave a donc le temps de se poser à son poste, et de commencer sa semaine dans le calme.*
*Une fois son poste démarré, il se souvient de la revue de code qu'il doit effectuer. Il appelle Deb Lopez, et lui soumet sa proposition de correction. Au bout de cinq secondes à peine, Deb Lopez tressaille sur sa chaise.*
*"Qu'est-ce que tu nous a fait là ?" demande-t-elle.*
*Dave Lawper lui explique alors son intention, en lui détaillant sa démarche. Deb Lopez met alors le doigt sur ce qui coince.*
*"Tu ne devrais pas t'y prendre de cette façon", affirme-t-elle.*
*Elle prend le clavier, et lui explique ligne après ligne ce qu'il a fait. Horrifié, il comprend son erreur. Il voit alors Deb Lopez proposer une bien meilleure correction. Il n'avait pas conscience de sa mauvaise pratique, et aura appris que c'en était une.*
*Le code correct est alors livré, et chacun peut récupérer le correctif et l'utiliser sur son poste, en tout sérénité.*

Alors, que s'est-il passé dans ce scénario idéal ? *Dave Lawper*, dans son ignorance, a implémenté un correctif sans se rendre compte de ce qu'il faisait vraiment. Certes, son code fonctionnait dans le cas précis qu'il a testé, mais pas dans beaucoup d'autres. 

*Deb Lopez* a pu mettre en évidence la **mauvaise pratique**, et l'expliquer avec un exemple concret (le bug à l'origine du correctif) en quoi c'en était une. Le correctif a pu servir de support d'explication. Comme *Dave Lawper* était extrêmement impliqué dans ce code, il a pu comprendre très facilement ce dont il retournait, et a pu se focaliser sur ce qui importait vraiment. Connaissant le code et ce qu'il était censé faire, il lui a été facile de comprendre l'explication fournie par *Deb Lopez*. Il ne refera pas cette erreur de sitôt, parce qu'il aura appris la **bonne pratique**.

Nous sommes tous amenés un jour ou un autre à toucher un code dans un projet tout nouveau et inconnu. Parfois même dans un langage que nous n'avons jamais vu. Qui pourrait blâmer *Dave Lawper* de ne pas respecter ce qu'il ignore ?

Les **mauvaises pratiques** ne se limitent pas à l'ignorance d'un langage. En arrivant sur un projet, personne n'en connait les subtilités, ni les points sensibles. Comment pouvez-vous savoir que votre correctif, si parfait vous semble-t-il, n'a pas révélé une faiblesse de la base de code existante ? Et si vous aviez échappé à la couverture de test ? Un développeur plus ancien et expérimenté sur le projet peut immédiatement pointer du doigt l'erreur que vous avez commise, et que vous ne pouviez pas deviner. Aucune architecture n'est parfaite, et vous n'êtes pas censé le savoir dès le premier jour.

Et même en connaissant un projet, pour peu qu'une nouvelle techno y soit ajoutée et que vous ne la connaissiez pas, il peut vous arriver de bidouiller un bout de code pour la plier à votre volonté, sans savoir que vous essayez de couper votre steak avec la fourchette.

Votre **réviseur de code** mettra le doigt dessus, et vous apprendra les bonnes pratique sur les outils que vous ne maîtrisez pas encore. De de fait, votre **qualité de code** en sera grandie et vous permettra de comprendre vos erreurs. Les **mauvaises pratiques** seront chassées bien plus rapidement que si vous aviez appris de vos erreurs ou par l'expérience seule.

Au final, outre le fait que vous aurez gagné en **qualité**, la **revue de code** vous aura également servi de réseau social. C'est bien par le **partage** de connaissance que vous êtes monté en compétence. Et c'est un nouvel effet de la **revue de code**

[Je veux lire la suite]({% post_url 2015-05-20-La_revue_de_code_3-Partage %}) !

[Ramène-moi au sommaire]({% post_url 2015-05-20-La_revue_de_code_0-Intro %}) !