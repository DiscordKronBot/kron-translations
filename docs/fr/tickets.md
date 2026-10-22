---
title: Tickets
category: modules
emoji: 🎫
summary: Panels à boutons ou menu, questions avant l'ouverture, prise en charge, fermeture automatique et transcriptions web.
order: 2
popular: true
---

Le module **Tickets** crée un salon privé entre un membre et ton équipe. Tout est personnalisable : le message du panel, chaque bouton, la catégorie, les rôles du support, le nom des salons, les questions et le message d'accueil.

## Installation rapide

**⚡ Installation rapide** crée tout en un clic : une catégorie `🆘┆Support`, un salon public `🎫┆tickets` avec un panel prêt à l'emploi, et dans ta catégorie de logs (réutilisée si elle existe) les salons privés `🔕┆logs-ticket` et `🔕┆ticket-transcripts`.

Choisis d'abord les rôles du staff : ils voient les tickets, les logs et les transcriptions. Tu choisis aussi :

- **la catégorie des tickets** : une catégorie existante, ou une nouvelle `🆘┆Support` ;
- **la catégorie des logs** : celle que Kron a créée en premier sur ton serveur est proposée d'office (conseil : configure le module [Logs](/docs/logs) avant, tous les modules rangent ensuite leurs logs au même endroit) ;
- **le salon des règles** et **un lien de doc ou FAQ** : ils apparaissent dans le texte du panel ;
- **l'apparence** du panel (voir plus bas). Dans l'aperçu **Sera créé**, clique sur une ligne pour la renommer, changer son emoji ou choisir qui peut la voir.

## Créer un panel

1. Ouvre **Tickets** puis **Nouveau panel**. Un modèle « Support » et « Plainte » est prêt.
2. **Message** : l'embed du panel (titre, description, couleur, image…). L'aperçu montre les boutons.
3. **Boutons** : un bouton par type de ticket (jusqu'à 10).
4. **Paramètres** : le salon où publier le panel, l'affichage (boutons ou menu), les transcriptions.
5. Enregistre avec la barre du bas, puis clique sur **📤 Publier**.

Après une modification, clique de nouveau sur **Publier** : Kron met à jour le message existant au lieu d'en créer un nouveau.

> [!NOTE]
> Le plan gratuit permet 1 panel. Chaque panel peut avoir jusqu'à 10 types de tickets.

## Apparence du panel

Dans l'onglet **Message**, quatre aperçus montrent ton vrai panel de quatre façons. Clique celui que tu préfères :

| Apparence | Ce que voient les membres |
|---|---|
| Embed + boutons | le message Discord classique, un bouton par type de ticket |
| Embed + menu déroulant | un seul menu, pratique avec beaucoup de types |
| Carte + boutons | la nouvelle mise en page de Discord (Components V2) : texte, image et boutons dans un seul bloc |
| Carte + menu déroulant | la carte, avec un menu |

Deux interrupteurs ajoutent **l'icône du serveur** à côté du texte et **la bannière du serveur** en bas (si ton serveur en a une). Le bloc **Contenu rapide** ajoute en une fois « lis les règles dans #règles » et ton lien de doc dans le message.

En passant d'un embed à une carte (ou l'inverse), **Publier** remplace l'ancien message : Discord ne permet pas de transformer l'un en l'autre.

## Régler un type de ticket

| Réglage | Effet |
|---|---|
| Texte, emoji | ce qui s'affiche sur le bouton |
| Couleur du bouton | bleu, gris, vert ou rouge |
| Description | sous l'option, en mode menu |
| Catégorie | où les salons de ticket sont créés |
| Nom du salon | une règle prête (`ticket-0001`, `ticket-bob`, `ticket-bobby`…) ou ton modèle avec `{number}` (0001), `{username}` (nom d'utilisateur) et `{nickname}` (pseudo sur le serveur) |
| Équipe de support | rôles qui voient les tickets, sont mentionnés et peuvent les gérer |
| Questions | jusqu'à 5, posées dans une fenêtre Discord avant l'ouverture : réponse écrite (courte ou longue) ou choix dans un menu déroulant (un ou plusieurs choix), obligatoire ou non |
| Message d'accueil | texte par défaut, ou message personnalisé avec l'éditeur |

Variables du message d'accueil : `{user}`, `{username}`, `{number}` (numéro sur 4 chiffres), `{server}`, `{type}`.

## La vie d'un ticket

1. **Ouverture** : le membre clique sur un bouton, répond aux questions éventuelles, et Kron crée le salon. Seuls le membre, l'équipe et Kron y ont accès. Les réponses s'affichent dans un embed, avec le nombre de tickets du membre et un lien vers son historique.
2. **🙋 Prendre en charge** : un membre de l'équipe signale qu'il s'en occupe.
3. **🔒 Fermer** : le membre ou l'équipe ferme, avec une raison optionnelle. Le membre garde la lecture mais ne peut plus écrire, et la transcription est envoyée.
4. **🔓 Rouvrir**, **📜 Transcription** ou **🗑️ Supprimer** : le salon est supprimé 5 secondes après.

## Fermeture automatique

Dans les réglages du module, **Fermeture automatique** ferme les tickets ouverts sans aucun message depuis un certain nombre d'heures (48 par défaut). Les tickets pris en charge sont ignorés par défaut. La transcription est sauvegardée comme d'habitude.

## Transcriptions

À la fermeture, Kron sauvegarde toute la conversation (messages, embeds, pièces jointes) sur une **page web** :

- le lien est publié dans le **salon des transcriptions** choisi ;
- et envoyé en **MP au membre** si l'option est cochée ;
- la page propose un bouton **Télécharger (.html)**.

Les membres retrouvent leurs tickets dans **Mes tickets** ; le staff voit l'historique complet d'un membre.

## Limites et sécurité

- **Tickets ouverts maximum par membre** (1 par défaut) : évite les doublons.
- Kron vérifie que les catégories et salons choisis appartiennent bien à ton serveur.

## Avec le module FiveM

Si le [module FiveM](/docs/fivem-fonctions) est activé avec l'option « Profil dans les tickets », chaque ticket affiche automatiquement les personnages du joueur en ville, avec les boutons staff **📍 Débloquer** et **🚗 Rapatrier un véhicule**.

## Questions fréquentes

**« Impossible de créer le salon du ticket ».** Kron n'a pas la permission Gérer les salons dans la catégorie choisie. Lance `$debug`.

**Le support ne voit pas les tickets.** Ajoute ses rôles dans « Équipe de support », sur chaque type de ticket.

**J'ai modifié le panel mais rien ne change dans Discord.** Clique sur **Publier** après avoir enregistré.

## Priorité, notes internes et satisfaction

- **🚦 Priorité** : le staff choisit Basse, Normale, Haute ou Urgente. Le nom du salon prend une pastille (🟢 🟠 🔴).
- **📝 Note** : une note interne, visible seulement par le staff sur la page web du ticket.
- **⭐ Note du membre** : à la fermeture, le membre note l'aide reçue de 1 à 5 étoiles.
- L'onglet **Statistiques** du module montre, par membre du staff, les tickets pris en charge et fermés, et la note moyenne.
