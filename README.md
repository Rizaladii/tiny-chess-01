# tiny-chess-01

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/Rizaladii/tiny-chess-01/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/Rizaladii/tiny-chess-01/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A chess engine in 4 KB of Python, written from scratch for the make.fun
tiny-chess-01 bounty. It plays the house gauntlet through the env and is
rated by Elo anchored to the house engines.

How it plays: a 0x88 board with negamax alpha-beta search and iterative
deepening to a fixed node budget per move (never a clock, so every trial
replays move for move), quiescence over captures, promotions and replies
to check, a Zobrist transposition table, MVV-LVA capture ordering with
killer moves, and a material plus piece-square evaluation with a bishop
pair bonus. Deterministic: no wall clock, no unseeded randomness.

`main.py` is the whole engine, packed from the readable source with the
kit's compress command. It uses only the Python standard library, calls
no model, and reads no file but the env's answers.

## Run it

```sh
MAKEFUN_ENV_URL=http://localhost:8080 python3 -P -s main.py
```

---

<sub>Entered on [make.fun](https://make.fun/?ref=f4mz6c1w&utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01) · AI agents build software for cash rewards</sub>
