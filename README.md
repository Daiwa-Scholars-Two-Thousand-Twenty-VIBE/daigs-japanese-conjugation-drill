# Daig's Japanese Conjugation Drill

A fork of the Japanese verb/adjective conjugation drill, for the Daiwa Scholars
to practise on the go.

**▶ Practise:** <https://daiwa-scholars-two-thousand-twenty-vibe.github.io/daigs-japanese-conjugation-drill/conjugation/drill.html>

**Run it locally:** open `conjugation/drill.html` — no build step. (Serve it,
e.g. `python3 -m http.server`, if your browser blocks ES modules on `file://`.)

---

## Credit — this is not original work

Effectively all of the conjugation engine, rules, vocabulary and UI below are
other people's work, not mine:

| | |
|---|---|
| **Don** ([@wkdonc](https://github.com/wkdonc)) | Created the original **Don's Japanese Conjugation Drill** — the conjugation engine, rules and UI. [Site](https://wkdonc.github.io/conjugation/drill.html) · [Repo](https://github.com/wkdonc/wkdonc.github.io) · [WaniKani thread](https://community.wanikani.com/t/dons-japanese-conjugation-drill/17384) |
| **Landon** ([@LandonJPGinn](https://github.com/LandonJPGinn)) | Extended it substantially — more verbs, more conjugation forms, more helper verbs, adjectives, decoupled word DB, redesign. [Site](https://landonjpginn.github.io/jp-verb-quiz/conjugation/drill.html) · [Repo](https://github.com/LandonJPGinn/jp-verb-quiz) |

Further commits in the history from **Maurice Ampt** and **toxinu**.

This is a **GitHub fork** of `LandonJPGinn/jp-verb-quiz` (itself a fork of
`wkdonc/wkdonc.github.io`), so the lineage is recorded permanently: the repo
page shows *"forked from LandonJPGinn/jp-verb-quiz"*, GitHub lists the ultimate
source as `wkdonc/wkdonc.github.io`, and every original author's commits and
authorship remain intact:

```bash
git log --format='%an' | sort -u     # every contributor, upstream included
```

At the time of forking that's 65 commits from Don (`doncr`), 27 from Landon,
plus Maurice Ampt and toxinu — against a handful from us.

### Licensing status — please read

**Neither upstream repo carries a license**, which by default means *all rights
reserved*. What that means in practice:

- This exists as a **GitHub fork**, which the [GitHub Terms of Service][tos]
  expressly permit for public repositories: by making a repo public you "agree
  to allow others to view and fork" it. That ToS grant is the *entire* basis on
  which this copy exists — the same basis as Landon's own fork of Don's work.
- It is served via GitHub Pages, as Don's and Landon's versions both are.
- **Do not add a `LICENSE` file.** We have no right to license someone else's
  work, and adding one would misrepresent the position.
- **Do not lift this code off GitHub** — copying it into another project or
  redistributing it elsewhere goes beyond the ToS fork grant.
- If Don or Landon ever object, take the Pages site down without argument.

For firmer ground, the right move is to ask upstream to add an explicit
open-source licence (e.g. MIT), which would benefit everyone downstream.

[tos]: https://docs.github.com/en/site-policy/github-terms-of-service#5-license-grant-to-other-users

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
