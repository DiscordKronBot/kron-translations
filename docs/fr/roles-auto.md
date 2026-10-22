---
title: Rôles automatiques
category: modules
emoji: 🏷️
summary: Donner des rôles à chaque nouveau membre, avec un délai et le filtrage d'adhésion de Discord.
order: 5
---

Le module **Rôles automatiques** donne un ou plusieurs rôles à chaque personne qui rejoint ton serveur. C'est la première étape d'une whitelist : le nouveau reçoit `@nouveau`, qui lui donne accès au salon du formulaire.

## Réglages

| Réglage | Effet |
|---|---|
| Membres | rôles donnés aux humains (ex. `@nouveau`) |
| Bots | rôles donnés aux bots qui rejoignent |
| Délai | de 0 seconde à 1 heure avant de donner les rôles |
| Attendre l'acceptation du règlement | si ton serveur utilise le filtrage d'adhésion de Discord, le rôle est donné seulement après l'acceptation |

## Avec la whitelist

1. Rôles automatiques : `@nouveau` pour les membres.
2. Whitelist, onglet Rôles : `@passport` à l'envoi du formulaire ; à l'acceptation, `@citoyen` ajouté et `@nouveau` + `@passport` retirés.

Voir [Whitelist et formulaires](/docs/whitelist).

> [!IMPORTANT]
> Les rôles doivent être sous le rôle de Kron. Ceux qu'il ne peut pas gérer sont ignorés.

> [!NOTE]
> Un délai est perdu si Kron redémarre pendant l'attente. Pour un rôle critique, garde un délai court.
