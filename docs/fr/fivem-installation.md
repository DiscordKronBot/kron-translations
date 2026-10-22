---
title: Installer le pont FiveM
category: fivem
emoji: 🎮
summary: Relier ton serveur FiveM à Kron en 4 étapes, sans ouvrir de port.
order: 1
popular: true
---

Le **pont FiveM** relie ton serveur de jeu à Kron. Une fois installé, les autres modules affichent les infos des joueurs en ville et ton staff peut agir depuis Discord.

## Prérequis

- **OneSync** activé.
- **oxmysql**.
- **QBCore** ou **Qbox** (ESX arrive bientôt).
- Les joueurs doivent avoir **Discord ouvert** quand ils se connectent : c'est ce qui relie leur compte Discord à leur licence FiveM.

## 1. Générer un token

1. Dashboard, module **🎮 Pont FiveM**.
2. Clique sur **🔑 Générer un token** et copie-le tout de suite : il ne sera plus affiché.

> [!WARNING]
> Le token donne accès à ton serveur depuis Kron. Garde-le secret comme un mot de passe. **Nouveau token** désactive immédiatement l'ancien.

## 2. Télécharger la ressource

Clique sur **⬇️ Télécharger le script** et décompresse `kronbot_bridge.zip` dans ton dossier de ressources, par exemple :

```
resources/[kron]/kronbot_bridge
```

## 3. Ajouter les lignes dans server.cfg

Après `oxmysql` et ton framework :

```cfg
set kron_token "kron_xxxxxxxxxxxxxxxx"
ensure kronbot_bridge
```

## 4. Redémarrer

Au démarrage, la console affiche :

```
[kronbot_bridge] Connecté à Kron (qbcore).
```

Dans le dashboard, le statut passe à **🟢 Serveur FiveM connecté**, avec le nombre de joueurs en ville.

## Configuration de la ressource

Le fichier `config.lua` de la ressource permet de régler :

| Réglage | Par défaut | Description |
|---|---|---|
| `Config.Locale` | `fr` | langue des messages vus en jeu (`fr` ou `en`) |
| `Config.ReportCommand` | `report` | nom de la commande de report en jeu ; ajoutée seulement si les reports sont activés dans le dashboard (`false` = jamais) |
| `Config.ReportCooldown` | `15` | secondes entre deux reports d'un joueur |
| `Config.UnstuckCoords` | Legion Square | point où « Débloquer » envoie le personnage |
| `Config.DefaultGarage` | `pillboxgarage` | garage utilisé si le véhicule n'en a pas |
| `Config.Framework` | `auto` | détection automatique de Qbox ou QBCore |
| `Config.Debug` | `false` | affiche les requêtes dans la console |

## Sécurité

- La ressource fait seulement des appels **sortants** vers kronbot.xyz en HTTPS : **aucun port à ouvrir**, rien n'est exposé.
- Le token est stocké chiffré (haché) de notre côté.
- Kron ne lit que ce dont tes modules ont besoin, et tu choisis les champs affichés (emploi, téléphone, argent, banque).

## Dépannage

| Message de la console | Solution |
|---|---|
| `Aucun token` | ajoute la ligne `set kron_token` dans `server.cfg` |
| `Token refusé par Kron` | génère un nouveau token et remplace l'ancien |
| `Framework "esx" not supported yet` | les profils et actions ne sont pas encore disponibles ; `/report` fonctionne |
| statut 🟠 « En attente du serveur » | le serveur n'a pas contacté Kron depuis plus de 90 secondes |
