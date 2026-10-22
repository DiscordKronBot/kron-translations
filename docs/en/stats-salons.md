---
title: Channel stats
category: modules
emoji: 📊
summary: Counters (members, humans, bots, boosts…) shown in the names of locked channels.
order: 11
---

## Create a counter

1. Pick the **type**: members, humans, bots, boosts, channels or roles.
2. Pick the **kind** of channel: voice (locked), text or category.
3. Adjust the **name**: `{count}` is replaced by the number, for example `👥┆Members: {count}`.
4. Click **Create counter**: Kron creates a channel **visible but locked** at the top of the server.

## Updates

Discord limits renaming a channel to twice per 10 minutes. Kron therefore updates counters **every 10 minutes**, only when the number changed.

> [!NOTE]
> Human and bot counters are computed for servers of 5000 members or fewer.

The Free plan allows 2 counters. A counter whose channel was deleted is marked "Channel deleted"; remove it from the list.
