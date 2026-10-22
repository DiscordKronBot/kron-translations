---
title: Honeypot
category: modules
emoji: 🍯
summary: A trap channel that catches spambots: they write, Kron bans or kicks them.
order: 17
---

Spambots write in every channel they can see. The **Honeypot** creates a trap channel where nobody has a reason to write: anyone who posts there is sanctioned right away.

## Setup

1. Turn on the **Honeypot** module.
2. Choose the channel **name** and, if you want, its **category**, then click **Create the trap channel**.
3. Kron creates the channel at the bottom of the list, open to everyone, with a clear warning: "Don't write here".

## Sanction

| Action | Effect |
|---|---|
| Ban | the account stays banned, with an **Unban** button in the log |
| Softban | bans then unbans right away: a kick that also deletes their messages |
| Kick | kicks only |

With **Delete messages**, the account's messages from the last hour are deleted (ban and softban).

## Log

Pick a **log channel**: every catch is reported there (member, account age, join date, message). If a ban was a mistake, the **Unban** button undoes it.

> [!NOTE]
> Members who can **Manage Messages** (staff) and the owner are never sanctioned.
