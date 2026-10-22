---
title: Role management
category: modules
emoji: 🧑‍⚖️
summary: Your staff gives and removes roles with /role, without the Manage Roles permission.
order: 5
---

On an RP server, a **@Customs** officer must be able to give **@Citizen** to a player and remove **@Newcomer** and **@Passport-filled**. Giving them **Manage Roles** is risky: with it, they could also **delete or edit** those roles.

With this module, Kron changes the roles. Your staff needs no role permission at all.

## Create an action

In the dashboard, **Role management → New action** (or **RP example: customs**):

| Setting | Example |
|---|---|
| Name and emoji | 🛂 Approve passport |
| Who can use it | @Customs |
| Roles added | @Citizen |
| Roles removed | @Newcomer, @Passport-filled |

The preview sums it up: "@Customs can: + @Citizen − @Newcomer @Passport-filled". Up to 25 actions.

## Use it on Discord

1. Type `/role member:@player`.
2. Kron only shows the actions allowed to your role (members who manage the server see them all).
3. Click the action: the roles change at once, and the answer says what changed.

## Safety

- An action **cannot give a role with moderation rights** (Administrator, Manage Server, Manage Roles, Manage Channels, Kick, Ban, Timeout, Webhooks). Kron checks it again on every use.
- Nobody can target a bot, themselves, or a member who manages the server (unless they manage it too).
- The **Kron** role must be above the roles added or removed.
- **Tracking channel**: every action is noted there (who, to whom, which roles).

> [!TIP]
> To repair deleted or damaged roles, see [Role backup](/docs/sauvegarde-roles).
