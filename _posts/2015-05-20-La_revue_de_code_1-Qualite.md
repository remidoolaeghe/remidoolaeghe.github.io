---
layout: post
title: La revue de code - Partie 1
subtitle: Ou comment gagner en qualité de code
category: lachezlesclaviers
tags: agile revue-de-code
feature-image: 2015-05-20-La_revue_de_code_0-feature-image.jpg
---

*Dave Lawper* a écrit son correctif en vitesse. C'était un vendredi soir, il était tard. Le fix était localisé dans une lib interne, que personne d'autre ne maitrisait. Tous ses petits camarades de jeu étaient déjà partis en week-end, pour un repos bien mérité après une semaine difficile, le laissant seul dans les locaux. *Dave Lawper* avait été laissé à l'abandon, sans aide extérieure. Il lui avait fallu agir, quelque soit le moyen.

Deux jours plus tard, le lundi matin, le premier développeur de l'équipe à récupérer les sources en mélangeant distraitement son café se met à paniquer. Au lancement de l'application, plus rien ne tourne rond. C'est la catastrophe. A mesure que les autres développeurs arrivent, personne ne comprend ce qui se passe. Ca court dans tous les sens comme des poulets sans tête. C'est la débandade.

*Dave Lawper* viendra tard, car sa soirée de vendredi l'a épuisé. A 10h, il arrive dans une équipe au bord de l'implosion. Il faudra deux bonnes heures avant de localiser le problème. Le fix de *Dave Lawper* a introduit une méchante régression que personne ne sait diagnostiquer. Personne n'y comprend rien, et même plus *Dave* qui s'est empressé d'oublier le peu qu'il avait compris au terme d'une session de debug acharné.

L'équipe de *Dave Lawper* a donc été confronté à une problématique de **qualité de code**. Le correctif apporté était de **mauvaise qualité**. La **revue de code** aurait pu éviter ce drame.

> Avant que tu nous expliques autre chose, c'est quoi un code de bonne qualité ?

Le sujet est vaste, et je ne citerai ici qu'une condition nécessaire. Un code de bonne qualité doit passer une revue de code avec succès. 

> Qu'est-ce que c'est que cette réponse bullshit ?

J'avoue, elle était facile. La vraie question à soulever est donc : Que garantit une revue de code au niveau de la **qualité** ? En d'autres termes, qu'apporte la **revue de code** en terme de **qualité** ?

Si *Dave Lawper* avait eu cette épée de Damoclès qu'est la **revue de code** au-dessus de la tête, il aurait su qu'un hack honteux et cradingue n'était pas une option. Si la **revue de code** n'avait pas été une option, une de ses collègues, *Deb Lopez*, aurait effectué une relecture du code, et aurait refusé qu'une telle horreur ne soit livrée sur le **SCM** (**Source Code Manager**). Et ça, *Dave Lawper* l'aurait su avant d'écrire la moindre ligne.

Car oui, la **revue de code** a ce premier effet proactif. Si le développeur sait pertinemment que son correctif sera refusé, il ne tentera même pas de l'implémenter, et il devra se forcer à faire les choses proprement. Il faut bien évidemment partir du constat que le réviseur sera intransigeant et non complaisant, ce qui est une condition pour effectuer une **revue de code** dans les règles de l'art.

> Que se serait-il passé avec une revue de code ?

Remontons un instant le temps et imaginons cette situation alternative où *Deb Lopez* effectue une **revue de code**.

Toute ligne de code écrite par *Dave Lawper* doit être approuvée par *Deb Lopez*. En conséquence, chaque ligne de code doit être aussi irréprochable que possible, i.e. qu'elle soit lisible et compréhensible. Les commentaires, la simplicité, la clarté... sont autant d'aspects que *Deb Lopez* prendra en compte. En conséquence, la **revue de code** permet d'améliorer ces points.

Si la **revue de code** est effectuée, ces aspects sont naturellement soulevés lorsque *Deb Lopez* relit les lignes écrites par *Dave Lawper*. Si elle n'y comprends rien, alors personne d'autre, à l'avenir, n'aura davantage de chance de saisir la substance du code. Si elle n'arrive pas à le lire sur le moment, imaginez donc un pauvre stagiaire catapulté sur ce terrible **hack**.

Dans cette éventualité, la conséquence immédiate pour ce pauvre stagiaire ou ce junior est la suivante : il sera dans l'obligation d'ajouter un nouveau **hack** tout aussi sale par-dessus, dégradant encore davantage la **qualité du code**. Et ça, *Deb Lopez* le sait. Elle demandera donc à *Dave Lawper* de repenser son correctif pour produire un code de **meilleure qualité**.

La **revue de code** a donc un effet réducteur sur le théorème suivant : *"Le mauvais code appelle le mauvais code"*. S'il est bon au départ, la vitesse de sa dégradation sera réduite (ou annulée dans un cas idéal, voire idéaliste). Dans tous les cas, le gain est non négligeable, et la base de code pourra vivre plus longtemps.

SI par contre, *Dave Lawper* avait écrit un code de bonne **qualité** dès le départ, la **revue de code** aurait eu un deuxième effet kiss kool. Il n'est pas à l'abri d'avoir corrigé son bug en oubliant une partie du problème. Connaissant l'application, *Deb Lopez* a une chance non négligeable de repérer un potentiel oubli, ou un effet de bord de la correction. Certes, elle ne pourra pas tous les voir. Si néanmoins elle peut en identifier ne serait-ce qu'un avant que le code ne parte en production, la revue n'aura pas été inutile sur le plan de la **qualité de code**.

> Donc la revue de code améliore la qualité...

Oui, la **revue de code** est une garantie, lorsqu'elle est effectuée dans les règles de l'art, d'avoir systématiquement un code clair, compréhensible et qui fait ce qu'il est censé faire. Les hacks honteux sont éliminés sans aucune forme de pitié et les magouilles dans les recoins sombres de la base de code ne seront plus une option. Le projet part donc avec une base saine et peut grandir sans craindre de se fragiliser sous sa croissance rapide outre des problèmes structurels. Mais ça, c'est une autre histoire.

> Chouette ! Mais au final, ça fait beaucoup de boulot pour un gain plutôt réduit, non ? On va passer des heures et des heures à relire du code pour y gagner pas grand chose...

La **revue de code** en soi est déjà un beau gain de **qualité de code** immédiat. Sur la durée, elle permettra également à la **dette technique** de ralentir son inexorable croissance.

En bonus, la **revue de code**  n'a pas que cet effet. Elle en a d'autres, comme celui d'éliminer les **mauvaises pratiques** !

[Je veux lire la suite]({% post_url 2015-05-20-La_revue_de_code_2-Mauvaises_pratiques %}) !

[Ramène-moi au sommaire]({% post_url 2015-05-20-La_revue_de_code_0-Intro %}) !


