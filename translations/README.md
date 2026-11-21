# Translating Void Trader

Void Trader's text lives in one file per language, and anyone can help translate it. Five languages are in the game now. They're **first drafts written by AI**, so some lines will be wrong, stiff or too literal, and a native speaker will spot them at once. Corrections are as welcome as whole new languages.

| File | Language | State |
|---|---|---|
| [`en.json`](en.json) | English | The original, and the template for a new language |
| [`de.json`](de.json) | Deutsch | AI draft, needs a native speaker's check |
| [`es.json`](es.json) | Español | AI draft, needs a native speaker's check |
| [`fr.json`](fr.json) | Français | AI draft, needs a native speaker's check |
| [`it.json`](it.json) | Italiano | AI draft, needs a native speaker's check |
| [`pt-BR.json`](pt-BR.json) | Português (Brasil) | AI draft, needs a native speaker's check |
| [`en.handbook.txt`](en.handbook.txt) | English | The Pilot's Handbook's GUIDE pages, the template for translating them (optional) |

The files here are always the ones in the latest release.

## Three ways to help

**1. Fix a few lines.** Open an issue with the [Offer a translation](https://github.com/Syncriel/void-trader/issues/new?template=translation.yml) form, choose the language and paste the lines with your corrections. You don't need to touch a file.

**2. Correct a whole file.** Open the file above, press the pencil (Edit) button and change what you like. When you're done, choose **Propose changes**: GitHub makes your own copy and sends us a pull request. You don't need git or any tools, just a free GitHub account.

**3. Add a new language.** Open the [Offer a translation](https://github.com/Syncriel/void-trader/issues/new?template=translation.yml) form first and say which language you're starting, so two people don't translate the same one. Then copy `en.json` to a new file named with the language's code (for example `nl.json` for Dutch or `sv.json` for Swedish), translate it and send it as a pull request in the same way.

## The rules of the file

- **Keep the names on the left as they are.** Only change the text on the right of each `:`.
- **Keep `{1}`, `{2}` ...** The game puts a number or a name there, in that order. You can move them within the sentence.
- **A line left as `""` stays in English.** Half a translation is fine: leave the lines you're unsure of.
- **Watch the `_max_` notes.** A `"_max_<name>"` line gives the most letters that line can have on screen. A longer translation is shown in English instead, so keep it short or abbreviate.
- **Button names stay in English** (CROSS, CIRCLE, SQUARE, TRIANGLE, D-PAD, L, R, START, SELECT), as in the Pilot's Handbook.
- **Set `_language`** to the language's name in that language (for example `"Nederlands"`), and add your name or GitHub username to `_translators` if you'd like to be credited. Remove the `"_draft": "AI"` line once the whole file has been checked by a person.
- **Letters:** the game's font has the Western European letters (all of Latin-1, plus Œ, œ and €). If your language needs others (Polish, Czech, Greek, Cyrillic and so on), tell us in the form: the font is built so more can be added.
- Save the file as UTF-8, which GitHub's editor does for you.

A few lines that build plurals (such as "1 tonne" and "2 tonnes") can't be translated yet; that's being fixed next.

## Try it on your Vita

You can see your translation in the game before sending it:

1. Close the game fully (Save & quit, then close it from the LiveArea).
2. With VitaShell, copy your file into `ux0:data/VoidTrader/VoidTrader/lang/` (make the `lang` folder if it isn't there). A file there replaces the game's own file with the same name, and a new code adds a new language.
3. Start the game and choose your language in **Pause > Settings > Language**. If you edit the file again, choosing the language again in Settings rereads it.
4. When you're done, delete your file from that folder, so you get the game's own file again with the next release.

The handbook's GUIDE pages are translated the same way: copy `en.handbook.txt` to, for example, `nl.handbook.txt`, next to `nl.json`.

## What happens next

Every file is checked on our side before it goes in: that it reads correctly, that every `{1}` is kept, and that nothing in your language runs off the screen or over other text in any of the game's screens. We'll reply on your pull request or issue with anything that needs changing.

Accepted translations go into the next release of the game, and then appear here. Because this repository only holds the releases, we close your pull request when the release is out rather than merging it here; your work is in the game all the same. You're thanked by your GitHub username in that release's notes, unless you ask us not to name you.

By sending a translation or correction, you confirm it's your own work and agree that it can be included in Void Trader, edited and given away with the game, free of charge.
