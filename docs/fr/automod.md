---
title: AutoMod
category: modules
emoji: 🤖
summary: Bloquer les mots interdits, les regex, le spam, les mentions de masse et les pseudos douteux avec l'AutoMod de Discord.
order: 13
---

Le module **AutoMod** configure l'AutoMod intégré à Discord depuis le dashboard. Les règles sont appliquées par Discord lui-même : un message bloqué n'est jamais publié, et tout fonctionne même si Kron est hors ligne.

## Mise en place

1. Active le module **AutoMod** dans le dashboard.
2. Choisis une **règle prête à l'emploi** (invitations Discord, liens, insultes, spam, mentions de masse, pseudos) ou crée une règle vide.
3. Ajuste les mots, les actions et les exemptions, puis clique sur **Enregistrer** en bas.

> [!IMPORTANT]
> Kron a besoin de la permission **Gérer le serveur** pour créer et modifier les règles. C'est une exigence de Discord pour toute gestion d'AutoMod.

## Types de règles

| Type | Ce qu'il bloque | Maximum |
|---|---|---|
| Mots-clés | Mots (avec `*`) et regex | 6 règles |
| Listes de Discord | Grossièretés, contenu sexuel, insultes | 1 |
| Spam | Messages jugés suspects par Discord | 1 |
| Mentions de masse | Trop de mentions dans un message | 1 |
| Pseudos | Pseudos et profils des membres | 1 |

Les maximums sont ceux de Discord. Les règles créées directement dans Discord apparaissent aussi dans le dashboard et peuvent y être modifiées.

## Mots et regex

- Un mot par ligne. `*` veut dire « n'importe quoi » : `*chat*` attrape aussi « achats », `chat` seul attrape seulement le mot entier.
- Les regex suivent la syntaxe Rust. Exemple pour les invitations : `(discord\.gg|discord\.com/invite)/\w+`
- Les **exceptions** ne déclenchent jamais la règle, même si elles contiennent un mot interdit.

## Actions

- **Bloquer le message** : il n'est pas publié. Tu peux montrer un court message à l'auteur.
- **Alerter le staff** : Discord publie une alerte avec le message dans le salon choisi.
- **Exclure temporairement** l'auteur (mots-clés et mentions seulement), de 1 minute à 1 semaine.
- Les règles de **pseudos** empêchent le membre d'écrire tant que son pseudo enfreint la règle.

## Exemptions

Chaque règle peut ignorer jusqu'à 20 rôles (le staff, en général) et 50 salons (par exemple un salon de partage de liens).

> [!TIP]
> Désactiver le module met en pause les règles créées par Kron. Le réactiver remet en marche exactement les mêmes.
