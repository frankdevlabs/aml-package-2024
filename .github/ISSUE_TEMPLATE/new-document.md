---
name: New document
about: Register a new official document (proposal, compromise text, report, opinion)
title: "[DOC] <institutional ID> — <short description> (<ISO date>)"
labels: document
---

## Document metadata

- **Institutional ID:** (e.g. AMLA-RTS-..., AMLA-SPD-..., REG-2024-1624, NL-...)
- **Title:**
- **Body / institution:** (AMLA / Commission / Netherlands / national supervisor / stakeholder)
- **Date (ISO):**
- **Restricted?:** (yes/no)
- **Authoritative URL:** (AMLA consultation page / EUR-Lex / wetgevingskalender / …)

## To do
- [ ] Add entry to `data/documents.yaml`
- [ ] Add row to `sources/README.md`
- [ ] Add to `TIMELINE.md`
- [ ] If a new AMLA draft instrument: add an extract file under `extracts/amla/` and a row in `docs/amla-pipeline.md` + `data/positions.csv`
- [ ] Update affected `docs/provisions/*`, `docs/netherlands.md` and `STATUS.md`
