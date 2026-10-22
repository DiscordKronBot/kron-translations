---
title: Questions fréquentes
category: help
emoji: ❓
summary: Les réponses aux questions qu'on nous pose le plus souvent.
order: 2
---

## Kron ne répond pas à une commande

1. Vérifie que le **module est activé** dans le dashboard (switch verte à côté du titre du module).
2. Tape `$debug` dans le salon : il montre les permissions qui manquent.
3. Les slash commands peuvent mettre quelques minutes à apparaître après l'arrivée du bot. Redémarre Discord si besoin (`Ctrl + R`).

## Kron ne donne pas un rôle

Le rôle de Kron doit être **au-dessus** du rôle à donner. Voir [Permissions et rôles](/docs/permissions).

## Je ne vois pas mon serveur dans le dashboard

Tu dois avoir **Gérer le serveur** ou **Administrateur** sur ce serveur. Clique sur **Actualiser** en haut de la liste : Discord peut prendre une minute à nous transmettre un nouveau serveur.

## J'ai modifié un panel mais rien ne change dans Discord

Les panels de tickets et les menus de rôles doivent être **republiés** (bouton 📤 Publier) après avoir enregistré.

## Est-ce que Kron lit mes messages ?

Kron reçoit les messages des salons où il est présent, comme tout bot qui a l'intent Message Content. Il ne les enregistre pas : le module Logs garde seulement les messages récents en mémoire **1 heure**, pour afficher le contenu d'un message supprimé. Les niveaux comptent les messages, jamais leur contenu. Voir la [politique de confidentialité](/legal/privacy).

## Comment supprimer mes données ?

Écris à [dev@kronbot.xyz](mailto:dev@kronbot.xyz) avec « Confidentialité » dans l'objet. Nous répondons dans un délai de 30 jours. Les données d'un serveur dont Kron a été retiré sont supprimées automatiquement après 30 jours.

## Kron est-il lié à Discord ?

Non. Kron est un produit indépendant, non affilié à Discord Inc.

## Une autre question ?

Ouvre un ticket sur notre serveur : [kronbot.xyz/support](https://kronbot.xyz/support).
