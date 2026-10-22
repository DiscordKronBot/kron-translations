---
title: Logs
category: modules
emoji: 📜
summary: Suivre les messages, arrivées, rôles, sanctions, vocaux et changements du serveur, chacun dans son salon.
order: 4
popular: true
---

Le module **Logs** enregistre ce qui se passe sur ton serveur dans des salons dédiés, comme sur les gros bots de modération.

## Mise en place rapide

1. Ouvre **Logs** et clique sur **✨ Créer les salons pour moi**.
2. Choisis les **rôles du staff** qui pourront lire les logs. Dans l'aperçu **Sera créé**, clique sur une ligne pour la renommer, changer son emoji ou choisir d'autres rôles pour ce salon.
3. Clique sur **Tout créer** : Kron crée une catégorie privée `📜┆Logs` avec un salon par type : `💬┆log-message`, `🚪┆log-join-part`, `👤┆log-members`, `🏷️┆log-roles`, `🛡️┆log-moderation`, `🔊┆log-voice`, `🏠┆log-server`.
4. Active le module avec la switch à côté de son titre.

Tu peux aussi choisir tes propres salons, type par type.

## Ce qui est enregistré

| Type | Événements |
|---|---|
| 💬 log-message | messages supprimés (avec le contenu), modifiés (avant / après), suppressions en masse |
| 🚪 log-join-part | arrivées (âge du compte, nombre de membres) et départs |
| 👤 log-members | changements de pseudo |
| 🏷️ log-roles | rôles ajoutés ou retirés aux membres, rôles créés, modifiés (nom, couleur, permissions…) et supprimés, avec l'auteur |
| 🛡️ log-moderation | bannissements, débannissements, expulsions, exclusions temporaires, avec l'auteur et la raison |
| 🔊 log-voice | arrivées, départs et changements de salon vocal |
| 🏠 log-server | salons créés, supprimés, renommés |

Chaque type a sa switch : tu peux en désactiver sans perdre le salon choisi.

## Filtres

- **Ignorer les messages des bots** (activé par défaut).
- **Salons ignorés** : rien n'est enregistré pour les messages de ces salons.
- **Rôles ignorés** : les actions des membres qui ont ces rôles ne sont pas enregistrées.

## Bon à savoir

> [!NOTE]
> Discord n'envoie pas le contenu d'un message supprimé. Kron garde les messages récents en mémoire **1 heure** pour pouvoir l'afficher. Au-delà, le log indique « Contenu inconnu ».

- L'auteur d'une sanction vient du journal d'audit : Kron a besoin de la permission **Voir les logs d'audit**.
- Garde les salons de logs privés : la catégorie créée automatiquement est déjà invisible pour @everyone.
