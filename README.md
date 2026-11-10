# RecompLauncher SDK

[RecompLauncher](https://recomplauncher.com) installs PC recomps from their developers' own GitHub releases and keeps them up to date. With the SDK, your recomp can also set itself up from the player's own copy of the game, show its settings on the game's page, and report achievements. Your recomp itself doesn't have to change.

| | What players get | What you add |
| --- | --- | --- |
| **Level 1: Plays from RecompLauncher** | Drop in a disc, it's checked and set up, Play starts the game. Shows as Easy Setup. | `game` and `start` in `recomplauncher.json` |
| **Level 2: Settings in the launcher** | Your video and gameplay settings on the game's page and in Big Picture mode | `config` and `settings` |
| **Level 3: Full setup** | Your own setup step, and a verified badge for clean dumps | `prepare` and `dumps` |
| **Recomp Achievements** | Achievements as they play, Mastered games, leaderboards | The [Recomp Achievements](https://github.com/elripalda/RecompAchievements) library |

Levels 1 to 3 all come from one file, `recomplauncher.json`, in your release or your repository. Level 1 takes about ten minutes.

## What's here

- [docs/guide.md](docs/guide.md): the full guide, the same one as [recomplauncher.com/sdk](https://recomplauncher.com/sdk)
- [schema/recomplauncher.json](schema/recomplauncher.json): the JSON schema. Add `"$schema": "https://recomplauncher.com/schema/recomplauncher.json"` to your file and most editors will check it as you type.
- [examples/](examples): two complete files, an Xbox 360 recomp with a settings file and a PS2 recomp with settings passed on the command line

## Get listed

[Submit your recomp](https://recomplauncher.com/submit?platform=pc), or get a free [developer account](https://recomplauncher.com/developers?signup=1) to manage your listing, see stats and push updates faster. Questions are welcome on GitHub issues or our Discord.

## License

The guide, schema and examples are MIT licensed: copy whatever you need into your own project. Recomp Achievements has its own license, in [its repository](https://github.com/elripalda/RecompAchievements).
