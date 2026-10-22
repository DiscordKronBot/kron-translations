---
title: Verification
category: modules
emoji: ✅
summary: Button or code on join, minimum account age, verified role.
order: 3
---

**Verification** makes new members click a button (or type a code) before they can access the server.

## Setup

1. Create a **Verified** role, below Kron's role.
2. Make your channels visible to **Verified** only, and a `✅┆verification` channel visible to @everyone.
3. In the dashboard: pick the channel, the role, the method, then **Publish the message**.

## Options

| Option | Effect |
|---|---|
| Method | **one click** on Verify, or a **code to type** (stops bots) |
| Minimum account age | refuses accounts that are too new (often raid accounts) |
| Removed role | removes an “Unverified” role given on join by [auto roles](/docs/roles-auto) |
| Message | the default message, or yours with the editor |
