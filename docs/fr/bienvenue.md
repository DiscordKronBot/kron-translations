---
title: Bienvenue et au revoir
category: modules
emoji: 👋
summary: Accueillir chaque nouveau membre dans un salon et en MP, et annoncer les départs.
order: 7
---

## Arrivée

- **Salon** : où publier le message de bienvenue.
- **Message dans le salon** : une carte par défaut (avatar, date de création du compte, bot ou membre, numéro du membre), ou ton message personnalisé avec l'éditeur, qui part de cette carte.
- **Message privé** : optionnel, envoyé directement au nouveau membre (par exemple le lien de ta whitelist ou ton règlement).

## Départ

- **Salon** et **message** d'au revoir, désactivés par défaut.

## Variables

| Variable | Remplacée par |
|---|---|
| `{user}` | mention du membre |
| `{username}` | nom du membre |
| `{server}` | nom du serveur |
| `{memberCount}` | nombre de membres |
| `{user.avatar}` | avatar du membre, à utiliser comme image ou miniature |
| `{user.id}` | ID du membre |
| `{user.created}` / `{user.createdAgo}` | date de création du compte / son âge (« il y a 2 ans ») |
| `{user.type}` | 🤖 Bot ou 👤 Membre |
| `{user.joined}` | arrivée sur le serveur (utile pour les départs) |
| `{server.icon}` | icône du serveur |

> [!TIP]
> Mets `{user.avatar}` dans la **miniature** de l'embed : chaque bienvenue affiche la photo du nouveau membre.

## Options

- **Ignorer les bots** (activé par défaut) : aucun message pour les bots qui rejoignent.
- Seul `{user}` peut mentionner le membre : jamais de @everyone ni de rôles par accident.
