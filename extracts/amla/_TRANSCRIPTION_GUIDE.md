# Transcription guide — AMLA Level-2/3 draft extracts

Internal standard for every file in `extracts/amla/`. Goal: a faithful, **diffable** record of the operative
text of each AMLA draft instrument (RTS / ITS / Guidelines) out for consultation, so that when AMLA publishes
the **final** instrument it can be added as a sibling file and `git diff` shows what changed.

## Source of truth
The committed consultation paper under [`../../sources/amla/`](../../sources/amla/), cross-checked against the
AMLA consultation page (see each file's header) and, on adoption, the final OJ text. Transcribe from the
committed PDF on disk — never from memory or a web summary.

## These are DRAFTS, not tracked-changes texts
Unlike Council compromise PDFs, AMLA consultation drafts are **clean** (no strikethrough/bold tracked changes).
So `pdftotext` is sufficient — the `transcribe-council-extract` skill's `pdf_changes.py`/`render_pdf.py`
(which need `pymupdf`, not installed on this host) are **not required** here. The CDD draft also ships a
separate "track changes from EBA draft" PDF — useful to see deltas from the EBA legacy draft, but the
authoritative consulted text is the clean consultation paper.

## What to extract
Only the **draft operative instrument** — for an RTS/ITS the "COMMISSION DELEGATED/IMPLEMENTING REGULATION"
block (recitals + articles + annexes), for Guidelines the numbered guidelines section. **Omit** the
consultation paper's background, "questions for consultation" and cost-benefit/impact-assessment annexes.

## Format — structured markdown with anchors (family standard)
Operative text is rendered as **structured markdown** (like the sibling trackers), NOT as a raw code-fenced
dump, so `docs/`, `STATUS.md` and `data/positions.csv` can deep-link a specific article. The conventions:
- **Article / section headings carry an anchor:** `### <a id="article-N"></a>Article N — Title`;
  for an ITS `### <a id="section-N"></a>SECTION N`; for Guidelines
  `### <a id="guideline-N"></a>Guideline N — Title` and `### <a id="sec-2-3"></a>2.3 …` for numbered sections.
- **Recitals** sit under `### <a id="recitals"></a>Recitals` (the `(1) …` items follow as text).
- **Annex tables are kept inside a ```text fence** (column-aligned tables mangle as markdown); anchor the
  annex heading itself (`## <a id="annex-i"></a>ANNEX I …`).
- Article/recital bodies are plain markdown paragraphs (de-fenced, left-stripped).
- Add a `▸` change-note where useful (e.g. "▸ builds on the EBA 30 Oct 2025 draft").

These files were first auto-extracted with `pdftotext -layout` (operative section only; form feeds, bare page
numbers and the repeating page footer stripped) and then marked up to the above. They remain **working**
transcriptions — pdftotext leaves minor artefacts (merged footnote superscripts, the odd two-line heading
truncated to its first line); verify article text against the committed PDF before relying on it.

## Faithfulness rules (hard)
- Operative wording is primary legal text — never paraphrase.
- Preserve the draft's own article/recital numbering and bracketed placeholders (e.g. `…/...`, `of XXX`,
  `[OP: …]`) exactly — those are undecided in the source, not `[illegible]`.
- Mark a genuinely illegible passage `[illegible in source]` — never guess.

## Naming & cross-links
- One file per consultation: `<TYPE>-<topic>-art<NN>_consultation-paper.md`. A later final instrument →
  sibling `<TYPE>-<topic>-art<NN>_final.md`.
- Relative links only. Link the matching [`../../docs/amla-pipeline.md`](../../docs/amla-pipeline.md) row and
  the [`../../sources/README.md`](../../sources/README.md) register entry. Verify with
  `python3 ../../.claude/skills/transcribe-council-extract/linkcheck.py ../..`.
