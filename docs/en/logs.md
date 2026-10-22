---
title: Logs
category: modules
emoji: 📜
summary: Track messages, joins, roles, sanctions, voice and server changes, each in its own channel.
order: 4
popular: true
---

The **Logs** module records what happens on your server in dedicated channels, like the big moderation bots.

## Quick setup

1. Open **Logs** and click **✨ Create the channels for me**.
2. Pick the **staff roles** that can read the logs. In the **Will be created** preview, click a line to rename it, change its emoji or pick other roles for that channel.
3. Click **Create everything**: Kron creates a private `📜┆Logs` category with one channel per type: `💬┆log-message`, `🚪┆log-join-part`, `👤┆log-members`, `🏷️┆log-roles`, `🛡️┆log-moderation`, `🔊┆log-voice`, `🏠┆log-server`.
4. Turn the module on with the switch next to its title.

You can also pick your own channels, type by type.

## What gets recorded

| Type | Events |
|---|---|
| 💬 log-message | deleted messages (with content), edited (before / after), bulk deletes |
| 🚪 log-join-part | joins (account age, member count) and leaves |
| 👤 log-members | nickname changes |
| 🏷️ log-roles | roles added to or removed from members, roles created, edited (name, color, permissions…) and deleted, with who did it |
| 🛡️ log-moderation | bans, unbans, kicks, timeouts, with the author and reason |
| 🔊 log-voice | voice joins, leaves and moves |
| 🏠 log-server | channels created, deleted, renamed |

Each type has its own switch: you can turn one off without losing its channel.

## Filters

- **Ignore bot messages** (on by default).
- **Ignored channels**: nothing is recorded for messages in these channels.
- **Ignored roles**: actions of members with these roles are not recorded.

## Good to know

> [!NOTE]
> Discord does not send the content of a deleted message. Kron keeps recent messages in memory for **1 hour** to show it. After that, the log says "Unknown content".

- The author of a sanction comes from the audit log: Kron needs **View Audit Log**.
- Keep log channels private: the category created for you is already hidden from @everyone.
