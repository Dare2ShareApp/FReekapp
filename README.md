# FReek Beta 0.2

This is the hand-out beta for testing the core two-phone FReek experience.

## What testers can do
1. Create or join a FReek.
2. Select a personal photo/video pool.
3. Pick a number.
4. The other phone resolves that number locally.
5. Choose FR PEEK to send the real item.
6. Choose EEK SNEEK to secretly choose one of three different items.
7. Repeat numbers and try to catch the other player.

## Important beta notes
- This is a web/PWA beta, not the final App Store/Google Play build.
- A browser cannot silently index the entire iPhone/Android photo library, so testers select the media pool for the game.
- Media is sent peer-to-peer in this beta using WebRTC/PeerJS.
- Beta transfer limit is 14 MB per item.
- EEK SNEEK shows a simulated $0.99 unlock; no real payment is taken.
- Production still needs native camera-library integration, hardened signaling/backend infrastructure, push notifications, real in-app purchases, moderation/reporting, analytics, reconnection handling, privacy/retention controls, and final store compliance.

## Put it online
Host these files on any HTTPS static host (GitHub Pages, Netlify, Vercel, etc.). Then share the HTTPS link with testers.

## Test script
- Use two phones.
- Create on Phone A and join on Phone B.
- Both select at least 10 items.
- Pick #7.
- On Phone B try FR PEEK.
- Repeat #7 and try EEK SNEEK.
- Pick #7 again.
- Close/reopen the browser, switch apps, use weak Wi-Fi/cellular, test photos and videos.
- Record every confusing moment or failure.
