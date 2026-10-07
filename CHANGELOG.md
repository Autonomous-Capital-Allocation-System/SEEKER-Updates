# SEEKER changelog

## 0.4.0-beta.7 (2026-10-07)

Gmail sign-in and Mac install fixes.

- Gmail now always signs in as SEEKER by ACAS Tools. A mailbox connected in an early beta with your own Google client file shows "Reconnect needed": choose Connect Google once.
- The Mac app is self-signed, so macOS no longer reports it as damaged. Approve the first launch with right-click > Open or System Settings > Privacy & Security > Open Anyway.

## 0.4.0-beta.6 (2026-10-07)

Safety, sign-in and update fixes.

- Install this build by hand once on Mac and Windows: it uses a new update key. Later builds arrive through Check for updates.
- Gmail now signs in through SEEKER by ACAS Tools. Reconnect each Gmail mailbox once after installing.
- iCloud replies are saved in your iCloud Sent folder, and SEEKER never answers the same email twice.
- SEEKER no longer replaces saved mailbox logins it cannot open; it explains how to fix the problem instead.
- Start-up errors show the real reason; SEEKER always restarts cleanly on Windows.
- Listing, Gmail and help links open in your browser.
- iPhone: empty starting profile, no lost edits during sync, no false "interrupted" sends, dismissed items cannot be sent, accented subjects display correctly.
