# 🥷 Ninja Reader — Belt Quest

A reading game for early readers (about ages 5–7) who like fighting games, snake games,
and ninja turtles. Read the word right, land the hit. Win fights, earn coins,
climb from white belt to black belt.

**One file, no install:** open `index.html` in any modern browser (Chrome, Safari,
Edge, Firefox) by double-clicking it. Works offline. Progress saves automatically
in that browser.

## How it plays

Each belt is a mini-campaign: **2 fighters + 1 boss**. Every correct answer is a
hit on the enemy; every miss is a hit on you. Beat the boss and you are promoted
to the next belt with harder words.

Four question types, weighted toward reading whole sentences:

| Type | What the child does | Skill |
|---|---|---|
| **Find the word** | Hears a word, taps it inside a sentence | Word recognition in context |
| **Which word fits?** | Picks the word that completes a sentence | Decoding + comprehension |
| **Read it** | Reads a word, taps the matching picture | Pure decoding (no audio clue) |
| **Listen** | Hears a word, picks the right spelling | Sound–spelling mapping |

## Belt progression (the reading curriculum)

1. **White** — short vowels, simple sentences
2. **Yellow** — blends (st, tr, cr, fl, sn, gr)
3. **Orange** — magic e (cake, bike, home)
4. **Green** — vowel teams (ai, ea, oa, ee)
5. **Blue** — two syllables and -ing / -ed endings
6. **Purple** — bossy r (ar, or, er, ir, ur)
7. **Brown** — oo, ou, ow, oi, oy
8. **Red** — soft c and g, tricky endings
9. **Black** — long mixed master sentences

## Coins and the shop

Coins come from correct answers (+10, more on a streak) and from winning fights
(+25, +50 for a boss, +100 for a belt). Spend them in the shop on eight ninja
characters, from the starter ninja up to the 1200-coin star ninja.

## Designed to keep a 6-year-old going

- **Nothing is ever timed.** No clock, no pressure to answer fast.
- **A wrong answer always teaches.** The right answer lights up and is read aloud,
  then the whole sentence is read, before the next question.
- **Running out of hearts costs nothing.** You get a "take a breath" screen,
  full hearts, and carry on against the same enemy — no lost progress.
- **A 💡 hint** removes one wrong choice, once per question, for free.
- **🔁 repeats the audio** as many times as he wants.
- Big tap targets, high contrast, no reading required to navigate the menus.

## Grown-up settings (⚙️)

- **Difficulty** — jump straight to any belt if the level is too easy or too hard.
- **Speaking speed** — slow the voice down for a child still sounding words out.
- **Voice** — pick any English voice installed on the device.
- **Progress** — correct/missed counts, accuracy, best streak, coins.
- **Words to practise together** — the words he missed most, for offline practice.
- **Reset progress** — start the whole quest over.

Keyboard shortcuts for a helper sitting alongside: `1` `2` `3` pick an answer,
`R` repeats the audio.

## Getting a natural-sounding voice

Speech uses the voices installed on the device, so quality depends on the
device rather than the game. Apple ships low-quality "compact" voices by
default and keeps the good neural ones as an opt-in download, which is why
the default can sound robotic.

**On iPhone or iPad:** Settings → Accessibility → Spoken Content → Voices →
English → tap a voice (Ava, Evan and Zoe are good) → download the **Enhanced**
or **Premium** version. Reload the game; it prefers those automatically, and
⚙️ Settings → Voice marks them with a ⭐.

The game also filters out Apple's joke voices (Albert, Zarvox, Bubbles and
friends) so the automatic pick can never land on one, and ⚙️ Settings has a
🔈 **Hear this voice** button to audition before handing the phone over.

Tap 🔊 anywhere to mute. The first tap on **PLAY** is what unlocks audio on
phones and tablets — that is a browser rule, not a bug.

## Hosting it privately

The game is a static site: any static host works, and no server, database or
API key is involved. The `_headers` and `robots.txt` files ask search engines
not to index it, so the address is only reachable by someone you send it to.

Easiest route (no GitHub connection, so the URL reveals nothing about your
other projects):

1. Go to **app.netlify.com/drop**
2. Drag the site folder (or `ninja-reader-site.zip`) onto the page
3. It deploys immediately and gives you a URL
4. Claim the site to a free account, then rename it under
   **Site settings → Change site name** to get something like
   `ninja-reader.netlify.app`

Cloudflare Pages (**dash.cloudflare.com → Workers & Pages → Create → Upload
assets**) works the same way and additionally offers **Cloudflare Access** on
its free tier, which puts a real email-based login in front of the site if an
unlisted URL is not private enough.

To ship an update, drag the folder again — or, on a Git-connected site, push.
The service worker is network-first for the page, so returning players pick up
the new version on their next visit.

