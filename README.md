# Daig's Japanese Conjugation Drill

A personal fork of the Japanese verb/adjective conjugation drill, kept for
ongoing study and development.

**Run it:** open `conjugation/drill.html` in a browser. No build step.

---

## Credit — this is not original work

Effectively all of the conjugation engine, rules, vocabulary and UI below are
other people's work, not mine:

| | |
|---|---|
| **Don** ([@wkdonc](https://github.com/wkdonc)) | Created the original **Don's Japanese Conjugation Drill** — the conjugation engine, rules and UI. [Site](https://wkdonc.github.io/conjugation/drill.html) · [Repo](https://github.com/wkdonc/wkdonc.github.io) · [WaniKani thread](https://community.wanikani.com/t/dons-japanese-conjugation-drill/17384) |
| **Landon** ([@LandonJPGinn](https://github.com/LandonJPGinn)) | Extended it substantially — more verbs, more conjugation forms, more helper verbs, adjectives, decoupled word DB, redesign. [Site](https://landonjpginn.github.io/jp-verb-quiz/conjugation/drill.html) · [Repo](https://github.com/LandonJPGinn/jp-verb-quiz) |

Further commits in the history from **Maurice Ampt** and **toxinu**.

This repo was duplicated from `LandonJPGinn/jp-verb-quiz` (itself a fork of
`wkdonc/wkdonc.github.io`) **with the full upstream git history preserved**, so
every original author's commits and authorship remain intact and inspectable:

```bash
git log --format='%an' | sort -u     # every contributor, upstream included
```

### Licensing status — read this before doing anything public

**Neither upstream repo carries a license**, which by default means *all rights
reserved*. Practical consequences:

- This copy is **private**, for personal study. Keep it that way.
- **Do not publish, deploy or redistribute** it — no GitHub Pages, no public
  repo — without permission from Don and Landon, or unless they add an explicit
  open-source licence upstream.
- **Do not add a `LICENSE` file here.** We have no right to license someone
  else's work.

If this should ever go public, the clean routes are: ask upstream to add a
licence (e.g. MIT), or fork publicly on GitHub, which the GitHub Terms of
Service do expressly permit.

---

## Changes in this fork

- Rebranded title/header to *Daig's Japanese Conjugation Drill*, keeping the
  credit line to Don and Landon visible in the UI itself.
- Removed `googlee4ee357c76ade084.html` — Landon's Google Search Console
  verification token, personal to him and meaningless here.
- Removed `sitemap.xml` — it pointed at `landonjpginn.github.io`.
- Replaced both links to Landon's personal Google feedback form, so bug reports
  don't land in his inbox.
- Removed the `og:url` meta pointing at Landon's site.

## How to use (from Landon's original notes)

- Set the filters you'd like prompts about, and start.
- The quiz prompts you to conjugate a verb into a specific form.
- Type the conjugation (romaji converts to hiragana as you type).
- It marks you right or wrong, and explains why.

## Layout

| path | what |
|---|---|
| `conjugation/drill.html` | the drill page |
| `conjugation/drill.js` | quiz logic |
| `conjugation/rules.js` · `rules.json` | conjugation rules |
| `conjugation/words.js` · `words.json` | vocabulary database |
| `conjugation/cache.py` | regenerates `count.json` (question-pool counts) from the JSON |
| `todo` | Landon's original roadmap, kept for context |

## Upstream roadmap ideas worth keeping

From Landon's list — still good directions: JLPT-level filtering, filter by most
common verbs, example sentences, sound bytes, performance work as the word count
grows.

## Related

Companion tool in this org:
[jita-drill](https://github.com/Daiwa-Scholars-Two-Thousand-Twenty-VIBE/jita-drill)
— 自他動詞 (transitive/intransitive) pair drill. Original work, no shared code.
