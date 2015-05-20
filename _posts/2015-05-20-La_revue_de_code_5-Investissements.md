---
layout: post
title: La revue de code - Partie 5
subtitle: Ou comment miser sur le futur
category: lachezlesclaviers
---

La semaine de *Dave Lawper* a été une des pires de sa carrière. Lorsqu'il repart le vendredi soir, il est dépité. Le projet sur lequel il travaille n'est déjà pas des plus folichons, et les obsctacles s'amoncellent devant lui sans qu'il n'ait jamais l'impression d'en voir le bout. Les cinq derniers jours risquent d'achever ce qui reste de sa détermination

Sur le trajet de son domicile, il peste, il rage. Il compare son entreprise à une bande de cochons troubadours des mers du sud. Il les maudit jusqu'à la treizième génération. Il rêve de démissionner, et d'abandonner le code qu'il a écrit, seul, sur ce projet.

Dès le lundi, il demande à son directeur de projet, le grand chef de son département dans l'ESN (ou SSII) qui l'emploie, de lui trouver autre chose. Bien embêté, le directeur de projet lui indique qu'il n'a aucune mission en sous-effectif en ce moment. En revanche, il lui en propose une dans une autre région de France. *Dave Lawper* ne réfléchit pas, et accepte de se faire muter pendant quelques mois. Il fait ses bagages et part au bout de quelques jours.

Pendant ce temps, son ancienne équipe continue de travailler. La recette découvre par ailleurs un comportement étrange dans une fonctionnalité, et génère un ticket de bug qui se retrouve attribué à *Deb Lopez*. C'est une sombre histoire de **multi-tenant**, ou un truc du genre. *Deb Lopez* n'a aucune idée de ce que cela signifie. Elle a un background très orienté **front-end**. De ce qu'elle a compris, ça a l'air de toucher à la base de données. *Brrrrr, la base de données*. Une fausse manip, et ce sont des paquets entiers de données qui peuvent se retrouver corrompus.

*Deb Lopez* est seule, sur ce coup. Comme toujours dans l'équipe, les tickets de bugs sont attribués à un membre plus ou moins au hasard, et chacun se débrouille avec ça. Il va bien falloir plonger les mains dedans.

Après deux jours de tentatives infructueuses et prudentes, *Deb Lopez* est toujours au point mort. L'ennui, c'est que ce problème nécessite une mise en production rapidement. Il faut donc mettre les bouchées doubles, et absolument diagnostiquer et réparer rapidement.

Le vendredi soir, *Deb Lopez* se retrouve seule, à se battre contre son bug. Elle finit néanmoins par comprendre ce dont il s'agit, vers 21h. Elle est pressée de rentrer chez elle, et épuisée. Néanmoins, le correctif ne peut pas attendre. Elle tente plusieurs manipulations, et Ô miracle, finit par trouver un correctif qui fonctionne bien sur l'instance de recette. Trop heureuse, elle livre son code et part en week-end.

La suite, vous la connaissez. L'histoire se répète. *Deb Lopez* endosse le rôle de *Dave Lawper*, et les catastrophes s'enchaînent.

Tout ça pourquoi ? Simplement parce que la **revue de code** ne fait pas partie des moeurs de l'équipe. Le code a été écrit par *Dave Lawper*, une pointure dans ce domaine. Mais il n'a jamais été revu par qui que ce soit. C'est un code de très grande qualité, mais les erreurs arrivent même aux meilleurs. La **revue de code** n'aurait probablement pas mis en évidence cette faiblesse. Néanmoins, quelqu'un dans l'équipe aurait eu connaissance de cette partie applicative. Le correctif aurait donc été bien plus rapide, facile et sûr.

Nous touchons au dernier avantage de la **revue de code** pour cette série d'articles. La **revue de code** casse le cercle vicieux du **code pourri**.

Vous connaissez probablement l'histoire sans fin de la réécriture de code : *Un développeura arrive sur un projet, et s'arrache les cheveux devant le code. Il propose de tout réécrire à son chef, qui lui donne le feu vert. Après quelques années, il finit par partir vers des prairies plus vertes et des horizons plus prometteurs, et se fait remplacer par un nouveau développeur. Ce dernier s'arrache les cheveux devant la qualité du code, et propose à son chef de tout réécrire...*

Ce cercle vicieux est plus ou moins celui vécu par *Dave Lawper* et *Deb Lopez*. La **revue de code** permet de le casser, car il ne survient généralement que parce que le code est écrit par un seul esprit, et jamais plusieurs. La **revue de code** partage les connaissances et fait tendre la **qualité de code** vers les sommets.

La **revue de code** est donc un **investissement pour l'avenir**. Si vous n'avez pas à réécrire trois fois chaque module d'une application historique, vous allez gagner un paquet de temps. Idem lorsqu'il s'agit d'enrichir une fonctionnalité existante. Si elle est mal architecturée ou mal comprise, il y a de fortes chances pour qu'elle finisse par être réécrite par un autre que l'auteur initial. La **revue de code** tend à gommer cette tendance dévastatrice pour les délais d'un projet.

Ainsi, le départ d'un auteur de l'application n'est pas un traumatisme, et l'équipe peut continuer de vivre tranquillement avec ce vide qui sera un jour ou l'autre remplacé par une nouvelle embauche. La transition est ainsi bien moins traumatisante et l'équipe peut avancer plus sereinement sans voir sa maîtrise technique du projet en pâtir plus que de raison.

[Je veux lire la suite]({% post_url 2015-05-20-La_revue_de_code_6-Bilan-et-FAQ %}) !

[Ramène-moi au sommaire]({% post_url 2015-05-20-La_revue_de_code_0-Intro %}) !