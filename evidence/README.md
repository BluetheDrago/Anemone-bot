# Evidence — Server Members intent application

Screenshots for the privileged-intent review of **Anemone** (application ID 1513739696599990293).
This folder is the public, non-expiring host the form's evidence links point at. Every image is a capture of
the running product or of Discord's own developer portal — no mockups, no rendered diagrams.

The rule for the set: show the bot **doing the job**, not a list of what it could do. A reviewer has to see the
member walk, the thresholds it acts on, the role arriving on a real member, and the commands as people use them.

## The shots

| file | what it must show | why it earns its place |
|---|---|---|
| `01-syncmigrate-walk.png` | `/syncmigrate` in AI Sponge: Rehydrated, mid-run or finished, with the member count it walked and the roles it changed | the only code path that iterates the guild member list (`guild.members`, `cogs/roles.py:330`) — the entire justification for the intent |
| `02-levelrole-list.png` | `/levelrole list` in the same server: the level-to-role thresholds actually configured | the mapping the walk acts on, in the server where it acts |
| `03-role-landing.png` | a member's level-up post and the reward role arriving on them, before/after visible in the member panel | the product working end to end for a real person |
| `04-commands-in-action.png` | a real channel with the bot answering several commands in a row — `/level` returning a rank card, `/leaderboard`, `/customize` — exactly as members see them | replaces the abstract "38 commands registered" list with the surface in use |
| `05-portal-permissions.png` | Dev Portal → the app's Bot tab: the privileged intent toggles **and** the bot's granted permissions (Manage Roles) in the same page | the practical half of the portal: not just which intent, but what the bot is permitted to do with the member list |

Optional sixth, only if it is easy: `/resync` restoring a rejoined member's roles from their stored level.

## Rules for the links

- Public URL, no sign-in, no expiry. Discord CDN links (`cdn.discordapp.com`, `?ex=` parameters) are not
  acceptable — they expire and the reviewer gets a 404 weeks later.
- One link per shot, pasted into the form's evidence field.
- Each link opened once while signed out, before submitting.
- Filenames `NN-what-it-shows.png`: lowercase, hyphens, no underscores.
