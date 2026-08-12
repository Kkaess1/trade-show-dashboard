# 2022 lead re-audit

Every 2022 lead record was re-read from the show's workbook. The recorded rating or qualification tag is authoritative. Narrative notes were retained in the row-level audit for traceability but were not used to promote or demote a lead.

## Results

| Show | Valid records | Hot | Warm | Cold / residual | Hot + Warm | Evidence used |
|---|---:|---:|---:|---:|---:|---|
| AAOS | 14 | 9 | 5 | 0 | 14 | CRM `Lead Rank` |
| Analytica | 51 | 9 | 25 | 17 | 34 | `REMARKS and TYPE of LEAD` contains the recorded Hot/Warm/Cold value |
| BIOMEDevice Boston | 19 | 3 | 4 | 12 | 7 | Separate Hot, Warm, and Cold survey fields |
| BIOMEDevice Silicon Valley | 32 | 9 | 12 | 11 | CRM `Lead Rank` |
| Hannover Messe | 56 | 8 | 26 | 22 | Raw export `Lead Value`; 20 Cold plus 2 unspecified |
| MD&M Minneapolis | 15 | 1 | 6 | 8 | CRM `Lead Rank` |
| MD&M West | 28 | 0 | 4 | 24 | Four source `Opportunity` tags counted Warm; Vendor and blank tags remain Cold |
| M-Tech Osaka | 144 | 2 | 23 | 119 | Source `ランク`: A=Hot, B=Warm, C/D/blank=Cold |
| OTC | 47 | 1 | 15 | 31 | 16 | Original show-close `Bal Seal Engineering Product Interest` rating |
| Robotics Summit | 31 | 2 | 8 | 21 | 10 | Source classification; two internal Bal Seal scans excluded |

The dashboard's 2022 total is therefore **172 qualified leads: 44 Hot + 128 Warm**. The 265 cold/residual records are excluded from the qualified-lead total; three additional source rows are excluded as internal/test scans.

## Source and row decisions

### OTC

The authoritative file is `otc leads - raw at show close - 05-05-22.xlsx`. Its recorded product-interest field contains 1 Hot, 15 Warm, 18 General/Cold, and 14 blanks. One blank is explicitly `Test Record2` / `Test lead` and was excluded, leaving 47 valid records. The 13 remaining blanks stay in the residual Cold group, producing 31 Cold and **16 qualified**.

The later `Lead Ready Template-OTC.xlsx` contains 3 Hot and 31 Warm. It was not used because it broadens the original show-close ratings and is the source of the inflated dashboard count.

### Hannover Messe

The authoritative file is `Hannover leads - 06-02-22.xlsx`. Its `Lead Value` field contains 8 Application/Hot, 26 Potential Application/Warm, 20 General Interest/Cold, and 2 unspecified records: **34 qualified and 22 Cold/residual**.

The contemporaneous post-show report independently states 8 Applications, 26 Potential Applications, 22 General Interest/current-customer leads, and 56 total contacts. Thus, the reported “about 22” is the unqualified group, not the Hot + Warm total.

### Other shows

- AAOS uses its 14-record CRM sheet. The raw export's numeric rating is not a Hot/Warm scale and includes two internal Bal Seal scans; neither was used as a qualified rating.
- Analytica uses the original visitor workbook, not the later CRM copy. The written qualification field resolves exactly to 9 Hot, 25 Warm, and 17 Cold.
- BIOMEDevice Boston and Silicon Valley, and MD&M Minneapolis, have explicit rating fields and require no interpretation.
- MD&M West has no Hot/Warm/Cold field. To avoid classifying from free-text notes, only the four records explicitly tagged `Opportunity` are qualified, conservatively as Warm. The three `Vendor` records and 21 untagged records remain Cold.
- M-Tech Osaka uses the workbook's A/B/C/D rank. The dashboard maps the two A records to Hot and the 23 B records to Warm; C, D, and blank ranks remain Cold.
- Robotics Summit contains 2 Hot, 8 Warm, 20 Cold, and 3 `No answer provided` records. Two unanswered rows are internal Bal Seal scans and were excluded; the remaining unanswered external record stays in residual Cold.

## Traceability

[`lead-audit-2022-detail.csv`](lead-audit-2022-detail.csv) contains all 440 reviewed source rows, including excluded records. For each row it records the show, source filename and row number, recorded rating/tag, counted rating, rule applied, and the original note. The note is evidence only and does not override the workbook rating.
