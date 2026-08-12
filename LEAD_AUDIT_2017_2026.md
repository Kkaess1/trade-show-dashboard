# Lead recount, 2017–2026

This audit covers every dashboard show-year from 2017 onward that has a lead source file: 62 files in total. Each dashboard source name was resolved to one unique workbook or CSV in the trade-show archive.

## Counting rules

- `Qualified leads = Hot + Warm`.
- Source classifications take priority. Exact Hot/Warm fields, legacy `Application` / `Potential Application`, iCapture ranking questions, and distributor A/B grades were mapped to Hot/Warm.
- A numeric star or `Lead Rating` field was not treated as a Hot/Warm scale. In files that contain both fields, the stars conflict with the written classifications.
- Seven files without a usable classification field were reviewed record by record from their application notes. A concrete, active application with a defined need or follow-up is Hot; a plausible future application or relevant product interest is Warm.
- General interest, vendors, competitors, internal Bal Seal records, test scans, blank records, and notes that explicitly say there is no application are not qualified.
- `Cold = valid source rows - Hot - Warm`. This includes unqualified and blank valid attendee records; worksheet summaries, template rows, internal staff, and test scans are removed before calculating the residual.
- Earlier ungraded years are unchanged.
- The 2022 re-audit uses the rating or qualification tag recorded in each workbook and does not override it from narrative notes. See [`LEAD_AUDIT_2022.md`](LEAD_AUDIT_2022.md) and the 440-row [`lead-audit-2022-detail.csv`](lead-audit-2022-detail.csv).

## Notable corrections

- Automatica 2025 was added using the supplied 2025 reference workbook: 11 combined Hot + Warm leads out of 50 total, leaving 39 Cold. The workbook does not provide a separate Hot-versus-Warm split, so the dashboard does not infer one.
- Compamed 2025 has 58 worksheet records, two of which are Bal Seal staff. The workbook's explicit, separate interest columns contain 5 Hot and 9 Warm external records, so the corrected qualified count is **14**, not 58. Six records are explicitly Cold and the remaining 36 valid records are blank/unqualified, giving a Cold residual of 42.
- OTC 2026 contains three Bal Seal staff scans. After removing those, it has 64 valid records: 8 Hot, 19 Warm, and 37 Cold, for 27 qualified leads.
- OTC 2022 now uses the original show-close rating instead of a later expanded CRM template: 1 Hot, 15 Warm, and 31 residual Cold across 47 valid records. Hannover Messe 2022 remains 34 qualified (8 Hot + 26 Warm); its 22-record figure is the separate General Interest/current-customer group.
- Several older CRM sheets contain summary lines below the contacts. Those lines are no longer counted as leads; for example, AAOS 2022 has 14 contact records, not 17.
- Test and internal scans were removed from MD&M West 2026, MD&M Minneapolis 2025, OTC 2025/2026, BIOMEDevice San Jose 2021/2025, and any other reviewed file where they appeared.

The complete per-show/year result, prior dashboard value, delta, method, and source filename are in [`lead-audit-2017-2026.csv`](lead-audit-2017-2026.csv).
