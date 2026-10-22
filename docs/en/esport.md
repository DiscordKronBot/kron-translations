---
title: Esport team
category: modules
emoji: 🏆
summary: Manage your teams (players, captains, staff, identity) and publish a professional embed that updates itself.
order: 26
---

The **Esport team** module (Pro) manages one or several competitive teams from the dashboard, then publishes each team in a Discord channel. The published message is **updated automatically** whenever a player, a captain or a piece of information changes: Kron never posts a new message for an update.

## Setup

1. Turn the **Esport team** module on in the dashboard (it needs a **Pro** plan).
2. Click **New team** and give it a name.
3. **Identity** tab: organisation, tag, game, region, division, season, status, colour, logo, banner, description, website, Discord invite, socials and optional information.
4. **Roster** tab: add your players, then pick the **captain** and the **vice-captain**.
5. **Staff** tab: coach, manager, analyst…
6. **Publication** tab: pick the channel and click **Publish**.

> [!TIP]
> Images (logo, banner, pictures) are **links**: host them where you want (Discord, Imgur, your site) and paste the URL.

## Players

Every player has a competitive nickname, a display name, a role (Top, Mid, IGL…), a number, a country, a bio, profile links, an optional Discord ID and a status:

| Status | In the embed |
|---|---|
| 🟢 Starter | shown normally |
| 🟡 Substitute | shown with its yellow dot |
| ⚪ Inactive | hidden, unless you turn on "Include inactive members" |

A player's **picture** becomes a link in the card (a 🖼️ icon in grid layout, a clickable name in list layout): a Discord embed only shows one image, kept for the logo and the banner.

The **display order** is changed with the ↑ ↓ arrows. The captain (🎖️) and the vice-captain (🥈) must be **players of the team**: removing them from the roster frees the badge on its own.

## The published embed

Two modes, in the **Embed** tab:

- **Automatic**: Kron builds the card from your data. You choose the title, description, footer, colour, thumbnail, image, roster layout, the sections shown and the player details (numbers, roles, country, Discord mention, bio).
- **Custom**: you write the whole message in the embed editor, with variables replaced when it is published: `{team.name}`, `{team.game}`, `{team.captain}`, `{roster}`, `{staff}`…

Four roster layouts: **Org chart** (the default), **Grid**, **List** and **Compact**.

The org chart uses *inline* fields: Discord aligns them in **three columns**, so names, roles and numbers stay lined up.

| Row | Content |
|---|---|
| 1 | 🎖️ Captain · 🥈 Vice-captain · 👥 Roster |
| 2 | 👥 **Starters** — up to 9 |
| 3 | 🟡 **Substitutes** — up to 3 |
| 4 | 🛡️ **Staff** — up to 6 |

Every section starts on a new row and the last row is padded with empty cells: the columns never drift. Past those numbers, a "+N more" shows in the section title (Discord caps an embed at 25 fields).

The **preview** shows exactly what Discord will display. Socials become link buttons (5 at most).

## Automatic publishing

- Kron remembers the **channel** and the **message** of each team, and edits that message on every change.
- A team can be published in **5 channels** at most; each team only ever touches its own messages.
- With **Automatic update** off in the settings, messages stay as they are until you click **Refresh all** (or run `/esport refresh`).
- If Kron loses access to the channel, the error shows in the panel and the data stays untouched: as soon as the permission is back, Kron retries by itself.
- If the message is **deleted** in Discord, the panel offers **Publish again**.

## Discord commands

The dashboard stays the main tool; commands are there for quick actions.

| Command | What it does |
|---|---|
| `/esport teams` | see the teams and open the action panel |
| `/esport publish` | publish a team in a channel |
| `/esport refresh` | update every publication |
| `/esport player` | add, edit or remove a player |
| `/esport captain` | change the captain |
| `/esport vice-captain` | change the vice-captain |
| `/esport settings` | see a team's settings |

Management commands need the **Manage Server** permission, or one of the **manager roles** chosen in the module settings. `/esport teams` can stay open to everyone (**Public command** setting).

## Common problems

- **"Kron cannot post in that channel"**: give it *View Channel*, *Send Messages* and *Embed Links* in that channel.
- **The message never changes**: check that the module is on, that the server still has its Pro plan, and that **Automatic update** is enabled.
- **"The message was deleted"**: click **Publish again** in the Publication tab.
- **The Pro plan expired**: nothing is deleted. The module pauses and the teams come back exactly as they were once the plan is active again.

## Limits

- 12 teams per server, 40 members per team.
- Org chart: 9 starters, 3 substitutes and 6 staff members listed; the other layouts go up to 24 people. The rest is summed up in one line.
- Links must start with `http://` or `https://`.
