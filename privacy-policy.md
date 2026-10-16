# Anemone — Privacy Policy

_Last updated: 17 October 2026_

Anemone is a community leveling bot for Discord: it awards XP and levels for participation, grants reward
roles at configured level thresholds, and lets members customise a rank card.

## What Anemone stores

Keyed by Discord user ID and server (guild) ID, Anemone stores:

- progression: XP, level, coins field, message and reaction counts
- badges awarded, and the character/badge display preferences
- rank-card cosmetics: colours, gradients, background, pattern, avatar shape, display description
- per-server settings: prefix, XP rates, cooldowns, level-to-role thresholds, ignored channels and roles

Anemone does **not** store message content. Message text is not read, stored or logged. Anemone does not
request Discord's Message Content privileged intent.

## What Anemone does not do

- No third-party services, no analytics, no advertising, no data brokers.
- No data is sold, shared or transferred to anyone.
- No message content, attachments, embeds or voice data are used or kept.

The only outbound requests Anemone makes are to Discord's own CDN, to fetch member avatars and custom emoji
images when rendering a rank card. Those images are held in a bounded in-memory cache and are never written
to disk.

## Where the data lives

Data is stored in a private database on the bot operator's own server. It is not hosted with, or shared
with, any external service.

## Retention and deletion

The progression record is kept while Anemone remains in the server where the record was created. A member
can ask for their record to be deleted at any time, and a server administrator can ask for records for
their server to be deleted. Requests are actioned by the bot owner and the records are removed.

Deleting a record removes it; Anemone does not keep a suppression list. If you continue to use Anemone after
your record is deleted (for example by continuing to chat in a server it is in), a new record is created for
you from that point. If Anemone is removed from a server, that server's records can be deleted on request.

## How we share data

Anemone does not share data with third parties: no analytics, no advertising, no data brokers, no selling or
licensing. Nothing is transmitted to Discord beyond the normal operation of the bot (commands, responses and
the images it posts). Member avatars and custom emoji images are fetched from Discord's CDN at render time,
held in a bounded in-memory cache, and never written to disk.

## Your rights

You can ask the bot owner for a copy of the data held about you (for example a readout of your progression
record), ask for it to be corrected, or ask for it to be deleted. Requests are actioned by the bot owner;
see the contact below.

## Children

Anemone is used inside Discord, which requires users to meet Discord's minimum age (13, or older where local
law requires it). Anemone does not knowingly hold data for anyone below that age.

## Contact

Deletion requests, data questions, and reports of any issue or violation relating to Anemone — contact the
bot owner on Discord:

**obelix.gaming** (the Discord account that operates Anemone)

## Changes

If this policy changes, the "last updated" date above changes with it. Continued use of Anemone after a
change means the updated policy applies.
