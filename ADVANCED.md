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
