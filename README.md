# FReek Beta 2.0

- Simplified main Join flow.
- Connected sessions hide Copy/Share.
- Individual sessions no longer show the global session list.
- Game, FReek decision, received media, and chat are contained in the active session.
- Received FReeks are near the top of the session.
- Old Build your FReek pool + READY workflow is replaced by a compact photo chooser that automatically marks the player ready after 3+ items.
- Browser privacy still requires the user to choose camera-roll media.
- FR PEEK / EEK SNEEK owner preview uses a FileReader-first renderer so the selected picture is visible before the decision.
- Received media renders in-app.
- YOU GO FIRST / THEY GO FIRST are removed.
- The shared wheel is the only first-turn selector. Player 1 controls it; both phones see the same spin/result.
- Selected media is stored in IndexedDB.
- PeerJS reconnection is attempted after visibility/focus/pageshow and connection close.
- Notification UI detects iPhone/Safari limitations instead of reporting unsupported notifications as simply OFF.

## Platform limitation
GitHub Pages + PeerJS cannot guarantee a live WebRTC data channel while iOS has fully suspended or killed the page. Reconnect is best-effort.

True locked-screen remote notifications require a push-notification backend/service-worker subscription system. PeerJS alone cannot wake a suspended/killed iPhone web app.
