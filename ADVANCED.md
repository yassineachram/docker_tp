L’utilisation de git rebase -i (rebase interactif) permet de réécrire l’historique des commits sur une branche de fonctionnalité pour le rendre plus clair et mieux organisé. Cela permet de réorganiser, fusionner, ou même modifier les commits avant de les fusionner avec la branche principale du projet.

Principales actions avec git rebase -i :
Fusionner des commits (squash ou fixup) :

On peut fusionner plusieurs petits commits en un seul commit plus significatif. Cela rend l'historique plus propre et plus facile à comprendre.

Modifier les messages des commits (reword) :

Si un commit a un message peu clair ou mal formulé, on peut le modifier pour qu’il reflète mieux ce qui a été fait.

Réorganiser les commits :

Il est possible de réorganiser l’ordre des commits pour qu’ils suivent une logique plus cohérente.

Supprimer des commits (drop) :

Si certains commits ne sont plus nécessaires ou sont des erreurs, ils peuvent être supprimés pour éviter d'encombrer l’historique.

Bénéfices de l’utilisation de git rebase -i pour l’historique du projet :
Un historique plus propre et lisible :

En fusionnant des commits et en supprimant ceux inutiles, on rend l’historique plus facile à lire et à comprendre, ce qui est essentiel pour suivre l’évolution du projet.

Un meilleur suivi des changements importants :

Fusionner des commits permet de garder une trace claire des changements majeurs sans que l’historique ne soit pollué par des petits ajustements ou des corrections mineures.

Faciliter les fusions :

Un historique propre et bien organisé réduit les risques de conflits lors de la fusion de branches et permet de mieux comprendre ce qui a été modifié.

Améliorer la communication entre les membres de l’équipe :

Des messages de commit précis et bien rédigés permettent à toute l’équipe de mieux comprendre l’intention derrière chaque changement, facilitant ainsi la collaboration.

Préparer l’intégration dans la branche principale :

Avant de fusionner une branche de fonctionnalité, il est important de la nettoyer pour s’assurer qu’elle ne contient que des commits importants et bien structurés. Cela permet d’éviter de polluer l’historique de la branche principale.

Introduction à git cherry-pick
La commande git cherry-pick permet de récupérer un commit spécifique d'une autre branche et de l'appliquer à la branche courante. Contrairement à une fusion (merge) qui applique tous les changements d'une branche à une autre, cherry-pick permet de sélectionner un commit précis, offrant ainsi un contrôle plus fin sur les modifications à intégrer. Cela est particulièrement utile lorsque l'on veut récupérer une correction, une fonctionnalité ou un ajustement sans inclure d'autres changements non désirés provenant de la même branche.

Application de git cherry-pick et Impact sur le suivi de version
Dans notre cas, l'utilisation de la commande git cherry-pick a été motivée par la nécessité d'appliquer un commit spécifique d'une autre branche sur la branche actuelle sans fusionner l'intégralité des changements de cette branche. On a identifié le commit avec notre hash 68e261b065b9d65bf85a3ab83c7a8e93de81d0b3, qui apportait une correction ou une fonctionnalité importante, mais on n'avais pas besoin de toute la branche. En utilisant git cherry-pick, on a extrait et appliqué uniquement ce commit spécifique sur notre branche actuelle, ce qui nous a permis de récupérer la modification sans affecter l'intégralité des autres commits de la branche d'origine.

Impact sur le suivi de version :
Précision dans l'historique des versions :
L'utilisation de git cherry-pick a permis de garder un historique clair et précis, car seul un commit spécifique a été appliqué. Cela évite de mélanger plusieurs changements non désirés, ce qui peut rendre l'historique plus difficile à comprendre et suivre.

Facilité de gestion des corrections et fonctionnalités :
Cette commande permet de récupérer des corrections de bugs ou des ajouts de fonctionnalités d'une branche sans avoir à fusionner d'autres changements inutiles. C'est particulièrement utile dans des projets avec plusieurs branches de développement indépendantes, où seules certaines parties des modifications sont nécessaires.

Maintien d'une branche stable :
En appliquant git cherry-pick, on a pu maintenir ma branche stable (comme master ou main) tout en appliquant seulement les améliorations ou corrections pertinentes. Cela a évité d'introduire des erreurs ou des fonctionnalités non validées, ce qui est crucial pour les branches de production ou de développement principal.

Conclusion
En résumé, l'utilisation de git cherry-pick nous a permis de transférer une modification spécifique d'une autre branche de manière contrôlée, en préservant l'intégrité de l'historique et en appliquant uniquement les changements nécessaires. Cette technique améliore la gestion des versions en permettant un suivi plus précis et en garantissant que seules les modifications pertinentes sont appliquées à la branche courante.


