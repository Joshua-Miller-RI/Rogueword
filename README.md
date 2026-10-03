# Rogueword

Previously "Roguewordle" (Had to change due to copyright rules)

Live at [https://joshua-miller-ri.github.io/Rogueword/](https://joshua-miller-ri.github.io/Rogueword/)

Guess words, earn gold, buy hints, go again.

## How a run works

You get 5 words, 6 guesses each. After every guess the tiles tell you:

- **Teal**: right letter, right spot
- **Ochre**: in the word, wrong spot
- **Dark**: not in the word

Every word you solve is worth 4 gold. Missing one doesn't end the run, it just doesn't pay.

**Endless** is the other mode. It keeps going until you miss a word.

## Shop

Gold goes toward permanent upgrades. Hints refill at the start of every run.

- **+1 Guess** (30): one more guess on every word
- **Super Hint** (25): shows a letter in its correct spot
- **Positive Hint** (15): shows a letter that's somewhere in the word
- **Negative Hint** (10): shows a letter that isn't in the word
- **Bonus Guess** (17): one extra guess on the current word

Everything except +1 Guess stacks up to 5 levels, one use per run per level.

## Modifiers

Turn these on from the menu if a normal run is too easy. They don't pay extra.

- **Extra word**: 6 words instead of 5
- **Fewer guesses**: 5 instead of 6
- **Boss round**: a 7-letter word at the end (every 5th word in Endless)
- **Timer**: 60 seconds per word

## Running it yourself

The game loads its word lists with `fetch`, so opening `index.html` straight from your files won't work. Serve the folder instead:

```
python -m http.server
```

Then go to http://localhost:8000.

Everything lives in `index.html`. The `.txt` files are the word lists: five-letter words, seven-letter boss answers, and the seven-letter words you're allowed to guess.

Progress saves in your browser's local storage.
