---
title: AutoMod
category: modules
emoji: 🤖
summary: Block banned words, regexes, spam, mass mentions and shady names with Discord's AutoMod.
order: 13
---

The **AutoMod** module sets up Discord's built-in AutoMod from the dashboard. Rules are enforced by Discord itself: a blocked message is never posted, and it all works even when Kron is offline.

## Setup

1. Turn on the **AutoMod** module in the dashboard.
2. Pick a **ready-made rule** (Discord invites, links, slurs, spam, mass mentions, names) or create an empty rule.
3. Adjust the words, actions and exemptions, then click **Save** at the bottom.

> [!IMPORTANT]
> Kron needs the **Manage Server** permission to create and edit rules. Discord requires it for any AutoMod management.

## Rule types

| Type          | What it blocks                                  | Maximum |
| ------------- | ----------------------------------------------- | ------- |
| Keywords      | words (with `*`) and regexes | 6 rules |
| Discord lists | profanity, sexual content, slurs                | 1       |
| Spam          | messages Discord deems suspicious               | 1       |
| Mass mentions | too many mentions in a message                  | 1       |
| Names         | member names and profiles                       | 1       |

The maximums are Discord's. Rules created directly in Discord show up in the dashboard too and can be edited there.

## Words and regexes

- One word per line. `*` means "anything": `*cat*` also catches "concatenate", `cat` alone only catches the whole word.
- Regexes use Rust syntax. Example for invites: `(discord\.gg|discord\.com/invite)/\w+`
- **Exceptions** never trigger the rule, even if they contain a banned word.

## Actions

- **Block the message**: it is not posted. You can show a short message to the author.
- **Alert staff**: Discord posts an alert with the message in the chosen channel.
- **Time out** the author (keywords and mentions only), from 1 minute to 1 week.
- **Name** rules stop the member from chatting while their name breaks the rule.

## Exemptions

Each rule can ignore up to 20 roles (usually staff) and 50 channels (for example a link-sharing channel).

> [!TIP]
> Turning the module off pauses the rules Kron created. Turning it back on resumes exactly those.
