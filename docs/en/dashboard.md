---
title: Using the dashboard
category: start
emoji: 🖥️
summary: Navigation, saving, drafts and the message editor: everything modules share.
order: 3
---

## Navigation

- **Your servers**: the servers you manage. Hover a server without Kron to see the **Invite** button.
- **Sidebar**: the server switcher at the top, then **Overview**, **Settings** and every module, grouped by category.
- **Overview**: active modules, members, language and plan. You can turn several modules on or off at once.

## The General page

**General**, at the top of the menu, holds the settings of the whole server:

- Kron's **language** and **signature** (Pro);
- **channel naming style**: separator (`┆`, `・`, `│`…) and font. Every channel Kron creates follows it: setups, **Create** buttons, channel builder packs. "Beautify names" uses it too;
- **text commands**: the default prefix of new tags (`!`, `?`, `.`…) and each existing tag's prefix;
- **logs category**: where every module puts its log channels;
- **dashboard tour**: restart the short guided tour of the first visit.

## Create a channel from a module

Next to channel pickers (verification, welcome, moderation logs, tickets…), **+ Create** makes the channel for you, in your server's style. Change the emoji and name first if you like; the preview shows the final name.

- A regular channel goes **to the top of the server**.
- A log channel goes into the server's **logs category** and keeps its access (staff only). When there is none yet, Kron asks which roles can see it.
- Kron never deletes a channel to make another one.

## Turning modules on and off

The switch next to a module's title saves right away: **green** when the module is on, **red** when it is off. A green check flashes once it is saved.

## Saving your changes

Every other change (a text, a role, a channel) is first a **draft**. As soon as you change something, a bar appears at the bottom of the screen:

- **Save** applies every change on the page.
- **Cancel** goes back to the last saved version.

If you leave the page (a link, another server, another tab of the module, an editor's back button) with unsaved changes, Kron asks what to do: **Save and continue**, **Leave without saving** or **Stay**. If you close the tab or the browser, your browser warns you too.

> [!NOTE]
> The Save button stays greyed out while a required field is empty or invalid (for example an empty message or a wrong URL).

## "Will be created" previews

When a module creates channels for you (tickets quick setup, logs, FiveM), it first shows what **will be created**. Click any line to change its emoji, its name or, for private channels, the roles that can see it, then **Save** or **Cancel** that line.

## The message editor

Wherever Kron sends a message (embeds, tickets, whitelist, welcome, birthdays, custom commands), you use the same editor, with a **live Discord preview**:

- **Message**: the text above the embeds (2000 characters).
- **Up to 10 embeds**, each with: author (name, link, icon), title and link, description (4096 characters), color, up to 25 fields (inline or not), image, thumbnail, footer with icon, and timestamp.
- **Up to 5 link buttons** under the message.
- Character **counters** and a warning when the total goes over Discord's 6000 character limit.
- **Import / copy the JSON**, compatible with Discord and Discohook.

Text accepts Discord formatting: `**bold**`, `*italic*`, `__underline__`, `~~strikethrough~~`, `` `code` ``, `> quote`, `# headings`, `- ` lists, `[text](https://…)` links and `||spoilers||`.

### Variables

Some modules offer variables in braces, replaced when the message is sent. Click a variable in the editor to copy it. Examples:

| Variable | Replaced by |
|---|---|
| `{user}` | the member's mention |
| `{username}` | their username |
| `{server}` | the server name |
| `{memberCount}` | the member count |
| `{user.avatar}` | the avatar URL (usable as an image) |

Each module's article lists its own variables.

## Plan limits

The Free plan limits some items (for example 5 saved embeds or 1 form). The counter shows next to the create button. See [Premium](/docs/premium) and [the plans](/pro).
