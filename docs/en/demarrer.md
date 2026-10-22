---
title: Add Kron to your server
category: start
emoji: 🚀
summary: Invite the bot, sign in to the dashboard and turn on your first module in 5 minutes.
order: 1
popular: true
---

Kron is an all-in-one Discord bot: tickets, whitelists with web forms, logs, roles, embeds, giveaways and much more. Everything is set up from the **kronbot.xyz** dashboard, without a line of code.

## 1. Invite Kron

1. Go to [kronbot.xyz/invite](https://kronbot.xyz/invite), or click **Add App** on Kron's Discord profile.
2. Pick the server. You need the **Manage Server** permission on it.
3. Leave every permission checked and click **Authorize**.

> [!IMPORTANT]
> Kron asks for **Administrator**: without it, private channels are invisible to it and several features break. It only does what you set up. Details in [Permissions and roles](/docs/permissions#why-administrator).

## 2. Place Kron's role

Discord only lets a bot manage a role if **its own role is higher** in the list.

1. Open **Server Settings → Roles**.
2. Drag the **Kron** role above the roles it must give or remove (for example `@new`, `@citizen`, your menu roles).
3. Save.

> [!TIP]
> In the dashboard, a role too high for Kron is flagged with ⚠️. The `$debug` command flags it too.

## 3. Sign in to the dashboard

1. Go to [kronbot.xyz](https://kronbot.xyz) and click **Log in**.
2. A quick bot check shows up, then Discord asks you to authorize Kron.
3. Kron only asks for your **profile** and your **server list**. It has no access to your messages.

You land on **Your servers**. Only servers you can **manage** are listed. Those without Kron yet have an **Invite** button.

## 4. Turn on a module

1. Click your server.
2. In the sidebar, pick a module (for example **Tickets**).
3. Flip the switch next to the module's title (green = on, red = off): it saves right away.
4. Configure the module. An **Unsaved changes** bar appears at the bottom: click **Save**.

> [!NOTE]
> A module that is off can be configured in advance. It works as soon as you turn it on.

## 5. Pick the language

In **Settings**, choose Kron's language for your server (French or English). It is used for the bot's public messages. Private messages and answers only one person sees follow each member's Discord language.

## What next?

- [Set up a whitelist](/docs/whitelist), with a web form and roles at each step.
- [Create a ticket system](/docs/tickets), fully customized.
- [Turn on logs](/docs/logs) in one click.
- [Link your FiveM server](/docs/fivem-installation) to show players' characters in tickets.
