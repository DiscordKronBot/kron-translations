---
title: Moderation
category: modules
emoji: 🛡️
summary: Warn, time out, kick, ban and purge, with a history per member.
order: 12
---

## Commands

| Command | Required permission | Effect |
|---|---|---|
| `/warn member reason` | Timeout Members | warning saved in the history |
| `/timeout member duration reason` | Timeout Members | timeout (1 minute to 28 days) |
| `/untimeout member` | Timeout Members | lifts the timeout |
| `/kick member reason` | Kick Members | kicks the member |
| `/ban member reason delete_days` | Ban Members | bans, can delete 0 to 7 days of messages |
| `/unban user_id reason` | Ban Members | unbans by ID |
| `/purge amount member` | Manage Messages | deletes 1 to 100 messages (under 14 days old) |
| `/infractions member` | Timeout Members | the last 15 sanctions |

## Safety

- You can't act on yourself, on the server owner, or on a member of equal or higher rank.
- Kron also checks that it can act on the member (its role position).

## Settings

- **Tell the member by DM**: they get the sanction and the reason. For a kick or ban, the DM goes out just before the action.
- **Sanctions channel** (optional): one embed per sanction. The [Logs module](/docs/logs) already records bans, kicks and timeouts with their author.

## History

The dashboard's **History** tab lists the last 100 sanctions, filterable by member ID. You can delete a sanction given by mistake.

> [!TIP]
> For automatic protection, see [AutoMod](/docs/automod), [Anti-raid](/docs/anti-raid) and the Honeypot trap channel.

## Automatic sanctions

In the dashboard, add rules: for example **3 warnings → 1 hour timeout**, **5 → kick**, **7 → ban**. Kron applies the sanction on the `/warn` that reaches the count, and records it in the history and logs.
