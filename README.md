# Tiny Chess 4K

[![make.fun · tiny-chess-01](https://make.fun/badge/tiny-chess-01.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![rank](https://make.fun/badge/tiny-chess-01/JefaCVC/tiny-chess-4k/rank.svg)](https://make.fun/bounty/tiny-chess-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)
[![reward](https://make.fun/badge/tiny-chess-01/JefaCVC/tiny-chess-4k/reward.svg)](https://make.fun/bounty/tiny-chess-01?utm_source=github&utm_medium=readme&utm_campaign=tiny-chess-01)

A 4 KB Python chess engine: 0x88 board, negamax with PVS + LMR,
quiescence, transposition table, tapered piece-square eval, null-move
pruning, history heuristic, middlegame check extensions, pawn-shield
king safety and a capped transposition table. Adaptive node budget per
move (80k middlegame / 40k endgame) — fully deterministic, no clock.

Round 2 drops the practice mate book to spend the bytes on search:
fresh-position practice Elo 1809 / 1279 / 1451 (trials 0/1/2, mean
1513, up from 1425).

Built for the [make.fun](https://make.fun) `tiny-chess-01` bounty.
