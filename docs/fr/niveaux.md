---
title: Niveaux et économie
category: modules
emoji: ⭐
summary: XP en discutant, niveaux, rôles en récompense, classement et monnaie du serveur.
order: 15
popular: true
---

Le module **Niveaux et économie** récompense les membres actifs : chaque message rapporte de l'XP, l'XP fait monter de niveau, et les niveaux peuvent donner des rôles.

## Gain d'XP

- Chaque message donne entre **15 et 25 XP** (réglable), une fois par **délai** (60 secondes par défaut) pour éviter le spam.
- Tu peux exclure des **salons** (ou des catégories entières) et des **rôles**.
- La courbe suit le standard : le niveau 1 demande 100 XP, chaque niveau suivant un peu plus.

## Passage de niveau

Choisis où annoncer un nouveau niveau : dans le salon du message, dans un **salon dédié** (pratique pour garder les autres salons propres), en message privé, ou nulle part.

Le message accepte les variables `{user}` (mention), `{username}` et `{level}`.

## Récompenses de rôles

Associe un rôle à un niveau : il est donné automatiquement quand le membre l'atteint. Par défaut, les anciens rôles sont gardés; désactive **Garder les anciens rôles** pour ne garder que le plus haut.

> [!NOTE]
> Le plan gratuit permet 5 récompenses. Pro les rend illimitées.

## Économie

Active l'économie pour donner une monnaie (nom et emoji au choix) :

- des pièces à chaque message qui donne de l'XP;
- une récompense quotidienne avec `/daily`;
- des dons entre membres avec `/pay`.

## Travail, vol, banque et boutique

- `/travail` : un gain au hasard (entre le minimum et le maximum), une fois par délai.
- `/voler @membre` : une chance de voler une partie de son portefeuille ; raté, tu paies une amende. Désactivable.
- `/banque` : dépose ton argent pour le protéger du vol, retire-le ou consulte ton solde.
- `/boutique` : achète des **rôles** et des **objets** avec le menu ; `/inventaire` montre ce que tu possèdes.

Tout se règle dans le dashboard : gains, délais, chances, et les articles de la boutique.

## Commandes

| Commande | Effet |
|---|---|
| `/rank [membre]` | Niveau, XP, rang et barre de progression |
| `/top [xp ou pièces]` | Les 10 premiers |
| `/balance [membre]` | Solde de pièces |
| `/daily` | Récompense quotidienne (toutes les 20 h) |
| `/pay membre montant` | Donner des pièces |
| `/xp give, remove, reset` | Staff (Gérer le serveur) : ajuster l'XP d'un membre |

Le classement complet est aussi dans le dashboard, onglet **Classement**, avec un bouton pour remettre un membre à zéro.
