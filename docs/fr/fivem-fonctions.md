---
title: Fonctions FiveM
category: fivem
emoji: 🕹️
summary: Profils des personnages dans les tickets, Débloquer, Rapatrier un véhicule, /report en ville, salons de jobs, tableau des joueurs et fiches RP.
order: 2
---

Chaque fonction a sa switch dans le module **🎮 Pont FiveM** ([offre Pro](/pro)). Elles sont toutes **désactivées par défaut** : active seulement ce que tu veux.

## Profil FiveM dans les tickets

Quand un joueur ouvre un ticket, Kron affiche sous le message d'accueil :

- son statut (🟢 en ville ou ⚫ hors ligne) et sa licence (abrégée) ;
- son personnage : nom, emploi et grade, téléphone, argent liquide, banque, citizenid ;
- s'il a **plusieurs personnages**, un menu **Voir un autre personnage…** permet de passer de l'un à l'autre.

Les champs affichés se choisissent dans **Infos affichées**. Montre seulement ce dont ton staff a besoin.

## Actions du staff

Sous le profil, deux boutons réservés au staff :

- **📍 Débloquer** : si le joueur est en ville, il est téléporté au point sécuritaire. S'il est hors ligne, sa position enregistrée est remplacée : il y apparaîtra à sa prochaine connexion.
- **🚗 Rapatrier un véhicule** : Kron liste les véhicules du personnage (sorti, au garage, fourrière). Choisis-en un : il est retiré du monde s'il y est encore, puis rangé au garage.

Le joueur est prévenu en jeu dans les deux cas.

**Qui est staff ?** Les rôles choisis dans **Staff FiveM**, ainsi que les membres qui ont la permission Exclure des membres ou Gérer le serveur.

## Commande /fivem

| Commande | Effet |
|---|---|
| `/fivem profil membre:@Joueur` | profil du joueur, avec les boutons d'action |
| `/fivem debloquer membre:@Joueur` | ouvre le profil pour choisir le personnage à débloquer |
| `/fivem garage membre:@Joueur` | ouvre le profil pour choisir le véhicule à rapatrier |

Les réponses ne sont visibles que par toi.

## /report en ville

1. Active **/report en ville**. Si ton serveur a déjà son propre `/report`, laisse-le désactivé : la ressource n'ajoute alors pas de commande.
2. Dans l'aperçu, ajuste le salon (privé `🚨┆reports-ville`) et qui peut le voir, puis clique sur **✨ Créer le salon pour moi**, ou choisis un salon. Ajoute les rôles à mentionner.
3. En jeu, le joueur tape `/report Je suis coincé sous la map`.
4. Kron crée un **fil** dans le salon, avec le message, le nom du joueur, son ID en jeu et ses boutons **👁️ Profil** et **🔒 Fermer**.
5. **Le staff écrit dans le fil** : chaque message est envoyé au joueur dans le chat en jeu (Kron réagit avec 📨).
6. Tant que le report est ouvert, les nouveaux `/report` du joueur s'ajoutent au même fil : c'est une vraie conversation.
7. **🔒 Fermer** archive le fil et prévient le joueur.

> [!TIP]
> Un délai (15 secondes par défaut) empêche un joueur de spammer `/report`.

## Salons de jobs et de gangs

Kron lit la liste des jobs et des gangs de ton serveur (QBCore ou Qbox) et crée une catégorie **JOBS** avec un salon privé par job : un « ticket permanent » entre le staff et chaque métier.

1. Active **Salons de jobs** dans la page FiveM du dashboard (ressource 1.2.0 ou plus, serveur en ligne).
2. Clique sur **Charger les jobs du serveur**, coche ceux qui t'intéressent (police, EMS, mécano, gangs…).
3. Pour chaque job, choisis le **rôle Discord** des membres de ce job. Sans rôle, seul le staff voit le salon.
4. Ajuste les noms et les emojis dans l'aperçu, puis crée les salons.

Chaque salon est visible par les rôles du staff FiveM, par Kron et par le rôle du job, et caché pour tout le monde.

## Tableau des joueurs en direct

Un message que Kron garde à jour dans un salon : état du serveur, joueurs en ligne et places, jobs en service (ressource 1.4.0 ou plus).

1. Active **Tableau des joueurs**.
2. Clique sur **✨ Créer le salon pour moi** (`📊┆ville-en-direct`, tout le monde peut le lire, seul Kron y écrit) ou choisis un salon.
3. Optionnel : un titre, et un lien **Rejoindre** (`https://cfx.re/join/...`) qui ajoute un bouton sous le tableau.

Kron regarde le serveur chaque minute et modifie le message seulement quand quelque chose a changé. S'il est supprimé, Kron en publie un nouveau.

## Fiches de personnages RP

Une fiche par personnage : nom, âge, métier, histoire et image, affichée dans une carte.

- **Créer ou modifier** (staff) : dans le profil FiveM d'un membre (`/fivem profil` ou en-tête de ticket), clique sur **📜 Fiche RP**, puis remplis le formulaire. Une fiche existante a un bouton **✏️ Modifier**.
- **Lire** (tout le monde) : `/fiche membre:@Joueur` (ou `/fiche` pour les tiennes). Un menu passe d'un personnage à l'autre.
- **Dashboard** : la section **Fiches de personnages** liste toutes les fiches pour les modifier ou les supprimer.

L'image doit être un lien `https://`.

## Tags FiveM

Quand le module est actif, tous les éditeurs de messages (bienvenue, embeds, commandes…) offrent ces tags :

| Tag | Valeur |
|---|---|
| `{fivem.server}` | nom du serveur FiveM |
| `{fivem.status}` | 🟢 ou 🔴 |
| `{fivem.players}` / `{fivem.maxPlayers}` | joueurs en ligne / places |
| `{fivem.police}` / `{fivem.ems}` | policiers / ambulanciers en service (ressource 1.4.0) |
| `{fivem.jobs}` | jobs les plus présents en service, ex. `Police 3 · EMS 1` |

## Questions fréquentes

**« Aucun compte FiveM lié ».** Le joueur ne s'est jamais connecté avec Discord ouvert. Demande-lui de relancer Discord puis FiveM.

**« Le serveur FiveM n'a pas répondu à temps ».** Le serveur est surchargé ou vient de redémarrer. Réessaie dans quelques secondes.
