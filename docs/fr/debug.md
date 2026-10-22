---
title: Diagnostic $debug et support
category: help
emoji: 🩺
summary: Vérifier en une commande ce qui bloque, et partager le rapport avec le support.
order: 1
popular: true
---

## La commande $debug

Tape `$debug` dans **n'importe quel salon** de ton serveur. Kron répond avec un diagnostic complet, puis efface ta commande.

Le rapport contient :

- **L'état général** : ✅ tout est en ordre, ou ⚠️ le nombre de problèmes détectés.
- **Les permissions** de Kron sur le serveur et dans ce salon (par exemple `🛡️ Serveur ┆ ✅ 12/12`), avec la liste précise de ce qui manque.
- **Le serveur** : nom, ID, membres, salons (sur 500), rôles (sur 250), boosts, langue, date de création.
- **Kron** : version, offre, modules actifs, position de son rôle, latence, temps en ligne, date d'arrivée.
- **Le salon** et **toi** : ton niveau (propriétaire, administrateur, gestionnaire, membre).

> [!TIP]
> Tape `$debug` **dans le salon qui pose problème** : le score « Salon » montre exactement ce que Kron peut faire à cet endroit.

## Le lien du rapport

Kron te donne un lien du type `kronbot.xyz/d/AbC123xYz9` :

- il ouvre une page web avec le même diagnostic, lisible sans Discord ;
- collé dans un salon Discord, il affiche un aperçu (état et score des permissions) ;
- il est conservé **90 jours**, puis supprimé automatiquement ;
- le code est aléatoire et impossible à deviner.

## Obtenir de l'aide

1. Tape `$debug` dans le salon concerné.
2. Rejoins notre serveur de support : [kronbot.xyz/support](https://kronbot.xyz/support).
3. Ouvre un ticket et colle le lien du rapport.

L'équipe voit alors exactement ce que tu vois. C'est le moyen le plus rapide d'obtenir une réponse.

> [!NOTE]
> Pour les questions de facturation ou de confidentialité, tu peux aussi écrire à [dev@kronbot.xyz](mailto:dev@kronbot.xyz).
