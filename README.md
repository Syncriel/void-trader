# Void Trader

A space trading game for the PS Vita: trade between real nearby stars, fight pirates, mine
asteroids, take missions for the powers and factions of a living galaxy, and dock by hand with
spinning stations. An unofficial fan homage to Elite and Frontier.

**This repository holds releases only.** Download the game from the
[Releases](../../releases) page. The game's source code is not published, and pull requests aren't
accepted.

## Installing

1. Your PS Vita needs homebrew enabled (HENkaku or Ensō) and VitaShell.
2. Download `voidtrader-vX.Y.Z.vpk` from the latest release.
3. Copy it to your Vita (for example over USB or FTP with VitaShell) and install it from VitaShell.
4. Void Trader appears on the home screen. Your saves are kept in `ux0:data/` and survive updates.

The Pilot's Manual (`VoidTrader-Manual-vX.Y.Z.pdf`) is on the same release page, and the game has
a Pilot's Handbook in its pause menu.

## Made with AI

Void Trader is written with an AI assistant (Claude, by Anthropic): it is "vibecoded". Created by
Syncriel & Claude.ai.

## Licences and notices

- The game: free to download, all rights reserved - see [LICENSE](LICENSE).
- The libraries it is built with (SDL2, vitaGL, vitaShaRK, SceShaccCgExt, math-neon, taiHEN) and
  the font and star data: see [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md) and
  [licenses/](licenses).
- Three of those libraries are under the LGPL. Each release has a **relink kit**
  (`voidtrader-relink-kit-vX.Y.Z.zip`) so you can rebuild the game against your own modified
  versions of them; its `README.md` explains how.

## Trademarks

Elite and Frontier are trademarks of Frontier Developments plc. Void Trader is not affiliated with
or endorsed by Frontier Developments. PlayStation and PS Vita are trademarks of Sony Interactive
Entertainment Inc.; Void Trader is unofficial homebrew, not affiliated with or endorsed by Sony.
