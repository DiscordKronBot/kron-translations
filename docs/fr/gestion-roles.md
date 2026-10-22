---
title: Gestion des rôles
category: modules
emoji: 🧑‍⚖️
summary: Ton staff donne et retire des rôles avec /role, sans la permission Gérer les rôles.
order: 5
---

Sur un serveur RP, un **@Douanier** doit pouvoir donner **@Citoyen** à un joueur et lui retirer **@Nouveau** et **@Passeport-rempli**. Lui donner la permission **Gérer les rôles** est risqué : avec elle, il pourrait aussi **supprimer ou modifier** ces rôles.

Avec ce module, c'est Kron qui change les rôles. Ton staff n'a besoin d'aucune permission de rôles.

## Créer une action

Dans le dashboard, **Gestion des rôles → Nouvelle action** (ou **Exemple RP : douane**) :

| Réglage | Exemple |
|---|---|
| Nom et emoji | 🛂 Valider le passeport |
| Qui peut l'utiliser | @Douanier |
| Rôles ajoutés | @Citoyen |
| Rôles retirés | @Nouveau, @Passeport-rempli |

L'aperçu résume : « @Douanier peut : + @Citoyen − @Nouveau @Passeport-rempli ». Jusqu'à 25 actions.

## L'utiliser sur Discord

1. Tape `/role membre:@joueur`.
2. Kron montre seulement les actions permises à ton rôle (les membres qui gèrent le serveur les voient toutes).
3. Clique l'action : les rôles changent d'un coup, et la réponse dit ce qui a changé.

## Sécurité

- Une action ne peut **pas donner un rôle avec des droits de modération** (Administrateur, Gérer le serveur, Gérer les rôles, Gérer les salons, Expulser, Bannir, Exclure, Webhooks). Kron le revérifie à chaque utilisation.
- On ne peut pas viser un bot, soi-même, ni un membre qui gère le serveur (sauf si on gère soi-même le serveur).
- Le rôle **Kron** doit être au-dessus des rôles ajoutés ou retirés.
- **Salon de suivi** : chaque action y est notée (qui, à qui, quels rôles).

> [!TIP]
> Pour réparer des rôles supprimés ou abîmés, vois [Sauvegarde des rôles](/docs/sauvegarde-roles).
