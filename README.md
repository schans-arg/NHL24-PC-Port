# NHL 24 on PC (experimental source patch)

This repository provides a source patch for the open-source HajDEO/nhl24pc compatibility runtime. It does not contain NHL 24, PS4 firmware, an update package, saves, or game assets. Provide your own legally obtained game dump; do not upload game files or saves here.

## Status

The local experimental build completed a full three-period Play Now match and launched from its desktop shortcut. Career/Be A Pro saving and reload remain unverified. In manual play, Career scenes advanced after shader-compiler fixes, but match rendering was corrupted, performance was around 20 FPS, and exiting a match/replay could freeze. The project is not ready to describe as fully playable.

## Apply the current patch

The patch was captured against HajDEO/nhl24pc commit `bef7999707db27884cabe5780f301c4a5d2abdc8` (the source fork is GPL-2.0; preserve its license and notices). Clone that source at the exact base commit, then apply `patches/nhl24pc-port.patch`. See `docs/PORT_STATUS.md` for known gaps and release requirements. This is a code patch; it does not include a runnable emulator package.

## Download the experimental Windows build

The first [Release](https://github.com/schans-arg/NHL24-PC-Port/releases) provides a separate Windows runtime ZIP and a complete local source archive. Extract the runtime ZIP, open `NHL 24.exe`, and select `eboot.bin` from your own extracted CUSA37933 base v01.00 copy. No game files are supplied. Update 1.60 is not supported by this preview. The portable launcher creates a new local profile; it does not include the project owner's saves, paths, logs, keys or caches.

The runtime is the modified MinGW build from October 17, not the older initial upstream executable. Known rendering corruption, low performance and exit/replay freezes remain; full Career save/reload is unverified. This is a community preview. The complete source ZIP attached to the Release contains the modified runtime tree, available submodule sources, launcher source and build directions. GitHub's automatically generated source archive contains this patch repository only.

## Contributing

Useful reports include game edition/update, Windows build, CPU/GPU/driver, exact steps, and sanitized logs. Do not attach a game dump, save, account information, or logs with personal file paths.

## Attribution and trademarks

This is an independent community project and is not affiliated with EA or Sony. NHL and EA SPORTS marks belong to their owners. The compatibility-runtime source remains under the license and notices in its upstream repository.
