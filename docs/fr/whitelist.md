---
title: Whitelist et formulaires
category: modules
emoji: 📝
summary: Un formulaire web, des rôles qui changent à chaque étape, et la révision des candidatures directement dans Discord.
order: 1
popular: true
---

Le module **Whitelist & formulaires** remplace les outils externes de candidature. Le joueur remplit un formulaire sur le web, connecté avec son compte Discord (aucun ID à taper), et ton staff accepte ou refuse en un clic dans Discord.

## Comment ça marche

1. Le nouveau membre arrive sur le serveur et reçoit `@nouveau` (module [Rôles automatiques](/docs/roles-auto)).
2. Il ouvre le lien du formulaire (`kronbot.xyz/f/xxxxxx`), se connecte avec Discord et répond aux questions.
3. Kron poste la candidature dans ton salon de révision, avec les boutons **✅ Accepter**, **❌ Refuser** et **🎙️ Entrevue**, et lui donne `@passport`.
4. Le staff accepte : Kron donne `@citoyen` et retire `@passport` et `@nouveau`. Le joueur reçoit un MP.
5. Ou le staff refuse avec une raison : Kron retire `@passport` et envoie la raison en MP. Le joueur peut réessayer après le délai choisi.

## Créer ton formulaire

1. Ouvre le module **Whitelist & formulaires** et clique sur **Nouveau formulaire**.
2. Choisis un **modèle** (whitelist, staff RP, modération, développeur) et sa **langue** (français ou anglais), ou un formulaire vide.
3. Ajuste chaque onglet, puis enregistre avec la barre du bas.
4. Copie le **lien public** dans l'onglet Général et partage-le (salon d'accueil, message de bienvenue, panel de tickets…).

> [!NOTE]
> Le plan gratuit permet **1 formulaire**. Le Pro permet des formulaires illimités (whitelist, recrutement staff, développeurs…).

## Onglet Général

| Réglage | Effet |
|---|---|
| Nom | visible seulement par le staff |
| Couleur | couleur de la page publique et de l'embed de candidature |
| Formulaire ouvert | décoché, le formulaire n'accepte plus de candidatures |
| Titre affiché | titre de la page publique |
| Description | texte d'introduction, avec mise en forme (gras, listes, liens) |
| Délai après un refus | heures avant de pouvoir renvoyer une candidature (0 = aucun) |

## Onglet Questions

Jusqu'à **25 questions**, dans l'ordre de ton choix :

| Type | Utilisation | Réglages |
|---|---|---|
| Texte court | nom, pseudo | caractères min / max (200 par défaut) |
| Paragraphe | histoire, motivation | caractères min / max (4000 par défaut) |
| Choix | une option parmi une liste | 2 options minimum, une par ligne |
| Nombre | âge, heures de jeu | valeur min / max |
| Case à cocher | « J'ai lu le règlement » | obligatoire = doit être cochée |

Chaque question peut avoir une **aide** affichée sous son titre, et être **obligatoire** ou non.

## Onglet Révision

- **Salon des candidatures** : là où arrivent les candidatures avec leurs boutons.
- **Rôles à mentionner** : notifiés à chaque nouvelle candidature.
- **Rôles qui peuvent accepter ou refuser** : en plus des membres qui ont Gérer le serveur.
- **Salon vocal d'entrevue** (optionnel) : active le bouton 🎙️ Entrevue, qui invite le joueur par MP à rejoindre ce salon.

## Onglet Rôles

Trois étapes, chacune avec ses rôles :

| Étape | Action |
|---|---|
| 📨 Formulaire envoyé | ajouter des rôles (ex. `@passport`) |
| ✅ Accepté | ajouter (ex. `@citoyen`) et retirer (ex. `@passport`, `@nouveau`) |
| ❌ Refusé | retirer (ex. `@passport`) |

> [!IMPORTANT]
> Le rôle de Kron doit être **au-dessus** de tous ces rôles. Sinon, Discord refuse le changement.

## Onglet Messages

Quatre messages privés envoyés au joueur : candidature reçue, acceptée, refusée, invitation à l'entrevue. Sans personnalisation, Kron envoie un texte par défaut. Coche **Personnaliser** pour utiliser l'éditeur complet.

| Variable | Remplacée par |
|---|---|
| `{user}` | mention du joueur |
| `{username}` | nom du joueur |
| `{server}` | nom du serveur |
| `{form}` | titre du formulaire |
| `{reason}` | raison du refus |
| `{channel}` | salon vocal d'entrevue |

## Réviser les candidatures

**Dans Discord** : clique sur ✅ ou ❌ sous la candidature. Le refus ouvre une fenêtre pour la raison (optionnelle, envoyée au joueur). L'embed passe au vert ou au rouge et indique qui a décidé. Si deux membres du staff cliquent en même temps, seul le premier compte.

**Dans le dashboard** : l'onglet **Candidatures** liste les candidatures en attente, acceptées et refusées, avec toutes les réponses.

## Ce que voit le joueur

- S'il n'est pas connecté, la page lui propose de se connecter avec Discord, puis le ramène au formulaire.
- S'il n'est pas membre du serveur, la page lui demande de rejoindre d'abord.
- S'il a déjà une candidature en attente, ou s'il est dans son délai après un refus, la page l'indique avec la date.
- Une vérification anti-robot protège l'envoi.

## Questions fréquentes

**Le joueur ne reçoit pas les MP.** Ses messages privés sont probablement fermés pour ce serveur. La candidature est quand même traitée.

**Les rôles ne changent pas.** Vérifie la position du rôle de Kron et lance `$debug`.

**Je veux plusieurs formulaires (staff, dev).** C'est possible avec le Pro. Chaque formulaire a son lien, ses questions, son salon et ses rôles.
