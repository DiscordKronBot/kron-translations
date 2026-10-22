---
title: Twitch and Kick alerts
category: modules
emoji: 🟣
summary: Announce automatically when a Twitch or Kick channel goes live.
order: 20
---

The **Twitch** and **Kick** modules (Pro) post an alert as soon as a followed channel goes live: stream title, category, viewer count, live preview and a **Watch** button.

## Follow a channel

1. Turn on the **Twitch** or **Kick** module.
2. Enter the channel name (the one in the URL, for example `twitch.tv/`**`xqc`**) and click **Add**: Kron checks that it exists.
3. Pick the alert **channel**, the **roles to mention** (up to 5) and, if you want, **@everyone**.
4. Customize the **message** if needed, then save.

Message variables: `{streamer}`, `{title}`, `{game}`, `{url}`.

## How it works

- Kron checks channels **every minute**. A stream is announced **only once**, even if Kron restarts during it.
- **Stream end**: the alert can turn grey with the stream duration, be deleted, or stay as is.
- Up to **50 channels** per server and per platform.
