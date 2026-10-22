---
title: Invite tracker
category: modules
emoji: 📨
summary: Who invited whom, a join message with the invite count, staff logs and a leaderboard.
order: 4
---

The **Invite tracker** module finds, on every join, the invite used and who created it.

## Public message

Pick a channel (your welcome channel, for example, or **+ Create** for `📨┆arrivals`). On every join:

> 👋 @Bob joined the server, invited by **Bill** who now has **25** invites!

Tick **Customize the message** to write your own (text or embed). Variables: `{user}`, `{username}`, `{inviter}` (mention, no ping), `{inviter.name}`, `{invites}`, `{code}`, plus the common ones (`{server}`, `{memberCount}`…).

Joined through the server's **custom link**: "through the custom link". Invite not found: only the join is announced.

## Staff logs

A log channel (**+ Create** puts it in the server's logs category) gets every join and leave: invite code, inviter, their total, account age.

## How it counts

| | |
|---|---|
| **Valid** | invited members still on the server |
| **Left** | those who left since |
| **Fake** | accounts created less than X days before joining (setting, 0 = never) |

A member who leaves and comes back counts once, with their latest join.

## Commands

- `/invites view [member]`: a member's invites (you by default).
- `/invites top`: the 10 best inviters. The full leaderboard is in the dashboard.

> [!NOTE]
> Kron needs the **Manage Server** permission to see invites (included in Administrator). Right after turning it on, the very first join can stay "unknown": Kron learns the server's invites then.
