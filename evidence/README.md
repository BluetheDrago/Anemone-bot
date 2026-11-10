# Evidence — Server Members intent application

Screenshots for the privileged-intent review of **Anemone** (application ID 1513739696599990293).
This folder is the public, non-expiring host the form's evidence links point at. Files are added as
`NN-what-it-shows.png`; nothing here is generated art, every image is a capture of the running product
or of Discord's own developer portal.

## The shots

| file | what it must show |
|---|---|
| `01-syncmigrate-walk.png` | `/syncmigrate` running in AI Sponge: Rehydrated, with the member count it walked. This is the only code path that iterates the server's member list (`guild.members`), i.e. the only reason the bot needs the intent. |
| `02-levelrole-list.png` | `/levelrole list` in the same server: the level-to-role thresholds actually configured. |
| `03-role-landing.png` | a reward role arriving on a member right after a level-up — the member before and after, or the level-up post with the member's roles visible. |
| `04-resync.png` | optional: `/resync` restoring a rejoined member's roles from their stored level. |

No screenshot of the developer portal is needed: the form's own intent selection is the portal state, and the bot's
live flags (`Server Members` on, `Message Content`/`Presence` off) can be read from the API at any time.

## Rules for the links

- Public URL, no sign-in, no expiry. Discord CDN links (`cdn.discordapp.com`, `?ex=` parameters) are
  not acceptable — they expire and the reviewer gets a 404 weeks later.
- One link per shot, pasted into the form's evidence field.
- Each link opened once while signed out, before submitting.
