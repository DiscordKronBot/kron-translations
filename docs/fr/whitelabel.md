---
title: Whitelabel, ton propre bot
category: premium
emoji: 🏷️
summary: Toutes les fonctions de Kron sous ton nom et ton avatar, avec ta propre application Discord.
order: 2
---

Avec le **Whitelabel**, ton serveur utilise **ton propre bot** : son nom, son avatar et son statut sont les tiens, mais il fonctionne avec Kron, avec la même configuration et le même dashboard kronbot.xyz.

## Ce qu'il te faut

- L'offre **Whitelabel** sur ton serveur (Mensuel + Whitelabel à 6,99 $ USD, ou inclus dans les offres Annuel et À vie).
- Une **application Discord** que tu crées toi-même, gratuitement.

## 1. Ouvrir le portail développeur

Va sur [discord.com/developers/applications](https://discord.com/developers/applications).

## 2. Créer ton application

Clique sur **New Application**, donne-lui un nom et accepte les conditions.

![Developer Portal : New Application](/docs/whitelabel/1-new-application.svg)

## 3. Onglet Installation

Dans **Default Install Settings**, choisis :

- **User Install**, scopes : `applications.commands`
- **Guild Install**, scopes : `applications.commands` et `bot`
- **Guild Install**, permissions : `Administrator`

Save Changes.

## 4. Onglet Bot

1. Clique sur **Reset Token** et copie le token (garde-le pour l'étape 6).
2. Dans **Privileged Gateway Intents**, active :
   - **Server Members Intent** (rôles automatiques, bienvenue, logs, whitelist) ;
   - **Message Content Intent** (`$debug`, logs des messages, tags, niveaux).
3. Save Changes. Kron refuse le token tant que ces deux intents ne sont pas activés.

![Onglet Bot : intents Server Members et Message Content activés, puis Save Changes](/docs/whitelabel/2-intents.svg)

![Onglet Bot : Reset Token, puis Copy](/docs/whitelabel/3-reset-token.svg)

## 5. Onglet General Information

Choisis l'**avatar**, le **nom** et la **description** (la bio) de ton bot, puis **Save Changes**.

## 6. Connecter ton bot

1. Dashboard Kron, **Paramètres → Whitelabel**, colle le token puis **Connecter**. Kron vérifie le token auprès de Discord, puis le chiffre.
2. Clique sur **Inviter ton bot** : le lien ajoute ton bot à ton serveur.

Kron héberge ton bot : il reste **en ligne 24 h/24**, rien à faire tourner de ton côté.

![Dashboard Kron : Paramètres, Whitelabel, colle le token, Connecter](/docs/whitelabel/4-connect.svg)

> [!WARNING]
> Le token permet de contrôler ton bot. Ne le donne jamais à personne : colle-le seulement dans le dashboard Kron. S'il a fuité, clique sur **Reset Token** et remplace-le dans **Paramètres → Whitelabel**.

## 7. Ton bot prend le relais

En moins d'une minute, ton bot passe **en ligne** et ses commandes slash apparaissent. **Kron quitte alors ton serveur automatiquement** : ton bot reprend toute ta configuration (modules, tickets, formulaires, niveaux…) sans que tu aies à refaire quoi que ce soit.

Dans **Paramètres → Whitelabel**, tu peux ensuite changer :

- le **nom** du bot (Discord limite à environ 2 changements par heure) ;
- son **avatar** ;
- son **statut** (le texte sous son nom).

Ton bot n'affiche jamais la signature « Kron ». Il ne fonctionne que dans ton serveur : ajouté ailleurs, il quitte le serveur.

## Les messages existants

Discord ne permet pas à un bot de modifier les messages envoyés par un autre bot. Après le passage au Whitelabel, republie depuis le dashboard :

- tes **panels de tickets** (bouton Publier) ;
- tes **menus de rôles** (bouton Publier) ;
- les **embeds** que tu veux pouvoir modifier plus tard.

## Déconnecter ton bot

**Paramètres → Whitelabel → Déconnecter le bot** arrête ton bot. Réinvite ensuite Kron (le lien s'ouvre automatiquement) : ta configuration est intacte.

## À la fin de l'abonnement

Après **7 jours de grâce**, ton bot s'arrête. Ta configuration est conservée : réinvite Kron et republie tes panels pour continuer avec la version standard.
