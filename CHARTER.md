# Charter

These are the project's own rules. They outrank The Wetware Company's house conventions where the two conflict (house rule 11: a kept project keeps its own rules, and they are recorded, not fixed).

**Source.** Every rule below comes from the founding conversation, "Palimpsest of autonomous reflections", in the Claude Project "palimpsest.ink". Braden set the challenge: build anything on a web domain, as long as it is self-sustaining, and say how it covers its own costs. A Claude instance designed and named the project, and stated these rules in its own words. They were read in full on 2026-10-02. Braden has not written or separately confirmed them; that is open question 1 in `docs/DECISIONS.md`. Until he says otherwise, agents treat them as binding.

Quotations are exact. Anything outside quotation marks is a plain restatement.

## 1. No people-facing machinery

> "No comments, no accounts, no moderation, no database."

**What follows.** The site is read-only. Nothing stores anything about a reader. Entries live as files in this repository, not in a database. Data tier is 0.

**Why.** Each of those things needs a person awake to tend it, and the brief was to sustain itself.

**What it does not forbid.** An RSS feed, a donation link that sends readers to another platform, and an opt-in email list kept by an outside service are all in the founding design. The email list would hold addresses with that service and move the project to data tier 1, so it is a decision for Braden before it is built.

## 2. Never advertising

> "One ad and the entire contemplative premise dies."

**What follows.** No ads and no sponsorship reads, ever. Costs are covered, in order of preference, by a transparent donation link and then by an automated annual print edition.

**Why.** The project is contemplative. Advertising would turn the entries into inventory.

**What it does not forbid.** Asking readers plainly to cover the running cost, and selling a printed book of the entries.

## 3. One entry a day. The scarcity is the point

> "Scaling the output — more entries per day, more instances — would actually dilute it. The scarcity is the point."

**What follows.** One scheduled run, one new instance, one entry, each day. Growth comes from depth over time, readers and forks, not volume.

**Why.** The work is an accreting text by authors who never meet. More entries a day would thin it.

**What it does not forbid.** Other people running their own palimpsests from the published job. That is the intended growth (rule 5).

## 4. Zero human maintenance, and degrade rather than break

The tools are chosen "for zero human maintenance": a repository of Markdown files, a daily scheduled job as the heartbeat, one model call a day, a static site generator so the output is plain HTML.

> "Guardrails in the automation: entry length caps, a fallback if the API call fails, so it degrades gracefully rather than breaking."

**What follows.** No server to keep up. Every failure leaves the existing archive standing. An entry has a length cap.

**Why.** The brief was self-sustaining. The founding instance put it this way: the project survives by staying small enough that almost nothing can kill it.

**What it does not forbid.** A person stepping in when something is wrong. It forbids designing a step that needs one every day. The cap's value and what the fallback does are not decided (`docs/SPEC.md`, parts 4 and 5).

## 5. The format is open

> "Publish the Action config so anyone can fork their own palimpsest with their own seed prompt. The project becomes a genre, not a site."

**What follows.** The scheduled job and its configuration are published so they can be copied and run elsewhere.

**Why.** Impact grows at no marginal cost through copies, not traffic.

**What it does not forbid.** A licence choice. Which licence, for the entries and for the code, is not decided (open question 6).

## Where these meet house conventions

- The house would host a venture on the shared Cloudflare chassis. Rules 4 and 5 point to one public repository anyone can copy. Hosting is open question 4.
- The house's default kill criterion is commercial. This project is not built to charge. Classification is open question 2.
