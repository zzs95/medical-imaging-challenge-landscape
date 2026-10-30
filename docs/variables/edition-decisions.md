# Edition identity and analytical inclusion

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

Edition-level reconciliation, conference affiliation, eligibility and inclusion decisions.

## Field groups

- [`challenge.analysis_unit_decision`](#analysis-unit-decision)
- [`challenge.annual_allocation_decision`](#annual-allocation-decision)
- [`challenge.conference_affiliation_review`](#conference-affiliation-review)
- [`challenge.current_completion_adjudication`](#current-completion-adjudication)
- [`challenge.current_inclusion_decision`](#current-inclusion-decision)
- [`challenge.edition_identity_review`](#edition-identity-review)
- [`challenge.eligibility_review`](#eligibility-review)
- [`challenge.expanded_inventory_inclusion`](#expanded-inventory-inclusion)
- [`challenge.identity_review`](#identity-review)

<a id="analysis-unit-decision"></a>

## `analysis_unit_decision`

JSON parent path: `challenge.analysis_unit_decision`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.analysis_unit_decision`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `aggregate_application_status` | string | Recorded state of aggregate application. Preserve the task/phase scope and source qualifications. |
| `analysis_id` | string | Identifier assigned to a review-defined analytical unit; historical combined-unit identifiers can be superseded. |
| `annual_group` | string | Annual bin assigned by the enclosing analytical decision; legacy assignments may be superseded. |
| `assessment_evidence_ids` | array; items: string | Identifiers of evidence items supporting assessment. |
| `assessment_scope` | string | Task, phase, cohort or source boundaries of assessment. |
| `assessment_value` | string | Recorded state or value of the assessment decision in the enclosing task/phase scope. |
| `authorized_by` | string | Person or role recorded as authorizing the enclosing decision; not evidence of organizer execution. |
| `count_once` | boolean | Whether the condition “count once” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `covered_years` | array; items: integer | Edition years covered by a combined or historical record, not necessarily separate included units. |
| `date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `decision_id` | string | Identifier of a review or adjudication decision. |
| `display_name` | string | Source-recorded display name for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `historical_inventory_note` | string | Qualification or source distinction concerning historical inventory. |
| `instruction` | string | Instruction recorded for the enclosing procedure or decision; distinguish organizer instructions from historical author/reviewer requests. |
| `methodological_note` | string | Qualification or source distinction concerning methodological. |
| `original_inventory_ids` | array; items: string | Structured entries for original inventory identifiers within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `participation_policy` | string | Permission, restriction or procedural rule governing participation. |
| `unit_type` | string | Kind of analytical or documentary unit represented by the enclosing decision. |

<a id="annual-allocation-decision"></a>

## `annual_allocation_decision`

JSON parent path: `challenge.annual_allocation_decision`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.annual_allocation_decision`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `analysis_id` | string | Identifier assigned to a review-defined analytical unit; historical combined-unit identifiers can be superseded. |
| `analysis_year` | integer | Calendar year assigned to analysis; preserve whether this concerns an edition, analysis, event or publication. |
| `authorized_by` | string | Person or role recorded as authorizing the enclosing decision; not evidence of organizer execution. |
| `count_once` | boolean | Whether the condition “count once” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `covered_years` | array; items: integer | Edition years covered by a combined or historical record, not necessarily separate included units. |
| `date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `decision_id` | string | Identifier of a review or adjudication decision. |
| `instruction` | string | Instruction recorded for the enclosing procedure or decision; distinguish organizer instructions from historical author/reviewer requests. |
| `note` | string | Contextual qualification, uncertainty or source distinction for the enclosing item. |

<a id="conference-affiliation-review"></a>

## `conference_affiliation_review`

JSON parent path: `challenge.conference_affiliation_review`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.conference_affiliation_review`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `analysis_conference` | string | Conference affiliation assigned for the analysis rather than the source directory name. |
| `assignment_basis` | string | Evidence or reasoning supporting assignment. |
| `note_zh` | string | Chinese-language qualification or explanation for the enclosing review decision. |
| `organizing_arrangement` | string | Source-recorded organizing arrangement for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `previous_analysis_conference` | string | Earlier/superseded value of analysis conference, preserved to document a revision rather than a current observation. |
| `primary_conference` | null / string | Main conference affiliation assigned to the edition for single-count analysis. |
| `primary_relationship` | string | Principal relationship used to interpret the edition's event affiliation. |
| `related_events` | array; items: object | Structured entries for related events within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `related_events[].count_as_primary` | boolean | Whether the condition “count as primary” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `related_events[].relationship` | string | Documented relationship between the enclosing entities, preserving affiliation, scope and timing qualifications. |
| `related_events[].venue` | string | Named venue of an event or publication, according to its enclosing record. |
| `related_events[].workshop` | string | Associated workshop and the nature of its relationship to the challenge. |
| `related_events[].year` | null / integer | Edition year in challenge records; publication year inside a publication entry. These years must not be interchanged. |
| `review_date` | string | Date of the review operation described in the enclosing object. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `sources` | array; items: object | Sources supporting the enclosing statement or dataset description, preserving document/source type and scope. |
| `sources[].local_source` | string | Path identifying a source in the original review archive, not a downloadable file inside this release. |
| `sources[].retrieval_method` | string | Source-recorded retrieval method for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `sources[].sha256` | string | Cryptographic checksum or revision identifier for the enclosing sha256; used for provenance rather than as a scientific measurement. |
| `sources[].supports` | string | Statements or fields that the source is recorded as supporting, limited by the source's actual task, phase and evidence scope. |
| `sources[].type` | string | Type of the enclosing source, document, artifact, observation or event; its vocabulary is specific to that parent context. |
| `sources[].url` | string | Web address of the enclosing source, document or resource. |

<a id="current-completion-adjudication"></a>

## `current_completion_adjudication`

JSON parent path: `challenge.current_completion_adjudication`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.current_completion_adjudication`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `public_final_scores_independently_verified` | boolean | Whether the condition “public final scores independently verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `source` | string | Source identifier, URL, citation, original wording or source object for the enclosing item. |
| `statement` | string | Recorded statement supporting the enclosing confirmation, decision or source interpretation. |
| `status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |

<a id="current-inclusion-decision"></a>

## `current_inclusion_decision`

JSON parent path: `challenge.current_inclusion_decision`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.current_inclusion_decision`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `analysis_include` | boolean | Whether this record belongs to the 337-edition primary analytical subset. |
| `date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `decision_basis` | string | Evidence or reasoning supporting decision. |
| `decision_date` | string | Date associated with decision. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `decision_scope` | string | Task, phase, cohort or source boundaries of decision. |
| `official_protocol` | string | Protocol identified as official for the stated edition/task, distinct from proof of implementation. |
| `reason` | string | Reason for the enclosing decision, revision, exclusion or qualification. |
| `source` | string | Source identifier, URL, citation, original wording or source object for the enclosing item. |

<a id="edition-identity-review"></a>

## `edition_identity_review`

JSON parent path: `challenge.edition_identity_review`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.edition_identity_review`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `analytical_units` | integer | Reported numerical value for analytical units within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `baseline` | string | Reference method or baseline result, distinguished from final competitive participant outcomes. |
| `challenge_family` | string | Recurring competition series or shared family name to which the edition belongs. |
| `competition_id` | integer | Identifier of the competition on its hosting platform, not its analytical edition count. |
| `competition_url` | string | Web address for competition. |
| `conference` | string | Named conference affiliation. Raw records preserve source wording; the analytical inventory contains the harmonized assignment. |
| `count_as_independent_challenge` | boolean | Whether the condition “count as independent challenge” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `counting_decision` | string | Recorded resolution of whether/how the enclosing entry contributes to the analysis. |
| `edition_evidence` | string | Recorded documentary support for edition. Preserve the task/phase scope and source qualifications. |
| `edition_identity_status` | string | Recorded state of edition identity. Preserve the task/phase scope and source qualifications. |
| `edition_year` | integer | Calendar year assigned to edition; preserve whether this concerns an edition, analysis, event or publication. |
| `final_evaluation_status` | string | Recorded state of final evaluation. Preserve the task/phase scope and source qualifications. |
| `internal_directions_add_units` | boolean | Whether the condition “internal directions add units” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `internal_evaluation_directions` | array; items: string | Structured entries for internal evaluation directions within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `note_zh` | string | Chinese-language qualification or explanation for the enclosing review decision. |
| `official_2026_final_ranking` | string | Source-recorded official 2026 final ranking for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `platform_id_reused_from_2025` | boolean | Whether the condition “platform identifier reused from 2025” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `publication_scope` | string | Task, phase, cohort or source boundaries of publication. |
| `reopening_date` | string | Date associated with reopening. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `review_date` | string | Date of the review operation described in the enclosing object. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `rules_scope` | string | Task, phase, cohort or source boundaries of rules. |
| `shared_data_with_2025` | boolean | Whether the condition “shared data with 2025” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `shared_dataset_url` | string | Web address for shared dataset. |
| `sources` | array; items: object | Sources supporting the enclosing statement or dataset description, preserving document/source type and scope. |
| `sources[].capture_date` | string | Date associated with capture. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `sources[].local_source` | string | Path identifying a source in the original review archive, not a downloadable file inside this release. |
| `sources[].sha256` | string | Cryptographic checksum or revision identifier for the enclosing sha256; used for provenance rather than as a scientific measurement. |
| `sources[].url` | string | Web address of the enclosing source, document or resource. |
| `sources[].verification` | string | Source-recorded verification for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |

<a id="eligibility-review"></a>

## `eligibility_review`

JSON parent path: `challenge.eligibility_review`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.eligibility_review`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `aggregate_application_status` | string | Recorded state of aggregate application. Preserve the task/phase scope and source qualifications. |
| `decision_basis` | string | Evidence or reasoning supporting decision. |
| `decision_date` | string | Date associated with decision. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `evidence_ids` | array; items: string | Identifiers of specific evidence items supporting the enclosing interpretation; archival ledgers may be outside this package. |
| `evidence_sources` | array; items: object | Sources supporting evidence. |
| `evidence_sources[].id` | string | Identifier of the enclosing source, task, participant or review item; its namespace is defined by the parent object. |
| `evidence_sources[].location` | string | Location relevant to the enclosing event, source or execution description; not automatically an image-acquisition site. |
| `evidence_sources[].retrieval_scope` | string | Task, phase, cohort or source boundaries of retrieval. |
| `evidence_sources[].snapshot` | string | Identifier or path of the snapshot in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `evidence_sources[].summary` | string | Concise summary of the enclosing source, review or observation. |
| `evidence_sources[].url` | string | Web address of the enclosing source, document or resource. |
| `include_in_primary_analysis` | boolean | Whether the condition “include in primary analysis” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `methodological_note` | string | Qualification or source distinction concerning methodological. |
| `participation_context` | object | Structured entries for participation context within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `participation_context.named_final_entries_observed` | array; items: string | Structured entries for named final entries observed within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `participation_context.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `participation_context.registered_users_snapshot` | integer | Number of registered users snapshot in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `participation_context.snapshot_date` | string | Date associated with snapshot. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `reason` | string | Reason for the enclosing decision, revision, exclusion or qualification. |
| `retain_source_record` | boolean | Whether the condition “retain source record” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `scope_qualification` | string | Source-recorded scope qualification for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `user_instruction` | string | Source-recorded user instruction for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `value` | string | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |

<a id="expanded-inventory-inclusion"></a>

## `expanded_inventory_inclusion`

JSON parent path: `challenge.expanded_inventory_inclusion`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.expanded_inventory_inclusion`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `analysis_include` | boolean | Whether this record belongs to the 337-edition primary analytical subset. |
| `decision_date` | string | Date associated with decision. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `reason` | string | Reason for the enclosing decision, revision, exclusion or qualification. |

<a id="identity-review"></a>

## `identity_review`

JSON parent path: `challenge.identity_review`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.identity_review`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `excluded_description` | string | Source description of excluded. |
| `qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `verified_challenge_name` | string | Source-recorded verified challenge name for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `verified_modality` | string | Source-recorded verified modality for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |

[Back to README](../../README.md#variable-dictionary)
