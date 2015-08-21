---
layout: post
title: Jekyll sur Windows
subtitle: Ou comment éviter une installation de VM
category: lesmainsdanslecambouis
tags: jekyll blog
feature-image: 2015-07-03-Jekyll_sur_Windows-feature-image.png
---

*Dave Lawper* aime beaucoup développer son blog en utilisant **Jekyll**. Il a débuté son développement sur une plateforme arborant un fruit avec lequel on fait de délicieuses compotes. Néanmoins, il aime également beaucoup les fenêtres. Donc il aimerait développer son blog sur **Windows**. Et comme le dit la [documentation de Jekyll](http://jekyllrb.com/docs/windows/) :

> Windows is not an officially-supported platform

Que les adorateurs de fenêtres se rassurent, *Madhur Ahuja* est arrivé à la rescousse !

![Photo de Madhur Ahuja]({{ site.images }}/2015-07-03-Madhur_Ahuja.jpg){: .center-image}

*Madhur Ahuja* a développé un petit projet visant à faire tourner **Jekyll** sous **Windows**, disponible [ici](https://github.com/madhur/PortableJekyll).

Le wiki détaille bien le peu à faire pour installer et faire tourner **Jekyll** sur **Windows**, si ce n'est deux choses.

La première, n'essayez pas d'exécuter la commande

{% highlight console %}
setpath.cmd
{% endhighlight %}

sur **PowerShell**. Pour une raison obscure, il refuse d'ajouter au **PATH** les chemins nécessaires pour faire tourner **Jekyll**.

La seconde, préférez ajouter directement à votre **PATH** le contenu du fichier **setpath.cmd**, en prenant soin d'adapter les chemins qui y sont contenus. Si vous ignorez comment faire, référez-vous [ici](http://sametmax.com/ajouter-un-chemin-a-la-variable-denvironnement-path-sous-windows/). Si exécutez directement **setpath.cmd** dans votre ligne de commande, il vous faudra réitérer l'opération à chaque redémarrage de l'invite de commande.

Et voilà, il ne vous reste plus qu'à exécuter la commande suivante

{% highlight console %}
jekyll serve
{% endhighlight %}
	
dans le dossier de votre site, et à vous connecter à

{% highlight console %}
localhost:4000
{% endhighlight %}
	
dans votre navigateur préféré !
 