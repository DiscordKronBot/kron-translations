---
title: Role backup
category: modules
emoji: 🛟
summary: Snapshots of roles, their permissions and who has them; repair a damaged server.
order: 6
---

A staff member deleted roles, changed their permissions or removed roles from everyone? **Role backup** puts the server back as it was.

## What is backed up

Every hour, Kron notes:

- every role: name, colour, shown separately, mentionable, **permissions**, place in the list;
- **who has which role**;
- the **roles' permissions in every channel**.

Nothing is stored when nothing changed. Kron keeps the last 60 automatic backups and the last 20 manual ones. **Back up now** makes one right away.

## Owner only

Only the **server owner** sees this page, turns the module on or off and starts a restore. They can let **Administrators** use it too. A member with "Manage Server" cannot do anything there: whoever caused the damage cannot erase the fix.

## Repair

1. Pick a backup from **before** the problem, then **Compare**. Kron shows what it would do, without changing anything:
   - deleted roles to create again (and how many members had them);
   - edited roles to set back;
   - members who get their roles back;
   - channel permissions to set back.
2. Tick the steps you want, confirm, then **Restore**. Progress shows live.

A restore **never removes anything**: it creates, repairs and gives back. A backup of the current state is made just before.

> [!NOTE]
> A role created again has a **new ID** (Discord cannot reuse the old one). Kron updates its own settings that pointed at the old role (tickets, forms, levels…). Other bots must be set up again.
>
> Members who **left** the server cannot be brought back.

## Alert

Pick an **alert channel**: when a role is deleted, Kron writes which one and **who** deleted it (audit log).

The **Kron** role must be at the very top of the role list to recreate and give back every role.
