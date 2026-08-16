# FReek Beta 1.9 — Major UX + Reliability Update

## What changed

### Main screen
- Simplified joining to one clear flow:
  - **CREATE FReek**
  - **6-digit FReek ID**
  - **JOIN FReek**
- Removed the duplicate Join button.
- Open sessions are shown only on the main/session-selection screen.
- Connected sessions no longer show COPY or SHARE.
- Session name is the clickable entry point.
- Each session keeps its own close (×) control.

### Individual FReek session
- The individual session no longer shows the global open-session list.
- Game/turn controls are integrated at the top of the session page.
- Chat stays directly below the game controls.
- Session name and connection status are shown at the top.
- Back to the main session screen is available without ending the session.

### Activity indicators
- A connected session can show **NEW** when it has a new FReek or chat message.
- Opening the session clears its new-activity indicator.
- The indicator still works when device notifications are disabled.

### Notifications
- Added a user-controlled notification permission button.
- Browser/device notification permission can be enabled or denied.
- Foreground/background notification scaffolding is included.
- Device-level notification behavior is ultimately controlled by the browser/OS.
- True locked-screen push notifications require a production push service/service worker backend; this static GitHub Pages beta cannot guarantee that behavior.

### Media previews
- Reworked local image preview to use FileReader/data URLs first, with an object-URL fallback.
- EEK SNEEK previews continue to use local media URLs with fallbacks.
- Received media remains rendered inside the session.

### Lock/background resilience
- Added reconnect attempts when the app becomes visible, focused, or returns through pageshow.
- Both host and guest attempt to restore their PeerJS connection after the browser suspends it.
- Session state remains in memory while the page remains alive.
- A browser/PWA can still be fully terminated by iOS; a static web app cannot guarantee a persistent WebRTC connection while the process is killed.

### Opening
- Added a very short, simple opening screen using the existing FReek app artwork and wordmark.
- No generated/reimagined mascot is used.

## Important beta limitation

FReek currently uses browser WebRTC/PeerJS. For a production App Store release, persistent background/locked-screen messaging needs a real push-notification backend and service worker architecture. Do not treat browser Notification permission alone as guaranteed lock-screen delivery.

## Test checklist

1. Main screen has only one Join button.
2. Create a FReek and give it a session name + player name.
3. Confirm the session name is clickable.
4. Connect a second phone; verify COPY/SHARE disappear.
5. Open the connected session and verify no session list appears inside it.
6. Verify game controls are above chat.
7. Send a chat message and confirm NEW appears on the main session list.
8. Send a FReek and confirm NEW appears and the received image displays.
9. Lock one phone, wait, unlock it, and confirm reconnect attempts happen automatically.
10. Test notification permission ON/OFF.
11. Test FR PEEK and EEK SNEEK previews with several photos.
