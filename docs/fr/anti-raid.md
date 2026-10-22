---
title: Anti-raid
category: modules
emoji: 🚧
summary: Détecter les vagues d'arrivées, mettre les invitations en pause et surveiller les comptes récents.
order: 14
---

Le module **Anti-raid** repère les raids (beaucoup de comptes qui rejoignent en même temps) et aide le staff à les arrêter en un clic.

## Détection

Tu choisis le seuil : par exemple **10 arrivées en 10 secondes**. Quand il est atteint, Kron passe en **mode raid** :

- il publie une alerte dans le salon choisi, en mentionnant les rôles du staff;
- il applique l'action choisie à chaque arrivée : **alerte seulement**, **expulser** ou **bannir** (les membres qui ont déclenché le raid compris);
- il peut **mettre les invitations en pause** grâce aux actions de sécurité de Discord.

Le mode raid se termine tout seul après quelques minutes sans nouvelle arrivée, ou avec le bouton **Terminer le raid**. Les invitations sont alors rétablies.

> [!TIP]
> Le bouton **Bannir les arrivées** bannit d'un coup tous les comptes arrivés pendant le raid (jusqu'à 200). La liste est gardée en mémoire : après un redémarrage de Kron, le bouton ne fonctionne plus.

## Comptes récents

Hors raid, Kron peut vérifier l'âge du compte de chaque nouveau membre. Si le compte a été créé il y a moins de X jours :

- **Alerte seulement** : un message dans le salon des alertes;
- **Expulser**;
- **Rôle de quarantaine** : un rôle qui ne voit, par exemple, qu'un salon de vérification.

## Permissions

Expulser, Bannir, Gérer les rôles (quarantaine) et Gérer le serveur (pause des invitations). Le rôle de Kron doit être au-dessus du rôle de quarantaine.
