# Nested

An infinite dictionary. One word fills the screen, and its definition is printed inside it, forty times smaller. Zoom into any underlined word to find its definition inside that, forever, until you land on a word you've already visited.

**Live:** https://nested-dictionary.vercel.app

It has a night mode, and a very quiet generated soundscape (room tone, a soft note on every dive, a chord when you close a loop) that starts on your first click and mutes with one button.

## Controls

| Input | Action |
|---|---|
| Click / tap a word | fall into its definition |
| Scroll · pinch · `+` `−` | zoom |
| Drag · arrow keys | pan |
| `Esc` · `Backspace` · Out | climb back out |
| `Tab`, then `Enter` | step between words and open one |
| `R` · `H` · `?` | random word · back to "universe" · help |
| `N` · `M` | night mode · sound on/off |

## Files

- `index.html`: the whole piece (inline CSS + JS, no build step)
- `prompt.md`: the prompt that recreates it
- `og.png`, `favicon.svg`, `favicon-32.png`, `apple-touch-icon.png`: share card and icons

Open `index.html` in a browser to run it locally.
