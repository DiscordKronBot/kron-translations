---
title: Levels and economy
category: modules
emoji: ⭐
summary: XP for chatting, levels, role rewards, leaderboard and a server currency.
order: 15
popular: true
---

The **Levels and economy** module rewards active members: each message earns XP, XP raises levels, and levels can give roles.

## Earning XP

- Each message gives **15 to 25 XP** (adjustable), once per **cooldown** (60 seconds by default) to avoid spam.
- You can exclude **channels** (or whole categories) and **roles**.
- The curve follows the usual standard: level 1 needs 100 XP, each next level a bit more.

## Level up

Choose where to announce a new level: in the message's channel, in a **dedicated channel** (handy to keep other channels clean), by DM, or nowhere.

The message accepts the `{user}` (mention), `{username}` and `{level}` variables.

## Role rewards

Link a role to a level: it is given automatically when the member reaches it. By default previous roles are kept; turn off **Keep previous roles** to keep only the highest.

> [!NOTE]
> The Free plan allows 5 rewards. Pro makes them unlimited.

## Economy

Turn on the economy to give a currency (name and emoji of your choice):

- coins with every message that gives XP;
- a daily reward with `/daily`;
- gifts between members with `/pay`.

## Work, rob, bank and shop

- `/work`: random pay (between the minimum and maximum), once per cooldown.
- `/rob @member`: a chance to steal part of their wallet; if caught, you pay a fine. Can be turned off.
- `/bank`: deposit your money to keep it safe from robbers, withdraw it or check your balance.
- `/shop`: buy **roles** and **items** from the menu; `/inventory` shows what you own.

Everything is set in the dashboard: pay, cooldowns, chances and the shop items.

## Commands

| Command | Effect |
|---|---|
| `/rank [member]` | level, XP, rank and progress bar |
| `/top [xp or coins]` | the top 10 |
| `/balance [member]` | coin balance |
| `/daily` | daily reward (every 20 h) |
| `/pay member amount` | give coins |
| `/xp give, remove, reset` | staff (Manage Server): adjust a member's XP |

The full leaderboard is also in the dashboard, **Leaderboard** tab, with a button to reset a member.
