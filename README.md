# RecompLauncher SDK

[RecompLauncher](https://recomplauncher.com) installs PC recomps from their developers' own GitHub releases and keeps them up to date. With the SDK, your recomp can also set itself up from the player's own copy of the game, show its settings on the game's page, and report achievements. Your recomp itself doesn't have to change.

| | What players get | What you add |
| --- | --- | --- |
| **Launch** | Drop in a disc, it's checked and set up, Play starts the game. Shows as Easy Setup. | `inputs` and `start` in `recomplauncher.json` |
| **Settings** | Your video and gameplay settings on the game's page and in Big Picture mode | `config` and `settings` |
| **Preparation** | Your own setup step that runs once before Play | `prepare` |
| **Verification** | A verified badge when the player's copy matches a known dump | `dumps` |
| **Recomp Achievements** | Achievements as they play, Mastered games, leaderboards | The [Recomp Achievements](https://github.com/elripalda/RecompAchievements) library |

The first four all come from one file, `recomplauncher.json`, in your release or your repository. Add the ones your game needs: Launch takes about ten minutes.

## What's here

- **[recomplauncher-agent.md](recomplauncher-agent.md)**: the whole SDK in one file, for your AI coding agent. Drop it in your project and ask it to follow it: it adds RecompLauncher support, fixes the easy Recomp Standards items, adds the badge, and ends with a report of what else would make your recomp better. Always current at https://recomplauncher.com/sdk-files/recomplauncher-agent.md

- [docs/guide.md](docs/guide.md): the full guide, the same one as [recomplauncher.com/sdk](https://recomplauncher.com/sdk)
- [docs/setup-inputs.md](docs/setup-inputs.md): named Easy Setup inputs, for several discs, DLC and the player's keys
- [schema/recomplauncher.json](schema/recomplauncher.json): the JSON schema. Add `"$schema": "https://recomplauncher.com/schema/recomplauncher.json"` to your file and most editors will check it as you type.
- [docs/standards.md](docs/standards.md): Recomp Standards, what makes a recomp easy to play: the file formats to accept (CHD, RVZ, NSP and more), releases, portable mode, settings and logs
- [examples/](examples): three complete files, an Xbox 360 recomp with a settings file, a PS2 recomp with settings passed on the command line, and a four-disc game with optional DLC (named Easy Setup inputs)

## Get listed

[Submit your recomp](https://recomplauncher.com/submit?platform=pc), or get a free [developer account](https://recomplauncher.com/developers?signup=1) to manage your listing, see stats and push updates faster. Questions are welcome on GitHub issues or our Discord.

## License

The guide, schema and examples are MIT licensed: copy whatever you need into your own project. Recomp Achievements has its own license, in [its repository](https://github.com/elripalda/RecompAchievements).
