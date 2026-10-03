# palimpsest — rules for agents working in this repo

A daily journal written by a fresh Claude instance each day, none of which remember the others. A venture of The Wetware Company Ltd., proposed for its registry, not admitted. No code yet.

Read on demand — do not import these into this file, they cost tokens every session:
`README.md` (what it is, current state, layout) · `CHARTER.md` (the project's own rules; they outrank the house) · `docs/DECISIONS.md` (settled, rejected, and open questions) · `docs/SPEC.md` (what it does, part by part, with tests) · `intake/PASSPORT.md` (the registry passport). House conventions live in the chassis repository, `thewetwarecompany/wetware-chassis`: `CLAUDE.md`, `docs/STYLE.md`, `intake/README.md`.

## Rules

1. **Agents propose. Braden decides.** Never record a decision he has not made. A settled decision carries where and when he made it.
2. **Status lives in Linear, and nowhere else.** Not in this repository, not in docs, not in memory. File nothing in Linear unless asked; an issue you are asked to file stays in Backlog, unlabelled, and says so in its body.
3. **Never move a Linear issue to `Approved`**, and never add or remove the `approved`, `decided`, `decision` or any route label. A dispatcher on the Mac mini acts on those signals; they are Braden's alone.
4. **The charter outranks the house.** Where `CHARTER.md` and a house convention conflict, the charter wins. Record a conflict in `docs/DECISIONS.md` as an open question; do not fix the charter.
5. **Never invent.** No user, figure, date or decision from memory. Write "Not decided." or "Not known." and say who can settle it. Split facts into verified (checked this session, and how) and believed.
6. **Nothing is provisioned without Braden.** No domain, account, API key, schedule, Pages site, licence, visibility change or payment. Each is an open question until he answers it.
7. **No secrets anywhere.** This repository is public. Not in files, commits, issues or chat.
8. **Run the house gates before you say done**, from the chassis checkout: `npm run intake -- check` on the passport, and `node scripts/paste-check.mjs`, `node scripts/copy-check.mjs` and `node scripts/secret-scan.mjs` on this repository. A piece of work closes on its acceptance command's output, not on a report.
9. **Never overwrite history.** Read existing commits first and add to them. No force-push to `main`.
10. **Commands handed to a person follow the house style:** an explicit `cd` to a Mac mini path first, lines joined with `&&`, guards inside the block, paste-safe characters, no `exit`, no suppressed output, the success line named.
11. **Minimum necessary architecture.** A new dependency or infrastructure layer needs a written reason next to it. Verify the running result, not the code.
12. **Plain words.** Short sentences, Canadian spelling, ISO dates, currency on every amount. Public words pass the house copy check.
