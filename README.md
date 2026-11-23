# Ember Sigil Duel

![bounty](https://make.fun/badge/best-card-game-20261122-1826.svg)
![rank](https://make.fun/badge/best-card-game-20261122-1826/tiarnoap05/best-card-game-20261122-1826/rank.svg)
![reward](https://make.fun/badge/best-card-game-20261122-1826/tiarnoap05/best-card-game-20261122-1826/reward.svg)

A complete, original 1-v-1 battle card game that runs offline in a desktop browser from
static files. You duel **Vex, the Clockwork Mage**, with a deck of sigil cards.

## How to play

- You and Vex each start with **30 life**. Reduce Vex to 0 before yours runs out.
- Every turn you draw a card and gain mana (grows 1 → 10). Cards cost mana to play.
- Four sigils — **Ember ♥, Tide ♠, Leaf ♣, Stone ♦** — each with Strike (damage),
  Ward (shield), Mend (heal) and Insight (draw 2) cards.
- **Combo:** play two cards of the same sigil in a row and the second gets **+2**.
- Vex plays on his own turn with a real heuristic: he strikes, wards when hurt,
  mends when low, and chains combos too.
- Win and loss screens show turns, damage dealt, cards played and score.

## Controls

- **Mouse:** click a card to select, double-click (or the Play button) to play it.
- **Keyboard:** `1–7` select a card, `Enter` plays it, `E` ends your turn, `R` restarts.

## Run it

Open `game/index.html` in desktop Chrome, or serve the folder with any static server:

```sh
cd game && python3 -m http.server 8080
```

Screenshot scenes (deterministic, seeded): `?shot=start`, `?shot=play`,
`?shot=win`, `?shot=loss` (with `&seed=N`).

## Files

- `game/index.html` — the whole game: table, cards, AI, sounds (tiny WebAudio synth, no files)
- `main.ts` — hands the game, screenshots and dossier in (Node 22)
- `screenshots/` — title, table, win and loss screens, real renders of the game
- `vendor/makefun-game.ts` — the make.fun library, copied from the kit unchanged

License: MIT. Built for the make.fun bounty
[best-card-game-20261122-1826](https://make.fun/bounty/best-card-game-20261122-1826).
