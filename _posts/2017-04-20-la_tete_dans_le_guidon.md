---
layout: post
title: La tête dans le guidon
subtitle: Et si on faisait une pause ?
category: lachezlesclaviers
tags: management amelioration-continue time-management
feature-image: 2017-04-20-la_tete_dans_le_guidon.jpg
excerpt_separator: <!--more-->
--- 

Vous vous souvenez de cette période de votre vie, pendant laquelle vous abattiez des journées de boulot de plus de 10h pendant des semaines ? Si si, ces jours lointains (ou pas) où vous commenciez à 7h30 et terminiez après 20h ? Ne me mentez pas, ça vous est déjà arrivé. Et si ce n'est pas le cas, rassurez-vous, ça vous arrivera bien un jour. Ne soyez pas jaloux de ceux qui ont déjà eu cette expérience fabuleuse, il y en aura pour tout le monde.

Parfois, ces périodes phares sont des passages obligés dans des projets critiques, ou soumis à une date de livraison dont la définition est bien hors de votre portée. Ou parfois, il s'agit simplement d'acharnement à vouloir enfoncer un clou à main nu dans un béton armé de 20 cm d'épaisseur.

<!--more-->

> Hein ? Mais je n'ai jamais fait ça, moi !

Laissez-moi vous raconter une petite histoire. Oh, elle vous semblera forcément familière, d'une façon ou d'une autre.

*Dave Lawper est au sein d'une équipe de développement, dans un service web d'une grande entreprise. Vient un jour durant lequel, pour valider un développement, il a besoin d'une masse de données importante dans sa base de données. Très naturellement, il s'enquiert auprès de ses petits camarades quelle est la procédure pour générer cette masse de données.*

*"Il suffit de faire une recopie partielle de la base de prod", lui répond-on.*

*Dave Lawper est un peu interloqué, mais il se conforme aux pratiques de son client. Après tout, il n'est que prestataire. Afin d'effectuer cette recopie, il se renseigne pour savoir comment effectuer cette action en pratique.*

*"On va te montrer", lui lance-t-on."*

*Deb Lopez vient alors à son poste et lui explique tout.*

*"Déjà, il faut que tu installes cet IDE SQL pour que tu puisses effectuer les requêtes. Ce n'est pas le même que celui qu'on utilise habituellement parce qu'il manque des fonctionnalités dans l'autre. Ensuite, tu dois exécuter un batch qui effectue un export. Par contre, attention, il faut que tu fasses gaffe aux paramètres que tu passes au batch en fonction de ce que tu souhaites faire. Ah, ces paramètres, il faut les passer dans ton IDE, parce qu'on génère ces exports sur le poste de développement. Ensuite, tu dois faire tourner ce petit outil supplémentaire qu'on a développé en interne, pour anonymiser les données. Tu comprends, on ne peut pas utiliser des données brutes ainsi. Quand tu auras terminé, il faudra que tu te connectes en ssh sur la machine distante de dév et que tu copies l'export que tu as effectué. Là, tu peux exécuter un second batch d'import qui, normalement, doit déterminer tout seul ses paramètres. Mais il faut quand même que tu fasses attention à la config qui se trouve dans tel répertoire, parce qu'on a plusieurs types d'imports possibles. Ca ira ?"*

*En guise de réponse, Dave Lawper blêmit, puis déglutit péniblement. Ensuite, il demande s'il n'existe pas une procédure automatisée pour laquelle il n'aurait qu'à appuyer sur un bouton.*

*"On n'a pas le temps de faire ça. Mais tu verras, avec l'habitude tu iras très vite."*

Vous aussi, vous sentez le truc qui pue ? Et pourtant, ce n'est pas si rare que ça. Je suis même quasiment certain que vous l'avez au moins vécu au moins une fois. Si si, creusez donc dans vos souvenirs. Voilà, exactement à ce moment-là.

Je ne m'attarderai pas sur les risques que comportent de telles pratiques (la liste est trop longue et mériterait un article entier). En revanche, ce que *Dave Lawper* ne sait pas encore, c'est qu'une telle procédure existe depuis 3 ans. Sans documentation. Tout est dans la tête de l'équipe. Enfin, de certaines têtes. Et jamais en totalité. Chacun en connait certains morceaux, hérités de camarades tombés au combat depuis longtemps.

Quand *Dave Lawper* demandera à *Herman Adgeur* s'il peut consacrer un peu de temps à l'automatisation de cette tâche (en argumentant sur le gain de temps et de sécurité), il sera rembarré avec un classique :

> On n'a pas le temps de faire ça. Il faut qu'on sorte les features 1, 2 et 3 **ASAP**

ASAP.

La source du problème est là. Trop souvent, on entend constamment qu'une tâche doit être effectuée ASAP. Dès que possible. Sans tarder. Voire même pour hier. Généralement, les tâches ASAP ne viennent jamais seules. Elles sont toujours suivies par une autre, et encore une autre, et toujours une autre, sans fin. Ce train d'ASAP est un cancer qui repousse toujours plus loin les remises en questions, ou les tentatives de capitalisation.

Posons-nous une minute. Qu'est-ce que ça aurait coûté à *Dave Lawper* de consacrer quelques efforts à cette automatisation. Oui, beaucoup de temps, c’est certain. Peut-être même une semaine. Et puis ça aurait été terminé. Il en aurait résulté une procédure automatisée, que n'importe qui aurait pu exécuter, sans un besoin de formation, sans un risque constant de commettre une erreur, et sans avoir à y passer une heure à chaque fois que cet export-import devait être effectué.

Faisons un bilan. Combien d'heures ont été perdues par ces exécutions manuelles de la procédure ? Combien de fois il aurait été possible d'implémenter cette automatisation dans ces heures perdues ? Combien d'erreurs ont été commises par inadvertance à cause de cette manipulation complètement manuelle ? Le bilan ferait peur.

La source du problème, c'est le ASAP. La tête dans le guidon perpétuellement. C'est comme si Henry Ford n'avait jamais automatisé ses chaînes de montage, et que les voitures continuaient d'être montées à la main parce qu'il fallait les sortir au plus vite.

Est-ce que ça vaut vraiment le coup, ne serait-ce que d'un point de vue budgétaire, de repousser éternellement cette automatisation ? Est-ce que ça ne vaut pas parfois le coup de se poser, une heure, et de se poser les questions et de remettre en cause ses pratiques ?

Songez à nouveau à ces journées stressantes de plus de 10h, provoquées par toutes ces petites perturbations qu'il aurait été facile de traiter unitairement lorsqu'elles se présentaient. Est-ce que ça ne vaut pas le coup de se pencher sur la question pour retrouver un équilibre dans ses journées de travail, et par conséquent de sa vie privée ?

Posons-nous la question de savoir si ces tâches sont vraiment urgentes et prioritaires, et si nos pratiques ne mériteraient pas d’être remises en question et améliorées. Sortons la tête du guidon avant de finir dans le mur.
