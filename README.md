![Fork the Dictator — punch the tyrant, topple the regime](https://raw.githubusercontent.com/karam2022/fork-the-dictator/main/og.png)

# 👊 FORK THE DICTATOR

A tiny browser game you can fork in 60 seconds. Punch a cartoon tyrant until the
regime topples, a sillier one rises, repeat. Built for **playground.dot** at
Web3 Summit and hosted on a `.dot` domain, so no server can take it down.

**Play:** click the tyrant, or mash **SPACEBAR**. Watch the combos, the growing
black eye, and the confetti when the regime falls.

## Mod this app (please do)
It's one self-contained `index.html`, no dependencies, no build step. Fork it,
open it, make it yours. Good first mods:

- **Swap the face.** The tyrant is an inline `<svg id="tyrantSvg">` near the top
  of the `<body>`. Re-skin it however you want.
- **New regime skins.** Add entries to the `PALETTES`, `TITLES`, and `SURNAMES`
  arrays so each toppled regime looks and sounds different.
- **Your own sound effects.** Edit the `WORDS` array (`POW!`, `BAM!`, `BONK!`...).
- **Go multiplayer.** There's a `Chain.live` adapter stub with four methods.
  Wire it to a shared backend or a contract and the whole room punches one boss.
- **Sound toggle, leaderboard tweaks, mobile polish** — all fair game.

## Deploy your own to .dot
```bash
# 1. Make it moddable: a public GitHub repo must exist first
gh auth login
gh repo create fork-the-dictator --public --source=. --remote=origin --push

# 2. Playground CLI
curl -fsSL https://raw.githubusercontent.com/paritytech/playground-cli/main/install.sh | bash
export PATH="$HOME/.polkadot/bin:$PATH"

pg login        # scan the QR with your phone
pg drip         # grab testnet tokens
pg decentralize --path . --dot forkthedictator --playground --moddable
```

Built with stubborn hope. Code as law, not tyrants as law.
