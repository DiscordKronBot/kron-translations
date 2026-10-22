---
title: Alertes Twitch et Kick
category: modules
emoji: 🟣
summary: Annoncer automatiquement quand une chaîne Twitch ou Kick passe en live.
order: 20
---

Les modules **Twitch** et **Kick** (Pro) publient une alerte dès qu'une chaîne suivie passe en live : titre du stream, catégorie, nombre de spectateurs, aperçu du live et bouton **Regarder**.

## Suivre une chaîne

1. Active le module **Twitch** ou **Kick**.
2. Entre le nom de la chaîne (celui de l'URL, par exemple `twitch.tv/`**`xqc`**) et clique sur **Ajouter** : Kron vérifie qu'elle existe.
3. Choisis le **salon** de l'alerte, les **rôles à mentionner** (jusqu'à 5) et, si tu veux, **@everyone**.
4. Personnalise le **message** au besoin, puis enregistre.

Variables du message : `{streamer}`, `{title}`, `{game}`, `{url}`.

## Fonctionnement

- Kron vérifie les chaînes **chaque minute**. Un live est annoncé **une seule fois**, même si Kron redémarre pendant le stream.
- **Fin du live** : l'alerte peut passer en gris avec la durée du stream, être supprimée, ou rester telle quelle.
- Jusqu'à **50 chaînes** par serveur et par plateforme.
