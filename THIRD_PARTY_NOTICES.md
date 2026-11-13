# Third-party notices

Void Trader's own code, ship and station models, sounds (all synthesised in code), icons and
text are original to this project. The PS Vita build (`voidtrader.vpk`) also contains the
libraries below, statically linked. Their full licence texts are in the `licenses/` folder.

## Libraries in the Vita build

| Component | Version | Licence | Copyright | Source |
|---|---|---|---|---|
| SDL2 | 2.32.8 | zlib | Sam Lantinga | https://www.libsdl.org |
| vitaGL | commit 2bdbe89 | LGPL-3.0 | Rinnegatamante | https://github.com/Rinnegatamante/vitaGL |
| vitaShaRK | 1.7 | LGPL-3.0 | Rinnegatamante | https://github.com/Rinnegatamante/vitaShaRK |
| SceShaccCgExt | 1.0.1 | LGPL-2.1 | bythos14 | https://github.com/bythos14/SceShaccCgExt |
| math-neon (libmathneon) | commit 0faab81 | MIT | Lachlan Tychsen-Smith | https://github.com/Rinnegatamante/math-neon |
| taiHEN (stubs) | 0.11 | MIT | Yifan Lu | https://github.com/yifanlu/taiHEN |
| QR Code generator library (C) | commit bcfe1b0 | MIT | Project Nayuki | https://github.com/nayuki/QR-Code-generator |

The QR Code generator (`src/qrcodegen.c`, `src/qrcodegen.h`, unchanged) is compiled into the game
itself, in both the Vita and desktop builds; it draws the pause menu's "Report a bug or idea" code.
The others are the versions in the VitaSDK package set the releases are built with. Each release's
relink kit lists the exact versions for that release in `library-versions.txt`, read from
VitaSDK's package manager by the build itself.

The build also uses the VitaSDK toolchain's C and C++ runtime libraries (newlib and GCC's
libstdc++/libgcc). The GCC runtime is covered by the GCC Runtime Library Exception, so it
places no conditions on the game. VitaSDK's headers and stub libraries are MIT-licensed.

### LGPL libraries (vitaGL, vitaShaRK, SceShaccCgExt) and the relink kit

These are linked statically, as all Vita homebrew is. The LGPL allows that as long as you can
rebuild the game against a modified copy of the library. Void Trader's source code is not
published, so every release comes with a **relink kit** instead (`voidtrader-relink-kit-vX.Y.Z.zip`,
on the same release page as the game), as LGPL-3.0 section 4 and LGPL-2.1 section 6 allow. It holds:

- the game's own compiled code (its object files, as `lib/libvoidtrader.a`), exactly as in the release;
- the link and packaging steps (`CMakeLists.txt`) and a how-to (`README.md`);
- the exact library versions the release was built with (`library-versions.txt`);
- the source code of vitaGL, vitaShaRK and SceShaccCgExt at those versions;
- these notices and the licence texts.

To rebuild: install your modified library into VitaSDK, then run `cmake -S . -B build` and
`cmake --build build` in the kit's folder and install `build/voidtrader.vpk`. The game's build checks
that this works before every release. The game's licence (`LICENSE`) allows modifying the game for
your own use and reverse engineering to debug such modifications, as the LGPL requires.

The licence texts are `licenses/LGPL-3.0.txt` (read together with `licenses/GPL-3.0.txt`, which
LGPL-3.0 builds on) and `licenses/LGPL-2.1.txt`.

## Font

The game's 8x16 text font and the PDF manual's text are made from **DejaVu Sans Mono / DejaVu
Sans**. DejaVu fonts are © Bitstream (Bitstream Vera licence); DejaVu changes are in the public
domain; glyphs from the Arev fonts are © Tavmjong Bah. See `licenses/DejaVu-Fonts.txt`.
https://dejavu-fonts.github.io

## Data

Star positions come from RECONS, "The One Hundred Nearest Star Systems"
(Georgia State University, list of 1 January 2012). https://www.recons.org

## Trademarks

Void Trader is an unofficial fan homage to Elite and Frontier. Elite and Frontier are trademarks
of Frontier Developments plc. Void Trader is not affiliated with or endorsed by Frontier
Developments. PlayStation and PS Vita are trademarks of Sony Interactive Entertainment Inc.;
Void Trader is unofficial homebrew, not affiliated with or endorsed by Sony.

## Made with AI

Void Trader is written with an AI assistant (Claude, by Anthropic): it is "vibecoded".
