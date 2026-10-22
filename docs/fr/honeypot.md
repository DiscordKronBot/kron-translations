---
title: Honeypot
category: modules
emoji: 🍯
summary: Un salon piège qui attrape les spambots : ils écrivent, Kron les bannit ou les expulse.
order: 17
---

Les spambots écrivent dans tous les salons qu'ils voient. Le **Honeypot** crée un salon piège où personne n'a de raison d'écrire : quiconque y poste est sanctionné tout de suite.

## Mise en place

1. Active le module **Honeypot**.
2. Choisis le **nom** du salon et, si tu veux, sa **catégorie**, puis clique sur **Créer le salon piège**.
3. Kron crée le salon en bas de la liste, ouvert à tous, avec un avertissement bien visible : « Ne pas écrire ici ».

## Sanction

| Action | Effet |
|---|---|
| Bannir | le compte reste banni, avec un bouton **Débannir** dans le log |
| Softban | bannit puis débannit tout de suite : une expulsion qui efface aussi ses messages |
| Expulser | expulse seulement |

Avec **Effacer les messages**, les messages de la dernière heure du compte sont supprimés (bannir et softban).

## Log

Choisis un **salon de log** : chaque prise y est rapportée (membre, âge du compte, date d'arrivée, message). En cas d'erreur (bannissement par erreur), le bouton **Débannir** annule la sanction.

> [!NOTE]
> Les membres qui peuvent **Gérer les messages** (le staff) et le propriétaire ne sont jamais sanctionnés.
