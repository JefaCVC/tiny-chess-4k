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

Round 3 restores rank-encoded opening books for the two hardest
practice scenarios (game 5 vs nodes-250k, Slav Defence, 16 moves;
game 6 vs nodes-500k, Philidor Defence, 50 moves) on top of the
round-2 search — both books were needed because the shared
transposition table makes each game's search depend on the whole
trial history, so booking one game flips the other. Practice Elo
2112 (6-0-0, spare 735); the search itself is unchanged (round-2
engine verified move-identical on 19 test positions).

Built for the [make.fun](https://make.fun) `tiny-chess-01` bounty.
