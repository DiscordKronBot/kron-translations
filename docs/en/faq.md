---
title: FAQ
category: help
emoji: ❓
summary: Answers to the questions we get most often.
order: 2
---

## Kron doesn't answer a command

1. Check that the **module is on** in the dashboard (green switch next to the module's title).
2. Type `$debug` in the channel: it shows the missing permissions.
3. Slash commands can take a few minutes to show up after the bot joins. Restart Discord if needed (`Ctrl + R`).

## Kron doesn't give a role

Kron's role must be **above** the role to give. See [Permissions and roles](/docs/permissions).

## I don't see my server in the dashboard

You need **Manage Server** or **Administrator** on that server. Click **Refresh** at the top of the list: Discord can take a minute to tell us about a new server.

## I changed a panel but nothing changes in Discord

Ticket panels and role menus must be **published again** (📤 Publish button) after saving.

## Does Kron read my messages?

Kron receives messages from the channels it is in, like any bot with the Message Content intent. It does not store them: the Logs module only keeps recent messages in memory for **1 hour**, to show the content of a deleted message. Levels only count messages, never their content. See the [privacy policy](/legal/privacy).

## How do I delete my data?

Write to [dev@kronbot.xyz](mailto:dev@kronbot.xyz) with "Privacy" in the subject. We answer within 30 days. Data of a server Kron was removed from is deleted automatically after 30 days.

## Is Kron linked to Discord?

No. Kron is an independent product, not affiliated with Discord Inc.

## Another question?

Open a ticket on our server: [kronbot.xyz/support](https://kronbot.xyz/support).
