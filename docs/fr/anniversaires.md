---
title: Anniversaires
category: modules
emoji: 🎂
summary: Souhaiter les anniversaires automatiquement, avec un rôle pour la journée.
order: 10
---

## Pour les membres

| Commande | Effet |
|---|---|
| `/birthday set day:14 month:3` | enregistrer sa date (l'année est optionnelle) |
| `/birthday set day:14 month:3 year:2001` | avec l'année, `{age}` devient disponible |
| `/birthday remove` | retirer sa date |
| `/birthday upcoming` | les 10 prochains anniversaires |

## Réglages

| Réglage | Effet |
|---|---|
| Salon | où publier les souhaits |
| Rôle du jour | donné le jour de l'anniversaire, retiré le lendemain |
| Heure de l'annonce | à partir de quelle heure les souhaits partent |
| Fuseau horaire | ex. `America/Toronto` : le « jour » suit ce fuseau |
| Message | texte par défaut, ou message personnalisé |

Variables : `{user}`, `{username}`, `{age}`, `{server}`, `{user.avatar}`.

> [!NOTE]
> Chaque anniversaire n'est souhaité qu'une seule fois par jour, même si Kron redémarre.
