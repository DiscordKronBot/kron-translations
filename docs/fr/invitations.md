---
title: Suivi des invitations
category: modules
emoji: 📨
summary: Qui a invité qui, message d’arrivée avec le nombre d’invitations, logs du staff et classement.
order: 4
---

Le module **Suivi des invitations** trouve, à chaque arrivée, l'invitation utilisée et qui l'a créée.

## Message public

Choisis un salon (par exemple ton salon de bienvenue, ou **+ Créer** pour `📨┆arrivées`). À chaque arrivée :

> 👋 @Bob a rejoint le serveur, invité par **Bill** qui a maintenant **25** invitations !

Coche **Personnaliser le message** pour écrire le tien (texte ou embed). Variables : `{user}`, `{username}`, `{inviter}` (mention, sans ping), `{inviter.name}`, `{invites}`, `{code}`, plus les variables communes (`{server}`, `{memberCount}`…).

Arrivée par le **lien personnalisé** du serveur : « grâce au lien personnalisé ». Invitation introuvable : seule l'arrivée est annoncée.

## Logs du staff

Un salon de logs (**+ Créer** le place dans la catégorie des logs du serveur) reçoit chaque arrivée et départ : code de l'invitation, inviteur, son total, âge du compte.

## Comment on compte

| | |
|---|---|
| **Valides** | les membres invités toujours sur le serveur |
| **Partis** | ceux qui ont quitté depuis |
| **Faux** | les comptes créés depuis moins de X jours à leur arrivée (réglable, 0 = jamais) |

Un membre qui part et revient compte une seule fois, avec sa dernière arrivée.

## Commandes

- `/invites voir [membre]` : les invitations d'un membre (toi par défaut).
- `/invites classement` : les 10 meilleurs inviteurs. Le classement complet est dans le dashboard.

> [!NOTE]
> Kron a besoin de la permission **Gérer le serveur** pour voir les invitations (comprise dans Administrateur). Juste après l'activation, la toute première arrivée peut rester « inconnue » : Kron apprend alors les invitations du serveur.
