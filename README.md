# SEVENTEEN Wire

An independent, unofficial English-language fan hub for SEVENTEEN/CARAT — news translation, release reviews, official-only video curation, a hiatus-and-return timeline, and a fan quiz, built to run on Google AdSense.

**Not affiliated with, endorsed by, or sponsored by PLEDIS Entertainment, HYBE, or the members of SEVENTEEN.**

## What's in this repo

This is a single static page — `index.html` — with everything (HTML, CSS, JS) inlined. No build step, no dependencies, no backend. It's meant to be served as-is by GitHub Pages. This repo follows the same template as [Bangtan Wire](https://fhzl0117-hue.github.io/bangtan-wire/), [Blackpink Wire](https://fhzl0117-hue.github.io/blackpink-wire/), [Stray Kids Wire](https://fhzl0117-hue.github.io/stray-kids-wire/), [aespa Wire](https://fhzl0117-hue.github.io/aespa-wire/), and [ENHYPEN Wire](https://fhzl0117-hue.github.io/enhypen-wire/) — part of the "Wire" series, one dedicated site per artist.

The page is organized into six "desks," each mapped to a content pillar:

| Desk | Section id | What it does |
|---|---|---|
| 01 · News | `#news` | Translated & summarized news dispatches, each linking to its original source |
| 02 · Review | `#reviews` | Album / track reviews, text only |
| 03 · Screening Room | `#screening` | Official YouTube embeds only — never re-uploaded video |
| 04 · Signal | `#signal` | An enlistment-and-return timeline with a live countdown, auto-converted to the visitor's local timezone |
| 05 · Quiz | `#quiz` | A lightweight interactive quiz, no backend, no data collection |
| 06 · Market | `#market` | Links to official stores (affiliate links go here) |

## A note on accuracy: the hiatus

As of this build, SEVENTEEN is in the middle of a mass, staggered military hiatus rather than any kind of breakup or departure. Jeonghan, Wonwoo, Hoshi, and Woozi were already serving as of mid-2026; Vernon began alternative service August 20, DK enlists September 8, Mingyu begins alternative service September 10, and Seungkwan and Dino enlist together October 26. Jeonghan has already completed his service (June 25, the first member to do so) and is preparing a new unit with Joshua. At their June 2026 "Carat Land" fan meeting, members said they expect the full group to reunite in two to three years. This is real, well-documented, and constantly moving — keep enlistment/discharge dates current and sourced in any future edit, and don't let the framing drift into either "the group broke up" or "nothing has changed." Cross-check dates against multiple outlets (Korea Times, Korea Herald, allkpop, Billboard, Soompi) before publishing an update.

## manifest.json — K-Wire Network auto-discovery

This repo carries a `manifest.json` at its root so it's automatically picked up by [K-Wire Network](https://fhzl0117-hue.github.io/), the directory hub for the whole "Wire" series. No manual edit to the hub repo is needed — its page fetches this file on every visit and lists this site automatically.

## Updating content

Everything is plain HTML — open `index.html` in any editor and look for the section with the matching `id` (e.g. `<section ... id="news">`) to update copy. There's no CMS yet; each dispatch, review, or signal-desk date is a hand-edited block. See the comments inside the `<script>` tag at the bottom for how the quiz and countdown timers work if you need to change their logic.

**Before adding new dates or news items,** verify the underlying facts against a real source and keep the "Read the original source" link pointing at it — that link is what keeps this page compliant with content policies (Google AdSense does not allow re-publishing copyrighted material, and this page's whole design is built around linking out and summarizing instead of reposting).

**Before adding any new YouTube embed,** verify it against the official channel using the oEmbed check: fetch `https://www.youtube.com/oembed?url=https://www.youtube.com/watch?v=<ID>&format=json` and confirm `author_name` matches HYBE LABELS (or the relevant member/subunit's own verified channel) — a search result titled "Official MV" is not proof by itself. During this site's initial build, candidates from a UK reaction channel, a YouTube Music "Topic" auto-channel, and an unrelated fan channel were all caught and rejected this way before a real HYBE LABELS upload was confirmed for each embed. Apply the same rigor to every future embed.

## License / ownership

Internal company project. Not licensed for redistribution outside the team without checking with whoever owns this repo.
