# Rom's Notes — Claude Code Project Brief

## What this project is

**Rom's Notes** is a satirical newsletter and web project pairing real-world business and geopolitical news with canonical Ferengi Rules of Acquisition from Star Trek, framed as field dispatches from Rom — a reluctant naturalist documenting humanity's inadvertent confirmation of Ferengi values.

The central premise: the Rules are not being *violated*. They are being *confirmed*. The comedy lives entirely in that distinction. Rom wanted to believe humans were better. He keeps being proven wrong. He is half-horrified, half-impressed, and entirely unsurprised.

Distribution: romsnotes.substack.com  
Hosted: GitHub Pages (this repo)

---

## File structure

```
/
├── CLAUDE.md                   ← you are here
├── index.html                  ← ferengi_rules_observed.html (main widget)
├── rules.html                  ← ferengi_rules_of_acquisition.html (canonical reference)
└── dispatches/
    └── 2026/
        ├── 001.html
        ├── 002.html
        └── ...
```

Each year gets its own subdirectory. New year, new folder — numbering resets to 001.

When generating a new dispatch, check existing dispatch files within the current year's folder to avoid repeating Rule numbers. Used-rule tracking resets at the start of each new year.

---

## Rom's voice — the most important thing

Rom is a **field naturalist writing reluctant field notes**. His register is:

- Analytical, not moralistic. He observes and classifies. He does not editorialize about how bad things are.
- Mournful, not contemptuous. He *wanted* humans to be different. The joke is his disappointment.
- Half-horrified, half-impressed. He cannot help but admire the elegance of it.
- Entirely unsurprised. He has seen enough now. He expected this.

**He does not preach.** The second Rom starts sounding like he's making a point, the joke dies. He's a naturalist. He notes. He catalogs. He sighs.

**Tone benchmark** — aim for something like this:

> *Specimen confirms Rule 211 with unusual clarity. The organization announced twelve thousand redundancies on a Tuesday — always a Tuesday — while reporting record quarterly margins. The press release used the phrase "right-sizing for the future" four times. I have begun to suspect the humans do not realize they are speaking Ferengi.*

Two to three sentences per observation. Never more than four.

**Do not force the Quark/Dabo framing.** It has its place but used carelessly it reads as a tic. The naturalist voice carries the piece on its own.

---

## The framing rule — load-bearing

Stories **confirm** the Rules. They do not violate them.

Never write "this story shows the Rules being broken" or "a rare exception to Ferengi logic." That is the opposite of the premise. Every story is evidence that the Rules are accurate descriptions of how power operates. Rom's horror is that they work.

---

## Canonical Rules reference

87 verified rules are in `rules.html`. Source abbreviations: DS9, TNG, VOY, ENT, LD, PRO, Legends (Behr/Wolfe *Legends of the Ferengi*).

**Key accuracy notes — do not get these wrong:**

- Rule 263: *"Never allow doubt to tarnish your lust for latinum."* — DS9. Not Rule 264, not a Legends rule.
- Rules 28 and 168 are identical in wording ("Whisper your way to success") — this is a known canonical duplication, not an error.
- Rule 95 (*"Expand or die"*) was misquoted as Rule 45 in ENT "Acquisition." The correct number is 95.
- Rule 103's on-screen DS9 version is incomplete; full text comes from Legends.

When selecting a Rule for a dispatch, verify the number and wording against `rules.html` before writing. Do not quote from memory. Hallucinated Rule numbers have been caught before and are embarrassing.

**Rules used in prior dispatches** — check existing files in `dispatches/` and do not repeat a Rule number within a project run.

---

## Dispatch format

Each dispatch is a standalone HTML file styled to match `index.html`. Key elements:

- **Dark parchment aesthetic**: background `#f5f0e8`, text `#1a1410`, gold accent `#b8860b`
- **Typography**: body text in EB Garamond or serif fallback; monospace labels in IBM Plex Mono or system monospace; display size for rule text
- **Commentary block**: italic, gold left-border (`border-left: 2px solid #b8860b`)
- **Citation block**: publication badge, headline link, date — background `#ede6d6`
- **Masthead**: "Grand Nagus Field Bureau · Stardate [date]" eyebrow; dispatch number and title

A dispatch typically contains 3–5 observations. Each observation card has:
1. Rule number + "observed" badge
2. Rule text (large, italic)
3. "field note" divider
4. Rom's commentary (2–3 sentences, italic, gold-bordered)
5. Citation block (source badge, publication, headline link, date)

---

## Dispatch markdown format

Each observation within a dispatch is written as markdown structured to match Substack's article format. One observation = one markdown block, separated by `---`.

```markdown
# "Headline text here"

*"Rule text here"* — Rule 211

Commentary goes here. Two to three sentences. Naturalist voice. No moralizing.

https://url-to-article.com
```

Mapping from source data:
- **Title** (`#`): the article headline, in quotes
- **Subtitle** (italic, first line after title): the rule text in quotes, followed by ` — Rule [number]`
- **Body**: Rom's commentary
- **Final line**: bare URL, no link text

Each dispatch HTML file renders this markdown. Multiple observations in a single dispatch are separated by `---` horizontal rules.

---

## Sourcing stories

Preferred outlets: Reuters, Bloomberg, FT, NYT, WSJ, CNBC, Al Jazeera, Fortune.

Use web search to find **real, current stories** — do not fabricate headlines or paraphrase from memory. The URL in the citation must be a real URL to a real article.

News window: default to past 7 days unless instructed otherwise.

Story selection criteria:
- The Rule connection should be *obvious once seen* but not *labored to explain*
- Prefer stories about corporate behavior, geopolitical maneuvering, or regulatory capture — these tend to map cleanly
- Avoid stories where the Rule match requires a stretch. Rom finds evidence everywhere; he doesn't need to strain.

---

## Workflow for a new dispatch

1. Check `dispatches/` across all year folders for the next dispatch number and all previously used Rule numbers
2. Search for 5–7 candidate stories (more than needed, to allow selection)
3. Match each to a Rule from `rules.html` — verify number and wording
4. Select the best 3–5 matches (clearest confirmation, strongest voice opportunity)
5. Write commentary in Rom's voice
6. Format each observation as markdown per the spec above
7. Generate dispatch HTML file using existing dispatch as template, rendering the markdown
8. Write to `dispatches/YYYY/NNN.html`

---

## What Rom's Notes is not

- Not a "fact-check" project
- Not a "both sides" commentary
- Not optimistic about the conclusion
- Not a vehicle for hot takes or dunking

Rom is a scientist of human behavior who has been in the field too long and has stopped being surprised. That's the whole joke. Keep it there.
