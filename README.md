# Anemone

A Discord leveling and progression bot for community servers: XP and levels from participation, reward roles at
admin-defined level thresholds, badges, and a rank card every member can customize.

This repository hosts Anemone's public [privacy policy](privacy-policy.md). The bot's source code is not
published.

## What it does

- **XP and levels** — XP from messages and reactions, with per-server rates, cooldowns, a randomized or fixed
  award range, and a configurable level curve.
- **Reward roles** — a server maps levels to Discord roles. On level-up the bot grants the role for the new level
  and removes the role for the level the member left. Changing a threshold or the curve re-syncs every affected
  member, and `/resync` lets a member restore their own roles after leaving and rejoining.
- **Rank cards** — a rendered card with rank, level, progress bar, badges and total XP. Every member picks their
  own background, geometric pattern, left bar color, text color, gradient, avatar shape and display description.
- **Badges** — progression milestones from message counts, a reaction trigger (another bot reacting to a message
  you posted), with an equip order and a per-server award breakdown. The attachment/embed counters and the
  administrator-configured keyword rewards exist in the code but stay inactive while the Message Content intent is
  off (see below).
- **Boards** — leaderboards for lifetime, weekly and daily periods, and a per-member level-up feed with opt-in
  pings (off by default).

## Commands

Everything is a slash command — 38 registered.

| member | |
|---|---|
| `/level` `/leaderboard` `/badges` | progression and boards |
| `/customize` `/color` `/textcolor` `/textgradient` `/background` `/pattern` `/setdescription` `/setemoji` `/levelupemoji` | rank card |
| `/notify` | opt in or out of level-up pings |
| `/resync` | restore the level roles you earned after leaving and rejoining |
| `/contact` `/ping` | operator contact, latency |

| administrator | |
|---|---|
| `/levelrole` `/setconfigrole` `/override` | who may change settings, and the level-to-role map |
| `/xpconfig` `/setlevel` `/addexp` `/removeexp` `/resetuser` `/resetlevels` | XP and levels |
| `/ignorechannel` `/unignorechannel` `/setcommandchannel` `/setlevelchannel` `/seterrorlog` | channels |
| `/levelupmessage` `/botname` `/emoji` `/badgestats` `/syncmigrate` `/migrate` `/syncarcane` `/setcharacter` | presentation and operations |

`/syncarcane` backfills XP from another bot's level-up feed; it is inactive while the Message Content intent is off.

## Privileged intents

Anemone requests **one** privileged intent: **Server Members**, for role synchronisation across a whole member
list. It does **not** request Message Content or Presence.

Stated plainly, because it matters: message text is never read. Three features depend on it and therefore do not
run — keyword badges (a badge earned by writing a configured word), the attachment/embed counters, and
`/syncarcane` (which reads another bot's level-up posts). Everything else — XP, levels, role synchronisation,
message-count and reaction badges, boards and the full rank card — works without the intent.

## Data

Anemone keeps a progression record keyed by user ID and server ID: XP, level, message and reaction counts, badge
awards, rank-card cosmetics, and each server's settings. There is no column holding message text.

No third-party services, no analytics, no advertising, no data sharing. The only outbound requests are to
Discord's own CDN, for avatars and custom emoji images at render time; those are held in a bounded in-memory
cache and never written to disk.

Members and server administrators can request a copy or deletion of their data with `/contact`, or by email to
**Dragohomestudios@gmail.com** — the operator's public mailing address. The full policy is in
[privacy-policy.md](privacy-policy.md).
