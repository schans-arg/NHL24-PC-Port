# Port status and release checklist

## Verified

- Play Now completed all three periods in a local test.
- The game started from the desktop shortcut.
- Be A Pro scenes progressed past two shader-related crash points after source changes.

## Known failures / unverified areas

- Be A Pro save/reload has not been validated.
- Manual testing reported approximately 20 FPS, severe scene/ice rendering corruption, and a freeze when leaving the match or replay.
- Controller/audio, broad arena coverage, extended sessions, and multiple hardware/driver combinations remain unverified.
- Do not advertise NHL 24 as fully playable or create a stable release while these are unresolved.

## Before a public tagged release

1. Rebuild from the exact upstream base commit and this patch using documented, reproducible commands.
2. Resolve submodule/license state and preserve upstream notices.
3. Check the patch for personal paths, local logs, screenshots, game data, saves, and binaries.
4. Validate Career save/reload, rendering, performance, and clean match exit on multiple configurations.
5. Publish a pre-release with the known issues and tested game update clearly stated.
