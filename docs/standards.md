# Recomp Standards

What makes a recomp easy to play, wherever players get it from. Nothing here is required to be listed on RecompLauncher. These are the things players trip over most, and most of them are small changes.

## The basics

**Never ship game files.** No ROMs, disc images, extracted assets or keys. Players bring their own copy.

**Accept the formats people actually have.** Most backups are packaged files, not the extracted folders a recomp is often first written for. Support the standard packaged formats where they apply:

| Console | Accept |
| --- | --- |
| PS1 | CHD, BIN/CUE, ISO |
| PS2 | CHD, ISO |
| PSP | CHD, ISO, CSO |
| PS3 | a decrypted ISO, or the game folder (PS3_GAME) |
| PS4 | the dumped game folder (CUSA…), or a fake-signed PKG |
| PS5 | the dumped game folder (PPSA…) |
| PS Vita | a decrypted dump: VPK or the game folder (PCSA…, PCSE…) |
| Dreamcast | CHD, GDI |
| Saturn, Sega CD / Mega CD | CHD, BIN/CUE |
| TurboGrafx-CD / PC Engine CD, Neo Geo CD | CHD, BIN/CUE |
| 3DO, Amiga CD32, Philips CD-i | CHD, BIN/CUE |
| GameCube, Wii | RVZ, ISO, GCZ (and WBFS for Wii) |
| N64 | .z64, .n64 and .v64 (any byte order), zipped |
| NES, SNES, GB, GBA, DS | the ROM, or zipped |
| Switch, Switch 2 | NSP, XCI and NUP, not only extracted exefs/romfs |
| Xbox | ISO (XISO), or an extracted folder |
| Xbox 360 | ISO, or an extracted folder with default.xex |

CHD is the format most disc-based backups come in, and the one players ask for most. Reading it is a small library ([libchdr](https://github.com/rtissera/libchdr), BSD licensed).

**Prefer files players can read directly.** Where a decrypted dump exists (a decrypted PS3 ISO, a dumped PS4 or PS5 folder, a decrypted Vita game), accept it as is. Then your recomp doesn't have to ship decryption code or keys, and players don't have to run a separate tool before they can play. Only reach for decryption when there's no other way, and never ship keys.

**Check the copy, then say what's wrong.** If you know the good dumps (from [Redump](http://redump.org) or [No-Intro](https://no-intro.org)), check against them. When a file is wrong, say why in one line ("This is the PAL version. The recomp needs the USA one.") instead of crashing later.

**Let the game's location be passed in.** A `--game <path>` option (a file or a folder) means launchers, scripts and Steam shortcuts can start your recomp without anyone moving files around. Keep your own picker for everyone else.

## Releases

- **Tag every release with a version** (`v1.2.0`) and attach the builds to the GitHub release, not just to the README or Actions.
- **One file per platform, with a name that says what it is**, the same way every time: `yourgame-1.2.0-windows-x64.zip`, `-linux-x86_64.AppImage`, `-macos-arm64.zip`.
- **Build for Linux and Mac too** when you can. A lot of players are on Steam Deck.
- **Say what changed** in the release notes, even in one line.

## On the player's PC

- **Portable when it can be.** If the folder next to the exe is writable, keep saves, settings and logs there. Otherwise use the usual per-user folder, and say where in the README.
- **Settings in a file a person can read**: TOML, INI or JSON, with every option written out and commented. Don't hide settings in the registry.
- **Logs in a known place**, kept for the last few runs, so players can send them when something breaks.
- **Controllers through SDL**, with buttons that can be remapped and a sensible default for Xbox, PlayStation and Switch pads.
- **No admin rights, no installer required.** Unzip and play.
- **Don't download anything at first start** without asking.

## Extras that players notice

- **[recomplauncher.json](guide.md)**: one-click setup and your settings on the game's page in RecompLauncher.
- **[Recomp Achievements](https://github.com/elripalda/RecompAchievements)**: achievements, Beaten and Mastered, leaderboards.
- **A "Get it on RecompLauncher" badge** in your README, from the [press kit](https://recomplauncher.com/press).
- **A short "How to play" at the top of the README**: what copy of the game you need, and where to put it.
