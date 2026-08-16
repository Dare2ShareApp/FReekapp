# FReek — Brand + UX Refresh 2.1

## What changed
- Exact approved FReek mascot is now the master mascot asset.
- Exact approved FReek wordmark is now used as the app logo everywhere.
- Main screen simplified to: **CREATE FReek → ID box → JOIN FReek**.
- Shared join links still auto-fill the 6-digit ID.
- Session/player naming moved into a single, simple in-app start sheet instead of browser prompts.
- Branding is consistent across home, sessions, game, chat, wheel, receiving and waiting states.
- Mascot and rotating FReek phrases add personality without forcing one rigid tagline.
- Notifications no longer throw a blocking browser error; availability/permission state is shown cleanly.
- Reconnect/state recovery strengthened for returning from lock/background/another app.
- Chat/session state is synchronized again after reconnect.
- Photo selection remains automatic after 3+ items; no READY button.

## Important platform limitation
A GitHub Pages browser app cannot keep a live WebRTC connection running while iOS has fully suspended the page. FReek now reconnects and restores state automatically when the user returns. True locked-screen remote notifications require a push-notification backend/service (APNs/Web Push); this static beta does not pretend otherwise.

## Upload
Upload the complete folder contents to GitHub Pages.
