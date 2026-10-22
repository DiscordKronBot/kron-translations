---
title: Games
category: modules
emoji: 🎮
summary: Tic-tac-toe, connect four, hangman, Wordle, blackjack, trivia and more, with bets and a leaderboard.
order: 21
---

The **Games** module adds the **/game** command: each game is played in an interactive card, with buttons and menus.

## The games

| Game | Command | How |
|---|---|---|
| ❌ Tic-tac-toe | `/game tictactoe` | against a member, or against Kron if you pick nobody |
| 🔴 Connect four | `/game connect4` | same, Kron blocks your winning moves |
| 🪢 Hangman | `/game hangman` | pick letters from the menus, 6 mistakes allowed |
| 🟩 Wordle | `/game wordle` | find the 5-letter word in 6 tries |
| 🃏 Blackjack | `/game blackjack bet:100` | hit, stand or double against the dealer |
| 🪙 Coin flip | `/game coinflip` | with an optional bet |
| ✊ Rock paper scissors | `/game rps` | against Kron |
| 🧠 Trivia | `/game trivia` | one question for the whole channel, first right answer wins |
| 🔢 Guess | `/game guess` | a number from 1 to 100 in 7 tries |
| 🎲 Dice / 🎱 8ball | `/game dice`, `/game 8ball` | for fun |

Words and questions follow the server language (French or English).

## Bets and rewards

Bets (blackjack, coin flip) and **coins per win** use the currency of the [Levels and economy](/docs/niveaux) module: turn the economy on for them to work. The maximum bet is set in the dashboard.

## Counting

A channel where members count together: **1**, **2**, **3**… one number per message.

- A right number gets ✅.
- A wrong number gets ❌ and Kron reminds everyone of the next number: the count keeps going, it does not start over.
- A member cannot count **twice in a row**: someone else has to play first.
- Messages that do not start with a number are ignored (chatting is fine).

In the dashboard, **Counting** section: pick a channel or click **🔢 Create** (name and emoji editable; Kron suggests your games or community category). The current count and the record show there.

## Settings

- **Available games**: untick a game to remove it from the server.
- **Game channels**: limit games to some channels (empty = everywhere).
- **Top players**: the wins leaderboard. `/game stats` shows a member's stats.
