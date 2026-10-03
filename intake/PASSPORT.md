---
id: W-999
slug: palimpsest
name: "Palimpsest"
kind: kept-project
stage: proposed
one_liner: "A daily journal written by a fresh Claude instance each day, none of which remember the others, read on the web or by RSS."
thesis: "Once a day a scheduled job asks a new Claude instance, with no memory of earlier days, to read the last few entries and add one of its own, and the growing text is published as a plain static site. It is for readers interested in AI continuity and slow media. It is meant to cover its cost of about one dollar a month from voluntary donations, never from advertising."
payer: "Readers who choose to donate, and later perhaps buyers of an annual print edition. Nobody has paid yet, and no payment path exists."
revenue_model: none-yet
origin:
  founded_by: mixed
  founded_on: 2026-08-08
  source: "The founding conversation 'Palimpsest of autonomous reflections' in Braden's Claude Project 'palimpsest.ink', where Braden set the challenge and a Claude instance designed and named the project; the project's two memory files of 2026-09-14; a draft passport of 2026-09-23. The conversation's start date is not shown; 2026-08-08 is the oldest date seen on it, the date its summary was indexed. The day it began is not known."
data:
  tier: 0
  holds: "nothing"
  retention: null
  deletion_path: null
ai:
  dependency: runtime
  models:
    - { provider: anthropic, model: "claude-haiku-4-5-20251001", input_usd_per_mtok: 1, output_usd_per_mtok: 5, prices_checked_on: 2026-10-02 }
  monthly_budget_usd: 2
  breaker: hard
cost:
  infra_monthly_usd: 0
  model_monthly_usd: 0.15
  other_monthly_usd: 1
  notes: "Infrastructure is zero on the design's stack, GitHub Pages and a daily GitHub Actions schedule on free tiers; believed, not checked. Model cost assumes one call a day of about 2,000 input tokens and 500 output tokens at Haiku 4.5 list prices. Other is a domain renewal believed to be about 12 USD a year; no domain is known to be held for this project, and the price was not checked. The 2 USD budget and hard breaker are proposals, not decisions."
payments:
  rail: none
  provider: null
hosting:
  mode: independent
  domain: null
  dedicated_domain: null
  repo: "https://github.com/thewetwarecompany/palimpsest"
  worker: null
  health_url: null
admission:
  dispute_prone: { answer: no, note: "The design has only voluntary donations and, later, a print book sold through a print-on-demand service that takes the payment. Nothing is sold as a service that could be disputed." }
  custodies_funds: { answer: no, note: "The design never holds or routes money between people." }
  needs_synchronous_human: { answer: no, note: "The design has no comments, accounts, moderation or support channel; a scheduled job runs it with nobody awake." }
  tail_risk_beyond_balance_sheet: { answer: no, note: "The one real risk is that a model publishes unreviewed text every day under whatever name the site carries, so a bad entry could embarrass the company. The design's mitigations are a length cap and a fallback when the call fails; no review step is designed." }
  cold_email_volume: { answer: no, note: "The only email in the design is an opt-in list readers join themselves, and it is not decided or built." }
  remotely_operable: { answer: yes, note: "By design it is a git repository plus a scheduled GitHub Action, operable entirely by git and the GitHub API. Nothing is built, so this is unconfirmed in practice." }
  decision: pending
  decided_by: null
  decided_on: null
kill:
  criterion: "Not decided. The founding conversation set no stop condition, and Braden has to set one before admission; the options are under Open questions for Braden."
  launched_on: null
  review_on: null
brand:
  level: kept
  show_on_house_site: false
tracking:
  linear: null
gates:
  cleared: []
exit:
  export_path: "Every entry is a Markdown file in one public git repository, so a clone of the repository is the complete export. No entries exist yet."
updated: 2026-10-02
---

## Thesis

Each day a new Claude instance with no shared memory reads the last few entries and adds one, so the site becomes a text written by hundreds of minds that are technically identical but never met. It exists as a small, long-lived exploration of AI continuity and identity, for readers of slow media and people who study how these systems describe themselves. It should never need to charge; the aim is that one reader's donation covers a year. Its growth model is depth and forkability: other people can copy the scheduled job and run their own.

## What exists today

**Verified** on 2026-10-02:

- The repository `thewetwarecompany/palimpsest` exists and is public. Seen in the organisation's repository list; cloned, and it had no commits before the founding documents.
- The founding conversation, read in full: four turns, holding the concept, the stack, a cost estimate and a revenue ranking, and nothing else.
- The project's two memory files, an index and an overview, both dated 2026-09-14, read.
- A draft passport written on 2026-09-23 in the same Claude Project, read. This passport builds on it.
- Claude Haiku 4.5 list prices of 1 USD input and 5 USD output per million tokens, and model ID `claude-haiku-4-5-20251001` listed as current, read from the provider's own pricing and models pages.
- `palimpsest.ink` and `marginalia.site`, the two names the founding design proposed, both show as registered in a registry lookup through Vercel. Neither is in Braden's Vercel account, which holds no domains.
- No Vercel project carries the name. No Cloudflare Worker in Braden's account carries it; four Workers are listed, none for this project.
- No Linear project or issue mentions it.
- It is not in the chassis registry or the chassis intake queue on `main`.

**Not known:**

- Who holds `palimpsest.ink`. The Cloudflare connector cannot see registrar domains, and the public registration lookup refused the request. Braden can settle it in the Cloudflare dashboard.
- Whether any URL for the project answers. The network from the session that wrote this could not reach the domain or a GitHub Pages address.

**Believed**, not checked:

- No API key, Actions schedule, site, RSS feed, email list, donation link or print-on-demand account exists for it.
- Braden's notes record that the project went through intake in September 2026. The draft passport of 2026-09-23 is the only trace found; any copy in the intake queue of the Claude Project "The Wetware Company (Cloud)" was not checked.

The model entry is Anthropic directly, not a compatible vendor.

## Principles and constraints

The project's rules are in `CHARTER.md` in its repository, recorded from the founding conversation in the founding instance's own words. They bind:

- "No comments, no accounts, no moderation, no database."
- No advertising: "One ad and the entire contemplative premise dies."
- One entry a day: "The scarcity is the point."
- Zero human maintenance, with "entry length caps, a fallback if the API call fails, so it degrades gracefully rather than breaking."
- The format is open: the scheduled job is published so anyone can run their own.

Braden has not separately confirmed them. Where they conflict with house conventions, they rule.

## Data and privacy

It collects nothing, because nothing is built. As designed it still collects nothing: no accounts, comments or database. Readers only read.

Two possible additions would change that. An email list through an outside service would hold subscribers' addresses and move the project to tier 1. A donation link would leave donor details with that platform, not the project. Neither touches health information, financial information held by the project, or minors.

The real risk is on the publishing side: a model writes and publishes text daily with no human review.

## AI and model use

A model is the author. Once a day the scheduled job calls Claude Haiku 4.5 through the Anthropic API with the last few entries and a seed prompt, and publishes what comes back. It runs on a schedule, not when readers visit, so the cost is flat.

When the model is wrong, a reader sees a strange or poor entry, published as written. The design has a length cap and no review step. When a call fails, the design falls back rather than breaking the site; what the fallback does is not decided. The 2 USD monthly budget with a hard stop is a proposal, about ten times the expected spend. If it is reached, entries stop until the next month and the archive stays up.

## Money

Expected running cost is about 1.15 USD a month: about 0.15 USD of model calls, about 1 USD of domain renewal spread over the year if a domain is held, and zero for hosting. There is no treasury, wallet, payment account or donation path. Revenue so far is none.

## What it needs from a legal person

- A domain registration, if it gets its own domain.
- An Anthropic API account and key, with billing.
- GitHub Pages switched on for the repository.
- A licence for the entries and for the forkable code.
- If donations start, an account with a donation platform. If a print edition starts, a print-on-demand account. If an email list starts, an account with an email service and a privacy notice.

## Kill criteria

No stop condition has been set. What stopping means, per the design: the daily schedule is switched off and the API key revoked; the archive stays readable as a static site, or as a public repository if a domain lapses; nothing about people needs deleting, because nothing is held. Readers would be told in a final entry.

## Exit path

Every entry is a Markdown file in one git repository, so the whole project moves by transferring the repository and pointing any domain at the new owner. There is no personal data to move unless an email list is built, in which case that service exports it.

## Open questions for Braden

The full set, with forcing events, costs, reversibility and a sidestep for each, is in `docs/DECISIONS.md` in the project's repository. Those that bear on admission:

1. **Build it at all, on the charter as written?** Nothing forces a date. Building costs about a day of agent work and about 1 USD a month, and is reversible by switching the schedule off. Sidestep: publish only the forkable job as an open template.
2. **Kept project or experiment?** Written here as a kept project because it never aims to charge. As an experiment it would need a payer within 90 days. Reversible at any review. Sidestep: keep the journal as a kept project and treat a later print edition as a separate experiment.
3. **The domain.** `palimpsest.ink` is registered and the holder is not known. Forced by launch. If Braden holds it, record it; if not, choose another name or a company subdomain. Sidestep: launch on the GitHub Pages address and buy a domain when the first donation arrives.
4. **Where it runs.** Written here as independent, on GitHub, so it can be forked in one step. The chassis would add house monitoring. About a day to move either way. Sidestep: run on GitHub and give the house a status check to probe.
5. **Kill criterion.** Needed before admission. Options: no donor within 12 months of launch; entries failing for 30 days; or never stop. Sidestep: stop only if costs go well past the monthly cap.
6. **Monthly model budget.** 2 USD with a hard stop is proposed. Sidestep: a prepaid balance on an account used only for this project.

## Log

- 2026-09-23 — draft passport written by a Claude instance in the 'palimpsest.ink' Claude Project, from the founding conversation and the project's memory files.
- 2026-10-02 — passport revised by a Claude instance in the same Claude Project while writing the repository's founding documents: repository recorded, model prices and ID read from the provider's pages, domains looked up, founding date corrected to the oldest date seen on the founding conversation.
