---
layout: post
title: J’en ai rêvé, Github pages l’a fait
subtitle: Ou comment mettre sur pied un site statique en trois clics
category: lesmainsdanslecambouis
tags: github blog
feature-image: 2015-04-22-Github_feature.jpeg
---

Ca me trottait dans la tête depuis quelques mois. Après avoir passé près de cinq ans la tête sous un monticule de bytecode depuis mon diplôme, l’idée a fini par germer jusqu’à atteindre le bon dosage d’engrais. Une bonne pelletée de **Devoxx**, parsemée d’une poignée de **Github pages**. Et paf, ça fait <del>des chocapic</del> un blog perso !

> Au fait, c’est quoi **Github pages** ?

Le meilleur moyen de raconter votre vie. Ou autre chose, d’ailleurs. Peu importe.
[**Github pages**](https://pages.github.com/) est un service proposé par [**Github**](https://github.com/). Installez git sur votre machine, créez un dépôt, et poussez-y un fichier **index.html**. Et le tour est joué, vous avez un site  perso.

> Je peux aussi le faire chez **Heroku** ou **Free**, c’est pas nouveau ton truc.

Certes, l’idée n’est pas forcément révolutionnaire. Sauf si on ajoute la fonctionnalité qui peut faire pencher la balance. Comme je l’ai expliqué, **Github pages** vous propose de monter votre propre site relié à votre compte **Github** en quelques minutes. Vous avez gratuitement le nom de domaine, l’hébergement et toutes les fonctionnalités de **Git** directement intégré à votre projet. Elle est pas belle, la vie ?

> C’est pas mal, en effet. Tu peux nous en dire plus ?

Œuf corse. **Github pages** vous propose donc un site très rapidement opérationnel. Et si vous aimez ça, chacun de vos projets hébergés sur **Github** peut bénéficier de son propre site également.
Certes, vous ne pouvez héberger que des sites statiques. Néanmoins, **Github pages** supporte nativement [**Jekyll**](http://jekyllrb.com/), un outil de génération de site statique. En quelques mots, **Jekyll** permet de gérer de la pagination automatique (pratique pour un blog), ou encore l’utilisation d’outils de markdown, comme par exemple [**Kramdown**](http://kramdown.gettalong.org/) qui vous permet de vous abstraire du code **HTML** pour vous focaliser sur une syntaxe simplifiée comme dans un wiki pour la rédaction de vos billets. **Githug pages** est capable de parser des billets de blog ainsi construits et poussés directement dans votre dépôt **Github** sans que vous ayez besoin de générer vous-même le site en exécutant **Jekyll** sur votre machine. Néanmoins, il est toujours possible de l’installer en local dans l’optique de vérifier votre travail avant de pousser sur votre dépôt à l'aide d'outils bien pratiques sur lesquels je ne vais pas m'étendre.

> Au final, tu peux te construire un blog statique en une heure ?

Exactement. Et en bonus, je peux citer deux fonctionnalités très appréciables. En premier lieu, il existe nombre de thèmes tout prêts à l’emploi, disponibles gratuitement, afin que vous n’ayez pas à personnaliser de A à Z l’ensemble de votre site. Une bonne base pour commencer vos recherches peut être [**Jekyll Themes**](http://jekyllthemes.org/). Faites un fork sur le dépôt d’un de ces thèmes, et il ne vous reste plus qu’à remplacer l’ensemble des placeholders par vos données persos. Et vous voilà avec un blog utilisable immédiatement.
L’autre fonctionnalité, vous pourrez l’expérimenter à la fin de ce billet. Il s’agit d’une intégration avec [**Disqus**](https://disqus.com/). En quelques lignes HTML, vous pouvez intégrer un système de commentaires à l’ensemble de vos billets, avec les outils d’administration qui vont bien, proposés sur le site de **Disqus**. Rien à coder, juste à apprécier.

Merci **Github pages** !

<hr>
***Bibliographie*** :

[Github](https://github.com)

[Github pages](https://pages.github.com)

[Jekyll](http://jekyllrb.com)

[Jekyll Themes](http://jekyllthemes.org)

[Kramdown](http://kramdown.gettalong.org/)

[Disqus](https://disqus.com)