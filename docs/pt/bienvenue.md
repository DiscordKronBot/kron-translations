---
title: Welcome and goodbye
category: modules
emoji: 👋
summary: Greet every new member in a channel and by DM, and announce departures.
order: 7
---

## Joining

- **Channel**: where to post the welcome message.
- **Channel message**: a default card (avatar, account creation date, bot or member, member number), or your custom message with the editor, which starts from that card.
- **Direct message**: optional, sent straight to the new member (for example your whitelist link or your rules).

## Leaving

- Goodbye **channel** and **message**, off by default.

## Variables

| Variable                               | Replaced by                                                          |
| -------------------------------------- | -------------------------------------------------------------------- |
| `{user}`                               | member mention                                                       |
| `{username}`                           | member name                                                          |
| `{server}`                             | server name                                                          |
| `{memberCount}`                        | member count                                                         |
| `{user.avatar}`                        | member avatar, usable as an image or thumbnail                       |
| `{user.id}`                            | member ID                                                            |
| `{user.created}` / `{user.createdAgo}` | account creation date / its age (“2 years ago”)   |
| `{user.type}`                          | 🤖 Bot or 👤 Member                                                  |
| `{user.joined}`                        | when they joined the server (useful for goodbyes) |
| `{server.icon}`                        | server icon                                                          |

> [!TIP]
> Put `{user.avatar}` in the embed **thumbnail**: every welcome shows the new member's picture.

## Options

- **Ignore bots** (on by default): no message for bots that join.
- Only `{user}` can ping the member: never @everyone or roles by accident.
