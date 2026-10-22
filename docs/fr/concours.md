---
title: Concours
category: modules
emoji: 🎁
summary: Lancer un concours en une commande ou depuis le dashboard, avec tirage au sort et nouveau tirage.
order: 8
---

## Lancer un concours

**Dans Discord :**

```
/giveaway start prize:Nitro 1 mois duration:2d winners:1
```

| Option | Description |
|---|---|
| `prize` | le prix (obligatoire) |
| `duration` | durée : `30m`, `2h`, `1d`, `1w`, combinables (`1d12h`). Entre 1 minute et 30 jours |
| `winners` | nombre de gagnants, de 1 à 20 (1 par défaut) |
| `channel` | salon du concours (le salon actuel par défaut) |
| `role` | rôle requis pour participer |

**Dans le dashboard :** prix, gagnants, durée, salon et rôle requis, puis **🎉 Lancer le concours**.

## Participer

Les membres cliquent sur **🎉 Participer**. Le compteur se met à jour, et un second clic retire la participation. Si un rôle est requis, les autres reçoivent un message les en informant.

## Fin et tirage

À l'heure prévue, Kron tire les gagnants au hasard (tirage cryptographique), met à jour le message et annonce les gagnants en les mentionnant.

- `/giveaway end id:12` : termine tout de suite.
- `/giveaway reroll id:12` : retire de nouveaux gagnants, en excluant les précédents.

Les commandes sont réservées aux membres qui ont **Gérer le serveur**. Le plan gratuit permet 5 concours actifs à la fois.
