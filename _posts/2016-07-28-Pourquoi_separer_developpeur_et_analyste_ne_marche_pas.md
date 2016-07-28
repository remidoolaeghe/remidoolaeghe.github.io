---
layout: post
title: Pourquoi séparer développeur et analyste ne marche pas
subtitle: Ou le meilleur moyen de décoréler métier et application
category: lachezlesclaviers
tags: management artisan-logiciel
feature-image: 2016-07-28-Pourquoi_separer_developpeur_et_analyse_est_une_mauvaise_idee.jpg
---

*Dave Lawper travaille au sein d'une DSI d'un grand groupe. Il est responsable de l'implémentation d'une application pour laquelle il a reçu des spécifications très détaillées, rédigées par Anne Alyste, une analyste qui lui a prémâché tout le travail. Anne a été en contact avec le métier durant des semaines, à décortiquer le moindre petit bout de métier qu'elle aura pu extraire des centaines d'heures de réunions passées avec les experts métier. Ses spécifications sont très détaillées, et il ne manque pas un seul aspect du métier concerné par le projet".*

*La spécification est extrêmement complète. Le beau document brillant en papier glacé de 300 pages a pu être remis à Dave Lawper. Tout est limpide, il ne reste pas une seule zone d'ombre. Dave Lawper n'a vraiment plus qu'à se remonter les manches et à faire une traduction machine dans son langage préféré presque mot-à-mot. Toutes les notions métier ont été simplifiées et traduites pour que Dave n'ait aucune question à se poser. Dave est heureux de ne pas avoir à apprendre plus d'une centaine de mots étranges du métier auxquels il n'aurait de toute façon rien compris. Il remercie intérieurement Anne de lui avoir à ce point prémâché le travail et simplifié au maximum.*

*L'application réalisée par Dave Lawper part en production. Aucun bug n'est remonté. Sa hiérarchie est aux anges, et l'application tourne durant des années sans aucune anomalie. Mais un jour, un gars du métier vient voir Dave Lawper, un certain Lex Permétier. Certaines fonctionnalités lui paraissent étranges, et le comportement ne colle plus vraiment à la réalité du métier. Il est temps de faire évoluer l'outil devenu obsolète.*

*Dave Lawper replonge dans l'application. Après des années sans y avoir touché, il la redécouvre complètement, comme s'il n'y avait jamais touché de sa vie. Lex lui pose des questions, puisqu'il n'a pas participé à l'élaboration de l'application à l'époque. Il tente de retrouver ses petits avec l'aide de Dave, en parcourant le code de l'application pour comprendre l'existant et faire une sorte de rétro-documentation. Lex et Dave ignorent ou ont oublié qu'il existait une documentation, perdue au fin fond d'un wiki oublié depuis des siècles.*

*Lex utilise des mots compliqués, que Dave ne comprend pas toujours. Un PAN ? Une nomenclature ? Un parcours client ? Un tunnel de commande ? Une déclinaison ? Mais de quoi il parle, ce Lex ? En parcourant le code, Dave Lawper ne retrouve pas les notions que lui indique Lex. Devant le désarroi de Dave et son air ahuri, Lex soupire bruyamment : "Ah, ces développeurs. Ils ne comprennent jamais rien à ce qu'on fait".*

Mais que s'est-il passé avec cette application ? Elle était pourtant propre, dépourvue du moindre bug, et jamais un utilisateur n'est venu remonter le moindre problème depuis sa mise en production. Une application parfaite, en somme ? Pas si sûr, lorsqu'on regarde les entrailles de la bête.

Notre bon vieux Dave a été victime du zèle d'Anne Alyste. Elle a passé tout son temps avec un expert métier, et a effectué de nombreuses traductions pour que l'équipe de développement n'ait pas à se poser de questions. Et c'est là que se révèle sa plus grande erreur. A moins que ce ne soit celle de son donneur d'ordre ? Lorsque Dave Lawper a implémenté son application, il s'est appuyé sur des spécifications où les notions métier avaient été au mieux altérées, au pire abstraites et simplifiées. Lorsqu'il a commencé à coder, il n'a eu aucun moyen de se raccrocher à la moindre discussion qu'il aurait dû avoir avec un expert métier. Dans son code, toutes ces notions ont donc disparu, au profit d'une simplification à outrance du vocabulaire. Le code n'était donc plus métier, mais purement une suite d'instructions sans aucune saveur de métier. Impossible pour un développeur de comprendre exactement ce que le code fait, ni de le rattacher aisément aux notions perdues dans les limbes de l'abstraction. Au mieux, quelques commentaire hiératiques peuvent lui donner des indices de ce que son code signifie vraiment, mais rien de plus.

Et si Anne Alyste et Dave Lawper n'avaient été qu'une seule et même personne ? Dans le pire des cas, Dave n'aurait pas fait mieux et se serait retrouvé tout autant le bec dans l'eau. Néanmoins, il aurait eu une chance supplémentaire de faire davantage ressembler le code à la réalité du métier en intégrant les termes métier **directement** dans le code. L'augmentation du nombre d'intermédiaire a inévitablement augmenté l'effet de téléphone arabe. L'application au bout du compte répond peut-être toujours au besoin, mais au prix de ne plus parler le même langage que le métier ?

Et vous, êtes-vous analyste, développeur ou les deux ?

Source d'inspiration et pour aller plus loin : 

<a href="http://blog.infosaurus.fr/public/docs/DDDViteFait.pdf">DDD vite fait</a>
