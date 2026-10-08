# SEEKER changelog

## 0.4.0-beta.9 (2026-10-08)

Conversation tracking: see what you replied to and who answered, without opening your mail app.

- The inbox is organized by stage: To answer, Waiting, They replied, Closed, and Apply on website.
- After each reply SEEKER confirms it in the sending mailbox's Sent folder ("In Gmail Sent" / "In iCloud Sent"), or warns you if it cannot find it.
- Every Sync checks your replied conversations. Recruiter answers move to They replied, are marked New, and show inside SEEKER as a conversation.
- Replies you send from Gmail, Mail, or Outlook are detected and tracked too.
- Conversations with no answer for 21 days close automatically; a later reply reopens them.
- Sync now works with only an iCloud mailbox connected.

## 0.4.0-beta.8 (2026-10-07)

Gmail sign-in and Mac install fixes (replaces 0.4.0-beta.7, which was withdrawn before release).

- Gmail now always signs in as SEEKER by ACAS Tools. A mailbox connected in an early beta with your own Google client file shows "Reconnect needed": choose Connect Google once.
- The Mac app is self-signed, so macOS no longer reports it as damaged. Approve the first launch with right-click > Open or System Settings > Privacy & Security > Open Anyway.

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
