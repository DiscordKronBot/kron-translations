---
title: Polls
category: modules
emoji: 📊
summary: Polls with an end time, several choices, hidden results and result bars.
order: 22
---

`/poll` posts a card with one button per choice and live result bars.

## Create a poll

```
/poll question:What do we eat Friday? choices:Pizza | Sushi | Tacos duration:60 multiple:false hidden:false
```

- **choices**: 2 to 10, separated by `|`.
- **duration**: in minutes; empty = until someone clicks **End**.
- **multiple**: each member can pick several choices.
- **hidden**: results stay hidden until the end.

A member changes their vote by clicking again. At the end, the winning choice gets 🏆.

## Who can create polls

By default, members who can manage messages. Add roles in the dashboard to open it to others. The dashboard also lists recent polls.
