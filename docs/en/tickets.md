---
title: Tickets
category: modules
emoji: 🎫
summary: Button or menu panels, questions before opening, claiming, closing, auto-close and web transcripts.
order: 2
popular: true
---

The **Tickets** module creates a private channel between a member and your team. Everything is customizable: the panel message, every button, the category, support roles, channel names, questions and the welcome message.

## Quick setup

**⚡ Quick setup** creates everything in one click: a `🆘┆Support` category, a public `🎫┆tickets` channel with a ready panel, and in your logs category (reused if it exists) the private `🔕┆logs-ticket` and `🔕┆ticket-transcripts` channels.

Pick the staff roles first: they see the tickets, logs and transcripts. In the **Will be created** preview, click a line to rename it, change its emoji, or choose who can see it. You also pick:

- **the tickets category**: an existing one, or a new `🆘┆Support`;
- **the logs category**: the first one Kron created on your server is suggested (tip: set up the [Logs](/docs/logs) module first, every module then keeps its logs in one place);
- **the rules channel** and **a docs or FAQ link**: they show in the panel text;
- **the panel look** (see below).

## Create a panel

1. Open **Tickets** then **New panel**. A "Support" and "Complaint" template is ready.
2. **Message**: the panel embed (title, description, color, image…). The preview shows the buttons.
3. **Buttons**: one button per ticket type (up to 10).
4. **Settings**: the channel to publish in, the display (buttons or menu), transcripts.
5. Save with the bottom bar, then click **📤 Publish**.

After a change, click **Publish** again: Kron updates the existing message instead of posting a new one.

> [!NOTE]
> The Free plan allows 1 panel. Each panel can have up to 10 ticket types.

## Panel look

In the **Message** tab, four previews show your real panel four ways. Click the one you like:

| Look | What members see |
|---|---|
| Embed + buttons | the classic Discord message, one button per ticket type |
| Embed + dropdown | one menu, handy with many types |
| Card + buttons | Discord's newer layout (Components V2): text, image and buttons in one block |
| Card + dropdown | the card, with a menu |

Two switches add **the server icon** beside the text and **the server banner** at the bottom (when your server has one). **Quick content** adds "read the rules in #rules" and your docs link to the message in one click.

Switching between embed and card, **Publish** replaces the old message: Discord cannot turn one into the other.

## Ticket type settings

| Setting | Effect |
|---|---|
| Text, emoji | what the button shows |
| Button color | blue, grey, green or red |
| Description | under the option, in menu mode |
| Category | where ticket channels are created |
| Channel name | a ready rule (`ticket-0001`, `ticket-bob`, `ticket-bobby`…) or your own template with `{number}` (0001), `{username}` (username) and `{nickname}` (server nickname) |
| Support team | roles that see tickets, are mentioned and can manage them |
| Questions | up to 5, asked in a Discord window before opening: written answer (short or long) or a dropdown choice (one or several), required or not |
| Welcome message | default text, or a custom message with the editor |

Welcome message variables: `{user}`, `{username}`, `{number}` (4-digit number), `{server}`, `{type}`.

## A ticket's life

1. **Open**: the member clicks a button, answers any questions, and Kron creates the channel. Only the member, the team and Kron can see it. Answers show in an embed, along with the member's ticket count and a link to their history.
2. **🙋 Claim**: a team member says they are on it.
3. **🔒 Close**: the member or the team closes it, with an optional reason. The member can still read but no longer write, and the transcript is sent.
4. **🔓 Reopen**, **📜 Transcript** or **🗑️ Delete**: the channel is deleted 5 seconds later.

## Auto-close

In the module settings, **Auto-close** closes open tickets with no message for a number of hours (48 by default). Claimed tickets are skipped by default. The transcript is saved as usual.

## Transcripts

On close, Kron saves the whole conversation (messages, embeds, attachments) as a **web page**:

- the link is posted in the chosen **transcripts channel**;
- and sent by **DM to the member** if the option is checked;
- the page offers a **Download (.html)** button.

Members see their own tickets at **My tickets**; staff see a member's full history.

## Limits and safety

- **Maximum open tickets per member** (1 by default): avoids duplicates.
- Kron checks that the chosen categories and channels belong to your server.

## With the FiveM module

If the [FiveM module](/docs/fivem-fonctions) is on with "Profile in tickets", every ticket shows the player's in-city characters, with the staff buttons **📍 Unstuck** and **🚗 Return a vehicle**.

## FAQ

**"Could not create the ticket channel".** Kron lacks Manage Channels in the chosen category. Run `$debug`.

**Support can't see tickets.** Add their roles in "Support team", on each ticket type.

**I changed the panel but nothing changes in Discord.** Click **Publish** after saving.

## Priority, internal notes and satisfaction

- **🚦 Priority**: staff pick Low, Normal, High or Urgent. The channel name gets a dot (🟢 🟠 🔴).
- **📝 Note**: an internal note, only staff see it on the ticket's web page.
- **⭐ Member rating**: when the ticket closes, the member rates the help from 1 to 5 stars.
- The module's **Stats** tab shows, per staff member, tickets claimed and closed, and the average rating.
