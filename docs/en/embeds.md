---
title: Embeds
category: modules
emoji: 🧱
summary: Build good-looking messages, keep them in a library, send them now or schedule them.
order: 3
---

The **Embeds** module is a visual Discord message editor, inspired by Discohook, with a library per server and scheduled sends.

## Library

1. **📚 Library** tab, then **New embed**.
2. Give it a name (only staff see it).
3. Build the message with the editor and its live preview (see [Using the dashboard](/docs/dashboard)).
4. Save with the bottom bar.

The Free plan keeps **5 embeds**; Pro, unlimited.

## Send

**📨 Send** tab:

1. Pick an embed from the library and a channel.
2. **Now**: the message goes out and a **View in Discord** link appears.
3. **Schedule**: pick the date, time and repeat (once, daily, weekly or monthly).

## Scheduled sends

**⏰ Scheduled** tab: the list with the next date, the repeat and the last error, if any. You can pause or delete a send. The Free plan allows **5 active scheduled sends**.

> [!NOTE]
> If Kron was offline at the planned time, the message goes out as soon as it is back, then the repeat continues as usual.

## Edit a message already sent

**✉️ Sent** tab: click **Edit**, change the message, then **Update in Discord**. The message is edited in place, no new one is posted. Ideal for rules or information that changes.

## Import and export

Under the editor:

- **Import JSON**: paste a message in Discord or Discohook format.
- **Copy JSON**: copy the message to reuse it elsewhere.

## FAQ

**"Kron can't write in this channel".** Check the channel permissions for the Kron role (View, Send, Embed Links).

**My image doesn't show.** The URL must start with `https://` and point straight to an image.
