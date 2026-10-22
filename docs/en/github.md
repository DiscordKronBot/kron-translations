---
title: GitHub
category: modules
emoji: 🐙
summary: Your repositories' pushes posted as clean embeds, one section per commit.
order: 19
---

The **GitHub** module (Pro) posts every push of your repositories in a channel: one message per push, one section per commit with its link, details and author. It is the same rendering as Kron's own #github channel.

## Follow a repository

1. Turn on the **GitHub** module.
2. Enter the repository (`owner/name`), a **branch** to filter on if you want (empty = all), and the channel.
3. Click **Create feed**. Kron shows a **URL** and a **secret**.
4. In GitHub: your repository → **Settings → Webhooks → Add webhook**.
   - **Payload URL**: the URL Kron gave you.
   - **Content type**: `application/json`.
   - **Secret**: the secret Kron gave you.
   - **Which events**: *Just the push event*.
5. Save. GitHub sends a ping, then every push lands in your channel.

> [!WARNING]
> The secret is shown only once. Lost it? Click **New secret** and update it in GitHub.

## Good to know

- Up to **10 repositories** per server.
- Pushes from another repository, or another branch than the chosen one, are ignored.
- Every request is checked with GitHub's signature: nobody else can post in your channel.
