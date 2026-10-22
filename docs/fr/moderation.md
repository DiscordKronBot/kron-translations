---
title: Modération
category: modules
emoji: 🛡️
summary: Avertir, exclure, expulser, bannir et purger, avec un historique par membre.
order: 12
---

## Commandes

| Commande | Permission requise | Effet |
|---|---|---|
| `/warn member reason` | Exclure des membres | avertissement enregistré dans l'historique |
| `/timeout member duration reason` | Exclure des membres | exclusion temporaire (1 minute à 28 jours) |
| `/untimeout member` | Exclure des membres | lève l'exclusion |
| `/kick member reason` | Expulser des membres | expulse le membre |
| `/ban member reason delete_days` | Bannir des membres | bannit, peut effacer 0 à 7 jours de messages |
| `/unban user_id reason` | Bannir des membres | débannit par ID |
| `/purge amount member` | Gérer les messages | supprime 1 à 100 messages (de moins de 14 jours) |
| `/infractions member` | Exclure des membres | les 15 dernières sanctions |

## Sécurité

- Impossible d'agir sur soi-même, sur le propriétaire du serveur ou sur un membre de rang égal ou supérieur.
- Kron vérifie aussi qu'il peut agir sur le membre (position de son rôle).

## Réglages

- **Prévenir le membre en MP** : il reçoit la sanction et la raison. Pour une expulsion ou un bannissement, le MP part juste avant l'action.
- **Salon des sanctions** (optionnel) : un embed par sanction. Le [module Logs](/docs/logs) enregistre déjà bannissements, expulsions et exclusions, avec l'auteur.

## Historique

L'onglet **Historique** du dashboard liste les 100 dernières sanctions, filtrables par ID de membre. Tu peux supprimer une sanction donnée par erreur.

> [!TIP]
> Pour une protection automatique, vois [AutoMod](/docs/automod), [Anti-raid](/docs/anti-raid) et le salon piège [Honeypot](/docs/honeypot).

## Sanctions automatiques

Dans le dashboard, ajoute des règles : par exemple **3 avertissements → exclusion 1 heure**, **5 → expulsion**, **7 → bannissement**. Kron applique la sanction au moment du `/warn` qui atteint le nombre, et l'inscrit dans l'historique et les logs.
