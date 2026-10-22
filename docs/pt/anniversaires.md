---
title: Birthdays
category: modules
emoji: 🎂
summary: Wish happy birthday automatically, with a role for the day.
order: 10
---

## For members

| Command                                  | Effect                                                   |
| ---------------------------------------- | -------------------------------------------------------- |
| `/birthday set day:14 month:3`           | save your date (the year is optional) |
| `/birthday set day:14 month:3 year:2001` | with the year, `{age}` becomes available                 |
| `/birthday remove`                       | remove your date                                         |
| `/birthday upcoming`                     | the next 10 birthdays                                    |

## Settings

| Setting           | Effect                                                                                              |
| ----------------- | --------------------------------------------------------------------------------------------------- |
| Channel           | where to post the wishes                                                                            |
| Role of the day   | given on the birthday, removed the next day                                                         |
| Announcement time | from what time the wishes go out                                                                    |
| Time zone         | e.g. `America/Toronto`: the "day" follows this zone |
| Message           | default text, or a custom message                                                                   |

Variables: `{user}`, `{username}`, `{age}`, `{server}`, `{user.avatar}`.

> [!NOTE]
> Each birthday is wished only once per day, even if Kron restarts.
