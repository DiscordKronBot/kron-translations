---
title: Jeux
category: modules
emoji: 🎮
summary: Morpion, puissance 4, pendu, Wordle, blackjack, quiz et plus, avec mises et classement.
order: 21
---

Le module **Jeux** ajoute la commande **/jeu** : chaque partie se joue dans une carte interactive, avec des boutons et des menus.

## Les jeux

| Jeu | Commande | Comment |
|---|---|---|
| ❌ Morpion | `/jeu morpion` | contre un membre, ou contre Kron si tu ne choisis personne |
| 🔴 Puissance 4 | `/jeu puissance4` | idem, Kron bloque tes coups gagnants |
| 🪢 Pendu | `/jeu pendu` | choisis les lettres dans les menus, 6 erreurs permises |
| 🟩 Wordle | `/jeu wordle` | trouve le mot de 5 lettres en 6 essais |
| 🃏 Blackjack | `/jeu blackjack mise:100` | carte, rester ou doubler contre le croupier |
| 🪙 Pile ou face | `/jeu pileouface` | avec une mise optionnelle |
| ✊ Chifoumi | `/jeu chifoumi` | pierre, feuille, ciseaux contre Kron |
| 🧠 Quiz | `/jeu quiz` | une question pour tout le salon, le premier qui répond juste gagne |
| 🔢 Devine | `/jeu devine` | un nombre entre 1 et 100 en 7 essais |
| 🎲 Dé / 🎱 8ball | `/jeu de`, `/jeu 8ball` | pour le fun |

Les mots et les questions suivent la langue du serveur (français ou anglais).

## Mises et récompenses

Les mises (blackjack, pile ou face) et les **pièces par victoire** utilisent la monnaie du module [Niveaux et économie](/docs/niveaux) : active l'économie pour qu'elles fonctionnent. La mise maximale se règle dans le dashboard.

## Comptage

Un salon où les membres comptent ensemble : **1**, **2**, **3**… un nombre par message.

- Un bon nombre reçoit ✅.
- Un mauvais nombre reçoit ❌ et Kron rappelle le prochain nombre : le compte continue, il ne repart pas à zéro.
- Un membre ne peut pas compter **deux fois de suite** : il faut attendre qu'un autre membre joue.
- Les messages qui ne commencent pas par un nombre sont ignorés (on peut jaser).

Dans le dashboard, section **Comptage** : choisis un salon ou clique sur **🔢 Créer** (nom et emoji modifiables ; Kron suggère ta catégorie de jeux ou de communauté). Le compte actuel et le record s'y affichent.

## Réglages

- **Jeux disponibles** : décoche un jeu pour le retirer du serveur.
- **Salons des jeux** : limite les parties à certains salons (vide = partout).
- **Meilleurs joueurs** : le classement des victoires. `/jeu stats` montre les statistiques d'un membre.
