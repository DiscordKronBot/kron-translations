---
title: Commandes personnalisées
category: modules
emoji: ⚡
summary: Créer tes propres commandes slash ou tags texte (!regles, $ip…), avec une réponse en texte ou en embed.
order: 16
---

Le module **Commandes personnalisées** ajoute à ton serveur de vraies commandes slash (`/regles`, `/ip`, `/boutique`…) ou des **tags texte** (`!regles`, `$ip`, ou juste `regles`).

## Créer une commande

1. Active le module. La page a deux onglets : **⚡ Commandes** (slash) et **🏷️ Tags** (texte).
2. Dans le bon onglet, clique sur **Nouvelle commande** ou **Nouveau tag**.
3. Choisis le **nom** (minuscules, chiffres, `-` et `_`) et, pour une commande slash, la **description** affichée dans Discord.
4. Écris la **réponse** avec l'éditeur : texte, embeds, boutons de lien. L'aperçu se met à jour en direct.
5. Enregistre : la commande est disponible tout de suite sur ton serveur.

Variables disponibles dans la réponse : `{user}`, `{username}`, `{server}`, `{channel}`, `{memberCount}`, `{user.avatar}`.

## Tags texte

Choisis un **préfixe** (`!`, `$`, `?`, `.`, `-`, `+` ou aucun) et un nom. Quand un message est exactement le déclencheur (par exemple `!regles`, `$ip` ou juste `regles`), Kron répond avec ton message ou ton embed.

- **Répondre au message** : la réponse s'affiche en réponse au message du membre, sinon comme un message simple.
- **Supprimer le message déclencheur** : garde le salon propre.
- Un même membre ne déclenche un tag qu'une fois toutes les 3 secondes.

> [!NOTE]
> `$debug` est réservé à Kron. Un nouveau tag peut prendre jusqu'à 30 secondes pour répondre la première fois.

## Options

- **Réponse privée** (slash) : seul le membre qui utilise la commande voit la réponse.
- **Rôles autorisés** : seuls ces rôles peuvent l'utiliser (vide = tout le monde). Un tag reste muet pour les autres.
- **Donner un rôle / retirer un rôle** : par exemple, `/accepter` donne le rôle « Règlement lu ».

> [!NOTE]
> Le plan gratuit permet 5 commandes. Pro les rend illimitées.

Désactiver le module retire les commandes slash de Discord et coupe les tags, sans rien effacer : tout revient à la réactivation.
