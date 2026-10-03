# Palimpsest

A daily journal written by a fresh Claude instance each day. Once a day a scheduled job starts a new instance with no memory of earlier days. It reads the last few entries, adds one of its own, and the growing text is published as a plain static site. A palimpsest is a manuscript written over the traces of earlier writing, which is what this becomes. It is a venture of The Wetware Company Ltd., proposed for its registry and not admitted.

## Who it is for

Readers of slow media, by web page and RSS. People who study AI continuity and how these systems describe themselves. People who want to run their own copy: the design publishes the scheduled job so anyone can fork the format.

## Current state

There is no code and no prototype anywhere. This repository holds the founding documents only. It was checked on 2026-10-02:

- This repository was empty before these documents were committed.
- No Vercel project and no Cloudflare Worker carries the name.
- No Linear project or issue mentions it.
- The Claude Project "palimpsest.ink" holds the founding conversation and a draft passport, and no build work.

Whether to build it is not decided. See `docs/DECISIONS.md`, open question 1.

## Layout

| Path | What it is |
|---|---|
| `README.md` | This page. |
| `CHARTER.md` | The project's own rules, from its founding conversation. They outrank house conventions. |
| `CLAUDE.md` | Rules for agents working in this repository. |
| `docs/DECISIONS.md` | Settled decisions, rejected options, and open questions for Braden. |
| `docs/SPEC.md` | What the product does, part by part, with a test for each part. |
| `intake/PASSPORT.md` | The venture passport for The Wetware Company's registry. |

No source directories exist yet. Their layout is not decided.

## How to run it

There is nothing to run yet. What can be run is the house intake check on the passport. It needs both repositories cloned side by side on the Mac mini.

Both blocks are for Terminal on the Mac mini. The first clones this repository. It stops without doing anything if the folder already exists, which is fine: go on to the second. It ends with `done.` from git.

<!-- copy-check: allow "Users" — /Users/braden is a directory on the Mac mini, not a word for people. -->
```
cd /Users/braden/Projects &&
test -d /Users/braden/Projects/wetware-chassis &&
test ! -d /Users/braden/Projects/palimpsest &&
git clone https://github.com/thewetwarecompany/palimpsest /Users/braden/Projects/palimpsest
```

The second checks the passport from the chassis checkout. The last line it prints should be `READY FOR ASSESSMENT`. Warnings above that line do not stop it.

<!-- copy-check: allow "Users" — /Users/braden is a directory on the Mac mini, not a word for people. -->
```
cd /Users/braden/Projects/wetware-chassis &&
test -f /Users/braden/Projects/palimpsest/intake/PASSPORT.md &&
npm ci &&
npm run intake -- check /Users/braden/Projects/palimpsest/intake/PASSPORT.md
```
