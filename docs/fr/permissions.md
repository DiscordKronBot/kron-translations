---
title: Permissions et rôles
category: start
emoji: 🔐
summary: Ce que Kron demande, pourquoi, et comment régler la hiérarchie des rôles.
order: 2
---

Quand tu invites Kron (bouton **Ajouter l'app** de son profil, lien du site ou du dashboard), il demande la permission **Administrateur**.

## Pourquoi Administrateur ?

Sur Discord, un salon privé se cache de **tous les rôles** qui n'y sont pas ajoutés, même d'un bot qui a « Gérer les salons ». Sans Administrateur, chaque salon privé devient invisible pour Kron, et beaucoup de fonctions cassent sans prévenir :

- **Embellir les noms** et le constructeur de salons ne peuvent pas renommer ni déplacer ces salons ;
- les **logs** ne voient pas les messages supprimés ou modifiés dans ces salons ;
- la **modération** (`/purge`), les **tickets**, les **compteurs** et l'**anti-raid** n'y agissent pas ;
- chaque nouveau salon privé demande d'y ajouter le rôle Kron à la main.

Avec Administrateur, Kron voit et gère tout ton serveur comme prévu, sans réglage salon par salon.

Ce que Kron fait avec :

- **seulement ce que tu configures** dans le dashboard ou par commande : il ne supprime jamais un salon, un rôle ou un message de lui-même, et l'embellissement ne fait que renommer ;
- chaque action dans le dashboard est faite au nom d'un membre qui a **Gérer le serveur** ou **Administrateur**, revérifié par nos serveurs à chaque fois ;
- les actions importantes laissent une trace dans le **journal d'audit** de Discord avec la raison « Kron : … ».

> [!NOTE]
> Tu peux retirer Administrateur et donner seulement les permissions de la liste ci-dessous. Kron fonctionne alors, mais il faut ajouter son rôle à chaque salon privé qu'il doit gérer. Le constructeur de salons marque d'un 🔒 les salons qu'il ne voit pas.

Les **rôles du staff** n'ont jamais besoin d'Administrateur pour utiliser Kron.

## Permissions utilisées

| Permission | Utilisée par |
|---|---|
| Voir les salons | tous les modules |
| Envoyer des messages | tous les modules |
| Intégrer des liens | embeds, logs, tickets, whitelist |
| Joindre des fichiers | transcriptions des tickets |
| Voir l'historique des messages | transcriptions, `/purge` |
| Gérer les messages | `/purge`, `$debug` (efface ta commande) |
| Gérer les salons | tickets, salons de logs, compteurs, salons FiveM, constructeur de salons |
| Gérer les rôles | whitelist, rôles automatiques, rôles par réaction, tickets, niveaux, commandes personnalisées |
| Voir les logs d'audit | module Logs (qui a banni, expulsé, exclu) |
| Gérer le serveur | AutoMod (règles de Discord), anti-raid (pause des invitations) |
| Expulser des membres | `/kick`, anti-raid |
| Bannir des membres | `/ban`, `/unban`, anti-raid, honeypot |
| Exclure temporairement des membres | `/timeout`, `/untimeout` |

> [!WARNING]
> Si tu retires une permission, le module qui en dépend arrête de fonctionner pour cette action. `$debug` affiche la liste exacte de ce qui manque.

## La hiérarchie des rôles

Discord applique une règle simple : **un bot ne peut gérer que les rôles placés sous son propre rôle**. Il ne peut pas non plus agir sur un membre dont le rôle le plus haut est au-dessus du sien.

Pour que tout fonctionne :

1. Ouvre **Paramètres du serveur → Rôles**.
2. Place le rôle **Kron** au-dessus de tous les rôles qu'il doit donner : rôles de whitelist, rôles automatiques, rôles des menus, rôle d'anniversaire, récompenses de niveaux.
3. Pour la modération, place-le au-dessus des membres qu'il doit pouvoir sanctionner.

> [!TIP]
> Dans le dashboard, chaque sélecteur de rôle marque d'un ⚠️ les rôles que Kron ne peut pas gérer.

## Permissions des salons

Une permission refusée dans un salon (ou dans sa catégorie) s'applique aussi à Kron. Si Kron ne peut pas écrire dans un salon, le dashboard le signale à l'envoi, et `$debug` tapé dans ce salon montre le score **Salon**.

## Qui peut utiliser les commandes ?

- Les commandes de **modération** sont réservées par défaut aux membres qui ont la permission Discord correspondante (Expulser, Bannir, Exclure, Gérer les messages).
- Tu peux affiner qui voit chaque commande dans **Paramètres du serveur → Intégrations → Kron**.
- Dans le dashboard, seuls les membres qui ont **Gérer le serveur** ou **Administrateur** peuvent configurer Kron. Les permissions sont revérifiées par nos serveurs à chaque action.
