# Schedule and competition phases

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

Phase dates, deadlines, revisions, date sources and timezone qualifications.

## Field groups

- [`challenge.schedule`](#schedule)

<a id="schedule"></a>

## `schedule`

JSON parent path: `challenge.schedule`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.schedule`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `algorithm_development_end` | string | Scheduled, revised or observed time for algorithm development end. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `algorithm_development_start` | string | Scheduled, revised or observed time for algorithm development start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `award_certificate_date` | string | Date associated with award certificate. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `batch1_training_release` | string | Scheduled, revised or observed time for batch1 training release. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `batch2_training_release` | string | Scheduled, revised or observed time for batch2 training release. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `challenge_announcement` | string | Scheduled, revised or observed time for challenge announcement. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `challenge_event` | null / string | Scheduled, revised or observed time for challenge event. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `challenge_launch` | string | Scheduled, revised or observed time for challenge launch. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `championship_phase_end` | string | Scheduled, revised or observed time for championship phase end. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `championship_phase_start` | string | Scheduled, revised or observed time for championship phase start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `classification_phase_end` | string | Scheduled, revised or observed time for classification phase end. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `conflicting_schedule_evidence` | object | Recorded documentary support for conflicting schedule. Preserve the task/phase scope and source qualifications. |
| `conflicting_schedule_evidence.organizer_source` | string | Source supporting organizer. |
| `conflicting_schedule_evidence.platform_advertised_close` | string | Source-recorded platform advertised close for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `conflicting_schedule_evidence.platform_evidence_scope` | string | Task, phase, cohort or source boundaries of platform evidence. |
| `conflicting_schedule_evidence.platform_source` | string | Source supporting platform. |
| `conflicting_schedule_evidence.platform_timezone` | null | Optional field for platform timezone in the enclosing record. It is unpopulated in this snapshot; neither a value nor a negative finding is established. |
| `conflicting_schedule_evidence.resolution` | string | Resolution of a recorded evidence conflict in review objects, or image/spatial resolution in imaging descriptions; use the parent field to distinguish them. |
| `conflicting_schedule_evidence.year_qualification` | string | Source-recorded year qualification for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `deadline_timezone` | string | Scheduled, revised or observed time for deadline timezone. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `development_end` | string | Scheduled, revised or observed time for development end. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `development_submission_start` | string | Scheduled, revised or observed time for development submission start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `documented_competition_period` | object | Structured entries for documented competition period within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `documented_competition_period.end` | string | Scheduled, revised or observed time for end. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `documented_competition_period.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `documented_competition_period.start` | string | Scheduled, revised or observed time for start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `edition_year` | integer | Calendar year assigned to edition; preserve whether this concerns an edition, analysis, event or publication. |
| `evaluation_end` | string | Scheduled, revised or observed time for evaluation end. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `evaluation_month` | string | Source-recorded evaluation month for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `evaluation_start` | string | Scheduled, revised or observed time for evaluation start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `final_event_period` | string | Scheduled, revised or observed time for final event period. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `final_phase_start` | string | Scheduled, revised or observed time for final phase start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `final_submission_confirmation` | string | Source-recorded final submission confirmation for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `final_submission_deadline` | null / string | Scheduled, revised or observed time for final submission deadline. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `final_submission_end` | null / string | Scheduled, revised or observed time for final submission end. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `final_submission_start` | string | Scheduled, revised or observed time for final submission start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `final_test` | object | Structured entries for final test within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `final_test.date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `final_test.encrypted_data_available` | string | Source-recorded encrypted data available for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `final_test.password_release_time` | string | Scheduled, revised or observed time for password release time. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `final_test.prediction_upload_deadline_time` | string | Scheduled, revised or observed time for prediction upload deadline time. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `final_test.source_reference` | string | Reference to the supporting document or source, possibly with section, URL and archival location. |
| `final_test.timezone` | null | Timezone specified for the enclosing schedule or observation; null means it was not established. |
| `final_test_results_date` | string | Date associated with final test results. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `final_test_results_date_review` | object | Source-linked review of final test results date. |
| `final_test_results_date_review.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `final_test_results_date_review.event` | string | Conference, workshop or other event affiliation and its edition-specific context. |
| `final_test_results_date_review.evidence_state` | string | State of the documentary evidence for the specific field or assessment, retaining ambiguity, missingness and structural non-applicability. |
| `final_test_results_date_review.interpreted_date` | string | Date associated with interpreted. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `final_test_results_date_review.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `final_test_results_date_review.source_date` | string | Date associated with source. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `final_test_results_date_review.source_text` | string | Original source wording supporting the enclosing field. |
| `final_test_results_date_review.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `final_test_submission_deadline` | string | Scheduled, revised or observed time for final test submission deadline. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `final_test_submission_start` | string | Scheduled, revised or observed time for final test submission start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `finalist_presentation` | string | Scheduled, revised or observed time for finalist presentation. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `full_training_release` | string | Scheduled, revised or observed time for full training release. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `kickoff_webinar` | string | Scheduled, revised or observed time for kickoff webinar. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `leaderboard_release` | string | Scheduled, revised or observed time for leaderboard release. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `method_description_deadline` | string | Scheduled, revised or observed time for method description deadline. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `model_submission_end` | null | Scheduled, revised or observed time for model submission end. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `open_submission_cycle_planned_start` | string | Scheduled, revised or observed time for open submission cycle planned start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `opening` | string | Scheduled, revised or observed time for opening. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `original_announced_schedule` | object | Structured entries for original announced schedule within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `original_announced_schedule.challenge_event` | string | Scheduled, revised or observed time for challenge event. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `original_announced_schedule.evaluation_setup_end` | string | Scheduled, revised or observed time for evaluation setup end. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `original_announced_schedule.evaluation_setup_start` | string | Scheduled, revised or observed time for evaluation setup start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `original_announced_schedule.model_submission_end` | string | Scheduled, revised or observed time for model submission end. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `original_announced_schedule.registration_end` | string | Scheduled, revised or observed time for registration end. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `original_announced_schedule.testing_end` | string | Scheduled, revised or observed time for testing end. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `original_announced_schedule.testing_start` | string | Scheduled, revised or observed time for testing start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `original_schedule_status` | string | Recorded state of original schedule. Preserve the task/phase scope and source qualifications. |
| `paper_submission_deadline` | string | Scheduled, revised or observed time for paper submission deadline. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `paper_submission_end` | string | Scheduled, revised or observed time for paper submission end. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `phase1` | string | Source-defined phase1 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `phase2` | string | Source-defined phase2 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `phase2_review` | string | Source-linked review of phase2. |
| `planned_awards` | object | Structured entries for planned awards within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `planned_awards.competition_name_on_program` | string | Competition title shown in the cited conference programme. |
| `planned_awards.date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `planned_awards.end_time` | string | Scheduled, revised or observed time for end time. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `planned_awards.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `planned_awards.start_time` | string | Scheduled, revised or observed time for start time. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `planned_awards.status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `planned_awards.timezone` | string | Timezone specified for the enclosing schedule or observation; null means it was not established. |
| `planned_awards.venue` | string | Named venue of an event or publication, according to its enclosing record. |
| `post_challenge_end` | string | Scheduled, revised or observed time for post challenge end. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `post_challenge_start` | string | Scheduled, revised or observed time for post challenge start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `postponement_announcement` | string | Scheduled, revised or observed time for postponement announcement. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `pre_evaluation_deadline` | string | Scheduled, revised or observed time for pre evaluation deadline. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `preliminary_phase_start` | string | Scheduled, revised or observed time for preliminary phase start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `protocol_reference` | object | Reference to the edition-specific protocol supporting the enclosing field; a protocol describes specification rather than proof of execution. |
| `protocol_reference.local_protocol` | string | Original archive path of a registered protocol; the protocol file itself is not included in this metadata package. |
| `protocol_reference.registered_task_index` | integer | Task position/identifier in the registered protocol; it can differ from later operational numbering. |
| `protocol_reference.section` | string | Section, figure, table or location within a supporting source. |
| `protocol_reference.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `registration_deadline` | string | Scheduled, revised or observed time for registration deadline. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `registration_end` | string | Scheduled, revised or observed time for registration end. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `registration_end_scope` | string | Task, phase, cohort or source boundaries of registration end. |
| `registration_start` | string | Scheduled, revised or observed time for registration start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `reopening` | string | Scheduled, revised or observed time for reopening. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `reported_deadline_source` | string | Source supporting reported deadline. |
| `reported_deadline_source_type` | string | Scheduled, revised or observed time for reported deadline source type. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `reported_final_deadline_month` | string | Scheduled, revised or observed time for reported final deadline month. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `results_announcement` | string | Scheduled, revised or observed time for results announcement. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `results_event_date` | string | Date associated with results event. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `results_release` | string | Scheduled, revised or observed time for results release. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `source_reference` | string | Reference to the supporting document or source, possibly with section, URL and archival location. |
| `status_note` | string | Qualification or source distinction concerning status. |
| `submission_open` | string | Source-recorded submission open for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `submission_start` | null / string | Scheduled, revised or observed time for submission start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `task1_data_release` | string | Scheduled, revised or observed time for task1 data release. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `task1_training_release_listed` | string | Scheduled, revised or observed time for task1 training release listed. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `task1_validation_release_listed` | string | Scheduled, revised or observed time for task1 validation release listed. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `task2_data_release` | string | Scheduled, revised or observed time for task2 data release. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `test1_deadline` | string | Scheduled, revised or observed time for test1 deadline. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `test2_deadline` | string | Scheduled, revised or observed time for test2 deadline. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `test2_start` | string | Scheduled, revised or observed time for test2 start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `test_data_public_release` | string | Scheduled, revised or observed time for test data public release. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `test_data_release` | string | Scheduled, revised or observed time for test data release. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `test_end` | string | Scheduled, revised or observed time for test end. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `test_phase_start` | string | Scheduled, revised or observed time for test phase start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `test_release` | string | Scheduled, revised or observed time for test release. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `test_start` | string | Scheduled, revised or observed time for test start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `test_submission_start` | string | Scheduled, revised or observed time for test submission start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `test_validation_release` | string | Scheduled, revised or observed time for test validation release. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `testing_end` | null | Scheduled, revised or observed time for testing end. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `testing_start` | null | Scheduled, revised or observed time for testing start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `topbrainv2_final_test` | object | Structured entries for topbrainv2 final test within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `topbrainv2_final_test.phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. |
| `topbrainv2_final_test.planned_opening_date` | string | Date associated with planned opening. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `topbrainv2_final_test.planned_opening_time_displayed` | string | Scheduled, revised or observed time for planned opening time displayed. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `topbrainv2_final_test.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `topbrainv2_final_test.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `topbrainv2_final_test.status_as_of_review` | string | Source-linked review of status as of. |
| `topbrainv2_final_test.timezone` | null | Timezone specified for the enclosing schedule or observation; null means it was not established. |
| `topbrainv2_final_test.verified_on` | string | Date of the specific verification described in the enclosing record. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `training_data_release` | string | Scheduled, revised or observed time for training data release. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `training_release` | string | Scheduled, revised or observed time for training release. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `validation_data_release` | string | Scheduled, revised or observed time for validation data release. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `validation_end` | string | Scheduled, revised or observed time for validation end. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `validation_phase_start` | string | Scheduled, revised or observed time for validation phase start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `validation_start` | string | Scheduled, revised or observed time for validation start. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `vein_stenosis_activity_period` | string | Source-recorded vein stenosis activity period for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `virtual_kickoff_revised` | string | Scheduled, revised or observed time for virtual kickoff revised. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `winner_announcement` | string | Scheduled, revised or observed time for winner announcement. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `winner_notification` | string | Scheduled, revised or observed time for winner notification. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `winners_announcement` | string | Scheduled, revised or observed time for winners announcement. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `year_evidence` | string | Recorded documentary support for year. Preserve the task/phase scope and source qualifications. |
| `year_specific_review` | object | Source-linked review of year specific. |
| `year_specific_review.interpretation` | string | Reviewer's scoped interpretation of the recorded source information; not additional organizer evidence. |
| `year_specific_review.official_page_heading` | string | Source-recorded official page heading for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `year_specific_review.page_mixes_years` | boolean | Whether the condition “page mixes years” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `year_specific_review.result_announcement_status_on_page` | string | Scheduled, revised or observed time for result announcement status on page. Preserve the original precision, timezone and source-specific status; a scheduled date does not establish occurrence. |
| `year_specific_review.stale_content` | string | Source-recorded stale content for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |

[Back to README](../../README.md#variable-dictionary)
