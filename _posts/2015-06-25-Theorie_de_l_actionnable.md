---
layout: post
title: Théorie de l'actionnable
subtitle: Ou comment ne plus dire "Il faut que" et "Y a plus qu'à"
category: lachezlesclaviers
tags: meeting lean actionnable
feature-image: 2015-06-25-Theorie_de_l_actionnable-feature-image.jpg
---
*Dave Lawper est membre d'une équipe affectée au développement d'une application tout juste budgetée. Toute belle toute neuve sur le papier. Le premier sprint est lancé, l'équipe est motivée. La vie est rose. Au terme du sprint, chacun a bossé dur, l'équipe a bien tourné. Bilan : tous les éléments du backlog n'ont pas été livrés. Les écueils ont été nombreux, et l'équipe n'a pas réussi à atteindre l'objectif fixé. Au terme de ce premier sprint, l'équipe a pris le temps d'effectuer une rétrospective, comme toute bonne équipe agiliste. De nombreuses problématiques ont été soulevées à cette occasion :*

- *De trop nombreuses perturbations extérieures nous ont fait perdre du temps.*
- *Nos estimations n'ont pas été bonnes, parce qu'elles ont été faites par des membres maîtrisant mieux les technos impliquées que la moyenne du reste de l'équipe.*
- *Le code n'était pas bien connu par l'ensemble de l'équipe, et on a perdu du temps à chaque fois qu'on avait à rentrer dans le code d'une nouvelle tâche.*
- *Notre documentation est insuffisante.*

*Le scrum master a donc mis tout le monde d'accord, en apportant les solutions suivantes au terme de la rétrospective :*

- *Eliminez les perturbations extérieures*
-  *Soyez plus larges dans les estimations des tâches*
- *Faites des revues de code*
- *Ecrivez de la documentation au fur et à mesure*

*Le second sprint a été lancé, puis achevé. Tout n'a pas encore été livré cette fois-ci. Le bilan est sans appel. Il est strictement identique au premier. Aucune amélioration notable n'a fait son apparition durant ce second sprint. Pourtant, tout le monde était d'accord sur les solutions aux problèmes mettre en place pour ce second sprint. Et personne n'a rien fait.*

> Le scrum master aurait dû surveiller, et il aurait vu que ça n'allait pas. C'est de sa faute.

Dans un sens, la faute incombe effectvement au scrum master. Mais elle ne se réside pas dans les actions (ou absences d'action) effectuées durant le sprint. La source du problème provient de la rétrospective du sprint précédent. Le scrum master aurait dû appliquer la **Théorie de l'actionnable**, provenant de la méthodologie **LEAN**.

# Theorie de l'actionnable

Lorsqu'une problématique quelconque se pose, et qu'une réunion est organisée pour y apporter une solution, l'erreur à ne pas commettre est d'y répondre par autre chose qu'un **actionnable**.

Avant de définir ce qu'est un actionnable, prêtez-vous à ce petit jeu : Reprenez les exemples de solutions proposés lors de la première rétrospective, et écrivez les solutions que vous auriez proposé vous-même, à la place du Scrum master. Ne lisez pas tout de suite le tableau qui suit.

Ca y est ? Vous l'avez fait ? J'en voix deux ou trois au fond qui ne l'ont pas fait.

Faîtes-le vraiment ! Vous ne pourrez progresser qu'en pratiquant.

C'est fait, cette fois ? Je vous propose donc les solutions suivantes. Elles ne sont pas universelles, mais répondent à la formule de l'actionnable que nous verrons plus tard.

|Non actionnable|Actionnable|
|---|---|
|"Eliminez les perturbations extérieures"|  "Redirigez les perturbations extérieure vers le scrum master dès qu'elles apparaissent" |
|"Soyez plus larges dans les estimations des tâches"|"Lors de l'estimation d'une tâche, faîtes valider le chiffrage par deux autres développeurs"|
|"Le code n'était pas bien connu par l'ensemble de l'équipe, et on a perdu du temps à chaque fois qu'on avait à rentrer dans le code d'une nouvelle tâche"|"Avant de livrer sur le SCM, effectuez une revue de code systématique avec un autre membre de l'équipe"|
|"Ecrivez de la documentation au fur et à mesure"|"Documentez votre code avant chaque livraison sur le SCM"|

> En fait, un actionnable, c'est une action à faire par quelqu'un à un moment bien déterminé  ?

Bingo ! En d'autres termes, un actionnable peut être formulé de la façon suivante :

    Quand <événement> alors <acteur> <action>

On peut reformuler le premier exemple de la façon suivante :

	Quand une perturbation survient alors vous la redirigez vers le Scrum master pour qu'il la prenne en charge.

La formulation initiale n'avait ni **Quand**, ni **qui** ni **quoi**. 
- Le **Quand** doit être clairement identifiable dans sa temporalité et dans son objet. Evitez les "Quand j'ai envie", ou "Quand j'ai le temps" ou toute autre formulation ambigue sujette à la subjectivité. Il est possible d'avoir un **Quand** implicite, qui signifie en général **tout de suite**.
- Le **Qui** doit être une personne unique, pas un groupe. Donner la responsabilité à un groupe ambigu est une assurance que chacun comptera sur les autres pour effectuer l'action.
- Le **Quoi** doit être une action atomique, clairement définie dans son périmètre. Il doit être aussi restreint que possible pour éviter qu'il ne soit que partiellement effectué.

> Oui, mais ton **Quoi** est ambigu. Que fait le scrum master dans ton exemple ?

Le **Quoi** peut être un autre actionnable. On pourrait imaginer ici un actionnable chaîné, avec un acteur différent :

	Quand une perturbation est signalée alors le scrum master planifie la résolution de la perturbation à une date ultérieure à la fin du sprint.

Et le tour est joué.

# Champ d'application

L'**actionnable** est une arme à dégainer dès lors que vous ou votre équipe cherche une solution à une problématique. Que vous la cherchiez seul ou en groupe, ne soyez jamais satisfait avant de trouver une solution **actionnable**. Peu importe la forme, tant qu'elle contient les trois ingrédients du **Quand**, **Qui**, **Quoi**.

En sortant d'une réunion de rétrospective de sprint, typiquement, ne soyez pas satisfait sans un **actionnable** ou une liste d'**actionnables**. Sans ça, vous sortirez d'une réunion inutile, dans laquelle tout le monde aura perdu son temps, et qui n'apportera aucune solution valable. Vous aurez donc fait perdre de l'argent à votre entreprise, qui aurait pu être investi dans quelque chose de plus rentable.

Pensez également à vérifier régulièrement que les **actionnables** périodiques (par opposition aux **actionnables** ponctuels, qui ne sont exécutés qu'une fois) que vous avez mis en place dans le passé ont toujours une raison d'être. C'est l'occasion de créer un **actionnable** dédié. "Quand le sprint se termine, alors le Scrum Master vérifie que chaque actionnable doit être conservé".

# Conclusion

Dès lors que vous pensez à une phrase du type "Il faudrait que", ou encore "On devrait", vous êtes face à un **actionnable** à enclencher. Dès que vous avez une problématique à laquelle répondre, et qu'aucune temporalité n'est apportée, c'est une occasion de créer un **actionnable**. Si votre solution contient un conditionnel, c'est qu'elle n'est pas **actionnable**. Pensez toujours qu'une problématique ne trouve une réponse que dans un **actionnable**. L'essayer, c'est l'adopter.

Cette théorie est applicable dans un champ professionnel, mais aussi dans une sphère privée. Alors faîtes comme *Dave Lawper* : "Quand il sort du boulot ce soir, alors il va acheter du pain pour le dîner" !