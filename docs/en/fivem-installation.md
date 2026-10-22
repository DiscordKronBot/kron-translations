---
title: Install the FiveM bridge
category: fivem
emoji: 🎮
summary: Link your FiveM server to Kron in 4 steps, without opening a port.
order: 1
popular: true
---

The **FiveM bridge** links your game server to Kron. Once installed, other modules show players' in-city info and your staff can act from Discord.

## Requirements

- **OneSync** enabled.
- **oxmysql**.
- **QBCore** or **Qbox** (ESX coming soon).
- Players must have **Discord open** when they connect: that is what links their Discord account to their FiveM license.

## 1. Generate a token

1. Dashboard, **🎮 FiveM bridge** module.
2. Click **🔑 Generate a token** and copy it right away: it won't be shown again.

> [!WARNING]
> The token gives Kron access to your server. Keep it secret like a password. **New token** disables the old one immediately.

## 2. Download the resource

Click **⬇️ Download the script** and unzip `kronbot_bridge.zip` into your resources folder, for example:

```
resources/[kron]/kronbot_bridge
```

## 3. Add the lines to server.cfg

After `oxmysql` and your framework:

```cfg
set kron_token "kron_xxxxxxxxxxxxxxxx"
ensure kronbot_bridge
```

## 4. Restart

On start, the console shows:

```
[kronbot_bridge] Connected to Kron (qbcore).
```

In the dashboard, the status turns **🟢 FiveM server connected**, with the number of players in the city.

## Resource configuration

The resource's `config.lua` lets you set:

| Setting | Default | Description |
|---|---|---|
| `Config.Locale` | `fr` | language of in-game messages (`fr` or `en`) |
| `Config.ReportCommand` | `report` | in-game report command name; only registered when reports are on in the dashboard (`false` = never) |
| `Config.ReportCooldown` | `15` | seconds between two reports from a player |
| `Config.UnstuckCoords` | Legion Square | where "Unstuck" sends the character |
| `Config.DefaultGarage` | `pillboxgarage` | garage used when the vehicle has none |
| `Config.Framework` | `auto` | detects Qbox or QBCore automatically |
| `Config.Debug` | `false` | prints requests in the console |

## Security

- The resource only makes **outgoing** HTTPS calls to kronbot.xyz: **no port to open**, nothing exposed.
- The token is stored hashed on our side.
- Kron only reads what your modules need, and you choose the fields shown (job, phone, cash, bank).

## Troubleshooting

| Console message | Fix |
|---|---|
| `No token` | add the `set kron_token` line to `server.cfg` |
| `Token refused by Kron` | generate a new token and replace the old one |
| `Framework "esx" not supported yet` | profiles and actions are not available yet; `/report` works |
| status 🟠 "Waiting for the server" | the server hasn't contacted Kron for over 90 seconds |
