---
title: Rappels
category: modules
emoji: ⏰
summary: Chaque membre crée ses rappels ponctuels ou répétés avec /remind.
order: 9
---

## Commandes

| Commande | Effet |
|---|---|
| `/remind me when:2h text:Sortir le chien` | rappel dans 2 heures |
| `/remind me when:1d text:Réunion staff repeat:weekly` | rappel répété chaque semaine |
| `/remind list` | tes rappels sur ce serveur, avec leur numéro |
| `/remind delete id:7` | supprimer un rappel |

Durées acceptées : `10m`, `2h`, `3d`, `1w`, combinables (`1h30m`), entre 1 minute et 1 an. Répétitions : `none`, `daily`, `weekly`, `monthly`.

## Réglages du serveur

- **Envoyer les rappels en MP** : sinon, Kron mentionne le membre dans le salon où il a créé le rappel.
- **Rappels maximum par membre** : 10 par défaut, jusqu'à 50.
