---
title: Ajouter Kron à ton serveur
category: start
emoji: 🚀
summary: Inviter le bot, te connecter au dashboard et activer ton premier module en 5 minutes.
order: 1
popular: true
---

Kron est un bot Discord tout-en-un : tickets, whitelist avec formulaires web, logs, rôles, embeds, concours et bien plus. Tout se configure depuis le dashboard **kronbot.xyz**, sans une ligne de code.

## 1. Inviter Kron

1. Va sur [kronbot.xyz/invite](https://kronbot.xyz/invite), ou clique sur **Ajouter l'app** dans le profil de Kron sur Discord.
2. Choisis le serveur. Tu dois avoir la permission **Gérer le serveur** sur ce serveur.
3. Laisse toutes les permissions cochées et clique sur **Autoriser**.

> [!IMPORTANT]
> Kron demande la permission **Administrateur** : sans elle, les salons privés lui sont invisibles et plusieurs fonctions ne marchent pas. Il ne fait que ce que tu configures. Le détail est dans [Permissions et rôles](/docs/permissions#pourquoi-administrateur).

## 2. Placer le rôle de Kron

Discord ne laisse un bot gérer un rôle que si **son propre rôle est placé plus haut** dans la liste.

1. Ouvre **Paramètres du serveur → Rôles**.
2. Glisse le rôle **Kron** au-dessus des rôles qu'il doit donner ou retirer (par exemple `@nouveau`, `@citoyen`, les rôles de tes menus).
3. Enregistre.

> [!TIP]
> Dans le dashboard, un rôle trop haut pour Kron est signalé par ⚠️. La commande `$debug` le signale aussi.

## 3. Te connecter au dashboard

1. Va sur [kronbot.xyz](https://kronbot.xyz) et clique sur **Se connecter**.
2. Une vérification anti-robot rapide s'affiche, puis Discord te demande d'autoriser Kron.
3. Kron ne demande que ton **profil** et la **liste de tes serveurs**. Il n'a aucun accès à tes messages.

Tu arrives sur **Tes serveurs**. Seuls les serveurs où tu peux **gérer le serveur** apparaissent. Ceux où Kron n'est pas encore présent ont un bouton **Inviter**.

## 4. Activer un module

1. Clique sur ton serveur.
2. Dans la barre latérale, choisis un module (par exemple **Tickets**).
3. Active la switch à côté du titre du module (vert = activé, rouge = désactivé) : elle s’enregistre tout de suite.
4. Configure le module. Une barre **Modifications non enregistrées** apparaît en bas : clique sur **Enregistrer**.

> [!NOTE]
> Un module désactivé peut être configuré à l'avance. Il fonctionnera dès que tu l'activeras.

## 5. Choisir la langue

Dans **Paramètres**, choisis la langue de Kron pour ton serveur (français ou anglais). Elle sert aux messages publics du bot. Les messages privés et les réponses visibles par une seule personne suivent la langue Discord de chaque membre.

## Et ensuite ?

- [Mettre en place une whitelist](/docs/whitelist), avec un formulaire web et des rôles par étape.
- [Créer un système de tickets](/docs/tickets) entièrement personnalisé.
- [Activer les logs](/docs/logs) en un clic.
- [Relier ton serveur FiveM](/docs/fivem-installation) pour afficher les personnages des joueurs dans les tickets.
