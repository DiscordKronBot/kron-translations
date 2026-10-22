---
title: Whitelist and forms
category: modules
emoji: 📝
summary: A web form, roles that change at each step, and application review right inside Discord.
order: 1
popular: true
---

The **Whitelist & forms** module replaces external application tools. The player fills a form on the web, signed in with their Discord account (no ID to type), and your staff accept or deny in one click inside Discord.

## How it works

1. The new member joins the server and gets `@new` ([Auto roles](/docs/roles-auto) module).
2. They open the form link (`kronbot.xyz/f/xxxxxx`), sign in with Discord and answer the questions.
3. Kron posts the application in your review channel with **✅ Accept**, **❌ Deny** and **🎙️ Interview** buttons, and gives them `@passport`.
4. Staff accept: Kron gives `@citizen` and removes `@passport` and `@new`. The player gets a DM.
5. Or staff deny with a reason: Kron removes `@passport` and sends the reason by DM. The player can try again after the chosen delay.

## Create your form

1. Open **Whitelist & forms** and click **New form**.
2. Pick a **template** (whitelist, RP staff, moderation, developer) and its **language** (French or English), or a blank form.
3. Adjust each tab, then save with the bottom bar.
4. Copy the **public link** from the General tab and share it (welcome channel, welcome message, ticket panel…).

> [!NOTE]
> On the Free plan you get **1 form**. Pro allows unlimited forms (whitelist, staff recruitment, developers…).

## General tab

| Setting | Effect |
|---|---|
| Name | only staff see it |
| Color | color of the public page and of the application embed |
| Form open | unchecked, the form no longer accepts applications |
| Displayed title | title of the public page |
| Description | intro text, with formatting (bold, lists, links) |
| Delay after a denial | hours before a new application (0 = none) |

## Questions tab

Up to **25 questions**, in the order you want:

| Type | Use | Settings |
|---|---|---|
| Short text | name, nickname | min / max characters (200 by default) |
| Paragraph | story, motivation | min / max characters (4000 by default) |
| Choice | one option from a list | 2 options minimum, one per line |
| Number | age, hours played | min / max value |
| Checkbox | "I read the rules" | required = must be checked |

Each question can have **help** text under its title, and be **required** or not.

## Review tab

- **Applications channel**: where applications arrive with their buttons.
- **Roles to mention**: pinged on every new application.
- **Roles that can accept or deny**: on top of members with Manage Server.
- **Interview voice channel** (optional): turns on the 🎙️ Interview button, which invites the player by DM to join that channel.

## Roles tab

Three steps, each with its roles:

| Step | Action |
|---|---|
| 📨 Form sent | add roles (e.g. `@passport`) |
| ✅ Accepted | add (e.g. `@citizen`) and remove (e.g. `@passport`, `@new`) |
| ❌ Denied | remove (e.g. `@passport`) |

> [!IMPORTANT]
> Kron's role must be **above** all these roles. Otherwise Discord refuses the change.

## Messages tab

Four DMs sent to the player: application received, accepted, denied, interview invitation. Without customization, Kron sends a default text. Check **Customize** to use the full editor.

| Variable | Replaced by |
|---|---|
| `{user}` | player mention |
| `{username}` | player name |
| `{server}` | server name |
| `{form}` | form title |
| `{reason}` | denial reason |
| `{channel}` | interview voice channel |

## Reviewing applications

**In Discord**: click ✅ or ❌ under the application. Deny opens a window for the reason (optional, sent to the player). The embed turns green or red and shows who decided. If two staff members click at the same time, only the first one counts.

**In the dashboard**: the **Applications** tab lists pending, accepted and denied applications, with every answer.

## What the player sees

- If they are not signed in, the page offers to sign in with Discord, then brings them back to the form.
- If they are not a member of the server, the page asks them to join first.
- If they already have a pending application, or are within their delay after a denial, the page says so with the date.
- A bot check protects the submission.

## FAQ

**The player doesn't get DMs.** Their DMs are probably closed for this server. The application is still handled.

**Roles don't change.** Check the position of Kron's role and run `$debug`.

**I want several forms (staff, dev).** That works with Pro. Each form has its own link, questions, channel and roles.
