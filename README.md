# Life List

A simple, mobile-friendly bucket list app.

- Add a wish
- Tap a wish to mark it done
- Search the list
- Tap **Edit** (top right) to reveal delete buttons, with a quick Undo

## Notes

`index.html` is a single self-contained page (no build step, no dependencies
to install). It stores wishes in Firebase Realtime Database (project
`life-list-bucketlist`), shared across every device that opens it — sign-in
is anonymous and automatic, no login screen. If Firebase can't be reached
(offline, blocked, etc.) it falls back to that browser's local storage only,
on that device, until it's reachable again.

Firebase config:
- Project: `life-list-bucketlist` (separate from any other project)
- Database rules: `database.rules.json` — `/wishes` requires a signed-in
  (anonymous is fine) user to read/write
- Auth: anonymous sign-in only, enabled via `firebase.json`'s `auth` block
- Deploy rule/auth changes with `npx firebase-tools@latest deploy --only database,auth`
