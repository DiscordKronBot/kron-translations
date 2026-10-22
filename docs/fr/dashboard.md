---
title: Utiliser le dashboard
category: start
emoji: 🖥️
summary: Navigation, enregistrement, brouillons et éditeur de messages : tout ce qui est commun aux modules.
order: 3
---

## Navigation

- **Tes serveurs** : la liste des serveurs que tu gères. Survole un serveur sans Kron pour voir le bouton **Inviter**.
- **Barre latérale** : le sélecteur de serveur en haut, puis **Vue d'ensemble**, **Paramètres** et tous les modules, classés par catégorie.
- **Vue d'ensemble** : le nombre de modules actifs, de membres, la langue et l'offre. Tu peux y activer ou désactiver plusieurs modules d'un coup.

## La page Général

**Général**, en haut du menu, regroupe les réglages de tout le serveur :

- **langue** de Kron et **signature** (Pro) ;
- **style des noms de salons** : séparateur (`┆`, `・`, `│`…) et police. Chaque salon que Kron crée le suit : installations, boutons **Créer**, packs du constructeur de salons. « Embellir les noms » s'en sert aussi ;
- **commandes texte** : le préfixe par défaut des nouveaux tags (`!`, `?`, `.`…) et celui de chaque tag existant ;
- **catégorie des logs** : là où tous les modules mettent leurs salons de logs ;
- **visite du dashboard** : relance la petite visite guidée du premier passage.

## Créer un salon depuis un module

À côté des choix de salon (vérification, bienvenue, logs de modération, tickets…), le bouton **+ Créer** fait le salon pour toi, dans le style de ton serveur. Tu peux changer l'emoji et le nom avant ; l'aperçu montre le nom final.

- Un salon normal se place **tout en haut du serveur**.
- Un salon de logs va dans **la catégorie des logs** du serveur et garde ses accès (staff seulement). S'il n'y en a pas encore, Kron demande quels rôles peuvent le voir.
- Kron ne supprime jamais un salon pour en créer un autre.

## Activer et désactiver un module

La switch à côté du titre d'un module s'enregistre tout de suite : **verte** quand le module est activé, **rouge** quand il est désactivé. Un crochet vert apparaît une fois l'enregistrement fait.

## Enregistrer tes modifications

Chaque autre changement (un texte, un rôle, un salon) est d'abord un **brouillon**. Dès que tu modifies quelque chose, une barre apparaît en bas de l'écran :

- **Enregistrer** applique tous les changements de la page.
- **Annuler** revient à la dernière version enregistrée.

Si tu quittes la page (lien, autre serveur, autre onglet du module, bouton retour d'un éditeur) avec des changements non enregistrés, Kron te demande quoi faire : **Enregistrer et continuer**, **Quitter sans enregistrer** ou **Rester**. Si tu fermes l'onglet ou le navigateur, ton navigateur affiche aussi un avertissement.

> [!NOTE]
> Le bouton Enregistrer est grisé tant qu'un champ obligatoire est vide ou invalide (par exemple un message vide ou une URL incorrecte).

## Les aperçus « Sera créé »

Quand un module crée des salons pour toi (installation rapide des tickets, logs, FiveM), il montre d'abord ce qui **sera créé**. Clique sur une ligne pour changer son emoji, son nom ou, pour un salon privé, les rôles qui peuvent le voir, puis **Enregistrer** ou **Annuler** cette ligne.

## L'éditeur de messages

Partout où Kron envoie un message (embeds, tickets, whitelist, bienvenue, anniversaires, commandes personnalisées), tu utilises le même éditeur, avec un **aperçu Discord en direct** :

- **Message** : le texte au-dessus des embeds (2000 caractères).
- **Jusqu'à 10 embeds**, chacun avec : auteur (nom, lien, icône), titre et lien, description (4096 caractères), couleur, jusqu'à 25 champs (en ligne ou non), image, miniature, pied de page avec icône, et heure d'envoi.
- **Jusqu'à 5 boutons-liens** sous le message.
- **Compteurs** de caractères et alerte si le total dépasse la limite de 6000 caractères de Discord.
- **Importer / copier le JSON**, compatible Discord et Discohook.

Le texte accepte la mise en forme Discord : `**gras**`, `*italique*`, `__souligné__`, `~~barré~~`, `` `code` ``, `> citation`, `# titres`, listes `- `, liens `[texte](https://…)` et spoilers `||secret||`.

### Les variables

Certains modules proposent des variables entre accolades, remplacées au moment de l'envoi. Clique sur une variable dans l'éditeur pour la copier. Exemples :

| Variable | Remplacée par |
|---|---|
| `{user}` | la mention du membre |
| `{username}` | son nom d'utilisateur |
| `{server}` | le nom du serveur |
| `{memberCount}` | le nombre de membres |
| `{user.avatar}` | l'URL de l'avatar (utilisable comme image) |

Chaque article de module liste ses propres variables.

## Les limites du plan gratuit

Le plan gratuit limite certains éléments (par exemple 5 embeds sauvegardés ou 1 formulaire). Le compteur apparaît à côté du bouton de création. Voir [Premium](/docs/premium) et [les offres](/pro).
