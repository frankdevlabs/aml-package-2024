---
name: register-document
description: >-
  Register ONE new official document on the EU file this repo tracks (see tracker.yaml)
  into the repo's single source of truth. Use when asked to add / register / file a new document
  (Commission proposal or working doc, Council ST/WK text, Parliament item,
  EDPB-EDPS / ECB / EESC opinion, a national-government non-paper or member-state
  position, a stakeholder paper) from a URL and/or a local PDF/DOCX. Commits the
  source, adds the data/documents.yaml entry, renders sources/README.md, and routes
  the substance to TIMELINE.md, STATUS.md and the right docs/ page. Hands a full
  Council compromise text off to the transcribe-council-extract skill — it does not
  transcribe operative text itself.
---

# register-document

`data/documents.yaml` is the **single source of truth** for every official document on the file;
`sources/README.md` is its rendered table. This skill generalises the `new-document` issue template
(`.github/ISSUE_TEMPLATE/new-document.md`) into a repeatable, link-checked workflow for adding one
document end to end.

## The one rule

**Register exactly ONE document per run and per branch/PR.** If asked to add several, loop once per
document — separate entry, separate commit/PR each. (A document plus its own cover note/annex counts
as one; commit them together under one entry with `local` / `local_cover` / `local_annex`.)

## Inputs and modes

Entry point is the `/register-document` command (or invoke this skill directly). `$ARGUMENTS` is a
URL or local path, plus an optional flag:

- **(url-or-path only)** → make all edits on a new `documents/<doc-id>` branch and **leave them in
  the working tree / committed locally** for review; do not push.
- **`--pr`** → also push the branch and open a **draft** PR.

If no URL/path is given, ask for one (or the document metadata) and stop.

## Workflow

1. **Gather metadata.** From the URL (WebFetch) and/or the local file, establish:
   `id`, `title`, `body`, `date` (ISO), `limite` (bool), authoritative `url`, and provenance
   (`mirror` / `national_parliament` / register reference) and `access` where relevant.
   - If the source is a PDF whose text won't extract via WebFetch, download it and **Read the PDF
     directly** to confirm the substance before summarising (don't rely on the landing-page blurb).
   - Apply the **scope rule** from [`tracker.yaml`](../../../tracker.yaml): in-scope only if it concerns
     the AML Package (AMLR 2024/1624 / AMLA 2024/1620 / AMLD6 2024/1640) or its implementation, not a
     `keep_apart` sibling. (Easy confusion: the criminal-law Directive (EU) 2018/1673, also "6AMLD" — out
     of scope. Check the CELEX/article number, not just the topic.)

2. **Pick the source folder by `body`** and commit the file there with the repo's filename
   convention `<ID>_<slug>_<ISO-date>.<ext>` (download with `curl -sL -A "Mozilla/5.0" <url> -o <path>`;
   confirm with `file <path>`):

   | `body` | folder | example filename |
   |---|---|---|
   | AMLA (consultation paper / SPD / final RTS-ITS-GL) | `sources/amla/` | `RTS-CDD-art28-1_consultation-paper_2026-02-09.pdf` |
   | Commission (adopted act / delegated regulation) | link-only (EUR-Lex) | (no committed file; use `celex`) |
   | Netherlands (Iwt / besluitenlijst / ATR / dossier) | link-only (or `sources/netherlands/`) | (often link-only) |
   | NGO / industry / law firm | link-only | (often link-only) |

   Link-only is fine when there is no committed file (set no `local:`). The adopted acts are link-only via
   EUR-Lex; AMLA's public consultation papers/SPD are committed under `sources/amla/`.

3. **Add the YAML entry** to `data/documents.yaml` (append in the documents list). Field reference:
   - Core: `id`, `title` (quoted), `body`, `date` (ISO), `limite` (bool), `url` (authoritative).
   - Files: `local` (primary committed path); `local_cover` / `local_annex` / `local_init` /
     `local_add1`… for accompanying files.
   - Provenance for restricted/mirrored items: `mirror`, `national_parliament`, `register`, `celex`.
   - `access` (omit = fully public). Allowed values seen in the file:
     `cite-only`, `screenshot-only`, `not-public`, `public-released`, `public-via-register`,
     `public-via-journalist`, `public-via-national-parliament`.
   - `lead_source` (`>-` block, optional) — **credit the lead that surfaced the document** when it
     reached the repo via something other than its own institutional feed. Here the lead is typically a
     Tier-2/Tier-3 / external tip that flags an **AMLA consultation paper / draft RTS-ITS-GL** (or a
     **member-state submission / transposition step**) ahead of the official AMLA / EUR-Lex / national
     feed. Record: who/what flagged it (name + handle/outlet), the watchlist code (e.g. a `T3-*` Bluesky
     source), the tip URL + date, and one clause on why it counts as the lead (e.g. "ahead of AMLA's own
     consultations page"). Set it whenever the `register-document` run was triggered by a
     `resolve-tracker-issue` Tier-2/Tier-3 hit, or by any external tip-off rather than a Tier-1
     institutional source. Render it in the `sources/README.md` row as `lead: [@handle](tip-url) (\`code\`)`.
   - `notes` (`>-` block): what it is, the substantive stance in 2–4 sentences, cross-links to the
     digest/positions page. New `body` values (e.g. `Netherlands`) are allowed.

4. **Render the table** — add the row to the matching `sources/README.md` section, mirroring the YAML
   (id · title · date · hosted-file link · provenance). Create a section if the document is a new
   class (e.g. the `## Member-state positions` section for national non-papers).

5. **Route the substance** to the right layer:
   - Procedural milestone / AMLA event (consultation opens/closes, hearing, final report, appointment) →
     dated row in `TIMELINE.md` and, if it changes the picture, update `STATUS.md` (and `docs/amla-pipeline.md`
     pipeline table / `data/positions.csv` for a consultation).
   - **Netherlands transposition** (Iwt step, cash-limit, ATR, DNB) → update `docs/netherlands.md` and the
     **Member States** row in `STATUS.md`.
   - Industry / law-firm / advisory analysis → `docs/stakeholders.md` (+ `docs/fault-lines.md` for contested points).
   - Before asserting a feature of the package, check `STATUS.md`'s "What changed" / `docs/what-changed.md`.

6. **If the document is a new AMLA draft instrument** (RTS/ITS/Guidelines consultation paper) → register it
   here, then add an extract under `extracts/amla/` per `extracts/amla/_TRANSCRIPTION_GUIDE.md` (clean PDFs —
   plain `pdftotext`; the `transcribe-council-extract` skill's `pymupdf` drivers are not needed/installed).

7. **Link-check.** `python3 .claude/skills/transcribe-council-extract/linkcheck.py .` — must end
   "0 broken". Also sanity-check the YAML:
   `python3 -c "import yaml; yaml.safe_load(open('data/documents.yaml'))"`.

8. **Per the mode:** leave on the branch (default) or push + draft PR (`--pr`). See below.

## Opening the PR (`--pr`)

```bash
doc_id="<the new id, lowercased>"
git checkout -b "documents/${doc_id}"
python3 .claude/skills/transcribe-council-extract/linkcheck.py .   # must end "0 broken"
git add data/documents.yaml sources/ TIMELINE.md STATUS.md docs/
git commit -m "docs: add <DOC-ID> — <short description>"
git push -u origin "documents/${doc_id}"
gh pr create --draft --title "docs: add <DOC-ID> — <short description>" \
  --body "Registers <DOC-ID> (<body>, <date>). Source committed under sources/<folder>/; entry in data/documents.yaml; summary in <the routed docs page>."
```

## Worked example — the NL non-paper (`NL-NONPAPER-2026-04-08`)

A national-government non-paper, published on rijksoverheid.nl and sent to the Tweede + Eerste Kamer.
- Metadata: `body: Netherlands`, `date: 2026-04-08`, `limite: false`, public — so no `access:` field;
  PDF text wouldn't extract, so it was read directly to capture the "clean cut" position.
- Files committed to **`sources/member-states/`** (new folder for this class): the non-paper +
  `local_cover` Kamerbrief.
- Entry appended to `data/documents.yaml`; new `## Member-state positions` section in
  `sources/README.md`.
- Substance routed to a dedicated **Netherlands** section in `docs/member-state-positions.md`, the
  **Member States** row in `STATUS.md`, a dated `TIMELINE.md` row, and NL cross-links in
  `docs/provisions/gdpr-art4-personal-data.md` and `gdpr-art33-breach-notification.md`.

## Conventions (inherited from the repo)
- Relative links only inside the repo; deep-link to `extracts/*.md#anchor`, not PDF pages.
- The link check must pass ("0 broken") before any commit.
- Working summaries are not official texts — always say "verify against the source"; keep the
  `NOTICE` faithfulness posture.
