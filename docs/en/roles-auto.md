---
title: Auto roles
category: modules
emoji: 🏷️
summary: Give roles to every new member, with a delay and Discord's membership screening.
order: 5
---

The **Auto roles** module gives one or more roles to everyone who joins your server. It is the first step of a whitelist: the newcomer gets `@new`, which opens the form channel.

## Settings

| Setting | Effect |
|---|---|
| Members | roles given to humans (e.g. `@new`) |
| Bots | roles given to bots that join |
| Delay | from 0 seconds to 1 hour before giving the roles |
| Wait for rules acceptance | if your server uses Discord's membership screening, the role is given only after acceptance |

## With the whitelist

1. Auto roles: `@new` for members.
2. Whitelist, Roles tab: `@passport` when the form is sent; on acceptance, `@citizen` added and `@new` + `@passport` removed.

See [Whitelist and forms](/docs/whitelist).

> [!IMPORTANT]
> Roles must be below Kron's role. Those it can't manage are skipped.

> [!NOTE]
> A pending delay is lost if Kron restarts during the wait. For a critical role, keep the delay short.
