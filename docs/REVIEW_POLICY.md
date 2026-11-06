# Remark review and cleanup policy

The package was prepared by reviewing the structure and remark fields of every individual challenge JSON. Rule-based checks covered all 353 files; candidate workflow and conflicting-history notes were inspected separately. This was a documentation audit, not a new external verification of every factual field. Source files were left unchanged.

## Changes allowed in the publication copy

1. **Repeated collection instructions:** 227 identical `_filling_rules` objects are stored once in `collection_rules_v1.2.json`. Shared schema information is stored there too; the per-file schema version is retained. The illustrative `example_challenge` label is not used as a source of identity.
2. **Common notes:** A small explicit list of general instructions is stored in `common_notes.json`. Applicable records retain `common_note_ids`, so the meaning and record association are preserved.
3. **Exact duplicate notes:** Only repeated occurrences within one record are removed; the first occurrence, or its shared-note reference, remains.
4. **Repeated field-evidence text:** A dated note is removed only when both its exact explanatory text and its review date are already present in that record's `provenance.field_evidence`.
5. **Empty remarks:** Empty optional fields whose names contain `note`, `comment` or `remark` are omitted. Null dataset values, outcomes, access conditions and other factual fields remain unchanged.
6. **Editorial reminders:** The sentence stating that the manuscript/figures have not yet been rebuilt, and one exact manuscript-synchronization reminder, are removed. The adjoining dated scientific statement is retained.

All other challenge fields are compared against the source after accounting for empty remarks. Public source URLs are checked for preservation. The index records hashes of both original and packaged files.

## Information retained

Evidence status, dated human confirmation, task and phase qualifiers, uncertainty, planned versus implemented policies, dataset units, source conflicts, and substantive review histories are retained. A field named `review`, `history` or `note` is not automatically redundant. Historical information has not been silently promoted to current verified evidence.

Internal archive references are retained as provenance identifiers. Files from those archives are not bundled and are not links to resources within this repository. This preserves evidence traceability without presenting unbundled material as publicly available.

## Specific interpretation issues found

- **ACROBAT 2023:** the record contains a superseded combined 2022–2023 analytical decision and a later 24 October decision to retain 2022 only. The file is isolated under `data/legacy/`; its old analytical fields must not be used for current totals.
- **HECKTOR 2022:** earlier webpage inconsistencies and a subsequent organizer-paper resolution coexist in the notes. These document changing evidence; removing one solely because both discuss dataset counts would obscure the source conflict.
- **Completion and outcome notes:** records such as BodyMaps 2024, FETUS 2026 and SLC-PFM 2025 retain earlier uncertainty and later human confirmation. A confirmation of event/evaluation completion does not automatically establish publicly available final numerical results or assessment of every task.
- **Protocol and source scope:** initial submission rules, later operational arrangements, and edition-specific updates can differ. These are not interchangeable duplicate notes.

`review/record_review.csv` gives one row per record and the number of cleanup actions, other remark fields, historical fields, archive references and workflow-language candidates. Candidate counts are inspection flags, not automatic deletion decisions. `review_summary.json` summarizes the audit. Detailed before/after values remain in the local packaging audit, outside this public-oriented package.

## Participation-cutoff update, 3 November 2026

The preceding cleanup audit describes the original 353-file package. The current package contains 357 indexed records (342 included, 14 excluded, one legacy). Four new records and the reinstated COBRA record were source-checked for participation opening by 1 November 2026. This is a substantive eligibility update, not merely a remark cleanup. Prior human-review claims apply to the original cohort; no independent human validation of the five supplemental records is claimed. Timetables are not treated as execution or outcome evidence.
