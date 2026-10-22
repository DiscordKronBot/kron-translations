---
title: Anti-raid
category: modules
emoji: 🚧
summary: Spot waves of joins, pause invites and watch brand-new accounts.
order: 14
---

The **Anti-raid** module spots raids (many accounts joining at once) and helps staff stop them in one click.

## Detection

You choose the threshold: for example **10 joins in 10 seconds**. When it is reached, Kron goes into **raid mode**:

- it posts an alert in the chosen channel, mentioning the staff roles;
- it applies the chosen action to every join: **alert only**, **kick** or **ban** (the members who triggered the raid included);
- it can **pause invites** with Discord's security actions.

Raid mode ends by itself after a few minutes without a new join, or with the **End raid** button. Invites are then resumed.

> [!TIP]
> The **Ban the joins** button bans every account that joined during the raid at once (up to 200). The list is kept in memory: after Kron restarts, the button no longer works.

## New accounts

Outside raids, Kron can check the account age of every new member. If the account was created less than X days ago:

- **Alert only**: a message in the alerts channel;
- **Kick**;
- **Quarantine role**: a role that only sees, for example, a verification channel.

## Permissions

Kick, Ban, Manage Roles (quarantine) and Manage Server (invite pause). Kron's role must be above the quarantine role.
