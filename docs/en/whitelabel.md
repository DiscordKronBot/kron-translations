---
title: Whitelabel, your own bot
category: premium
emoji: 🏷️
summary: Every Kron feature under your name and avatar, with your own Discord application.
order: 2
---

With **Whitelabel**, your server uses **your own bot**: its name, avatar and status are yours, but it runs on Kron, with the same settings and the same kronbot.xyz dashboard.

## What you need

- The **Whitelabel** plan on your server (Monthly + Whitelabel at $6.99 USD, or included in the Yearly and Lifetime offers).
- A **Discord application** you create yourself, for free.

## 1. Open the Developer Portal

Go to [discord.com/developers/applications](https://discord.com/developers/applications).

## 2. Create your application

Click **New Application**, give it a name and accept the terms.

![Developer Portal: New Application](/docs/whitelabel/1-new-application.svg)

## 3. Installation tab

Under **Default Install Settings**, pick:

- **User Install**, scopes: `applications.commands`
- **Guild Install**, scopes: `applications.commands` and `bot`
- **Guild Install**, permissions: `Administrator`

Save Changes.

## 4. Bot tab

1. Click **Reset Token** and copy the token (keep it for step 6).
2. Under **Privileged Gateway Intents**, turn on:
   - **Server Members Intent** (auto roles, welcome, logs, whitelist);
   - **Message Content Intent** (`$debug`, message logs, tags, levels).
3. Save Changes. Kron refuses the token until both intents are on.

![Bot tab: Server Members and Message Content intents on, then Save Changes](/docs/whitelabel/2-intents.svg)

![Bot tab: Reset Token, then Copy](/docs/whitelabel/3-reset-token.svg)

## 5. General Information tab

Choose your bot's **avatar**, **name** and **description** (its bio), then **Save Changes**.

## 6. Connect your bot

1. Kron dashboard, **Settings → Whitelabel**, paste the token then **Connect**. Kron checks the token with Discord, then encrypts it.
2. Click **Invite your bot**: the link adds your bot to your server.

Kron hosts your bot: it stays **online 24/7**, nothing to run on your side.

![Kron dashboard: Settings, Whitelabel, paste the token, Connect](/docs/whitelabel/4-connect.svg)

> [!WARNING]
> The token controls your bot. Never give it to anyone: only paste it in the Kron dashboard. If it leaked, click **Reset Token** and replace it in **Settings → Whitelabel**.

## 7. Your bot takes over

Within a minute, your bot comes **online** and its slash commands appear. **Kron then leaves your server automatically**: your bot picks up all your settings (modules, tickets, forms, levels…) with nothing to redo.

In **Settings → Whitelabel** you can then change:

- the bot's **name** (Discord allows about 2 changes per hour);
- its **avatar**;
- its **status** (the text under its name).

Your bot never shows the "Kron" signature. It only works in your server: added elsewhere, it leaves.

## Existing messages

Discord does not let a bot edit messages sent by another bot. After switching to Whitelabel, publish again from the dashboard:

- your **ticket panels** (Publish button);
- your **role menus** (Publish button);
- the **embeds** you want to edit later.

## Disconnect your bot

**Settings → Whitelabel → Disconnect the bot** stops your bot. Then invite Kron back (the link opens automatically): your settings are intact.

## When the subscription ends

After **7 days of grace**, your bot stops. Your settings are kept: invite Kron back and publish your panels again to continue with the standard version.
