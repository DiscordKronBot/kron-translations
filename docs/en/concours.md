---
title: Giveaways
category: modules
emoji: 🎁
summary: Start a giveaway with one command or from the dashboard, with a random draw and rerolls.
order: 8
---

## Start a giveaway

**In Discord:**

```
/giveaway start prize:Nitro 1 month duration:2d winners:1
```

| Option | Description |
|---|---|
| `prize` | the prize (required) |
| `duration` | duration: `30m`, `2h`, `1d`, `1w`, combinable (`1d12h`). Between 1 minute and 30 days |
| `winners` | number of winners, 1 to 20 (1 by default) |
| `channel` | giveaway channel (the current one by default) |
| `role` | role required to enter |

**In the dashboard:** prize, winners, duration, channel and required role, then **🎉 Start the giveaway**.

## Entering

Members click **🎉 Enter**. The counter updates, and a second click withdraws. If a role is required, others get a message telling them.

## End and draw

At the planned time, Kron draws the winners at random (cryptographic draw), updates the message and announces the winners with a mention.

- `/giveaway end id:12`: ends it now.
- `/giveaway reroll id:12`: draws new winners, excluding the previous ones.

Commands are limited to members with **Manage Server**. The Free plan allows 5 active giveaways at a time.
