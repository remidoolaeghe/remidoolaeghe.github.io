---
layout: post
title: Comment nous avons géré nos branches SVN
subtitle: Aussi valable pour git
category: lachezlesclaviers
tags: artisan-logiciel scm svn git
feature-image: 2015-08-24-Comment_nous_avons_gere_nos_branches_SVN-feature_image.png
---

La philosophie des branches mise en pratique dans un gestionnaire de version tel que **Git** ou **SVN** est trop souvent une question à laquelle on s'emploie à répondre lorsqu'il est déjà trop tard. Lorsqu'on commence à vivre le cauchemar des fusions de branches, on se demande si on n'aurait pas dû s'y prendre autrement. Un système de branches bien défini peut vous éviter de perdre des cheveux trop précocement et permettra à n'importe qui dans l'équipe de procéder aux fusions et autre gestion de branches sans avoir à se poser de question ni y semer la zizanie. Cet article a pour vocation de vous indiquer la façon dont nous avons procédé au sein de *Perigee*, où j'ai sévi pendant près de trois ans. Ceci est un témoignage d'un modèle qui a fonctionné pour nous, et non une recette de cuisine qui fonctionne dans toutes les situations.

![Logo de Perigee]({{ site.images }}/2015-08-24-Perigee.gif){:.center-image}

Avant de parler de **branche**, il est nécessaire d'être bien carré avec la notion de **gestion sémantique de version**. En quelques mots, l'industrie du développement est parvenue sur un ensemble de bonnes pratiques quant à la définition des numéros de version. Les conventions en sont arrivées au quasi standard suivant :

    MAJEURE.MINEURE.CORRECTIF
	
Par exemple : 2.1.4. La **majeure** représente une évolution importante pouvant introduire une rétro-incompatibilité avec la **majeure** précédente (l'**API** peut changer). La **mineure** respecte la rétro-compatibilité, et se contente généralement d'ajouts de fonctionnalités ou d'implémentation, mais pas d'**API**. Le **correctif** n'apporte aucune nouveauté, simplement un changement de comportement pour répondre à une spécification de façon plus correcte.

Pour plus de détails, je vous invite à consulter [semver](http://semver.org/), qui traite de la gestion sémantique des versions dans le détail.

> Pourquoi tu nous parles de gestion sémantique des versions alors que l'article est sensé traiter de branches au sein d'un gestionnaire de versions ?

De la bonne gestion de vos versions applicatives dépendra la bonne tenue de vos branches. Si vos versions ne sont pas carrées, vous avez un risque de perdre le contrôle de votre gestionnaire de versions. C'est de cette façon que démarre l'**enfer des fusions de branches** et des **livraisons**.

#Initialisation
Au démarrage de notre projet chez *Perigee*, nous avons opté pour une solution simple. Etant donné qu'il n'y avait aucune matière ni socle sur lequel travailler, la question ne se posait pas. Il était nécessaire de poser les bases, et donc de travailler tous ensemble sur la même **branche** tant que la première **release** n'était pas sortie. Nous étions donc sur un schéma de **branche** très simple le temps de construire les fondations de l'application.

![Modèle de branches avant release]({{ site.images }}/2015-08-24-init.png){:.center-image}

#Première release
Lorsque l'application a atteint le stade du **MVP** (Minimal Viable Product - Produit Minimum Viable), nous avons effectué une **release**. En pratique, cela signifie estampiller l'application d'une version 1.0.0. Côté **gestionnaire de sources**, cela se traduit par la création d'une **branche** que nous appellerons 1.0 dans **SVN**, et la création d'un **tag** **1.0.0** également.

![Modèle de branches pour la 1.0]({{ site.images }}/2015-08-24-Version-1-0.png){:.center-image}

Par la suite, cette **branche** n'a plus accueilli que des correctifs pour les versions 1.0.n, n étant un entier naturel. Je reviendrai sur la notion de correctif dans la suite de cet article.

Rétrospectivement, il aurait été plus homogène de créer dès le démarrage du projet la **branche** 1.0 et d'y développer directement notre socle applicatif. Néanmoins, cela ne nous a pas gênés en pratique. Si c'était à refaire, je créerais malgré tout d'abord la **branche** 1.0 pour y effectuer les développement initiaux en n'utilisant jamais le **trunk**, puis en créant le tag 1.0.0 au moment de la **release**.

![Modèle de branches alternatif pour la 1.0]({{ site.images }}/2015-08-24-Version-1-0_redo.png){:.center-image}

#Releases suivantes
En vue des nouvelles fonctionnalités à destination de la version 1.1.0, au moment de la **release** 1.0.0, nous avons créé une **branche** 1.1.0 en partant de la **branche** 1.0.0. En règle générale, une **branche** de version est toujours issue de la **branche** de la version précédente.

![Modèle de branches pour les releases suivantes]({{ site.images }}/2015-08-24-Version-multi.png){:.center-image}

Dans la théorie, cela peut poser problème s'il vous vient à l'idée de venir créer une branche intermédiaire. Typiquement, si nous avions voulu créer une **branche** 1.2 après la 2.0, nous aurions été bloqués. En pratique, nous n'avons pas été confrontés à cette problématique.

#Nouvelle fonctionnalité
Je n'ai pas encore parlé de la méthode employée pour développer une nouvelle fonctionnalité. Le principe reste simple. Lorsqu'une fonctionnalité est entamée, une **branche** dédiée est créée pour l'occasion, que nous appelons **branche de fonctionnalité** ou **branche de développement** (par opposition aux **branches de version**). Chez *Perigee*, nous avions l'habitude de nommer ce type de **branche** sous la forme **[version-ciblée]-[identifiant de la fonctionnalité dans notre backlog de produit]-[court descriptif]**. Par exemple : **2.0-125-ma_fonctionnalité**.

![Modèle de branches pour une nouvelle fonctionnalité]({{ site.images }}/2015-08-24-feature.png){:.center-image}

A intervalle régulier, il est sage d'effectuer des fusions depuis la **branche de version** d'origine vers la **branche de développement**, de façon à récupérer régulièrement les modifications de la **branche** d'origine et d'en tenir compte dans les développements. A terme, il est généralement plus facile de faire une dernière fusion vers la **branche de développement** avant d'effectuer la fusion dans l'autre sens. Les conflits seront moins nombreux.

#Correctifs
Dans la vaste majorité des cas, les correctifs peuvent être effectués directement dans la **branche de version** dans laquelle ils sont ciblés. Lorsqu'un nombre satisfaisant de correctifs est atteint, il est temps d'effectuer une nouvelle **release**. Dans les faits, cela se traduit par la création d'un **tag**. Par exemple, lorsque je me trouve en version 1.0.0 et que je souhaite faire une **release**, alors je crée simplement un **tag** 1.0.1, et j'effectue ensuite une fusion de ma **branche de version** avec mes **branches de version** descendantes.

![Modèle de branches pour un tag de correctif]({{ site.images }}/2015-08-24-tag.png){:.center-image}

L'avantage d'une telle descendance de **branches** est indéniablement la facilité à effectuer des fusions de **branches de version**. Imaginons que j'aie besoin d'effectuer une correction dans une très ancienne version, par exemple la 1.0.0 qui est encore en production chez un client. La correction peut être ensuite très facilement fusionnée vers les **branches de version** enfants.

![Modèle de branches pour un correctif sur une ancienne branche]({{ site.images }}/2015-08-24-fix-old-version.png){:.center-image}

#Élagage
Afin de rester propre et d'éliminer nos déchets, nous avions pris le réflexe d'éliminer les **branches de développement** dès lors qu'elles étaient réintégrées à leur **branche de version** d'origine. De cette façon, seule subsistaient les branches vivantes.

#Remarques
La gestion des **tags** chez *Perigee* n'était pas manuelle. Elle était effectuée par **Jenkins** lorsque le département de la QA estimait la version suffisamment stable pour en faire une **release**. La création des **branches de version** et de **développement**, ainsi que les fusions, étaient effectuées par un développeur pour vérifier la bonne résolution des conflits de fusion.

#Récapitulatif

##Démarrage d'une nouvelle version majeure ou mineure
Une branche au nom de la **mineure** est créée (1.2)

##Création d'une release
Un tag est créé avec le nom de la **version du correctif** (1.2.3), puis des fusions sont effectuées dans les **branches de versions** descendantes. Cette fusion est considérée comme un **correctif** dans la **branche** destination.

##Correctifs
Les correctifs sont effectués directement dans la **branche de version**, puis intégrés dans une **release** lorsque l'autorité compétente décrète sa création.

##Développement d'une fonctionnalité.
Une **branche de développement** à part est créée, partant de la **branche de version** ciblée. Des fusions sont effectuées régulièrement jusqu'à réintégration de la **branche de développement**. Celle-ci est alors détruite.

#Conclusion
Ce modèle de branche en cascade est celui qui nous a permis d'obtenir le meilleur rapport temps d'administration/facilité d'utilisation. C'est un modèle peu coûteux, qui permet les fusions rapidement, tout en maintenant toutes les branches dans un état utilisable à tout moment. Les développements en cours sont bien décorrélés, et les correctifs sont accessibles à tous puisque présents dans les **branches de versions**.

Nous l'avons utilisé pour **SVN**. Il est probable que nous utiliserions un modèle similaire pour tout autre **SCM** tel que **Git**.

Une alternative est possible pour la gestion des **correctifs**. J'ai indiqué que les **correctifs** étaient effectués directement dans la **branche de version**, et qu'une **release** était effectuée quand nous avions atteint un "nombre suffisant de correctifs". Les tickets de bugs étaient priorisés, si bien qu'il n'était pas nécessaire de sélectionner lesquels devaient être inclus dans une **release**. Pour certains autres types d'organisations où les correctifs sont plus critiques, il est possible d'imaginer créer une **branche** par correction d'anomalie, puis une réintégration des correctifs dans la **branche de version** à la demande, de façon à n'intégrer dans une **release** que les correctifs expressément demandés. Néanmoins, ce mode de fonctionnement nécessite beaucoup plus de travail administratif et nous n'en avions pas besoin.

#Crédits
Les diagrammes ont été réalisés à l'aide de [dia](http://sourceforge.net/projects/dia-installer/).

