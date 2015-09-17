---
layout: post
title: Scrum vs Kanban, le duel
subtitle: Entre les méthodes à Gilles, mon coeur balance
category: lachezlesclaviers
tags: scrum kanban agile
feature-image: 2015-09-17-Scrum_vs_Kanban-feature_image.jpg
---

Lorsqu'on parle des méthodes <del>à Gilles</del> agiles, **Scrum** est généralement le premier mot venant aux lèvres. Ce **cadre** est pour la plupart le point de départ lors de la première expérimentation de l'**agilité**. Parfois, **Scrum** est adapté, et répond plutôt bien au besoin. D'autres fois, ce **cadre** nécessite d'être tellement plié et tordu pour répondre à un besoin qu'il n'a plus rien à voir avec les préconisations d'usage. Le point de départ n'est donc pas forcément le bon. **Kanban** pourrait également répondre au besoin initial. Ou pas tout à fait. Mais alors, comment choisir ?

**Pré-requis** : Cet article considère que vous avez une connaissance au moins théorique sur le fonctionnement des deux **cadres** que sont **Scrum** et **Kanban**. Si ce n'est pas le cas, vous pourriez ne pas saisir toute la substance de cet article.

Ces deux **cadres méthodologiques** répondent à deux problématiques différentes. **Scrum** a pour vocation de **fiabiliser les dates de livraisons**, là où **Kanban** se focalise sur la **vitesse de livraison**, ou **Time To Market (TTM)**.

> Est-ce si simple que cela, dans les faits ? 

Peut-être pas. Un certain nombre de paramètres sont à prendre en compte en fonction de vos besoins. Chacun des deux **cadres méthodologiques** que sont **Scrum** et **Kanban** les adressera différemment. Et si nous les passions en revue ? C'est parti !

# Duel

## Réactivité
Les **méthodes agiles** ont pour vocation de permettre une bonne **réactivité**. Il ne faudra que peu de temps pour prendre en compte et traiter une demande urgente. Néanmoins, **Kanban** est plus adapté sur ce point. Lorsqu'un **sprint** est commencé dans **Scrum**, il est fortement déconseillé (pour ne pas dire interdit !) de modifier le **backlog de sprint**, au risque de mettre en péril la **date de livraison** ou le **périmètre** du **sprint** en cours. En cas de changement de priorité ou d'arrivée d'une urgence à traiter, il sera bien souvent nécessaire d'attendre l'achèvement du **sprint** pour planifier ladite tâche. Les **sprints** étant généralement courts, ce n'est souvent pas un problème. Cela dit, une urgence en prod n'attend pas...

**Kanban** s'en tire haut la main dans cette situation, puisque l'équipe ne s'est pas engagée dans un **sprint** sur un **périmètre** fonctionnel. Elle peut alors abandonner ce qu'elle a entamé, et se consacrer avec énergie au traitement de l'urgence, et ainsi répondre très rapidement à l'apparition de la tâche.

> Dans **Scrum**, il suffit d'éliminer un item du backlog de sprint et de le remplacer par l'urgence à traiter, non ?

Dans la théorie, cette idée peut paraître séduisante. Dans les faits, cela fonctionne rarement. Les **histoires** présentes dans le **sprint** ont toute une **estimation de coût**, certes, mais un indicateur plus fourbe n'apparaît pas toujours clairement. Chaque **histoire** a également un **facteur de risque** (d'un point de vue de tenue de délai), dû généralement à sa complexité ou sa difficulté d'exécution, voire à sa nature exploratoire. Une équipe **Scrum** aura tendance à limiter ce type de **histoires** dans un **sprint** afin d'assurer le coup. Si par malchance la tâche urgente est **hautement risquée** et qu'elle en remplace une autre tâche de **même coût apparent** mais de **risque très faible**, l'équipe prend un risque supplémentaire et accepte de s'engager sur une pente savonneuse, puisque le **sprint** sera plus difficile à boucler dans les temps. Donc en pratique, modifier un **backlog de sprint** en cours de route est rarement une bonne idée et mène trop souvent à la catastrophe.

Lorsqu'on parle de **réactivité**, cela ne se cantonne pas à la capacité à répondre à l'urgence. Il s'agit également de se rendre rapidement compte des goulets d'étranglement dans le tableau des tâches. **Kanban** limite le nombre de tâches dans une colonne donnée du tableau de tâches. Lorsqu'une **bulle d'air** apparaît dans le tableau (une colonne vide), cela constitue un indicateur immédiat qu'un obstacle dans la colonne précédente obstrue le flux des tâches dans le tableau, et il est aisé de l'identifier et de le traiter dès son apparition.

![Tableau de Kanban avec une bulle d'air dans la colonne "A livrer"]({{ site.images }}/2015-09-17-Kanban-bulle-d-air.png){: .center-image}

**Scrum** ne permet pas d'identifier d'une façon aussi visuelle ce type de problématique, et nécessitera généralement plusieurs sprints avant de pouvoir réaliser qu'un problème persiste.

**Kanban** marque donc son premier point sur la **réactivité** tant au niveau du traitement de l'urgence que de l'**inspection** et l'**adaptation**.

## Prévisibilité/Visibilité
**Scrum** et **Kanban** se démarquent fortement sur le plan de la **prévisibilité** et prennent chacun une direction totalement opposée.

**Scrum** est basé sur la notion de **sprint**, qui implique un **engagement de l'équipe** sur un **périmètre réduit** pour une **durée fixe**. La conclusion de la **prévisibilité** est donc immédiate, puisqu'il devient évident à quelle date une **histoire** sera livrée en théorie à partir du moment où elle est planifiée dans un **sprint**. En revanche, il n'est pas possible pour un **backlog** complet de se voit attribuer un ensemble de date de fin pour chacune des **histoires**, qui reviendrait à non pas faire du **Scrum** mais du **cycle en V**.

Afin d'assurer cette **prévisibilité**, il est nécessaire pour chaque **histoire** d'être estimée de façon relativement fiable, afin de réduire autant que possible le risque de lever un loup au beau milieu du **sprint** et de le mettre en danger.

Ces estimations et cet engagement permettent de dessiner au jour le jour un **graphique d'avancement** ou **burndown chart**, afin de visualiser quotidiennement la bonne avancée des **histoires** dans le temps et réagit en cas de divergence entre la courbe d'avancement théorique et réelle.

![Tableau d'avancement de Scrum]({{ site.images }}/2015-09-17-Burndown-chart.gif){: .center-image}

Ce graphique devient un bon indicateur de la charge du **sprint**, et permet de déterminer s'il est nécessaire de retirer une **histoire** ou si, dans des cas plus rares, il est possible de charger la barque avec une nouvelle **histoire** courte.

**Kanban** ne dispose pas de cet outil, puisque les **estimations** sont optionnelles dans ce **cadre**. Etant donné que l'équipe ne s'engage pas sur un **périmètre** sur une **durée**, les estimations deviennent bien moins centrales que dans le cadre **Scrum**. Un tel graphique n'a donc pas de sens (que mettre en abscisse et en ordonnée, là où **Scrum** utilise le TAF - travail à faire - et la date courante ?). En ce sens, il devient très ardu de fournir une date de livraison d'une **histoire** en cours de traitement. **Kanban** n'indique donc aucune **date de livraison**, et donc aucune **(pré)visibilité**.

**Scrum** évite également le phénomène de la **histoire** qui "sera prête quand elle sera prête". **Kanban** autorise de travailler sur une **histoire** quelle que soit sa taille. Il est tout à fait possible de se retrouver avec une **histoire** dont le traitement peut durer 6 mois, puisqu'elle n'aura pas eu besoin d'être préalablement découpée en **histoires** plus petites pour rentrer dans la durée d'un **sprint**. Il y a donc un risque plus fort d'effet tunnel pour des **histoires** de gros volume. **Scrum** force donc à travailler sur des **histoires** de taille beaucoup plus gérables et donc prévisibles. **Scrum** est donc particulièrement adapté pour une équipe ayant des difficultés à fiabiliser ses **délais de livraison**.

**Scrum** marque donc son premier point sur la **(pré)visibilité**.

## Adaptabilité/Introspection
Le propre d'une **méthode agile** est de ne pas être figée dans le temps. Elle préconise d'expérimenter, d'inspecter et d'adapter les points qui ne fonctionnent pas. En ce sens, **Kanban** et **Scrum** ne diffèrent pas.

En revanche, chacun de ces deux **cadres** se focalise sur une problématique différente.

L'outil privilégié de **Kanban** est le **diagramme de flux**.

![Diagramme de flux de Scrum]({{ site.images }}/2015-09-17-Diagramme de flux.gif){: .center-image}

Ce diagramme permet de visualiser la durée qui s'est écoulée entre le début et la fin de traitement d'une **histoire**. Il devient alors facile de visualiser quelle étape est la plus **chronophage**, et ainsi de se focaliser sur son amélioration.

**Scrum** préfère le **tableau d'avancement** comme cité au paragraphe précédent. Le **flux** n'apparaît pas, et la durée entre le début et la fin d'une **histoire** n'a pas d'importance, tant que son traitement tient dans le **sprint** dans lequel elle est planifiée.

Aucun des deux **cadres** ne marque de point, étant donné qu'ils répondent chacun à une problématique différente.

## Structuration/Organisation
**Scrum** impose un minimum de **structuration** qui se matérialise à travers les **rendez-vous** forts suggérés par le **cadre** : la **réunion de planification de sprint**, les **mêlées quotidiennes**, la **démonstration de fin de sprint** et la **rétrospective de sprint**. L'équipe dispose donc d'un garde-fou lui permettant de ne pas déraper et auquel se raccrocher en période difficile. Les objectifs de ces réunions sont clairement définis, et il devient bien plus facile de ne pas laisser échapper un aspect important dans la conduite du projet. **Scrum** est donc particulièrement adapté pour une équipe dont l'expérience agile est encore un peu verte.

En revanche, **Kanban** laisse beaucoup plus de liberté sur ces aspects, puisque le **cadre** ne préconise pas cette structuration aussi évidente. Ces rendez-vous peuvent avoir lieu, mais leur déclenchement n'est pas "automatiquement" défini par le **cycle de vie** d'un **sprint**. C'est alors à l'équipe de garder un oeil sur les indicateurs et de provoquer volontairement ces rendez-vous lorsqu'ils deviennent nécessaires. A contrario, il est donc possible de les éviter lorsqu'ils ne sont pas nécessaires. **Kanban** nécessite donc davantage une équipe expérimentée capable de s'autogérer, et dont les membres sont aptes à travailler tous ensemble en bonne intelligence et à avancer dans la même direction.

Ici encore, aucun des deux **cadres** ne remporte de point, puisqu'ils répondent chacun à une problématique différente.

## Composition des équipes
**Scrum** préconise d'impliquer dans un **sprint** une équipe **multidisciplinaire**. Etant donné qu'un livrable doit être produit en fin de **sprint**, il est hors de question de n'impliquer que des développeurs ou que des recetteurs. Il est donc nécessaire d'adjoindre à l'équipe les membres impliqués dans toute la chaîne de production du livrable. Il n'est donc pas question de constituer une équipe de spécialistes purement focalisée sur un seul aspect du **sprint**.

**Kanban**, en revanche, permet l'implication de **plusieurs équipes de spécialistes** pour **un tableau de tâches** (là où Scrum a une équipe **multidisciplinaire**). Chacune des équipes de spécialistes peut être affectée à une ou plusieurs colonnes du tableau et ainsi réagir en conséquence et s'adapter aux **variations de charge** qui peuvent survenir. Etant donnée l'**absence d'engagement** sur les **délais**, les collaborateurs impliqués peuvent ainsi **ne pas avoir une disponibilité totale** pour un tableau de tâche, et peuvent très bien être répartis entre **plusieurs tableaux**. Citons l'exemple d'une équipe de production responsable de la maintenance de plusieurs applications en production.

**Scrum**, quant à lui, gère assez mal les collaborateurs dont la **disponibilité** n'est pas de **100%**, étant donné que l'équipe s'engage sur un nombre de **points d'histoire** sur une durée. Cet engagement repose donc sur un ensemble de forces vives dont l'engagement est assuré. S'il s'avère qu'un collaborateur doit s'absenter au beau milieu d'un **sprint** pour répondre à d'autres priorités, la force vive impliquée dans le **sprint** s'en retrouve brusquement réduite, mettant en péril l'engagement du **périmètre du sprint** sur la durée prévue.

A nouveau, ni **Scrum** ni **Kanban** ne marque de point, puisque chacun a ses forces et faiblesses en fonction du contexte dans lesquels ils sont appliqués.

# Faisons le bilan
**Scrum** et **Kanban** sont tous deux agiles, mais répondent néanmoins à des problématiques différentes. Ils nécessitent également des pré-requis divergents pouvant répondre ou non à une organisation existante. J'ai volontairement laissé de côté un certain nombre de paramètres qui pourraient être étudiés, tels que la taille des équipes (**Scrum** préconise des équipes d'une dizaine de collaborateurs au maximum là où **Kanban** laisse la liberté), le type de projet (**Scrum** s'adapte mieux aux phases de développement, **Kanban** à la maintenance), le budget (**Scrum** permet une meilleure maîtrise et permet d'arrêter un projet au moment propice). Globalement, il apparaît qu'il n'y a pas de vainqueur dans l'absolu.

Résumons néanmoins le point fort de chacun d'entre eux.

## Scrum
**Scrum** puise sa force dans sa **prédictibilité** et permet de **fiabiliser** les **dates de livraison**. Il favorise l'**adaptabilité** en encourageant l'**introspection** et l'**adaptation** au travers de rendez-vous programmés aux objectifs prédéfinis. Il répond bien à une équipe multidisciplinaire complète englobant l'ensemble de la chaîne de construction du livrable, et surtout à une équipe dont la charge de travail reste relativement constante.

## Kanban
**Kanban** est le champion incontesté de la **réactivité** et favorise une **optimisation du flux** et de la **vitesse de livraison** en compressant le **TTM**. Il permet une grande **adaptabilité** pour une équipe mature et bien rodée, et répond bien pour des équipes spécialisées impliquées dans un ensemble de flux de travail.

# Et si vous deviez choisir ?
La réponse n'est pas directe. A la lumière de cette étude, vous pourrez constater qu'il n'y a pas de recette miracle. Si vous tombez exactement dans tous les points forts d'un **cadre** en évitant ses points faibles, vous avez une sacrée chance. Dans le cas contraire, pourquoi ne pas expérimenter un **Scrumban** ? Prenez le meilleur des deux dans votre situation, mélangez énergiquement pendant deux minutes, et enfournez. A la sortie du four, vous aurez une méthode maison basée sur les **principes agiles**, tout en choisissant les éléments les plus pertinents dans votre situation. Ne respectez jamais dogmatiquement les consignes de ces **cadres**. Ce sont des points de départs d'où vous pourrez bâtir le socle de votre propre méthode.

Alors comme le préconise **Gilles**, essayez, inspectez et adaptez !

#Bibliographie

Pour aller plus loin, je vous recommande ces deux ouvrages accessibles pour un novice en agilité ou pour un vétéran aguerri, proposant plusieurs niveaux de lecture en fonction de votre expérience :

[Scrum et XP depuis les tranchées](http://www.infoq.com/resource/news/2007/06/scrum-xp-book/en/resources/ScrumAndXpFromTheTrenches_French.pdf)

[Kanban et Scrum](http://www.infoq.com/resource/news/2010/01/kanban-scrum-minibook/en/resources/KanbanAndScrum-French.pdf)


