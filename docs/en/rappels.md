---
title: Reminders
category: modules
emoji: ⏰
summary: Each member creates one-off or repeating reminders with /remind.
order: 9
---

## Commands

| Command | Effect |
|---|---|
| `/remind me when:2h text:Walk the dog` | reminder in 2 hours |
| `/remind me when:1d text:Staff meeting repeat:weekly` | reminder repeated every week |
| `/remind list` | your reminders on this server, with their number |
| `/remind delete id:7` | delete a reminder |

Accepted durations: `10m`, `2h`, `3d`, `1w`, combinable (`1h30m`), between 1 minute and 1 year. Repeats: `none`, `daily`, `weekly`, `monthly`.

## Server settings

- **Send reminders by DM**: otherwise Kron mentions the member in the channel where they created the reminder.
- **Maximum reminders per member**: 10 by default, up to 50.
