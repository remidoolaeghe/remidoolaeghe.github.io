---
layout: post
title: La revue de code
subtitle: Ou comment gagner en qualité de code
category: lachezlesclaviers
---

*Dave Lawper* a écrit son correctif en vitesse. C'était un vendredi soir, il était tard. Le fix était localisé dans une lib interne, que personne d'autre ne maitrisait

Qu'est-ce qu'un code de bonne qualité ? Le sujet est vaste, et je ne citerai qu'une condition nécessaire. Un code de bonne qualité doit passer une revue de code avec succès. Que garantit donc une revue de code ?
Lorsqu'un développeur a cette épée de Damoclès au-dessus de la tête, il sait qu'un hack honteux n'est pas une option. Celui du petit conte aurait donc eu cette menace planant au-dessus de lui : Si je fais ce hack, mon réviseur me tombera dessus et il faudra que je recommence. Car oui, la revue de code a ce premier effet avant même d'avoir lieu. Si le développeur sait pertinemment que son correctif sera refusé, il ne tentera même pas de l'implémenter, et il devra se forcer à faire les choses proprement. Il faut bien évidemment partir du constat que le réviseur sera intransigeant et non complaisant.
La revue de code a donc cet effet proactif de forcer à écrire un code propre, lisible et compréhensible. Si le réviseur ne comprend rien à ce qui a été produit, cela signifie qu'un développeur effectuant une maintenance sur ce bout de code, plusieurs années plus tard, sera tout aussi perdu. En conséquence, il sera dans l'obligation d'ajouter un nouveau hack par-dessus, dégradant encore davantage la qualité du code. Le mauvais code appelle le mauvais code. S'il est bon au départ, il minimisera la vitesse de sa dégradation (ou l'annulera dans un cas idéal, voire idéaliste). Dans tous les cas, le gain est non négligeable.
Dans l'hypothèse où le développeur écrit un code de bonne qualité, la revue de code a un deuxième effet kiss kool. Il n'est pas à l'abri d'avoir corrigé son bug en oubliant une partie du problème. Le réviseur a une chance non négligeable de repérer un potentiel oubli, ou un effet de bord de la correction. Il ne pourra pas tous les voir. Si néanmoins il peut en identifier ne serait-ce qu'un avant que le code ne parte en production, la revue n'aura pas été inutile.

La revue de code est déjà un beau gain de qualité de code. Elle cumule également un autre gros avantage, celui d’être un réseau social !