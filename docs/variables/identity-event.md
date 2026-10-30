# Record identity, events and organizers

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

Record wrapper, challenge identity, event affiliations, organizers and related records.

## Record wrapper and challenge identity

Top-level fields in each individual challenge JSON:

| Variable | Observed type | Definition |
| --- | --- | --- |
| `challenge` | object | Structured information about one recorded challenge edition or explicitly identified historical record. |
| `common_note_ids` | array; items: string | Identifiers of shared qualifications that apply to this record; resolve each identifier in docs/common_notes.json. |
| `release_format_version` | string | Version of the publication wrapper used to consolidate repeated instructions. |
| `schema_version` | string | Version of the original challenge-metadata collection schema. |

### Challenge object: identity and field groups

All fields below are inside the top-level `challenge` object. Nested variables are defined in the thematic files linked from the README.

| Variable | Observed type | Definition |
| --- | --- | --- |
| `aliases` | array; items: string | Alternative names or abbreviations associated with the same challenge record. |
| `analysis_count` | integer | Number of units assigned by the associated analytical decision; legacy values must not override the current index. |
| `analysis_display_name` | string | Name assigned for presentation of the analytical unit, including any historical merged-unit naming. |
| `analysis_id` | string | Identifier assigned to a review-defined analytical unit; historical combined-unit identifiers can be superseded. |
| `analysis_unit_decision` | object | Structured entries for analysis unit decision within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `analysis_year_group` | string | Year/bin assigned by the associated analytical decision; historical assignments can be superseded. |
| `annual_allocation_decision` | object | Structured entries for annual allocation decision within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `assessment_evidence` | object | Documentary evidence concerning intended assessments, execution and outcomes; task and phase scope must be retained. |
| `challenge_id` | string | Identifier of the individual challenge record, used to join its metadata and review decisions. |
| `challenge_name` | string | Recorded short or customary name of the competition edition. |
| `child_challenge_ids` | array; items: string | Identifiers of constituent tracks or challenges linked to a parent record; do not automatically count each as a separate edition. |
| `clinical_classification_review` | object | Review of anatomical and disease categories, with source scope and qualifications. |
| `clinical_domain` | object | Imaging modality, anatomical scope and explicitly documented disease or clinical context. |
| `conference_affiliation_review` | object | Source-linked review of conference affiliation. |
| `count_in_core_medical_imaging_review` | boolean | Record-level inclusion flag from the underlying review; use the current package index for the final analytical subset. |
| `count_in_edition_statistics` | boolean | Record-level flag indicating whether an entry should contribute to edition counts under its associated decision. |
| `covered_years` | array; items: integer | Edition years covered by a combined or historical record, not necessarily separate included units. |
| `current_completion_adjudication` | object | Latest scoped judgment about edition completion, with its evidence type and limitations. |
| `current_inclusion_decision` | object | Latest recorded inclusion/exclusion decision within that source record; the package index gives the final current analytical subset. |
| `current_output_classification` | object | Structured entries for current output classification within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `data_access` | object | Conditions governing access to challenge data and their use; administrative access and reuse permissions are distinct. |
| `data_license_review` | object | Review of applicable data licences and use terms, separate from software or publication licences. |
| `data_usage_mode` | object | How data and methods are exchanged and executed during development and assessment. |
| `data_usage_mode_external_note` | string | Qualification or source distinction concerning data usage mode external. |
| `dataset` | object | Source cohorts, quantities, splits, acquisition conditions and associated data characteristics. |
| `edition_identity_review` | object | Source-linked review of edition identity. |
| `eligibility_review` | object | Source-linked review of eligibility. |
| `evaluation` | object | Assessment metrics, implementation, ranking and results, preserving task and phase distinctions. |
| `event` | object | Conference, workshop or other event affiliation and its edition-specific context. |
| `expanded_inventory_inclusion` | object | Structured entries for expanded inventory inclusion within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `full_name` | null / string | Expanded official challenge title when documented. |
| `identity_review` | object | Source-linked review of identity. |
| `labels_and_targets` | object | Label definitions, target entities and reference-annotation information documented for the task. |
| `links` | object | URLs to organizer pages, data, code, platforms and related publications. |
| `literature_followups` | array; items: object | Structured entries for literature followups within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `literature_review_leads` | array; items: object | Structured entries for literature review leads within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `modality_harmonization_review` | object | Source-linked review of modality harmonization. |
| `name_variants` | array; items: object | Structured entries for name variants within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `notes` | array; items: string | Contextual qualifications and source distinctions retained after removal of empty or exact redundant remarks. |
| `organizers` | object | Organizer institutions or persons and any explicitly recorded organizational characteristics. |
| `parent_challenge_id` | string | Identifier of a parent competition or umbrella record. |
| `participant_method_evidence` | array; items: object | Recorded documentary support for participant method. Preserve the task/phase scope and source qualifications. |
| `participation_statistics` | object | Source-reported participation and submission counts with original units, dates and task/phase scope. |
| `previous_review_coding` | object | Earlier classification retained for history; do not substitute it for the current analytical inventory. |
| `previous_scope_notes` | array; items: string | Earlier/superseded value of scope notes, preserved to document a revision rather than a current observation. |
| `protocol_history` | array; items: object | Earlier protocol descriptions retained separately from later or implemented arrangements. |
| `provenance` | object | Source references, observation dates, field-level supporting evidence and review history. |
| `publication` | object | Related publications, publication policies and publication-status evidence; not automatically evidence of challenge outcomes. |
| `record_field_review` | object | Source-linked review of record field. |
| `record_level` | string | Level represented by the record, such as an edition, parent event or constituent track. |
| `record_relationships` | object | Structured entries for record relationships within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `registered_task_taxonomy` | object | Structured entries for registered task taxonomy within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `related_conferences` | array; items: string | Structured entries for related conferences within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `resource_characteristics_review` | object | Review of dataset/resource quantities, units, centers and related source characteristics. |
| `resource_information_review` | object | Source-scoped review of acquisition geography, continuing resources and reported participation. |
| `resource_protocol_review` | object | Review of development access and data/model-flow or execution protocols, with phase-specific scope. |
| `result_evidence_review` | object | Source-linked review of result evidence. |
| `review_coding` | object | Review-derived classifications of task families, objectives, scope or related analytical variables. |
| `schedule` | object | Announced, revised or observed challenge dates and phases, with source and timezone qualifications. |
| `scope_status` | string | Recorded relationship of the competition to the medical/biomedical imaging review scope. |
| `submission` | object | Required artifacts, submission routes, runtime constraints and phase-specific procedures. |
| `submission_history` | array; items: object | Earlier submission rules or classifications, preserving the distinction between proposal and operational procedure. |
| `task_objective_review` | object | Source-linked review of task outputs and organizer-defined emerging AI objectives, including scope and changes. |
| `task_profile` | object | Task-specific inputs, outputs, goals and relationships within the edition. |
| `task_taxonomy` | object | Original task-family flags. True, false and null retain their source meaning; use the harmonized inventory for aggregate counts. |
| `task_taxonomy_scope` | string | Task, phase, cohort or source boundaries of task taxonomy. |
| `year` | integer | Edition year in challenge records; publication year inside a publication entry. These years must not be interchanged. |

## Field groups

- [`challenge.event`](#event)
- [`challenge.organizers`](#organizers)
- [`challenge.name_variants`](#name-variants)
- [`challenge.record_relationships`](#record-relationships)

<a id="event"></a>

## `event`

JSON parent path: `challenge.event`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.event`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `additional_affiliations` | array; items: string | Structured entries for additional affiliations within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `additional_associations` | array; items: object | Structured entries for additional associations within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `additional_associations[].conference` | string | Named conference affiliation. Raw records preserve source wording; the analytical inventory contains the harmonized assignment. |
| `additional_associations[].registration_doi` | string | DOI of the registered challenge protocol or registration record. |
| `additional_associations[].relationship` | string | Documented relationship between the enclosing entities, preserving affiliation, scope and timing qualifications. |
| `additional_associations[].source` | string | Source identifier, URL, citation, original wording or source object for the enclosing item. |
| `additional_conference_relationships` | array; items: object | Structured entries for additional conference relationships within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `additional_conference_relationships[].conference` | string | Named conference affiliation. Raw records preserve source wording; the analytical inventory contains the harmonized assignment. |
| `additional_conference_relationships[].formal_challenge_affiliation_confirmed` | null | Optional field for formal challenge affiliation confirmed in the enclosing record. It is unpopulated in this snapshot; neither a value nor a negative finding is established. |
| `additional_conference_relationships[].note` | string | Contextual qualification, uncertainty or source distinction for the enclosing item. |
| `additional_conference_relationships[].relationship` | string | Documented relationship between the enclosing entities, preserving affiliation, scope and timing qualifications. |
| `additional_conference_relationships[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `additional_workshop_affiliation` | string | Source-recorded additional workshop affiliation for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `challenge_event_date` | null / string | Date of the challenge meeting or results event when specified, not necessarily the competition deadline. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `conference` | string | Named conference affiliation. Raw records preserve source wording; the analytical inventory contains the harmonized assignment. |
| `conference_relationship_review` | object | Source-linked review of conference relationship. |
| `conference_relationship_review.conference_assignment` | string | Decision assigning the edition to a conference group, with supporting scope and qualifications. |
| `conference_relationship_review.confirmation` | object | Structured entries for confirmation within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `conference_relationship_review.confirmation.date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `conference_relationship_review.confirmation.public_source` | string | Source supporting public. |
| `conference_relationship_review.confirmation.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `conference_relationship_review.confirmation.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `conference_relationship_review.confirmation.source_type` | string | Kind of data or evidence source. In dataset records this describes cohort origin; in provenance it describes the supporting document or confirmation. |
| `conference_relationship_review.confirmation.statement` | string | Recorded statement supporting the enclosing confirmation, decision or source interpretation. |
| `conference_relationship_review.counting_rule` | string | Rule for counting editions, tasks or observations without double counting in the stated scope. |
| `conference_relationship_review.current_inventory_year` | integer | Calendar year assigned to current inventory; preserve whether this concerns an edition, analysis, event or publication. |
| `conference_relationship_review.evidence_urls` | array; items: string | Structured entries for evidence URLs within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `conference_relationship_review.existing_record` | string | Source-recorded existing record for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `conference_relationship_review.isbi_relationship` | string | Source-recorded isbi relationship for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `conference_relationship_review.midl_actual_results_session_presentation` | null | Optional field for midl actual results session presentation in the enclosing record. It is unpopulated in this snapshot; neither a value nor a negative finding is established. |
| `conference_relationship_review.midl_formal_endorsement` | null | Optional field for midl formal endorsement in the enclosing record. It is unpopulated in this snapshot; neither a value nor a negative finding is established. |
| `conference_relationship_review.midl_formal_endorsement_evidence` | string | Recorded documentary support for midl formal endorsement. Preserve the task/phase scope and source qualifications. |
| `conference_relationship_review.midl_relationship` | string | Source-recorded midl relationship for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `conference_relationship_review.note_zh` | string | Chinese-language qualification or explanation for the enclosing review decision. |
| `conference_relationship_review.organizations` | array; items: string | Structured entries for organizations within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `conference_relationship_review.primary_conference` | string | Main conference affiliation assigned to the edition for single-count analysis. |
| `conference_relationship_review.relationship` | string | Documented relationship between the enclosing entities, preserving affiliation, scope and timing qualifications. |
| `conference_relationship_review.review_date` | string | Date of the review operation described in the enclosing object. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `conference_relationship_review.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `conference_relationship_review.secondary_conference` | string | Additional documented conference affiliation that does not create another edition count. |
| `conference_relationship_review.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `conference_relationship_review.status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `conference_relationship_review.timeline_url` | string | Web address for timeline. |
| `conference_relationship_review.unique_edition_count` | integer | Number of distinct edition-level analytical units assigned by the enclosing deduplication/affiliation decision. |
| `conference_relationships` | array; items: object | Structured entries for conference relationships within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `conference_relationships[].conference` | string | Named conference affiliation. Raw records preserve source wording; the analytical inventory contains the harmonized assignment. |
| `conference_relationships[].confirmation_basis` | string | Evidence or reasoning supporting confirmation. |
| `conference_relationships[].date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `conference_relationships[].documentary_limit` | string | Limit on the conclusion supported by the available documents, distinct from a later human judgment. |
| `conference_relationships[].location` | string | Location relevant to the enclosing event, source or execution description; not automatically an image-acquisition site. |
| `conference_relationships[].relationship` | string | Documented relationship between the enclosing entities, preserving affiliation, scope and timing qualifications. |
| `conference_relationships[].status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `endorsing_organizations` | array; items: string | Structured entries for endorsing organizations within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `event_type` | null / string | Kind of event, such as a conference challenge, workshop challenge, standalone competition or benchmark. |
| `final_event_year` | integer | Calendar year assigned to final event; preserve whether this concerns an edition, analysis, event or publication. |
| `location` | null / object | Location relevant to the enclosing event, source or execution description; not automatically an image-acquisition site. |
| `location.city` | null / string | City of the enclosing event or acquisition source as explicitly identified by the surrounding record. |
| `location.country` | null / string | Country of the enclosing event or acquisition source; organizer country must not be substituted for dataset geography. |
| `location.room` | null / string | Room assigned to the challenge event or presentation session. |
| `location.venue` | null / string | Named venue of an event or publication, according to its enclosing record. |
| `name_review` | object | Source-linked review of name. |
| `name_review.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `name_review.previous_conference_label` | string | Earlier/superseded value of conference label, preserved to document a revision rather than a current observation. |
| `name_review.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `name_review.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `name_review.source_file` | string | Identifier or path of the source file in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `official_programme_row_numbers` | null / string | Source-recorded official programme row numbers for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `official_registration_id` | string | Identifier assigned in the official challenge registration or programme. |
| `official_venue_name` | string | Venue/workshop name explicitly recorded from organizer or conference material. |
| `openreview_venue_title` | string | Venue title shown by OpenReview for the cited paper or programme. |
| `parent_event` | null / string | Umbrella event or series associated with the challenge. |
| `secondary_conferences` | array; items: string, object | Structured entries for secondary conferences within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `secondary_conferences[].conference` | string | Named conference affiliation. Raw records preserve source wording; the analytical inventory contains the harmonized assignment. |
| `secondary_conferences[].formal_endorsement` | null | Optional field for formal endorsement in the enclosing record. It is unpopulated in this snapshot; neither a value nor a negative finding is established. |
| `secondary_conferences[].relationship` | string | Documented relationship between the enclosing entities, preserving affiliation, scope and timing qualifications. |
| `series` | string | Name of the recurring challenge, workshop or publication series in the enclosing record. |
| `verification_note` | object | Qualification or source distinction concerning verification. |
| `verification_note.date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `verification_note.event` | string | Conference, workshop or other event affiliation and its edition-specific context. |
| `verification_note.location` | string | Location relevant to the enclosing event, source or execution description; not automatically an image-acquisition site. |
| `verification_note.organization` | string | Named organization associated with the enclosing event, resource or contribution. |
| `verification_note.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `verification_note.track` | string | Track identifier, name or description within the competition. |
| `verification_note.verification_basis` | string | Evidence or reasoning supporting verification. |
| `website_launch_date` | string | Date associated with website launch. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `workshop` | string / object | Associated workshop and the nature of its relationship to the challenge. |
| `workshop.end_date` | string | Date associated with end. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `workshop.name` | null / string | Name of the enclosing task, institution, dataset, source, method or event; the parent field identifies the entity. |
| `workshop.proceedings` | null / string | Proceedings series or volume associated with the workshop or publication. |
| `workshop.relationship` | null / string | Documented relationship between the enclosing entities, preserving affiliation, scope and timing qualifications. |
| `workshop.start_date` | string | Date associated with start. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `year` | integer | Edition year in challenge records; publication year inside a publication entry. These years must not be interchanged. |

<a id="organizers"></a>

## `organizers`

JSON parent path: `challenge.organizers`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.organizers`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `evidence_scope` | string | Boundary of what the supporting evidence establishes, including specification versus actual execution. |
| `institutions` | null / array; items: string | Named organizing or contributing institutions; organizer institutions do not establish acquisition-center diversity. |
| `international` | null / boolean | Whether the relevant organizers or dataset sources span countries, according to the enclosing field; not a population-representativeness claim. |
| `protocol_reference` | object | Reference to the edition-specific protocol supporting the enclosing field; a protocol describes specification rather than proof of execution. |
| `protocol_reference.local_protocol` | string | Original archive path of a registered protocol; the protocol file itself is not included in this metadata package. |
| `protocol_reference.registered_task_index` | integer | Task position/identifier in the registered protocol; it can differ from later operational numbering. |
| `protocol_reference.section` | string | Section, figure, table or location within a supporting source. |
| `protocol_reference.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `registered_authors` | array; items: object | Structured entries for registered authors within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `registered_authors[].affiliation` | null / string | Documented association with the named conference, workshop or organization. |
| `registered_authors[].name` | string | Name of the enclosing task, institution, dataset, source, method or event; the parent field identifies the entity. |

<a id="name-variants"></a>

## `name_variants`

JSON parent path: `challenge.name_variants`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.name_variants`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `[].name` | string | Name of the enclosing task, institution, dataset, source, method or event; the parent field identifies the entity. |
| `[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `[].source` | string | Source identifier, URL, citation, original wording or source object for the enclosing item. |

<a id="record-relationships"></a>

## `record_relationships`

JSON parent path: `challenge.record_relationships`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.record_relationships`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `analytical_unit` | string | Entity treated as one observation in the associated analysis or inclusion decision. |
| `child_challenge_ids` | array; items: string | Identifiers of constituent tracks or challenges linked to a parent record; do not automatically count each as a separate edition. |
| `child_mapping_note` | string | Qualification or source distinction concerning child mapping. |
| `count_parent_additionally` | boolean | Whether the condition “count parent additionally” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `parent_challenge_id` | null / string | Identifier of a parent competition or umbrella record. |
| `registration_aliases` | array; items: string | Structured entries for registration aliases within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `related_challenges` | array; items: object | Structured entries for related challenges within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `related_challenges[].challenge_id` | string | Identifier of the individual challenge record, used to join its metadata and review decisions. |
| `related_challenges[].counting_rule` | string | Rule for counting editions, tasks or observations without double counting in the stated scope. |
| `related_challenges[].identity_review_status` | string | Recorded state of identity review. Preserve the task/phase scope and source qualifications. |
| `related_challenges[].relationship` | string | Documented relationship between the enclosing entities, preserving affiliation, scope and timing qualifications. |
| `related_challenges[].same_competition_round` | boolean | Whether the condition “same competition round” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `same_edition_subtasks_counted_separately` | boolean | Whether the condition “same edition subtasks counted separately” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |

[Back to README](../../README.md#variable-dictionary)
