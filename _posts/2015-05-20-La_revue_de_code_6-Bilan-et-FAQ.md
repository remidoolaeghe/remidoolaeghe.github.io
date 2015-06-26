---
layout: post
title: La revue de code - Final
subtitle: Ou pourquoi l'adopter
category: lachezlesclaviers
feature-image: 2015-05-20-La_revue_de_code_0-feature-image.jpg
---



> Dis donc, tu vas encore nous bourrer le mou longtemps avec la revue de code ?

Vous avez raison, il est l'heure de faire le bilan de tout ce que la **revue de code** peut vous apporter.

Nous avons suivi les déboires de ce malheureux *Dave Lawper*. Vous me direz certainement que la plupart de ces situations sont caricaturales. Néanmoins, vous les avez rencontré (ou les rencontrerez un jour) toutes à un degré plus ou moins élevé.

Qui n'a jamais été affecté à un projet dont la **qualité de code** était épouvantable, au point que vous osiez à peine ouvrir les yeux de crainte de vous brûler la rétine ? Ou de peur de tout fiche en l'air parce que vous n'y comprendriez rien ? Ou de juste glisser un correctif discrètement entre deux lignes bien cradingues parce que vous craigniez d'introduire une régression en poussant le vice plus loin ? La **revue de code** est un excellent remède pour relever la **qualité du code**.

Qui ne s'est jamais retrouvé catapulté dans un environnement technique nouveau, laissé à l'abandon, où vous deviez faire marcher quelque chose tant bien que mal, quel que soit le moyen ? Et au final pour vous faire dire que votre code était cradingue et mal architecturé ? La **revue de code** aide à la propagation des **bonnes pratiques**.

Qui n'a jamais observé une techno de loin, dans un projet, sans jamais oser y toucher à cause d'un grand gourou qui avait tout écrit sans jamais rien expliquer de ce qu'il avait fait ? La **revue de code** encourage le **partage des connaissances, des compétences**.

Qui ne s'est jamais retrouvé dans une équipe où chacun codait dans son coin, et où les réunions hebdomadaires étaient le seul moment où vous échangiez vaguement quelques phrases avec vos collègues ?  La **revue de code** est un catalyseur pour la **cohésion** d'une équipe.

Qui n'a jamais vécu le cercle vicieux de la réécriture de code en boucle, où vous débarquez sur un projet sans que personne ne sache vous expliquer quoi que ce soit sur les composants que vous êtes censé reprendre en main ? La **revue de code** est un **investissement pour l'avenir**.

Alors, qu'attendez-vous pour vous y mettre ?

> Tu essaies de nous vendre du rêve, mais j'ai quand même quelques objections, là !

C'est donc le bon moment de faire une petite...

# FAQ

> C'est bien gentil de nous conseiller de faire des revues de code, mais tu ne nous dis même pas comment faire !

Avant de savoir faire, il fallait bien en comprendre l'intérêt. Ce sera donc l'objet d'un prochain article à paraître.

> La revue de code fait perdre beaucoup de temps, vu qu'il faut le faire avant chaque livraison (commit).

A la louche, une revue de code doit prendre 5% du temps d'écriture du code lui-même. En contrepartie, votre code sera : 

 - plus lisible, plus compréhensible. Un développeur repassant dessus perdra donc beaucoup moins de temps à en saisir la substance. Quand on sait qu'un développeur passe 70% de son temps à lire du code...
 - moins buggé. Vous passerez donc moins de temps à produire des correctifs, et plus de temps à ajouter de la fonctionnalité.
 - mieux connu. Un développeur qui a effectué une revue de votre code, ou d'une partie, aura des billes pour investiguer un problème futur englobant votre code.
 - mieux conçu puisque exempt de hack affreux. Il ne nécessitera donc pas de refactoring à tout va (ou beaucoup moins vite).
 - Et j'en passe

> C'est bien beau, mais il faut que le réviseur fasse bien son travail et regarde vraiment le code en profondeur et avec attention.

Oh mon dieu, il faut donc bien faire son travail !

> Tu dis que la revue de code garantit un code de bonne qualité, mais pas forcément.

Oui, la qualité ne sera pas forcément **bonne**. Mais elle sera toujours **meilleure** que dans le cas de base.

> Dans ton exemple avec Dave Lawper, il a livré son code le vendredi soir parce que c'était urgent. Et dans l'alternative où il fait la revue de code, ça ne l'est pas ! Tu triches !

Oui, j'avoue. Mais posons-nous un instant la question : vaut-il mieux livrer un code pourri partant en production, ou attendre deux jours pour assurer le coup ?

> La revue de code est d'après toi une bonne forme de partage de connaissances. Une bonne formation est tout aussi efficace.

Non, pour une simple raison. Les formations sont généralement prodiguées lorsque vous arrivez sur un projet ou que vous découvrez une techno. Vous n'avez donc pas encore eu le temps de tomber dans les pièges qu'il/elle cache ou de vous familiariser avec. Vous raterez probablement bon nombre des subtilités que votre formateur pourra vous amener.

La revue de code étant régulière, vous allez être confronté régulièrement mais sans overdose à ce code ou cette techno. Entre deux revues, vous aurez le temps de réfléchir, vous y confronter à nouveau, et avoir de nouvelles questions lors de la session suivante. En cela, la revue de code est dix fois plus efficace.

> Selon toi, Dave Lawper aurait dû demander de l'aide quand il a commencé à patauger dans le code client. A ce compte, on finit toujours par être dérangé par tout le monde et on n'avance jamais !

C'est un vaste sujet, et il mériterait un article. En quelques mots, évitez en effet de déranger vos pairs à tout bout de champ. Interrompre quelqu'un concentré sur une tâche lui fait perdre le focus et il aura besoin de temps pour se reconcentrer.

Néanmoins, lorsque vous êtes vraiment bloqué sans aucune bonne alternative, il faut demander de l'aide pour éviter de perdre des jours et des jours pour rien, juste pour économier un quart d'heure de son temps à un collègue. Une équipe est aussi faite pour cela.

----------

J'espère vous avoir convaincu de donner une chance à la **revue de code**. De mon expérience, l'équipe à laquelle j'appartiens en a retiré beaucoup de positif au final, même s'il faut un petit temps d'adaptation. Alors essayez-la donc chez vous !

[Ramène-moi au sommaire]({% post_url 2015-05-20-La_revue_de_code_0-Intro %}) !