# Participation and continuing resources

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

Registrations, teams, submissions, source geography and post-challenge resources.

## Field groups

- [`challenge.participation_statistics`](#participation-statistics)
- [`challenge.resource_information_review`](#resource-information-review)

<a id="participation-statistics"></a>

## `participation_statistics`

JSON parent path: `challenge.participation_statistics`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.participation_statistics`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `active_participants` | null | Number of active people under the source's definition and stated phase. |
| `active_teams` | null | Number of active teams under the source's definition and stated phase. |
| `additional_platform_snapshots` | array; items: object | Structured entries for additional platform snapshots within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `additional_platform_snapshots[].participant_accounts` | integer | Reported participation/submission measure for participant accounts. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `additional_platform_snapshots[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `additional_platform_snapshots[].submission_count` | integer | Reported participation/submission measure for submission count. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `additional_platform_snapshots[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `edition_test_algorithm_submissions` | integer | Reported participation/submission measure for edition test algorithm submissions. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `evaluated_algorithms` | integer | Reported participation/submission measure for evaluated algorithms. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `finalist_teams` | null / integer | Number of finalist teams; not necessarily all active teams in the competition. |
| `notes` | string / array; items: string | Contextual qualifications and source distinctions retained after removal of empty or exact redundant remarks. |
| `participants_with_submission` | null | Number of people/accounts with at least one qualifying submission in the recorded scope. |
| `participating_teams` | integer | Reported participation/submission measure for participating teams. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `participation_observations` | array; items: object | Structured entries for participation observations within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `participation_observations[].lower_bound` | boolean | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `participation_observations[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `participation_observations[].unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `participation_observations[].value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `platform_snapshot` | object | Structured entries for platform snapshot within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `platform_snapshot.participant_accounts` | integer | Reported participation/submission measure for participant accounts. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `platform_snapshot.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `platform_snapshot.submission_count` | integer | Reported participation/submission measure for submission count. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `qualified_teams` | null | Number of teams meeting the source's eligibility or qualification criterion. |
| `registered_participants` | null / integer | Number of registered people/accounts as reported; registration does not establish active participation. |
| `registered_teams` | null / integer | Number of registered teams as reported; distinct from teams submitting results. |
| `reported_counts` | array; items: object | Structured entries for reported counts within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `reported_counts[].countries` | integer | Reported participation/submission measure for countries. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `reported_counts[].researchers` | integer | Reported participation/submission measure for researchers. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `reported_counts[].reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `reported_counts[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `reported_counts[].source_type` | string | Kind of data or evidence source. In dataset records this describes cohort origin; in provenance it describes the supporting document or confirmation. |
| `reported_counts[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `reported_counts[].submissions` | integer | Submission-count information grouped by phase, task or platform scope. |
| `reported_counts[].teams` | integer | Reported participation/submission measure for teams. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `reported_participants` | object | Reported participation/submission measure for reported participants. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `reported_participants.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `reported_participants.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `reported_participants.relation` | string | Relationship between the enclosing observations, datasets or resources. |
| `reported_participants.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `reported_participants.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `reported_participating_teams` | integer / object | Reported participation/submission measure for reported participating teams. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `reported_participating_teams.definition_limit` | string | Restriction on interpreting the source's definition or comparing its counts with other records. |
| `reported_participating_teams.location` | string | Location relevant to the enclosing event, source or execution description; not automatically an image-acquisition site. |
| `reported_participating_teams.source_term` | string | Original term used by the source for a counted entity or category. |
| `reported_participating_teams.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `reported_participating_teams.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `reported_participating_teams.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `shared_platform_snapshot` | object | Structured entries for shared platform snapshot within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `shared_platform_snapshot.edition_scope` | string | Task, phase, cohort or source boundaries of edition. |
| `shared_platform_snapshot.evidence_ids` | array; items: string | Identifiers of specific evidence items supporting the enclosing interpretation; archival ledgers may be outside this package. |
| `shared_platform_snapshot.notes` | array; items: string | Contextual qualifications and source distinctions retained after removal of empty or exact redundant remarks. |
| `shared_platform_snapshot.platform_registered_users` | integer | Reported participation/submission measure for platform registered users. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `shared_platform_snapshot.previous_snapshot` | object | Earlier/superseded value of snapshot, preserved to document a revision rather than a current observation. |
| `shared_platform_snapshot.previous_snapshot.platform_registered_users` | integer | Reported participation/submission measure for platform registered users. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `shared_platform_snapshot.previous_snapshot.snapshot_date` | string | Date associated with snapshot. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `shared_platform_snapshot.previous_snapshot.test_submissions` | integer | Reported participation/submission measure for test submissions. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `shared_platform_snapshot.previous_snapshot.validation_submissions` | integer | Reported participation/submission measure for validation submissions. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `shared_platform_snapshot.snapshot_date` | string | Date associated with snapshot. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `shared_platform_snapshot.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `shared_platform_snapshot.submissions_by_phase` | array; items: object | Reported participation/submission measure for submissions by phase. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `shared_platform_snapshot.submissions_by_phase[].count` | integer | Number of the entity identified by unit, source_term and the enclosing task/phase. |
| `shared_platform_snapshot.submissions_by_phase[].official_phase_name` | string | Phase name exactly as shown by the organizer or platform. |
| `shared_platform_snapshot.submissions_by_phase[].unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `shared_platform_snapshot.unique_submitting_teams` | null | Reported participation/submission measure for unique submitting teams. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `source_reported_counts` | array; items: object | Structured entries for source reported counts within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `source_reported_counts[].interpretation` | string | Reviewer's scoped interpretation of the recorded source information; not additional organizer evidence. |
| `source_reported_counts[].open_validation_submissions` | integer | Reported participation/submission measure for open validation submissions. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `source_reported_counts[].publication_date` | string | Date associated with publication. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `source_reported_counts[].reported_participants` | integer | Reported participation/submission measure for reported participants. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `source_reported_counts[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `source_reported_counts[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `statistics_snapshot_date` | null / string | Date on which the participation/platform figures were observed, not a competition or data-acquisition date. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `statistics_status` | null / string | Temporal or interpretive status of the participation snapshot, such as post-challenge or cumulative. |
| `submissions` | null / object | Submission-count information grouped by phase, task or platform scope. |
| `submissions.by_phase` | array; items: object | Entries broken down by competition phase; counts can involve the same teams across phases. |
| `submissions.by_phase[].count` | integer | Number of the entity identified by unit, source_term and the enclosing task/phase. |
| `submissions.by_phase[].evidence_source` | string | Source supporting evidence. |
| `submissions.by_phase[].local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `submissions.by_phase[].official_phase_name` | string | Phase name exactly as shown by the organizer or platform. |
| `submissions.by_phase[].phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. |
| `submissions.by_phase[].previous_snapshot` | object | Earlier/superseded value of snapshot, preserved to document a revision rather than a current observation. |
| `submissions.by_phase[].previous_snapshot.snapshot_date` | string | Date associated with snapshot. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `submissions.by_phase[].previous_snapshot.submission_count` | integer | Reported participation/submission measure for submission count. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `submissions.by_phase[].statistics_snapshot_date` | string | Date on which the participation/platform figures were observed, not a competition or data-acquisition date. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `submissions.by_phase[].submission_count` | integer | Reported participation/submission measure for submission count. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `submissions.by_task` | null | Entries broken down by task; entries can involve overlapping teams or data. |
| `submissions.directory_summary_submissions` | null | Submission count shown in a platform directory summary at the observation date; scope can span phases or editions. |
| `submissions.total_submissions` | null | Number of submission attempts or entries within the stated scope, not the number of independent teams. |
| `submissions.valid_submissions` | integer | Reported participation/submission measure for valid submissions. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `supplementary_method_entries` | object | Reported participation/submission measure for supplementary method entries. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `supplementary_method_entries.note` | string | Contextual qualification, uncertainty or source distinction for the enclosing item. |
| `supplementary_method_entries.participant_method_entries` | integer | Reported participation/submission measure for participant method entries. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `supplementary_method_entries.unique_people` | null | Reported participation/submission measure for unique people. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `supplementary_method_entries.unique_teams` | null | Reported participation/submission measure for unique teams. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `supplementary_method_entries.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `teams_with_final_submission` | integer | Reported participation/submission measure for teams with final submission. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `teams_with_submission` | null / integer | Number of teams with at least one qualifying submission in the recorded scope. |
| `track_team_counts` | array; items: object | Reported participation/submission measure for track team counts. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |
| `track_team_counts[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `track_team_counts[].teams_with_submission` | integer | Number of teams with at least one qualifying submission in the recorded scope. |
| `validation_teams` | integer | Reported participation/submission measure for validation teams. Preserve whether the entity is a person, account, team, algorithm or submission and the stated phase/date. |

<a id="resource-information-review"></a>

## `resource_information_review`

JSON parent path: `challenge.resource_information_review`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.resource_information_review`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `codebook` | string | Identifier/path of the operational coding definitions used in the original review. |
| `fields` | object | Named variables examined in the enclosing review; child keys identify the individual coding domains. |
| `fields.geography` | object | Explicit acquisition geography or identifiable source locations, retaining partial coverage and plans. |
| `fields.geography.evidence` | array; items: object | Source-linked observations supporting the enclosing variable or assessment; preserve type, scope and date. |
| `fields.geography.evidence[].excerpt` | string | Passage copied or extracted from a supporting source for the enclosing item. |
| `fields.geography.evidence[].kind` | string | Type of observation or evidence item used in the enclosing review. |
| `fields.geography.evidence[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `fields.geography.evidence[].snapshot` | string | Identifier or path of the snapshot in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `fields.geography.evidence[].snapshot_date` | string | Date associated with snapshot. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `fields.geography.evidence[].source_field` | string | Field within the original record from which an observation was extracted. |
| `fields.geography.evidence[].source_path` | string | Path of the original source or evidence record; archive paths may refer to files not included in this package. |
| `fields.geography.evidence[].sources` | array; items: object | Sources supporting the enclosing statement or dataset description, preserving document/source type and scope. |
| `fields.geography.evidence[].sources[].local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `fields.geography.evidence[].sources[].local_source` | string | Path identifying a source in the original review archive, not a downloadable file inside this release. |
| `fields.geography.evidence[].sources[].qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `fields.geography.evidence[].sources[].retrieval_scope` | string | Task, phase, cohort or source boundaries of retrieval. |
| `fields.geography.evidence[].sources[].retrieved_on` | string | Date when the cited source was retrieved or captured. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `fields.geography.evidence[].sources[].reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `fields.geography.evidence[].sources[].section` | string | Section, figure, table or location within a supporting source. |
| `fields.geography.evidence[].sources[].snapshot_sha256` | string | Cryptographic checksum or revision identifier for the enclosing snapshot; used for provenance rather than as a scientific measurement. |
| `fields.geography.evidence[].sources[].source_accessible` | boolean | Whether the condition “source accessible” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `fields.geography.evidence[].sources[].source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `fields.geography.evidence[].sources[].supports` | array; items: string | Statements or fields that the source is recorded as supporting, limited by the source's actual task, phase and evidence scope. |
| `fields.geography.evidence[].sources[].type` | string | Type of the enclosing source, document, artifact, observation or event; its vocabulary is specific to that parent context. |
| `fields.geography.evidence[].sources[].url` | null / string | Web address of the enclosing source, document or resource. |
| `fields.geography.evidence[].summary` | string | Concise summary of the enclosing source, review or observation. |
| `fields.geography.evidence[].url` | string | Web address of the enclosing source, document or resource. |
| `fields.geography.evidence[].value` | null / string / object | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.geography.evidence[].value.anonymized` | null / boolean | Whether anonymization/de-identification is explicitly reported for the dataset. |
| `fields.geography.evidence[].value.cancer_type_count` | integer | Reported numerical value for cancer type count within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `fields.geography.evidence[].value.center_count` | null / integer | Number of acquisition/source centers in the stated data scope; not the number of organizer institutions. |
| `fields.geography.evidence[].value.center_type` | null | Source-center structure described for the dataset, such as single-center, multicenter or multinational. |
| `fields.geography.evidence[].value.collection_period` | object | Period during which the underlying imaging/data were acquired, distinct from the metadata collection date. |
| `fields.geography.evidence[].value.collection_period.end_year` | null | Last year of the enclosing acquisition period or explicitly identified interval. |
| `fields.geography.evidence[].value.collection_period.start_year` | null | First year of the enclosing acquisition period or explicitly identified interval. |
| `fields.geography.evidence[].value.contributing_institution_count` | integer | Number of institutions explicitly contributing to the stated data/resource scope. |
| `fields.geography.evidence[].value.countries` | array; items: string | Structured entries for countries within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fields.geography.evidence[].value.country_count` | integer | Number of explicitly represented countries in the stated source scope; not a claim of population representativeness. |
| `fields.geography.evidence[].value.data_components` | null / array; items: string | Types of images, labels, metadata or outcomes included in the dataset. |
| `fields.geography.evidence[].value.dataset_structure` | object | Structured entries for dataset structure within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fields.geography.evidence[].value.dataset_structure.external_validation` | string | Description of an external validation data source or setting; assess source independence from its accompanying evidence. |
| `fields.geography.evidence[].value.dataset_structure.training_reference` | string | Supporting source reference for training. |
| `fields.geography.evidence[].value.ethical_approval` | null / boolean | Whether ethics approval is explicitly reported; this field is not an independent assessment of compliance. |
| `fields.geography.evidence[].value.institutions_description` | null / string | Source wording identifying or describing institutions contributing data. |
| `fields.geography.evidence[].value.international` | boolean | Whether the relevant organizers or dataset sources span countries, according to the enclosing field; not a population-representativeness claim. |
| `fields.geography.evidence[].value.modalities` | null / array; items: string | Structured entries for modalities within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fields.geography.evidence[].value.modality_count_observations` | array; items: object | Structured entries for modality count observations within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fields.geography.evidence[].value.modality_count_observations[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `fields.geography.evidence[].value.modality_count_observations[].value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.geography.evidence[].value.multi_center` | boolean | Whether acquisition at multiple centers is explicitly documented; does not imply institution-held-out testing. |
| `fields.geography.evidence[].value.population` | object | Population-level dataset quantities and characteristics, preserving their stated units. |
| `fields.geography.evidence[].value.population.image_series_count` | integer | Number of imaging series, distinct from patients, studies or individual images. |
| `fields.geography.evidence[].value.population.patient_count` | null / integer | Number of patients in the stated cohort or split; not interchangeable with studies, scans or images. Unit/format: patients; stated cohort/split. |
| `fields.geography.evidence[].value.population.scan_count` | object | Number of scans in the stated scope, possibly represented as a value/approximation/raw-text object. Unit/format: scans; stated cohort/split. |
| `fields.geography.evidence[].value.population.scan_count.approximate` | null / boolean | Whether the enclosing quantity is approximate rather than exact. |
| `fields.geography.evidence[].value.population.scan_count.raw_text` | null / string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `fields.geography.evidence[].value.population.scan_count.value` | null / integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.geography.evidence[].value.population.study_count` | null / integer | Number of studies/examinations in the stated cohort or split; a patient may contribute more than one. Unit/format: studys; stated cohort/split. |
| `fields.geography.evidence[].value.population.test_count` | null / integer / object | Test-set quantity in the unit explicitly specified by the enclosing source. |
| `fields.geography.evidence[].value.population.test_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `fields.geography.evidence[].value.population.test_count.lower_bound` | boolean | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `fields.geography.evidence[].value.population.test_count.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `fields.geography.evidence[].value.population.test_count.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `fields.geography.evidence[].value.population.test_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.geography.evidence[].value.population.train_count` | null / integer / object | Training-set quantity in the unit explicitly specified by the enclosing source. |
| `fields.geography.evidence[].value.population.train_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `fields.geography.evidence[].value.population.train_count.lower_bound` | boolean | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `fields.geography.evidence[].value.population.train_count.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `fields.geography.evidence[].value.population.train_count.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `fields.geography.evidence[].value.population.train_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.geography.evidence[].value.population.validation_count` | null / integer | Validation-set quantity in the unit explicitly specified by the enclosing source. |
| `fields.geography.evidence[].value.raw_whole_slide_images_available` | boolean | Whether the condition “raw whole slide images available” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `fields.geography.evidence[].value.reported_scope` | string | Task, phase, cohort or source boundaries of reported. |
| `fields.geography.evidence[].value.routine_clinical_practice` | null / boolean | Whether the dataset is explicitly described as originating from routine clinical practice. |
| `fields.geography.evidence[].value.slide_count_consistency` | string | Source-recorded slide count consistency for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `fields.geography.evidence[].value.slide_count_observations` | array; items: object | Structured entries for slide count observations within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fields.geography.evidence[].value.slide_count_observations[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `fields.geography.evidence[].value.slide_count_observations[].value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.geography.evidence[].value.source_datasets` | array; items: string | Structured entries for source datasets within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fields.geography.evidence[].value.source_type` | null / string | Kind of data or evidence source. In dataset records this describes cohort origin; in provenance it describes the supporting document or confirmation. |
| `fields.geography.evidence[].value.split_details` | object | Details or qualifications concerning dataset partitions, overlap, cohorts and quantity units. |
| `fields.geography.evidence[].value.split_details.batch1` | object | Source-defined batch1 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `fields.geography.evidence[].value.split_details.batch1.CTA_center4` | integer | Quantity for source-defined data subgroup `CTA_center4`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `fields.geography.evidence[].value.split_details.batch1.MRA_center2` | integer | Quantity for source-defined data subgroup `MRA_center2`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `fields.geography.evidence[].value.split_details.batch2` | object | Source-defined batch2 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `fields.geography.evidence[].value.split_details.batch2.CTA_center2` | integer | Quantity for source-defined data subgroup `CTA_center2`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `fields.geography.evidence[].value.split_details.batch2.CTA_center4` | integer | Quantity for source-defined data subgroup `CTA_center4`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `fields.geography.evidence[].value.split_details.batch2.MRA_center1` | integer | Quantity for source-defined data subgroup `MRA_center1`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `fields.geography.evidence[].value.split_details.batch2.MRA_public_center5` | integer | Quantity for source-defined data subgroup `MRA_public_center5`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `fields.geography.evidence[].value.split_details.count_unit` | string | Unit to which the reported count refers. |
| `fields.geography.evidence[].value.split_details.note` | string | Contextual qualification, uncertainty or source distinction for the enclosing item. |
| `fields.geography.evidence[].value.split_details.stated_total_pairs` | integer | Quantity for source-defined data subgroup `stated_total_pairs`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `fields.geography.evidence[].value.split_details.test` | string | Test-stage subset, quantity, procedure or outcome under the parent field; preserve its recorded unit and phase. |
| `fields.geography.evidence[].value.split_details.test_Instituto_Alexander_Fleming_Argentina` | integer | Quantity for source-defined data subgroup `test_Instituto_Alexander_Fleming_Argentina`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `fields.geography.evidence[].value.split_details.test_Radboud_Netherlands` | integer | Quantity for source-defined data subgroup `test_Radboud_Netherlands`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `fields.geography.evidence[].value.split_details.test_phase1` | integer | Quantity for source-defined data subgroup `test_phase1`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `fields.geography.evidence[].value.split_details.test_phase2` | integer | Quantity for source-defined data subgroup `test_phase2`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `fields.geography.evidence[].value.split_details.train_unique_patients` | integer | Quantity for source-defined data subgroup `train_unique_patients`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `fields.geography.evidence[].value.split_details.training` | string | Training-stage data, quantities, rules or model-use arrangements, according to the parent field. |
| `fields.geography.evidence[].value.split_details.training_ATLAS_v2_train_and_former_validation` | integer | Quantity for source-defined data subgroup `training_ATLAS_v2_train_and_former_validation`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `fields.geography.evidence[].value.split_details.training_SOOP` | integer | Quantity for source-defined data subgroup `training_SOOP`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `fields.geography.evidence[].value.split_details.training_new` | integer | Quantity for source-defined data subgroup `training_new`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `fields.geography.evidence[].value.split_details.validation` | string | Validation-stage data, quantities, submissions or results; not automatically final-test evidence. |
| `fields.geography.evidence[].value.test_image_mask_pairs` | object | Structured entries for test image mask pairs within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fields.geography.evidence[].value.test_image_mask_pairs.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `fields.geography.evidence[].value.test_image_mask_pairs.lower_bound` | boolean | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `fields.geography.evidence[].value.test_image_mask_pairs.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `fields.geography.evidence[].value.test_image_mask_pairs.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.geography.prior_narrow_state` | string | Documentary coding state of prior narrow. Preserve the task/phase scope and source qualifications. |
| `fields.geography.state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. |
| `fields.post_challenge_resources` | object | Continuing data, code or evaluation resources, policies or plans identified for the edition; these evidence types remain distinct. |
| `fields.post_challenge_resources.evidence` | array; items: object | Source-linked observations supporting the enclosing variable or assessment; preserve type, scope and date. |
| `fields.post_challenge_resources.evidence[].excerpt` | string | Passage copied or extracted from a supporting source for the enclosing item. |
| `fields.post_challenge_resources.evidence[].kind` | string | Type of observation or evidence item used in the enclosing review. |
| `fields.post_challenge_resources.evidence[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `fields.post_challenge_resources.evidence[].snapshot` | string | Identifier or path of the snapshot in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `fields.post_challenge_resources.evidence[].snapshot_date` | string | Date associated with snapshot. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `fields.post_challenge_resources.evidence[].source_field` | string | Field within the original record from which an observation was extracted. |
| `fields.post_challenge_resources.evidence[].source_path` | string | Path of the original source or evidence record; archive paths may refer to files not included in this package. |
| `fields.post_challenge_resources.evidence[].sources` | array; items: object | Sources supporting the enclosing statement or dataset description, preserving document/source type and scope. |
| `fields.post_challenge_resources.evidence[].sources[].basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `fields.post_challenge_resources.evidence[].sources[].limits` | string | Set of limits applied to the enclosing resources or procedures. |
| `fields.post_challenge_resources.evidence[].sources[].local_pdf` | string | Identifier or path of the local pdf in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `fields.post_challenge_resources.evidence[].sources[].local_snapshot` | null / string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `fields.post_challenge_resources.evidence[].sources[].local_source` | string | Path identifying a source in the original review archive, not a downloadable file inside this release. |
| `fields.post_challenge_resources.evidence[].sources[].locations` | string | Source-recorded locations for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `fields.post_challenge_resources.evidence[].sources[].propagated_on` | string | Date an existing review decision/evidence item was copied into the canonical record; not a new external verification date. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `fields.post_challenge_resources.evidence[].sources[].retrieval_scope` | string | Task, phase, cohort or source boundaries of retrieval. |
| `fields.post_challenge_resources.evidence[].sources[].retrieved_on` | string | Date when the cited source was retrieved or captured. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `fields.post_challenge_resources.evidence[].sources[].review_record` | string | Identifier/path of the corresponding review entry or ledger; it may refer to an unbundled archive. |
| `fields.post_challenge_resources.evidence[].sources[].reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `fields.post_challenge_resources.evidence[].sources[].section` | string | Section, figure, table or location within a supporting source. |
| `fields.post_challenge_resources.evidence[].sources[].source_accessible` | boolean | Whether the condition “source accessible” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `fields.post_challenge_resources.evidence[].sources[].source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `fields.post_challenge_resources.evidence[].sources[].supports` | array; items: string | Statements or fields that the source is recorded as supporting, limited by the source's actual task, phase and evidence scope. |
| `fields.post_challenge_resources.evidence[].sources[].title` | string | Title of the enclosing source document, publication, method or programme entry. |
| `fields.post_challenge_resources.evidence[].sources[].type` | string | Type of the enclosing source, document, artifact, observation or event; its vocabulary is specific to that parent context. |
| `fields.post_challenge_resources.evidence[].sources[].url` | null / string | Web address of the enclosing source, document or resource. |
| `fields.post_challenge_resources.evidence[].summary` | string | Concise summary of the enclosing source, review or observation. |
| `fields.post_challenge_resources.evidence[].url` | string | Web address of the enclosing source, document or resource. |
| `fields.post_challenge_resources.evidence[].value` | null / boolean / string / array; items: object | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.post_challenge_resources.evidence[].value[].official_phase_name` | string | Phase name exactly as shown by the organizer or platform. |
| `fields.post_challenge_resources.evidence[].value[].submission_count` | integer | Number of submission count in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.post_challenge_resources.prior_narrow_state` | string | Documentary coding state of prior narrow. Preserve the task/phase scope and source qualifications. |
| `fields.post_challenge_resources.state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. |
| `fields.reported_participation` | object | Reported team/person participation observations with original units and task/phase scope. |
| `fields.reported_participation.evidence` | array; items: object | Source-linked observations supporting the enclosing variable or assessment; preserve type, scope and date. |
| `fields.reported_participation.evidence[].excerpt` | string | Passage copied or extracted from a supporting source for the enclosing item. |
| `fields.reported_participation.evidence[].kind` | string | Type of observation or evidence item used in the enclosing review. |
| `fields.reported_participation.evidence[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `fields.reported_participation.evidence[].snapshot` | string | Identifier or path of the snapshot in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `fields.reported_participation.evidence[].snapshot_date` | string | Date associated with snapshot. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `fields.reported_participation.evidence[].source_field` | string | Field within the original record from which an observation was extracted. |
| `fields.reported_participation.evidence[].source_path` | string | Path of the original source or evidence record; archive paths may refer to files not included in this package. |
| `fields.reported_participation.evidence[].sources` | array; items: object | Sources supporting the enclosing statement or dataset description, preserving document/source type and scope. |
| `fields.reported_participation.evidence[].sources[].local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `fields.reported_participation.evidence[].sources[].local_source` | string | Path identifying a source in the original review archive, not a downloadable file inside this release. |
| `fields.reported_participation.evidence[].sources[].retrieved_on` | string | Date when the cited source was retrieved or captured. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `fields.reported_participation.evidence[].sources[].section` | string | Section, figure, table or location within a supporting source. |
| `fields.reported_participation.evidence[].sources[].supports` | array; items: string | Statements or fields that the source is recorded as supporting, limited by the source's actual task, phase and evidence scope. |
| `fields.reported_participation.evidence[].sources[].title` | string | Title of the enclosing source document, publication, method or programme entry. |
| `fields.reported_participation.evidence[].sources[].type` | string | Type of the enclosing source, document, artifact, observation or event; its vocabulary is specific to that parent context. |
| `fields.reported_participation.evidence[].sources[].url` | string | Web address of the enclosing source, document or resource. |
| `fields.reported_participation.evidence[].summary` | string | Concise summary of the enclosing source, review or observation. |
| `fields.reported_participation.evidence[].url` | string | Web address of the enclosing source, document or resource. |
| `fields.reported_participation.evidence[].value` | object | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.reported_participation.evidence[].value.active_participants` | null | Number of active people under the source's definition and stated phase. |
| `fields.reported_participation.evidence[].value.active_teams` | null | Number of active teams under the source's definition and stated phase. |
| `fields.reported_participation.evidence[].value.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `fields.reported_participation.evidence[].value.comparable` | boolean | Whether the condition “comparable” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `fields.reported_participation.evidence[].value.details` | string | Source-recorded details for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `fields.reported_participation.evidence[].value.evaluated_algorithms` | integer | Number of evaluated algorithms in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.finalist_teams` | null / integer | Number of finalist teams; not necessarily all active teams in the competition. |
| `fields.reported_participation.evidence[].value.notes` | array; items: string | Contextual qualifications and source distinctions retained after removal of empty or exact redundant remarks. |
| `fields.reported_participation.evidence[].value.participants_with_submission` | null | Number of people/accounts with at least one qualifying submission in the recorded scope. |
| `fields.reported_participation.evidence[].value.participating_teams` | integer | Number of participating teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.qualified_teams` | null | Number of teams meeting the source's eligibility or qualification criterion. |
| `fields.reported_participation.evidence[].value.registered_participants` | integer | Number of registered people/accounts as reported; registration does not establish active participation. |
| `fields.reported_participation.evidence[].value.registered_teams` | null / integer | Number of registered teams as reported; distinct from teams submitting results. |
| `fields.reported_participation.evidence[].value.reported_counts` | array; items: object | Structured entries for reported counts within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fields.reported_participation.evidence[].value.reported_counts[].countries` | integer | Reported numerical value for countries within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `fields.reported_participation.evidence[].value.reported_counts[].researchers` | integer | Number of researchers in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.reported_counts[].reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `fields.reported_participation.evidence[].value.reported_counts[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `fields.reported_participation.evidence[].value.reported_counts[].source_type` | string | Kind of data or evidence source. In dataset records this describes cohort origin; in provenance it describes the supporting document or confirmation. |
| `fields.reported_participation.evidence[].value.reported_counts[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `fields.reported_participation.evidence[].value.reported_counts[].submissions` | integer | Submission-count information grouped by phase, task or platform scope. |
| `fields.reported_participation.evidence[].value.reported_counts[].teams` | integer | Number of teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.reported_participants` | object | Structured entries for reported participants within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fields.reported_participation.evidence[].value.reported_participants.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `fields.reported_participation.evidence[].value.reported_participants.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `fields.reported_participation.evidence[].value.reported_participants.relation` | string | Relationship between the enclosing observations, datasets or resources. |
| `fields.reported_participation.evidence[].value.reported_participants.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `fields.reported_participation.evidence[].value.reported_participants.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.reported_participation.evidence[].value.reported_participating_teams` | integer / object | Structured entries for reported participating teams within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fields.reported_participation.evidence[].value.reported_participating_teams.definition_limit` | string | Restriction on interpreting the source's definition or comparing its counts with other records. |
| `fields.reported_participation.evidence[].value.reported_participating_teams.location` | string | Location relevant to the enclosing event, source or execution description; not automatically an image-acquisition site. |
| `fields.reported_participation.evidence[].value.reported_participating_teams.source_term` | string | Original term used by the source for a counted entity or category. |
| `fields.reported_participation.evidence[].value.reported_participating_teams.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `fields.reported_participation.evidence[].value.reported_participating_teams.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `fields.reported_participation.evidence[].value.reported_participating_teams.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.reported_participation.evidence[].value.source_reported_counts` | array; items: object | Structured entries for source reported counts within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fields.reported_participation.evidence[].value.source_reported_counts[].interpretation` | string | Reviewer's scoped interpretation of the recorded source information; not additional organizer evidence. |
| `fields.reported_participation.evidence[].value.source_reported_counts[].open_validation_submissions` | integer | Number of open validation submissions in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.source_reported_counts[].publication_date` | string | Date associated with publication. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `fields.reported_participation.evidence[].value.source_reported_counts[].reported_participants` | integer | Number of reported participants in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.source_reported_counts[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `fields.reported_participation.evidence[].value.source_reported_counts[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `fields.reported_participation.evidence[].value.statistics_snapshot_date` | string | Date on which the participation/platform figures were observed, not a competition or data-acquisition date. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `fields.reported_participation.evidence[].value.statistics_status` | string | Temporal or interpretive status of the participation snapshot, such as post-challenge or cumulative. |
| `fields.reported_participation.evidence[].value.submissions` | object | Submission-count information grouped by phase, task or platform scope. |
| `fields.reported_participation.evidence[].value.submissions.by_phase` | array; items: object | Entries broken down by competition phase; counts can involve the same teams across phases. |
| `fields.reported_participation.evidence[].value.submissions.by_phase[].official_phase_name` | string | Phase name exactly as shown by the organizer or platform. |
| `fields.reported_participation.evidence[].value.submissions.by_phase[].submission_count` | integer | Number of submission count in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.submissions.by_task` | null | Entries broken down by task; entries can involve overlapping teams or data. |
| `fields.reported_participation.evidence[].value.submissions.directory_summary_submissions` | null | Submission count shown in a platform directory summary at the observation date; scope can span phases or editions. |
| `fields.reported_participation.evidence[].value.submissions.total_submissions` | null | Number of submission attempts or entries within the stated scope, not the number of independent teams. |
| `fields.reported_participation.evidence[].value.task1_listed_teams` | integer | Number of task1 listed teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.task2_listed_teams` | integer | Number of task2 listed teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.teams_with_final_submission` | integer | Number of teams with final submission in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.teams_with_submission` | integer | Number of teams with at least one qualifying submission in the recorded scope. |
| `fields.reported_participation.evidence[].value.track_team_counts` | array; items: object | Structured entries for track team counts within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fields.reported_participation.evidence[].value.track_team_counts[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `fields.reported_participation.evidence[].value.track_team_counts[].teams_with_submission` | integer | Number of teams with at least one qualifying submission in the recorded scope. |
| `fields.reported_participation.evidence[].value.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `fields.reported_participation.evidence[].value.validation_teams` | integer | Number of validation teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.reported_participation.prior_narrow_state` | string | Documentary coding state of prior narrow. Preserve the task/phase scope and source qualifications. |
| `fields.reported_participation.state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. |
| `method` | string | Method or procedure used for the enclosing evaluation, extraction or analysis; preserve whether organizer-defined or reviewer-applied. |
| `reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |

[Back to README](../../README.md#variable-dictionary)
