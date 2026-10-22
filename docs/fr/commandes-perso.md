---
title: Custom commands
category: modules
emoji: ⚡
summary: Create your own slash commands or text tags (!rules, $ip…), with a text or embed answer.
order: 16
---

The **Custom commands** module adds real slash commands to your server (`/rules`, `/ip`, `/shop`…) or **text tags** (`!rules`, `$ip`, or just `rules`).

## Create a command

1. Turn the module on. The page has two tabs: **⚡ Commands** (slash) and **🏷️ Tags** (text).
2. In the right tab, click **New command** or **New tag**.
3. Choose the **name** (lowercase, digits, `-` and `_`) and, for a slash command, the **description** shown in Discord.
4. Write the **answer** with the editor: text, embeds, link buttons. The preview updates live.
5. Save: the command is available right away on your server.

Variables in the answer: `{user}`, `{username}`, `{server}`, `{channel}`, `{memberCount}`, `{user.avatar}`.

## Text tags

Pick a **prefix** (`!`, `$`, `?`, `.`, `-`, `+` or none) and a name. When a message is exactly the trigger (for example `!rules`, `$ip` or just `rules`), Kron answers with your message or embed.

- **Reply to the message**: the answer shows as a reply to the member's message, otherwise as a plain message.
- **Delete the trigger message**: keeps the channel clean.
- A member triggers a tag at most once every 3 seconds.

> [!NOTE]
> `$debug` is reserved for Kron. A new tag can take up to 30 seconds to answer the first time.

## Options

- **Private answer** (slash): only the member using the command sees the answer.
- **Allowed roles**: only these roles can use it (empty = everyone). A tag stays silent for others.
- **Give a role / remove a role**: for example, `/accept` gives the "Read the rules" role.

> [!NOTE]
> The Free plan allows 5 commands. Pro makes them unlimited.

Turning the module off removes slash commands from Discord and mutes tags, without deleting anything: everything comes back when it is turned on again.
