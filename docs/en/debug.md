---
title: $debug diagnostics and support
category: help
emoji: 🩺
summary: Check what is blocking in one command, and share the report with support.
order: 1
popular: true
---

## The $debug command

Type `$debug` in **any channel** of your server. Kron answers with a full diagnostic, then deletes your command.

The report contains:

- **Overall state**: ✅ all good, or ⚠️ the number of problems found.
- Kron's **permissions** on the server and in this channel (for example `🛡️ Server ┆ ✅ 12/12`), with the exact list of what is missing.
- **The server**: name, ID, members, channels (out of 500), roles (out of 250), boosts, language, creation date.
- **Kron**: version, plan, active modules, its role position, latency, uptime, join date.
- **The channel** and **you**: your level (owner, administrator, manager, member).

> [!TIP]
> Type `$debug` **in the channel that has the problem**: the "Channel" score shows exactly what Kron can do there.

## The report link

Kron gives you a link like `kronbot.xyz/d/AbC123xYz9`:

- it opens a web page with the same diagnostic, readable without Discord;
- pasted in a Discord channel, it shows a preview (state and permission score);
- it is kept **90 days**, then deleted automatically;
- the code is random and impossible to guess.

## Getting help

1. Type `$debug` in the channel concerned.
2. Join our support server: [kronbot.xyz/support](https://kronbot.xyz/support).
3. Open a ticket and paste the report link.

The team then sees exactly what you see. It is the fastest way to get an answer.

> [!NOTE]
> For billing or privacy questions, you can also write to [dev@kronbot.xyz](mailto:dev@kronbot.xyz).
