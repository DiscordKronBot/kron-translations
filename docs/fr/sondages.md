---
title: Sondages
category: modules
emoji: 📊
summary: Sondages avec durée, choix multiples, résultats cachés et barres de résultats.
order: 22
---

`/sondage` publie une carte avec un bouton par choix et des barres de résultats en direct.

## Créer un sondage

```
/sondage question:Quel repas vendredi ? choix:Pizza | Sushis | Tacos duree:60 multiple:non cache:non
```

- **choix** : de 2 à 10, séparés par `|`.
- **duree** : en minutes ; vide = jusqu'à ce qu'on clique sur **Terminer**.
- **multiple** : chaque membre peut cocher plusieurs choix.
- **cache** : les résultats restent cachés jusqu'à la fin.

Un membre change son vote en recliquant. À la fin, le choix gagnant reçoit 🏆.

## Qui peut créer des sondages

Par défaut, les membres qui peuvent gérer les messages. Ajoute des rôles dans le dashboard pour l'ouvrir à d'autres. Le dashboard liste aussi les sondages récents.
