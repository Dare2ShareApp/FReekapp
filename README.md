# FReek Beta 1.8 — Clean Main Screen + Independent Sessions

## What changed

- Removed the splash animation completely. FReek now opens directly to the main screen.
- Kept the existing FReek mascot/logo and blue/pink visual identity unchanged.
- Main screen uses one simple join flow:
  - **CREATE FReek**
  - **6-digit ID**
  - **JOIN FReek**
- A shared invite link automatically fills the session ID; the recipient only needs to tap **JOIN FReek**.
- Manual 6-digit ID entry is supported.
- Creating a session asks for a **session name** and **player name**.
- Session names are clickable in the open-session list.
- Connected sessions hide the extra OPEN/SHARE controls; the session has an **×** close control.
- Sessions remain independent and have their own game/chat state.
- Chat is available inside each session.
- Existing shared-wheel, turn-taking, media-pool, and media-transfer behavior remains in this beta.
- README is updated with each build.

## Current beta flow

**Main screen → Create/Join → Session name + player name → independent game/chat screen.**

Invite flow:

**Share link → FReek opens → ID fills automatically → JOIN FReek.**

## Files to upload

- `index.html`
- `manifest.json`
- `icon-180.png`
- `icon-192.png`
- `icon-512.png`
- `README.md`

## Important

Upload all six files to the same GitHub Pages repository/folder. Do not upload the old `splash.gif`; Beta 1.8 does not use it.
