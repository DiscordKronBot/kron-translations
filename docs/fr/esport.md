---
title: Équipe esport
category: modules
emoji: 🏆
summary: Gère tes équipes (joueurs, capitaines, staff, identité) et publie un embed professionnel qui se met à jour tout seul.
order: 26
---

Le module **Équipe esport** (Pro) sert à gérer une ou plusieurs équipes compétitives depuis le tableau de bord, puis à publier chaque équipe dans un salon Discord. Le message publié est **mis à jour automatiquement** dès qu'un joueur, un capitaine ou une information change : Kron ne republie jamais un nouveau message.

## Installation

1. Active le module **Équipe esport** dans le tableau de bord (il demande un plan **Pro**).
2. Clique sur **Nouvelle équipe** et donne-lui un nom.
3. Onglet **Identité** : organisation, tag, jeu, région, division, saison, statut, couleur, logo, bannière, description, site, invitation Discord, réseaux sociaux et informations facultatives.
4. Onglet **Effectif** : ajoute tes joueurs, puis choisis le **capitaine** et le **vice-capitaine**.
5. Onglet **Staff** : coach, manager, analyste…
6. Onglet **Publication** : choisis le salon et clique sur **Publier**.

> [!TIP]
> Les images (logo, bannière, photos) sont des **liens** : héberge-les où tu veux (Discord, Imgur, ton site) et colle l'URL.

## Les joueurs

Chaque joueur a un pseudo compétitif, un nom affiché, un rôle (Top, Mid, IGL…), un numéro, un pays, une biographie, des liens vers ses profils, un ID Discord facultatif et un statut :

| Statut | Dans l'embed |
|---|---|
| 🟢 Titulaire | affiché normalement |
| 🟡 Remplaçant | affiché avec sa pastille jaune |
| ⚪ Inactif | caché, sauf si tu actives « Inclure les inactifs » |

La **photo** d'un joueur devient un lien dans la carte (icône 🖼️ en grille, nom cliquable en liste) : un embed Discord n'affiche qu'une seule image, gardée pour le logo et la bannière.

L'**ordre d'affichage** se change avec les flèches ↑ ↓. Le capitaine (🎖️) et le vice-capitaine (🥈) doivent être des **joueurs de l'équipe** : si tu les retires de l'effectif, le badge se libère tout seul.

## L'embed publié

Deux modes, dans l'onglet **Embed** :

- **Automatique** : Kron construit la carte avec tes données. Tu choisis le titre, la description, le pied de page, la couleur, la miniature, l'image, la présentation de l'effectif, les sections affichées et les détails des joueurs (numéros, rôles, pays, mention Discord, biographie).
- **Personnalisé** : tu écris le message au complet dans l'éditeur d'embeds, avec des variables remplacées à la publication : `{team.name}`, `{team.game}`, `{team.captain}`, `{roster}`, `{staff}`…

Quatre présentations de l'effectif : **Organigramme** (par défaut), **Grille**, **Liste** et **Compacte**.

L'organigramme utilise des champs *inline* : Discord les aligne sur **trois colonnes**, alors les noms, les rôles et les numéros restent droits les uns sous les autres.

| Rangée | Contenu |
|---|---|
| 1 | 🎖️ Capitaine · 🥈 Vice-capitaine · 👥 Effectif |
| 2 | 👥 **Titulaires** — jusqu'à 9 |
| 3 | 🟡 **Remplaçants** — jusqu'à 3 |
| 4 | 🛡️ **Staff** — jusqu'à 6 |

Chaque section commence sur une nouvelle rangée et la dernière rangée est complétée avec des cases vides : les colonnes ne se décalent jamais. Au-delà de ces nombres, un « +N autres » s'affiche dans le titre de la section (Discord limite un embed à 25 champs).

L'**aperçu** montre exactement ce que Discord affichera. Les réseaux sociaux deviennent des boutons (5 au maximum).

## Publication automatique

- Kron retient le **salon** et le **message** de chaque équipe, et modifie ce message à chaque changement.
- Une équipe peut être publiée dans **5 salons** au maximum ; chaque équipe ne touche qu'à ses propres messages.
- Si tu coupes **Mise à jour automatique** dans les réglages, les messages restent tels quels jusqu'à ce que tu cliques sur **Tout actualiser** (ou `/esport actualiser`).
- Si Kron perd l'accès au salon, l'erreur s'affiche dans le panneau et les données restent intactes : dès que la permission revient, Kron réessaie tout seul.
- Si le message est **supprimé** dans Discord, le panneau propose **Republier**.

## Commandes Discord

Le tableau de bord reste l'outil principal ; les commandes servent aux actions rapides.

| Commande | Ce qu'elle fait |
|---|---|
| `/esport equipes` | voir les équipes et ouvrir le panneau d'actions |
| `/esport publier` | publier une équipe dans un salon |
| `/esport actualiser` | actualiser toutes les publications |
| `/esport joueur` | ajouter, modifier ou retirer un joueur |
| `/esport capitaine` | changer le capitaine |
| `/esport vice-capitaine` | changer le vice-capitaine |
| `/esport configuration` | voir la configuration d'une équipe |

Les commandes de gestion demandent la permission **Gérer le serveur**, ou un des **rôles gestionnaires** choisis dans les réglages du module. `/esport equipes` peut rester ouvert à tout le monde (réglage **Commande publique**).

## Problèmes courants

- **« Kron n'a pas accès à ce salon »** : donne-lui *Voir le salon*, *Envoyer des messages* et *Intégrer des liens* dans ce salon.
- **Le message ne bouge plus** : vérifie que le module est actif, que le serveur a toujours son plan Pro, et que **Mise à jour automatique** est allumée.
- **« Le message a été supprimé »** : clique sur **Republier** dans l'onglet Publication.
- **Le plan Pro a expiré** : rien n'est effacé. Le module se met en pause et les équipes reviennent telles quelles quand le plan est de retour.

## Limites

- 12 équipes par serveur, 40 membres par équipe.
- Organigramme : 9 titulaires, 3 remplaçants et 6 membres du staff affichés ; les autres présentations vont jusqu'à 24 personnes. Le reste est résumé en une ligne.
- Les liens doivent commencer par `http://` ou `https://`.
