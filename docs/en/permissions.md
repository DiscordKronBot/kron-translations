---
title: Permissions and roles
category: start
emoji: 🔐
summary: What Kron asks for, why, and how to set the role hierarchy.
order: 2
---

When you invite Kron (the **Add App** button of its profile, the website or the dashboard link), it asks for the **Administrator** permission.

## Why Administrator?

On Discord, a private channel hides itself from **every role** not added to it, even from a bot with "Manage Channels". Without Administrator, every private channel is invisible to Kron, and many features break silently:

- **Beautify names** and the channel builder cannot rename or move those channels;
- **logs** do not see deleted or edited messages there;
- **moderation** (`/purge`), **tickets**, **counters** and **anti-raid** cannot act there;
- every new private channel needs the Kron role added by hand.

With Administrator, Kron sees and manages your whole server as intended, with no per-channel setup.

What Kron does with it:

- **only what you set up** in the dashboard or with a command: it never deletes a channel, role or message on its own, and beautifying only renames;
- every dashboard action is made for a member with **Manage Server** or **Administrator**, checked again by our servers each time;
- important actions are listed in Discord's **audit log** with the reason "Kron: …".

> [!NOTE]
> You can remove Administrator and give only the permissions listed below. Kron then works, but its role must be added to every private channel it should manage. The channel builder marks the channels it cannot see with 🔒.

**Staff roles** never need Administrator to use Kron.

## Permissions used

| Permission | Used by |
|---|---|
| View Channels | every module |
| Send Messages | every module |
| Embed Links | embeds, logs, tickets, whitelist |
| Attach Files | ticket transcripts |
| Read Message History | transcripts, `/purge` |
| Manage Messages | `/purge`, `$debug` (deletes your command) |
| Manage Channels | tickets, log channels, counters, FiveM channels, channel builder |
| Manage Roles | whitelist, auto roles, reaction roles, tickets, levels, custom commands |
| View Audit Log | Logs module (who banned, kicked, timed out) |
| Manage Server | AutoMod (Discord rules), anti-raid (invite pause) |
| Kick Members | `/kick`, anti-raid |
| Ban Members | `/ban`, `/unban`, anti-raid, honeypot |
| Timeout Members | `/timeout`, `/untimeout` |

> [!WARNING]
> If you remove a permission, the module that needs it stops working for that action. `$debug` shows exactly what is missing.

## The role hierarchy

Discord applies a simple rule: **a bot can only manage roles below its own role**. It also cannot act on a member whose highest role is above its own.

For everything to work:

1. Open **Server Settings → Roles**.
2. Place the **Kron** role above every role it must give: whitelist roles, auto roles, menu roles, birthday role, level rewards.
3. For moderation, place it above the members it must be able to sanction.

> [!TIP]
> In the dashboard, every role picker flags roles Kron can't manage with ⚠️.

## Channel permissions

A permission denied in a channel (or its category) applies to Kron too. If Kron can't write in a channel, the dashboard tells you when sending, and `$debug` typed in that channel shows the **Channel** score.

## Who can use the commands?

- **Moderation** commands are limited by default to members with the matching Discord permission (Kick, Ban, Timeout, Manage Messages).
- You can fine-tune who sees each command in **Server Settings → Integrations → Kron**.
- In the dashboard, only members with **Manage Server** or **Administrator** can configure Kron. Our servers check permissions again on every action.
