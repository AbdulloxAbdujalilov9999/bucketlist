# Life List

A simple, mobile-friendly bucket list app.

- Add a wish
- Tap a wish to mark it done
- Search the list
- Tap **Edit** (top right) to reveal delete buttons, with a quick Undo

Live version: https://claude.ai/artifact/VW6PSVFPcYHkiKV7EMDhRY

## Notes

`index.html` is a single self-contained page (no build step, no dependencies
to install). Opened inside a Claude Artifact, it stores wishes in a
persistent store shared across devices. Opened anywhere else (e.g. GitHub
Pages), it falls back to that browser's local storage only, on that device.
