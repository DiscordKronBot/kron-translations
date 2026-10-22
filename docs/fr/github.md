---
title: GitHub
category: modules
emoji: 🐙
summary: Les pushes de tes dépôts publiés en embeds propres, une section par commit.
order: 19
---

Le module **GitHub** (Pro) publie chaque push de tes dépôts dans un salon : un message par push, une section par commit avec son lien, ses détails et son auteur. C'est le même rendu que le salon #github de Kron.

## Suivre un dépôt

1. Active le module **GitHub**.
2. Entre le dépôt (`propriétaire/nom`), une **branche** si tu veux filtrer (vide = toutes), et le salon.
3. Clique sur **Créer le flux**. Kron affiche une **URL** et un **secret**.
4. Dans GitHub : ton dépôt → **Settings → Webhooks → Add webhook**.
   - **Payload URL** : l'URL donnée par Kron.
   - **Content type** : `application/json`.
   - **Secret** : le secret donné par Kron.
   - **Which events** : *Just the push event*.
5. Enregistre. GitHub envoie un ping, puis chaque push arrive dans ton salon.

> [!WARNING]
> Le secret n'est affiché qu'une fois. Perdu ? Clique sur **Nouveau secret** et mets-le à jour dans GitHub.

## Bon à savoir

- Jusqu'à **10 dépôts** par serveur.
- Les pushes d'un autre dépôt ou d'une autre branche que celle choisie sont ignorés.
- Chaque requête est vérifiée avec la signature de GitHub : personne d'autre ne peut publier dans ton salon.
