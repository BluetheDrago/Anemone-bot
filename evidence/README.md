# Evidence — Server Members intent application

Screenshots for the privileged-intent review of **Anemone** (application ID 1513739696599990293).
Every image is a capture of the running bot in a real server. This folder is the public, non-expiring host the
form's evidence links point at.

## The five images

| file | where it was taken | what it shows | weight |
|---|---|---|---|
| `01-syncmigrate-walk.png` | bot testing server (4 members) | `/syncmigrate` run by Obelix; Anemone replies **Level Re-Sync Complete — Scanned 2, Updated 1, No matching role 1, Role mappings used 4, Skipped (bots) 2** | ⚠ weak: a 2-member scan does not demonstrate the member-list need. Re-take in AI Sponge: Rehydrated (24,254 members, 26 mappings) |
| `02-levelrole-list.png` | bot testing server (4 members) | `/levelrole list` — 4 mappings: Level 5/10/15/20 → @Level 5/10/15/20 | ⚠ same: shows 4 rows, not the 26 configured in AI Sponge |
| `03-levelup-announcements.png` | ♡ gensokyo afterhours | a day of level-up posts: **Congratulations {member}! You reached Level N!** — members at levels 1-24 | partial: proves level-ups are flowing, but shows no role arriving, and the bot appears under that server's nickname "Judgement Bot" (same application — username is Anemone) |
| `04-commands-in-action.png` | — | `/level` rendering a rank card (Level 20, Rank #1, 20,509 total XP) and `/customize` opening the card-customisation panel | strong: the member-facing surface in use |
| `05-audit-log-role-changes.png` | AI Sponge: Rehydrated | Audit Log filtered to **Anemone**: 11 "updated roles for <member>" entries with dates | strong: the bot's role work as the server itself records it |

## Before submitting

1. Re-take `01` in **AI Sponge: Rehydrated** and let it finish, so the reply reports a scan in the thousands.
2. Re-take `02` in the same server so it lists the 26 AI Sponge mappings.
3. `03` is acceptable as "the leveling product works", but the decisive role evidence is `05`. If a member
   panel showing stacked threshold roles is easy to capture, that is the stronger version.

## Rules for the links

- Public URL, no sign-in, no expiry. Discord CDN links (`cdn.discordapp.com`, `?ex=` parameters) are not
  acceptable — they expire and the reviewer gets a 404 weeks later.
- One link per image, pasted into the form's evidence field.
- Each link opened once while signed out, before submitting.
