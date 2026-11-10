# Evidence — Server Members intent application

Screenshots for the privileged-intent review of **Anemone** (application ID 1513739696599990293).
Every image is a capture of the running bot in a real server. This folder is the public, non-expiring host the
form's evidence links point at.

## The images

### `01-syncmigrate-walk.png` — the decisive exhibit

`/syncmigrate` run by the operator in **AI Sponge: Rehydrated** (24,254 members), completed 2026-11-10 23:56,
reply ephemeral:

```
Level Re-Sync Complete
Scanned 24,527   Updated 96   Unchanged 3,332
No matching role 20,811   Role mappings used 26   Skipped (bots) 15
Left the server (untouched) 288
```

Measured against a database snapshot taken immediately before the run: the 96 updated members rose by **289 level
steps in total, largest single rise +10**, **0 members were lowered**, and **0 XP was removed** — the write is a
floor (`apply_level_floor`), so a member already above the tier is a no-op and in-level progress survives.

`01b-syncmigrate-progress.png` is the mid-run frame from the same run: *"125/24527 members scanned…"*.

### The rest

| file | where | what it shows |
|---|---|---|
| `02-levelrole-list.png` | ⚠ bot testing server | `/levelrole list` — only 4 rows (Level 5/10/15/20). Re-take in AI Sponge so it lists the 26 mappings the run above used, or leave it out of the form. |
| `03-levelup-announcements.png` | ♡ gensokyo afterhours | a day of level-up posts: **Congratulations {member}! You reached Level N!** The bot carries that server's nickname "Judgement Bot"; the username is Anemone — same application. |
| `04-commands-in-action.png` | — | `/level` rank card (Level 20, Rank #1, 20,509 total XP) and `/customize` opening the card panel. |
| `05-audit-log-role-changes.png` | AI Sponge: Rehydrated | Audit Log filtered to **Anemone**: 11 "updated roles for <member>" entries with dates. |

## Rules for the links

- Public URL, no sign-in, no expiry. Discord CDN links (`cdn.discordapp.com`, `?ex=` parameters) are not
  acceptable — they expire and the reviewer gets a 404 weeks later.
- One link per image, pasted into the form's evidence field.
- Each link opened once while signed out, before submitting.
