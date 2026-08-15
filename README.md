# FReek Beta 0.5 — Connection Fix

This build fixes the biggest beta problems from 0.2:

- The invite now uses the full PeerJS connection ID inside a shareable URL. The old "last 8 characters" display was not a valid connection code.
- The two players' media counts are synchronized. The picker chooses from the OTHER player's count, not their own.
- Turns are locked. One player picks a number; the owner decides FR PEEK or EEK SNEEK; only after the FReek is delivered does the next turn begin.
- EEK SNEEK no longer randomly sends an item. The owner gets exactly 3 alternative choices and must select one.
- File transfer is chunked and buffered before the recipient renders the file, fixing the blank-media behavior caused by trying to display an incomplete transfer.
- The UI explains whose turn it is and whose pool the number applies to.
- The approved app icon assets are included.

Important beta limitations:
- This is still a browser/PWA beta, not a production App Store build.
- A browser requires the player to select the media pool; production should use native photo-library access.
- PeerJS's public signaling service is used for this beta. Production should use a dedicated backend/signaling service.
- EEK SNEEK displays the $0.99 concept but does not charge real money yet.
- Production still needs authentication, durable rooms, reconnect handling, push notifications, native media permissions, real in-app purchases, moderation/reporting, analytics, privacy/retention controls, and final store compliance.
- Keep test media non-sensitive; this beta is for controlled testing.

Test:
1. Open the host link on Phone A and create a FReek.
2. Tap SHARE INVITE and send the link to Phone B.
3. Phone B opens the link and joins.
4. Both select at least 5 items and tap READY.
5. Phone A starts: Phone B's item count appears. Phone A picks a number.
6. Phone B sees the exact selected item and chooses FR PEEK or EEK SNEEK.
7. EEK SNEEK shows 3 alternatives. Select one and send.
8. Phone A receives the media, then the next turn starts.
9. Repeat the same number in later turns. The point is to see whether the recipient can catch a sneek.


## 0.5 connection fix

The browser now gives PeerJS multiple ICE paths, including the Open Relay TURN service on ports 80 and 443. TURN is specifically designed to relay WebRTC traffic when two devices cannot establish a direct path. This is intended to address the `negotiation-failed` result seen on the iPhone beta.

The Open Relay documentation lists the public test configuration used here and notes that TURN is needed when a direct WebRTC connection cannot be established. This public test configuration is suitable for controlled beta testing, not the final production app. Production should use application-scoped/dynamic TURN credentials and a managed signaling/backend layer.
