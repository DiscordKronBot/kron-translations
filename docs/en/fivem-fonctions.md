---
title: FiveM features
category: fivem
emoji: 🕹️
summary: Character profiles in tickets, Unstuck, Return a vehicle, in-city /report, job channels, live player board and RP sheets.
order: 2
---

Each feature has its own switch in the **🎮 FiveM bridge** module ([Pro plan](/pro)). They are all **off by default**: turn on only what you want.

## FiveM profile in tickets

When a player opens a ticket, Kron shows under the welcome message:

- their status (🟢 in the city or ⚫ offline) and their license (shortened);
- their character: name, job and grade, phone, cash, bank, citizenid;
- with **several characters**, a **See another character…** menu switches between them.

Pick the shown fields in **Displayed info**. Show only what your staff needs.

## Staff actions

Under the profile, two staff-only buttons:

- **📍 Unstuck**: if the player is in the city, they are teleported to the safe spot. If offline, their saved position is replaced: they spawn there next time.
- **🚗 Return a vehicle**: Kron lists the character's vehicles (out, in garage, impounded). Pick one: it is removed from the world if still there, then stored in the garage.

The player is told in game in both cases.

**Who is staff?** The roles picked in **FiveM staff**, plus members with Timeout Members or Manage Server.

## /fivem command

| Command | Effect |
|---|---|
| `/fivem profil membre:@Player` | the player's profile, with the action buttons |
| `/fivem debloquer membre:@Player` | opens the profile to pick the character to unstuck |
| `/fivem garage membre:@Player` | opens the profile to pick the vehicle to return |

Answers are only visible to you.

## In-city /report

1. Turn on **In-city /report**. If your server already has its own `/report`, leave it off: the resource then adds no command.
2. In the preview, adjust the channel (private `🚨┆city-reports`) and who can see it, then click **✨ Create the channel for me**, or pick a channel. Add the roles to mention.
3. In game, the player types `/report I'm stuck under the map`.
4. Kron creates a **thread** in the channel, with the message, the player's name, their in-game ID and the **👁️ Profile** and **🔒 Close** buttons.
5. **Staff write in the thread**: each message goes to the player in the in-game chat (Kron reacts with 📨).
6. While the report is open, the player's new `/report`s join the same thread: a real conversation.
7. **🔒 Close** archives the thread and tells the player.

> [!TIP]
> A cooldown (15 seconds by default) stops a player from spamming `/report`.

## Job and gang channels

Kron reads your server's jobs and gangs (QBCore or Qbox) and creates a **JOBS** category with a private channel per job: a "permanent ticket" between staff and each job.

1. Turn on **Job channels** in the dashboard's FiveM page (resource 1.2.0 or later, server online).
2. Click **Load the server's jobs** and check the ones you want (police, EMS, mechanic, gangs…).
3. For each job, pick the **Discord role** of that job's members. Without a role, only staff see the channel.
4. Adjust names and emojis in the preview, then create the channels.

Each channel is visible to the FiveM staff roles, to Kron and to the job's role, and hidden from everyone else.

## Live player board

One message Kron keeps up to date in a channel: server state, players online and slots, jobs on duty (resource 1.4.0 or later).

1. Turn on **Player board**.
2. Click **✨ Create the channel for me** (`📊┆city-live`, everyone can read it, only Kron writes) or pick a channel.
3. Optional: a title, and a **Join** link (`https://cfx.re/join/...`) that adds a button under the board.

Kron checks the server every minute and edits the message only when something changed. If the message is deleted, Kron posts a new one.

## RP character sheets

One sheet per character: name, age, occupation, story and image, shown in a card.

- **Create or edit** (staff): in a member's FiveM profile (`/fivem profil` or a ticket header), click **📜 RP sheet**, then fill the form. An existing sheet has an **✏️ Edit** button.
- **Read** (everyone): `/fiche membre:@Player` (or `/fiche` for yours). A menu switches between characters.
- **Dashboard**: the **Character sheets** section lists every sheet to edit or delete it.

The image must be an `https://` link.

## FiveM tags

When the module is on, every message editor (welcome, embeds, commands…) offers these tags:

| Tag | Value |
|---|---|
| `{fivem.server}` | FiveM server name |
| `{fivem.status}` | 🟢 or 🔴 |
| `{fivem.players}` / `{fivem.maxPlayers}` | players online / slots |
| `{fivem.police}` / `{fivem.ems}` | police / EMS on duty (resource 1.4.0) |
| `{fivem.jobs}` | busiest jobs on duty, e.g. `Police 3 · EMS 1` |

## FAQ

**"No linked FiveM account".** The player never connected with Discord open. Ask them to restart Discord, then FiveM.

**"The FiveM server did not answer in time".** The server is overloaded or just restarted. Try again in a few seconds.
