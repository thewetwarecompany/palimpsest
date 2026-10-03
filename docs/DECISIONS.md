# Decisions

Agents propose. Braden decides. A decision lands here only once he has made it, with where and when. Work status does not live here; it lives in Linear.

Reversibility uses the house terms: *reversible*, *costly to reverse*, *one-way door*.

## Settled

**1. The project is called Palimpsest, and its repository is `thewetwarecompany/palimpsest`.**
Reason: the name describes the work, a text written over the traces of earlier writing. `palimpsest` was preferred to `palimpsest.ink` because a dot in a repository name is awkward in some tooling.
Reversibility: *reversible* until launch, then *costly to reverse*. GitHub redirects a renamed repository, but the slug becomes part of public URLs.
Source: Braden created the repository on 2026-10-02 (GitHub shows it at 2026-10-03 02:12 UTC), after the two names were laid out in the chat that also wrote these documents.

**2. The repository is public.**
Reason: GitHub Pages and Actions are free for a public repository on a free organisation plan, and charter rule 5 wants the format copyable.
Reversibility: visibility is *reversible* in settings. Anything committed while public is a *one-way door*: assume it has been copied. No secret is ever committed.
Source: Braden created it public on 2026-10-02, in the same chat. Visibility checked on 2026-10-02 in the organisation's repository list.

**3. One repository per venture under the `thewetwarecompany` GitHub organisation, never a monorepo. The chassis kit is copied into a venture when it is created, not used as a live dependency.**
Reason: Braden's concern that merging the ventures into one folder would let them contaminate each other.
Reversibility: *costly to reverse*.
Source: Braden, 2026-09-24, recorded in the Wetware notes in Claude's memory. Believed, not re-checked with him.

## Rejected

- **Advertising.** Rejected in the founding design: it would kill the contemplative premise. Charter rule 2. Source: founding conversation, read 2026-10-02.
- **More than one entry a day, or more instances.** Rejected in the founding design: volume dilutes the work. Charter rule 3. Same source.
- **A monorepo for all Wetware ventures.** Rejected by Braden on 2026-09-24, for the reason under settled decision 3.
- **`palimpsest.ink` as the repository name.** Not chosen on 2026-10-02: dots are awkward in some tooling. The domain itself is a separate question (open question 3).
- **A private repository.** Not chosen on 2026-10-02: GitHub Pages from a private repository needs a paid plan, and it would work against charter rule 5.

## Open questions for Braden

Each one is self-contained. Nothing here has been decided.

### 1. Build it at all, and on the charter's rules?

The project exists only as a design and these documents. Its rules in `CHARTER.md` were written by the founding Claude instance and never confirmed by you.
Forcing event: none. Nothing waits on it except every other question below.
- **Build, on the charter as written.** About a day of agent work, then about 1 USD a month in expected running cost. *Reversible*: switch the schedule off and the archive stays.
- **Build, with the charter amended.** Same cost, plus the time to say which rule changes. *Reversible*.
- **Do not build.** Costs nothing. The repository stays as a record of a design. *Reversible*.
- **Sidestep:** publish only the forkable job as an open template, with no journal of your own, so the format exists without the company running one.

### 2. Kept project or experiment?

The house has two kinds. An experiment is a commercial test: by default it is stopped if it has no paying customer within 90 days of launch. A kept project is a mission project with its own identity that may never charge. The passport proposes kept project, because the design never aims to charge.
Forcing event: admission to the registry. Intake cannot record a decision without it.
- **Kept project.** No extra cost. It keeps its own rules and its own kill criterion. *Reversible* at any review.
- **Experiment.** It must find a payer within 90 days or be killed, which the design does not aim for. It would live on a company subdomain, not its own domain. *Reversible*.
- **Sidestep:** keep the journal as a kept project and treat only a later print edition as a separate experiment.

### 3. The domain

The founding design proposed `palimpsest.ink`, or `marginalia.site` as an alternative. On 2026-10-02 both showed as registered, by a registry lookup through Vercel. Neither is in your Vercel account, which holds no domains at all. Who holds `palimpsest.ink` is not known: the Cloudflare connector here cannot see registrar domains, and the public registration lookup refused the request. You can settle it in the Cloudflare dashboard, under Domain Registration, where `thewetwarecompany.com` and `wetwareco.com` are registered.
Forcing event: public launch. Nothing before that needs a domain.
- **If you hold `palimpsest.ink`:** record it as this project's domain. About 12 USD a year is believed; the real renewal price was not checked. *Reversible* while you keep renewing.
- **If someone else holds it:** pick another name, or a company subdomain such as `palimpsest.thewetwarecompany.com` at no extra cost. A new domain is a registration only you can make. *Reversible*, but a lapsed name may be taken.
- **Launch on the GitHub Pages address.** Free, and needs no decision now. *Reversible*: a domain can be pointed at it later.
- **Sidestep:** launch on the GitHub Pages address and buy a domain only when the first donation arrives, so the project pays for its own name.

### 4. Where it runs

The design is a public repository with GitHub Pages for the site and GitHub Actions for the daily run. The house default is the shared Cloudflare chassis.
Forcing event: the first build, if open question 1 is answered build.
- **Independent, on GitHub Pages and Actions.** About zero cost on free tiers, believed and not checked. Copyable in one fork, as charter rule 5 wants. The house's uptime probe and model adapter would not cover it. *Reversible*: about a day to move.
- **On the chassis.** House monitoring, the house model adapter with its budget breaker, and a company subdomain. Harder to fork, and the chassis has gates that must clear first. *Reversible*: about a day to move.
- **Sidestep:** run it on GitHub, and give the house only a read-only status check it can probe.

### 5. Kill criterion

The founding conversation set no stop condition. Intake needs one before admission.
Forcing event: admission to the registry.
- **Stop if no donor covers a year's cost within 12 months of launch.** Cheap to test. *Reversible*.
- **Stop if entries fail for 30 days running.** Measures whether it runs, not whether it pays. *Reversible*.
- **Never stop; let the archive stand.** Matches the founding idea that it should be nearly indestructible. Costs the domain renewal for as long as it runs. *Costly to reverse* once promised in public.
- **Sidestep:** tie the criterion to the budget alone: it stops only if running costs go well past the monthly cap.

### 6. Licence

No licence is chosen. Without one, nobody may legally copy the job or the entries, which works against charter rule 5. The entries and the code can take different licences.
Forcing event: the first public commit of code, or launch, whichever is first.
- **An open licence for the code and a share-alike licence for the entries.** Fits charter rule 5. *One-way door* for anything already published under it.
- **Code open, entries all rights reserved.** Others can run their own, but cannot reprint this one. *Reversible* toward more openness, not less.
- **No licence yet.** Free, and blocks forks. *Reversible*.
- **Sidestep:** publish the forkable job as its own small repository under an open licence, and leave the entries' licence until the print question (12) comes up.

### 7. Monthly model budget and what happens when it is reached

The passport proposes a 2 USD monthly cap with a hard stop: about ten times the expected model cost of about 0.15 USD a month. That cost assumes one call a day of about 2,000 input tokens and 500 output tokens at Claude Haiku 4.5's list prices, read on 2026-10-02 as 1 USD in and 5 USD out per million tokens.
Forcing event: admission, which refuses a runtime model without a budget.
- **2 USD, hard stop.** Entries stop until next month; the archive stays up. *Reversible*.
- **A higher cap, soft breaker.** Entries keep coming and you are alerted. More exposure to a runaway loop. *Reversible*.
- **Sidestep:** a prepaid API balance held only for this project, so the account itself is the cap.

### 8. Unreviewed text published under the company's name

By design a model writes and publishes one entry a day with no human review, only a length cap. A bad entry would appear under whatever name the site carries.
Forcing event: launch.
- **Publish under The Wetware Company, unreviewed.** Fits the zero-maintenance rule. A strange entry is the company's problem. *Reversible*: an entry can be removed, but it may already be copied.
- **Add an automated check before publishing.** A second model call that can veto an entry. Small extra cost, and it bends charter rule 4 less than a human step would. *Reversible*.
- **Sidestep:** present it as an independent project the company stewards, with the README saying the choices are the model's. The house's Asof fixture describes that pattern.

### 9. The seed prompt, how many entries each instance reads, and the entry length cap

These shape every entry. The founding design names the kinds of entry (a reflection on an idea, a close reading of a public-domain poem, a question it cannot resolve, a note to whoever comes next) and says it reads "the last few entries". It sets no numbers.
Forcing event: the first build.
- **You write the seed prompt.** Your voice sets the tone. A few hours of your time. *Reversible* for future entries; past entries stand.
- **An agent proposes one, you approve it.** Less of your time. *Reversible*.
- **Sidestep:** let the first instance write the seed prompt as entry zero, published as the first entry, so the project starts by choosing its own premise.

### 10. Who holds the model account and pays for it

Each daily run needs an Anthropic API key with billing. Whose account that is has not been said.
Forcing event: the first build.
- **The Wetware Company's account.** The cost sits with the company that owns the venture. *Reversible*.
- **A separate account for this project only.** Cleanest exit and its own spending limit. One more account to keep. *Reversible*.
- **Sidestep:** answer 7 with a prepaid balance on its own account, which settles this at the same time.

### 11. Where its work is tracked

Work status lives in Linear and nowhere else. On 2026-10-02 no Linear project or issue mentioned Palimpsest. Agents here file nothing in Linear unless asked.
Forcing event: the first piece of build work.
- **A Linear project for Palimpsest.** Its status has a home. *Reversible*.
- **Issues under an existing Wetware project.** Less to keep up. *Reversible*.
- **Sidestep:** none needed until open question 1 is answered build.

### 12. The add-ons: email list, donation link, print edition

The founding design ranks how it would cover its cost: a donation link first, an annual print edition second. It also proposes an email list. Each needs an outside account whose terms only you can accept, and the email list moves the project to data tier 1, with a privacy notice.
Forcing event: none before launch.
- **None at launch.** Costs nothing. *Reversible*.
- **Donation link at launch.** One account, no personal data held by the project. *Reversible*.
- **Sidestep:** RSS only, which needs no account and holds no data, and revisit after the first year of entries.
