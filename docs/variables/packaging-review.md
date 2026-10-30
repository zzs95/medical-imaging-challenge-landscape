# Packaging-review variables

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

These fields describe the documentation-cleanup audit, not the scientific evaluation of a challenge.

## `record_review.csv`

| Variable | Observed type | Definition |
| --- | --- | --- |
| `consolidated_common_notes` | string | Number of record-specific occurrences moved to shared notes with an explicit common_note_ids link. |
| `consolidated_template` | string | Indicator/count that an identical collection template was moved to the shared documentation file. |
| `edition_id` | string | Identifier of the analytical edition used to join the index, inventory and individual record. |
| `internal_archive_references` | string | Number of values containing references to the original internal review archive; those files are not bundled by implication. |
| `original_bytes` | string | Byte size of the source JSON before publication cleanup. |
| `other_remark_fields` | string | Number of other nested fields identified as notes/comments/remarks in the source record. |
| `package_path` | string | Relative path to the exported record within the data package. |
| `packaged_bytes` | string | Byte size of the exported individual JSON after publication cleanup. |
| `record_group` | string | Membership in the included, excluded or legacy package group. |
| `removed_editorial_sentences` | string | Number of manuscript-build/synchronization reminder sentences removed while retaining adjacent substantive information. |
| `removed_empty_remarks` | string | Number of empty optional note/comment/remark fields omitted from the publication copy. |
| `removed_exact_duplicates` | string | Number of exactly repeated notes removed from this record's publication copy. |
| `removed_repeated_field_evidence` | string | Number of notes removed because the same text and date remain in that record's field-level evidence. |
| `retained_history_fields` | string | Number of retained history fields identified by the packaging audit; not a count of separate assessments. |
| `review_status` | string | Whether this individual JSON was covered by the packaging documentation/remark review. |
| `source_path` | string | Path of the original source or evidence record; archive paths may refer to files not included in this package. |
| `top_level_notes` | string | Number of entries in the source challenge.notes array reviewed during packaging. |
| `workflow_language_candidates` | string | Number of text values flagged for historical workflow language; a flag is not an instruction to delete scientific evidence. |

## `review_summary.json`

| Variable | Observed type | Definition |
| --- | --- | --- |
| `annual_analysis_counts` | object | Counts of included editions by calendar year, using the 337-edition analytical inventory. |
| `annual_analysis_counts.2022` | integer | Number of included analytical editions assigned to calendar year 2022. |
| `annual_analysis_counts.2023` | integer | Number of included analytical editions assigned to calendar year 2023. |
| `annual_analysis_counts.2024` | integer | Number of included analytical editions assigned to calendar year 2024. |
| `annual_analysis_counts.2025` | integer | Number of included analytical editions assigned to calendar year 2025. |
| `annual_analysis_counts.2026` | integer | Number of included analytical editions assigned to calendar year 2026. |
| `cleanup_actions` | object | Counts of the different conservative documentation-cleanup operations applied during packaging. |
| `cleanup_actions.consolidate_collection_rules` | integer | Number of identical per-record collection-rule blocks consolidated into shared documentation. |
| `cleanup_actions.consolidate_common_note` | integer | Number of general-note occurrences moved into shared notes with per-record references. |
| `cleanup_actions.consolidate_schema_header` | integer | Number of repeated schema headers consolidated while retaining each record's schema version. |
| `cleanup_actions.remove_duplicate_note` | integer | Number of exactly duplicated note occurrences removed after preserving the first occurrence. |
| `cleanup_actions.remove_editorial_status_sentence` | integer | Number of manuscript-build reminder sentences removed from notes. |
| `cleanup_actions.remove_empty_remark` | integer | Number of empty optional remark fields removed during packaging. |
| `cleanup_actions.remove_repeated_field_evidence` | integer | Number of notes removed because identical explanatory text and review date remain in field_evidence. |
| `files_with_history` | integer | Number of individual records containing retained history fields. |
| `files_with_internal_archive_references` | integer | Number of individual records containing original-archive path references. |
| `files_with_workflow_candidates` | integer | Number of individual records containing text flagged as historical workflow language. |
| `groups` | object | Counts of included, excluded and legacy individual records in the packaging summary. |
| `groups.excluded` | integer | Number of records in the current manifest excluded from the primary analysis. |
| `groups.included` | integer | Number of challenge records in the 337-edition primary analysis. |
| `groups.legacy` | integer | Number of additional historical records outside the current manifest. |
| `inventory_hash_differences` | array | Edition identifiers whose current source JSON checksum differs from the checksum stored in the original analytical inventory. |
| `original_record_bytes` | integer | Combined byte size of the original individual challenge JSON files. |
| `package_date` | string | Date associated with package. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `packaged_record_bytes` | integer | Combined byte size of the exported individual challenge JSON files. |
| `records_reviewed` | integer | Number of individual challenge JSON files reviewed during packaging. |
| `remark_entries_reviewed` | integer | Number of note entries or remark fields covered by the packaging audit. |
| `validation` | object | Results of package-preservation and coverage checks; not model-validation or challenge-evaluation results. |
| `validation.all_venue_json_files_indexed` | boolean | Whether every individual JSON found in the audited venue directories is represented in the package index. |
| `validation.non_remark_fields_preserved` | boolean | Whether the packaging comparison found all substantive non-remark challenge fields unchanged. |
| `validation.public_source_urls_preserved` | boolean | Whether all public source URLs in the source challenge records were preserved through cleanup or shared-note consolidation. |
| `validation.source_files_modified` | boolean | Whether the original working JSON files were changed by packaging; false records that cleanup affected export copies only. |

[Back to README](../../README.md#variable-dictionary)
