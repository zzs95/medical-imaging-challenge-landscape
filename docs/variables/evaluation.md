# Evaluation, metrics, rankings and results

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

Scoring procedures, metrics, ranking rules and source-scoped result evidence.

## Field groups

- [`challenge.evaluation`](#evaluation)
- [`challenge.result_evidence_review`](#result-evidence-review)

<a id="evaluation"></a>

## `evaluation`

JSON parent path: `challenge.evaluation`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.evaluation`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `additional_assessments` | object | Structured entries for additional assessments within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `additional_assessments.boston_external_testing` | object | Structured entries for boston external testing within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `additional_assessments.boston_external_testing.declared` | boolean | Whether the condition “declared” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `additional_assessments.boston_external_testing.design_source` | string | Source supporting design. |
| `additional_assessments.boston_external_testing.execution_status` | string | Recorded state of execution. Preserve the task/phase scope and source qualifications. |
| `additional_assessments.boston_external_testing.performed` | null | Whether the specified assessment or action was performed, according to its documented evidence state and scope. |
| `additional_assessments.expert_radiologist_assessment` | object | Structured entries for expert radiologist assessment within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `additional_assessments.expert_radiologist_assessment.declared` | boolean | Whether the condition “declared” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `additional_assessments.expert_radiologist_assessment.design_source` | string | Source supporting design. |
| `additional_assessments.expert_radiologist_assessment.execution_status` | string | Recorded state of execution. Preserve the task/phase scope and source qualifications. |
| `additional_assessments.expert_radiologist_assessment.performed` | null | Whether the specified assessment or action was performed, according to its documented evidence state and scope. |
| `additional_assessments.report_supervised_multi_tumor_segmentation` | object | Structured entries for report supervised multi tumor segmentation within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `additional_assessments.report_supervised_multi_tumor_segmentation.declared` | boolean | Whether the condition “declared” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `additional_assessments.report_supervised_multi_tumor_segmentation.design_source` | string | Source supporting design. |
| `additional_assessments.report_supervised_multi_tumor_segmentation.execution_status` | string | Recorded state of execution. Preserve the task/phase scope and source qualifications. |
| `additional_assessments.report_supervised_multi_tumor_segmentation.performed` | null | Whether the specified assessment or action was performed, according to its documented evidence state and scope. |
| `additional_assessments.report_supervised_multi_tumor_segmentation.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `automatic_scoring_trigger` | null | Event or procedure that triggers automatic score computation, when documented. |
| `caption_baseline_evidence` | object | Recorded documentary support for caption baseline. Preserve the task/phase scope and source qualifications. |
| `caption_baseline_evidence.assessment_type` | string | Kind of evaluation performed or proposed, retaining differences among task scores, expert review and other assessments. |
| `caption_baseline_evidence.caption_baseline_assessment` | string | Evidence/status of evaluating a baseline caption-generation method, distinct from competitive final evaluation. |
| `caption_baseline_evidence.competition_caption_final_assessment` | string | Evidence/status specifically for final competition caption assessment, not validation-only results. |
| `caption_baseline_evidence.count_as_confirmed_competition_caption_assessment` | boolean | Whether the condition “count as confirmed competition caption assessment” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `caption_baseline_evidence.dataset_scope_note` | string | Qualification or source distinction concerning dataset scope. |
| `caption_baseline_evidence.interpretation` | string | Reviewer's scoped interpretation of the recorded source information; not additional organizer evidence. |
| `caption_baseline_evidence.metrics` | array; items: string | Metrics assigned to the enclosing task or assessment; a metric list alone does not define the ranking formula. |
| `caption_baseline_evidence.models` | array; items: string | Structured entries for models within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `caption_baseline_evidence.results` | array; items: object | Reported findings or results for the enclosing task, phase, method or publication. |
| `caption_baseline_evidence.results[].BLEU-1` | number | Reported value or specification of the source-named metric `BLEU-1` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `caption_baseline_evidence.results[].BLEU-4` | number | Reported value or specification of the source-named metric `BLEU-4` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `caption_baseline_evidence.results[].METEOR` | number | Reported value or specification of the source-named metric `METEOR` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `caption_baseline_evidence.results[].ROUGE-1` | number | Reported value or specification of the source-named metric `ROUGE-1` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `caption_baseline_evidence.results[].ROUGE-L` | number | Reported value or specification of the source-named metric `ROUGE-L` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `caption_baseline_evidence.results[].cosine_similarity` | number | Reported value or specification of the source-named metric `cosine_similarity` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `caption_baseline_evidence.results[].model` | string | Model named or described in the enclosing entry; not evidence of the challenge's organizer-defined objective by itself. |
| `caption_baseline_evidence.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `caption_baseline_evidence.sample_count` | integer | Number of source-defined samples; interpret with sample_unit or the original source wording. |
| `caption_baseline_evidence.sample_unit` | string | Definition of one sample in the reported evaluation or dataset quantity. |
| `caption_baseline_evidence.snapshot` | string | Identifier or path of the snapshot in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `caption_baseline_evidence.source_location` | string | Location of the source passage or evidence item within the original document/archive. |
| `caption_baseline_evidence.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `caption_competition_evidence` | object | Recorded documentary support for caption competition. Preserve the task/phase scope and source qualifications. |
| `caption_competition_evidence.baseline_separation` | string | Explanation separating organizer/local baseline experiments from competition assessment evidence. |
| `caption_competition_evidence.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `caption_competition_evidence.caption_competition_assessment` | string | Evidence/status of competitive caption assessment in the specified phase. |
| `caption_competition_evidence.declared_captioning_objective` | string | Source-recorded declared captioning objective for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `caption_competition_evidence.evidence_state` | string | State of the documentary evidence for the specific field or assessment, retaining ambiguity, missingness and structural non-applicability. |
| `caption_competition_evidence.include_in_confirmed_caption_assessment_count` | boolean | Whether the condition “include in confirmed caption assessment count” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `caption_competition_evidence.independently_verified_complete_final_rankings` | string | Source-recorded independently verified complete final rankings for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `caption_competition_evidence.participant_paper_doi` | string | DOI of the participant publication cited as supporting the enclosing statement. |
| `caption_competition_evidence.published_evaluation_protocol` | string | Source-recorded published evaluation protocol for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `caption_competition_evidence.published_participant_result` | string | Source-recorded published participant result for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `caption_competition_evidence.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `caption_competition_evidence.supersedes` | string | Earlier statement or record that the enclosing revision replaces. |
| `caption_competition_evidence.verification_limit` | string | Specific limit on what was verified from the available source. |
| `caption_protocol_metrics` | object | Structured entries for caption protocol metrics within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `caption_protocol_metrics.evidence_basis` | string | Evidence or reasoning supporting evidence. |
| `caption_protocol_metrics.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `caption_protocol_metrics.metrics` | array; items: string | Metrics assigned to the enclosing task or assessment; a metric list alone does not define the ranking formula. |
| `caption_protocol_metrics.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `completion_evidence` | object | Recorded documentary support for completion. Preserve the task/phase scope and source qualifications. |
| `completion_evidence.event_state` | string | Documentary coding state of event. Preserve the task/phase scope and source qualifications. |
| `completion_evidence.evidence` | string | Source-linked observations supporting the enclosing variable or assessment; preserve type, scope and date. |
| `completion_evidence.evidence_ids` | array; items: string | Identifiers of specific evidence items supporting the enclosing interpretation; archival ledgers may be outside this package. |
| `completion_evidence.evidence_state` | string | State of the documentary evidence for the specific field or assessment, retaining ambiguity, missingness and structural non-applicability. |
| `completion_evidence.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `completion_evidence.note` | string | Contextual qualification, uncertainty or source distinction for the enclosing item. |
| `completion_evidence.overall_winner` | string | Winner identified for the stated overall competition scope, not necessarily winner of every component. |
| `completion_evidence.ranking_note` | string | Qualification or source distinction concerning ranking. |
| `completion_evidence.reason` | string | Reason for the enclosing decision, revision, exclusion or qualification. |
| `completion_evidence.results_presentation_event` | string | Source-recorded results presentation event for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `completion_evidence.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `completion_evidence.value` | string | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `completion_evidence.winning_teams` | array; items: string | Structured entries for winning teams within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `completion_review` | object | Source-linked review of completion. |
| `completion_review.event_state` | string | Documentary coding state of event. Preserve the task/phase scope and source qualifications. |
| `completion_review.evidence_ids` | array; items: string | Identifiers of specific evidence items supporting the enclosing interpretation; archival ledgers may be outside this package. |
| `completion_review.evidence_state` | string | State of the documentary evidence for the specific field or assessment, retaining ambiguity, missingness and structural non-applicability. |
| `completion_review.reason` | string | Reason for the enclosing decision, revision, exclusion or qualification. |
| `completion_review.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `completion_review.source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `completion_review.value` | string | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `cross_task_rule` | null / string | Rule linking outputs, assessments or rankings across tasks within the competition. |
| `design_document` | string | Registered protocol or other document describing the proposed challenge design. |
| `efficiency_metrics` | array; items: string | Structured entries for efficiency metrics within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `evaluated_task_scope` | array; items: object | Task, phase, cohort or source boundaries of evaluated task. |
| `evaluated_task_scope[].description` | string | Description of the enclosing entity, procedure, data or result as retained from the source or review. |
| `evaluated_task_scope[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `evaluated_task_scope[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `evaluation_execution` | string | Description or evidence state of running the relevant assessment procedure. |
| `evaluation_maps` | array; items: string | Structured entries for evaluation maps within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `event_conduct_evidence` | object | Recorded documentary support for event conduct. Preserve the task/phase scope and source qualifications. |
| `event_conduct_evidence.finding` | string | Specific documentary or analytical observation recorded from the source or review. |
| `event_conduct_evidence.limit` | string | Limit applied to the enclosing resource, score, submission or procedure; retain its unit and phase. |
| `event_conduct_evidence.location` | string | Location relevant to the enclosing event, source or execution description; not automatically an image-acquisition site. |
| `event_conduct_evidence.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `event_conduct_evidence.value` | string | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `executed_2025_scope` | object | Task, phase, cohort or source boundaries of executed 2025. |
| `executed_2025_scope.boston_external_test_used_for_official_evaluation_or_ranking` | boolean | Whether the condition “boston external test used for official evaluation or ranking” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `executed_2025_scope.expert_radiologist_human_evaluation_performed` | boolean | Whether the condition “expert radiologist human evaluation performed” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `executed_2025_scope.modalities` | array; items: string | Structured entries for modalities within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `executed_2025_scope.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `executed_2025_scope.source_role` | string | Role of the source, such as organizer protocol, participant report or supporting reference. |
| `executed_2025_scope.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `execution_details` | object | Structured entries for execution details within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `execution_details.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `execution_details.completed_execution_confirmed` | null | Recorded confirmation that the relevant execution occurred, retaining whether public documentation or human confirmation supplies the basis. |
| `execution_details.method` | string | Method or procedure used for the enclosing evaluation, extraction or analysis; preserve whether organizer-defined or reviewer-applied. |
| `execution_details.named_technical_service` | null | Technical service explicitly identified in the reviewed source; no execution mechanism is inferred from the service name alone. |
| `execution_details.note` | string | Contextual qualification, uncertainty or source distinction for the enclosing item. |
| `execution_details.operator` | string | Party operating the procedure or service described by the enclosing field. |
| `execution_details.physical_execution_environment` | null | Hardware/location environment in which the model or evaluation process is run, when explicitly documented. |
| `execution_details.responsible_party` | string | Person, organization or service responsible for the action described by the parent record. |
| `execution_details.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `execution_details.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `execution_details.submission_service` | null | Service receiving the scored submission, distinct from inference and scoring execution. |
| `execution_evidence_scope` | string | Task, phase, cohort or source boundaries of execution evidence. |
| `execution_mode` | string | How the relevant method or assessment is run, including participant versus organizer/platform execution where specified. |
| `execution_note` | string | Qualification or source distinction concerning execution. |
| `execution_operator` | string | Person, organization or platform responsible for executing the relevant method or assessment. |
| `fairness_variables` | array; items: string | Structured entries for fairness variables within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `final_assessment_evidence` | object | Recorded documentary support for final assessment. Preserve the task/phase scope and source qualifications. |
| `final_assessment_evidence.confirmation_basis` | string | Evidence or reasoning supporting confirmation. |
| `final_assessment_evidence.confirmation_record` | object | Structured entries for confirmation record within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `final_assessment_evidence.confirmation_record.confirmation_scope` | string | Task, phase, cohort or source boundaries of confirmation. |
| `final_assessment_evidence.confirmation_record.date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `final_assessment_evidence.confirmation_record.edition_id` | string | Identifier of the analytical edition used to join the index, inventory and individual record. |
| `final_assessment_evidence.confirmation_record.public_document_scope` | string | Task, phase, cohort or source boundaries of public document. |
| `final_assessment_evidence.confirmation_record.reviewer_name` | null | Name/identifier recorded for the person responsible for the enclosing review or confirmation. |
| `final_assessment_evidence.confirmation_record.reviewer_role` | string | Role of the reviewer or confirming person as described by the source. |
| `final_assessment_evidence.confirmation_record.rule_version` | string | Version/date of the rule set to which the enclosing procedure or qualification applies. |
| `final_assessment_evidence.confirmation_record.source_type` | string | Kind of data or evidence source. In dataset records this describes cohort origin; in provenance it describes the supporting document or confirmation. |
| `final_assessment_evidence.confirmation_record.statement` | string | Recorded statement supporting the enclosing confirmation, decision or source interpretation. |
| `final_assessment_evidence.confirmation_record.supporting_document` | string | Document cited to support the enclosing factual or review statement. |
| `final_assessment_evidence.event_state` | string | Documentary coding state of event. Preserve the task/phase scope and source qualifications. |
| `final_assessment_evidence.evidence_ids` | array; items: string | Identifiers of specific evidence items supporting the enclosing interpretation; archival ledgers may be outside this package. |
| `final_assessment_evidence.evidence_state` | string | State of the documentary evidence for the specific field or assessment, retaining ambiguity, missingness and structural non-applicability. |
| `final_assessment_evidence.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `final_assessment_evidence.public_documentary_final_assessment_confirmed` | boolean | Whether the condition “public documentary final assessment confirmed” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `final_assessment_evidence.reason` | string | Reason for the enclosing decision, revision, exclusion or qualification. |
| `final_assessment_evidence.rule_version` | string | Version/date of the rule set to which the enclosing procedure or qualification applies. |
| `final_assessment_evidence.value` | string | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `final_scoring_automated` | boolean | Whether the condition “final scoring automated” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `final_test_evaluated` | boolean | Whether the condition “final test evaluated” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `final_test_evidence_basis` | string | Evidence or reasoning supporting final test evidence. |
| `hidden_test_set` | null / boolean | Whether the designated test set or its protected component is described as hidden; read inputs/labels visibility separately. |
| `implemented_track_assessments` | array; items: object | Structured entries for implemented track assessments within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `implemented_track_assessments[].basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `implemented_track_assessments[].completion_status` | string | Recorded edition-level conduct or completion status; does not establish execution of every proposed assessment. |
| `implemented_track_assessments[].evidence_state` | string | State of the documentary evidence for the specific field or assessment, retaining ambiguity, missingness and structural non-applicability. |
| `implemented_track_assessments[].leaderboard_count` | integer | Reported numerical value for leaderboard count within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `implemented_track_assessments[].metrics` | array; items: string | Metrics assigned to the enclosing task or assessment; a metric list alone does not define the ranking formula. |
| `implemented_track_assessments[].reporting_strata` | array; items: string | Structured entries for reporting strata within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `implemented_track_assessments[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `implemented_track_assessments[].subtask_count` | integer | Number of subtasks represented in the stated task/source scope; not a count of separate annual editions. |
| `implemented_track_assessments[].track_id` | string | Identifier of a competition track; a track is not automatically a separate analytical edition. |
| `metrics` | null / array; items: object | Metrics assigned to the enclosing task or assessment; a metric list alone does not define the ranking formula. |
| `metrics[].averaging` | string | Rule for combining metric values across classes, cases or other units. |
| `metrics[].classes` | integer | Target class names, codes or their mapping within the stated task. |
| `metrics[].name` | string | Name of the enclosing task, institution, dataset, source, method or event; the parent field identifies the entity. |
| `metrics[].role` | string | Role of the enclosing task, source, artifact or person; context determines whether it is scored, auxiliary or supporting. |
| `metrics[].task` | string | Task name or task-specific result/description associated with the enclosing entry. |
| `metrics[].weight` | number | Weight assigned to the enclosing metric, class or scoring component in the specified formula. |
| `model_executor` | string | Party running the submitted model or algorithm in the described phase. |
| `official_final_ranking` | string | Organizer/platform record of final ranking for the stated task/edition scope. |
| `online_evaluation` | null / boolean | Whether an online evaluation process is specified or reported; does not by itself establish automated inference or scoring. |
| `overall_ranking` | string | Overall ranking rule or outcome across the components explicitly included by the organizer. |
| `phase_execution_evidence` | object | Recorded documentary support for phase execution. Preserve the task/phase scope and source qualifications. |
| `phase_execution_evidence.Phase I` | object | Source-defined Phase I branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `phase_execution_evidence.Phase I.count_scope` | string | Task, phase, cohort or source boundaries of count. |
| `phase_execution_evidence.Phase I.example` | object | Structured entries for example within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `phase_execution_evidence.Phase I.example.algorithm` | string | Algorithm or executable method named in the enclosing submission or evaluation record. |
| `phase_execution_evidence.Phase I.example.evaluation_url` | string | Web address for evaluation. |
| `phase_execution_evidence.Phase I.example.result_date` | string | Date associated with result. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `phase_execution_evidence.Phase I.example.score` | number | Reported score for the enclosing task, phase, metric or evaluation record; not automatically an overall final result. |
| `phase_execution_evidence.Phase I.example.status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `phase_execution_evidence.Phase I.example.submission_date` | string | Date associated with submission. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `phase_execution_evidence.Phase I.example.user` | string | Account or reviewer identity as recorded by the enclosing source; not a count of independent teams. |
| `phase_execution_evidence.Phase I.executed_assessment_status` | string | Recorded state of executed assessment. Preserve the task/phase scope and source qualifications. |
| `phase_execution_evidence.Phase I.public_leaderboard_rows` | integer | Reported numerical value for public leaderboard rows within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `phase_execution_evidence.Phase I.submission_count` | integer | Number of submission count in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `phase_execution_evidence.Phase II` | object | Source-defined Phase II branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `phase_execution_evidence.Phase II.eligible_competitive_final_scoring_status` | string | Recorded state of eligible competitive final scoring. Preserve the task/phase scope and source qualifications. |
| `phase_execution_evidence.Phase II.example` | object | Structured entries for example within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `phase_execution_evidence.Phase II.example.algorithm` | string | Algorithm or executable method named in the enclosing submission or evaluation record. |
| `phase_execution_evidence.Phase II.example.evaluation_url` | string | Web address for evaluation. |
| `phase_execution_evidence.Phase II.example.result_date` | string | Date associated with result. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `phase_execution_evidence.Phase II.example.score` | number | Reported score for the enclosing task, phase, metric or evaluation record; not automatically an overall final result. |
| `phase_execution_evidence.Phase II.example.status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `phase_execution_evidence.Phase II.example.submission_date` | string | Date associated with submission. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `phase_execution_evidence.Phase II.example.user` | string | Account or reviewer identity as recorded by the enclosing source; not a count of independent teams. |
| `phase_execution_evidence.Phase II.final_ranking_status` | string | Recorded state of final ranking. Preserve the task/phase scope and source qualifications. |
| `phase_execution_evidence.Phase II.public_leaderboard_rows` | integer | Reported numerical value for public leaderboard rows within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `phase_execution_evidence.Phase II.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `phase_execution_evidence.Phase II.submission_count` | integer | Number of submission count in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `phase_execution_evidence.Phase II.successful_scoring_record_exists` | boolean | Whether the condition “successful scoring record exists” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `phase_execution_evidence.Phase II.winner_announcement_status` | string | Recorded state of winner announcement. Preserve the task/phase scope and source qualifications. |
| `phase_scoring` | object | Structured entries for phase scoring within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `phase_scoring.final_test` | object | Structured entries for final test within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `phase_scoring.final_test.automated_container_execution` | string | Statement about automated execution of submitted containers; not established solely from the word Docker or a platform name. |
| `phase_scoring.final_test.classification_weight` | number | Coefficient assigned to the classification component in the specified composite score/ranking. |
| `phase_scoring.final_test.processing_time_weight` | number | Coefficient assigned to processing time in the specified composite score/ranking. |
| `phase_scoring.final_test.ranking_responsibility` | string | Party responsible for determining or publishing the ranking. |
| `phase_scoring.final_test.segmentation_weight` | number | Coefficient assigned to the segmentation component in the specified composite score/ranking. |
| `phase_scoring.final_test.time_normalization` | string | Rule for normalizing processing time when it enters an efficiency measure or composite score. |
| `phase_scoring.validation` | object | Validation-stage data, quantities, submissions or results; not automatically final-test evidence. |
| `phase_scoring.validation.immediate_automated_scoring_verified` | boolean | Whether the condition “immediate automated scoring verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `phase_scoring.validation.maximum_points` | integer | Maximum available points for the specified component or score. |
| `phase_scoring.validation.metrics` | array; items: string | Metrics assigned to the enclosing task or assessment; a metric list alone does not define the ranking formula. |
| `phase_scoring.validation.runtime_included` | boolean | Whether the condition “runtime included” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `phases` | array; items: object | Structured entries for phases within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `phases[].competition_id` | integer | Identifier of the competition on its hosting platform, not its analytical edition count. |
| `phases[].data_model_flow` | string | Direction of data/model exchange across the competition workflow, preserving phase-specific differences. |
| `phases[].eligible_participants` | string | Source-recorded eligible participants for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `phases[].evaluation_status` | string | Recorded state of evaluation. Preserve the task/phase scope and source qualifications. |
| `phases[].execution_evidence` | string | Evidence that the specified assessment or execution actually occurred within the recorded task and phase. |
| `phases[].inference_executor` | string | Party executing model inference on the designated evaluation inputs; distinct from the submission service or metric-computation party. |
| `phases[].phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. |
| `phases[].platform` | string | Named service involved in the enclosing data, submission or evaluation operation; service naming alone does not establish the executor. |
| `phases[].scoring_submission` | string | Artifact or submission record used for scoring, distinct from auxiliary verification materials. |
| `phases[].submission_format` | null / string | Required file/packaging format for the stated scored or auxiliary submission. |
| `phases[].test_data` | string | Input data provided or withheld for the stated testing stage. |
| `platform` | null / string | Named service involved in the enclosing data, submission or evaluation operation; service naming alone does not establish the executor. |
| `platform_evidence_stage` | string | Stage represented by the evidence naming the platform, such as registered design versus operational execution. |
| `platform_scope` | string | Task, phase, cohort or source boundaries of platform. |
| `platform_url` | string | Web address for platform. |
| `primary_metric` | null | Metric designated as primary for the stated task or assessment. |
| `protocol_evidence_note` | string | Qualification or source distinction concerning protocol evidence. |
| `protocol_metrics` | array; items: string | Structured entries for protocol metrics within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `protocol_scope_note` | string | Qualification or source distinction concerning protocol scope. |
| `protocol_status` | string | Recorded state of protocol. Preserve the task/phase scope and source qualifications. |
| `ranking` | null / object | Rule used to order participants or methods in the stated task/phase, or its source description. |
| `ranking.formula` | string | Explicit mathematical expression for the enclosing metric, score or aggregation rule, as stated by the source. |
| `ranking.method` | string | Method or procedure used for the enclosing evaluation, extraction or analysis; preserve whether organizer-defined or reviewer-applied. |
| `ranking.weights` | object | Weights assigned to multiple metrics, classes or components; preserve the named aggregation scope. |
| `ranking.weights.macro_auc` | number | Weight/coefficient assigned to the source-defined target or component `macro_auc` in the enclosing formula. |
| `ranking.weights.macro_precision` | number | Weight/coefficient assigned to the source-defined target or component `macro_precision` in the enclosing formula. |
| `ranking.weights.macro_sensitivity` | number | Weight/coefficient assigned to the source-defined target or component `macro_sensitivity` in the enclosing formula. |
| `ranking_evidence_note` | string | Qualification or source distinction concerning ranking evidence. |
| `registered_design_tasks` | array; items: object | Structured entries for registered design tasks within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `registered_design_tasks[].design_status` | string | Recorded state of design. Preserve the task/phase scope and source qualifications. |
| `registered_design_tasks[].evidence_section` | string | Source-recorded evidence section for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `registered_design_tasks[].metrics` | array; items: string | Metrics assigned to the enclosing task or assessment; a metric list alone does not define the ranking formula. |
| `registered_design_tasks[].ranking` | null | Rule used to order participants or methods in the stated task/phase, or its source description. |
| `registered_design_tasks[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `scoring_execution_environment` | object | Structured entries for scoring execution environment within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `scoring_execution_environment.evidence_state` | string | State of the documentary evidence for the specific field or assessment, retaining ambiguity, missingness and structural non-applicability. |
| `scoring_execution_environment.note` | string | Contextual qualification, uncertainty or source distinction for the enclosing item. |
| `scoring_execution_environment.value` | null | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `scoring_executor` | string | Party computing the evaluation scores; it need not be the same party that runs model inference. |
| `scoring_software` | null | Software or scripts used to calculate metrics or rankings. |
| `source_reference` | string | Reference to the supporting document or source, possibly with section, URL and archival location. |
| `task_metric_mapping_status` | string | Recorded state of task metric mapping. Preserve the task/phase scope and source qualifications. |
| `task_platforms` | array; items: object | Structured entries for task platforms within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `task_platforms[].competition_url` | null / string | Web address for competition. |
| `task_platforms[].evidence_status` | string | Recorded state of evidence. Preserve the task/phase scope and source qualifications. |
| `task_platforms[].platform` | null / string | Named service involved in the enclosing data, submission or evaluation operation; service naming alone does not establish the executor. |
| `task_platforms[].qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `task_platforms[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `task_platforms[].source_snapshot` | string | Identifier or path of the source snapshot in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `task_platforms[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `task_platforms[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `task_platforms[].url` | null / string | Web address of the enclosing source, document or resource. |
| `tasks` | array; items: object | Task-specific objects or descriptions; each has its own scope, inputs, outputs or assessment information where available. |
| `tasks[].any_severe_scalar` | number | Reported numerical value for any severe scalar within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `tasks[].competition_outcome` | string | Source-recorded competition outcome for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `tasks[].design_status` | string | Recorded state of design. Preserve the task/phase scope and source qualifications. |
| `tasks[].evidence_scope` | string | Boundary of what the supporting evidence establishes, including specification versus actual execution. |
| `tasks[].evidence_section` | string | Source-recorded evidence section for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `tasks[].metrics` | null / array; items: string | Metrics assigned to the enclosing task or assessment; a metric list alone does not define the ranking formula. |
| `tasks[].metrics_reference` | object | Supporting source reference for metrics. |
| `tasks[].metrics_reference.local_protocol` | string | Original archive path of a registered protocol; the protocol file itself is not included in this metadata package. |
| `tasks[].metrics_reference.registered_task_index` | integer | Task position/identifier in the registered protocol; it can differ from later operational numbering. |
| `tasks[].metrics_reference.section` | string | Section, figure, table or location within a supporting source. |
| `tasks[].metrics_reference.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `tasks[].notes` | string | Contextual qualifications and source distinctions retained after removal of empty or exact redundant remarks. |
| `tasks[].outcome_evidence_ids` | array; items: string | Identifiers of evidence items supporting outcome. |
| `tasks[].protocol_reference` | object | Reference to the edition-specific protocol supporting the enclosing field; a protocol describes specification rather than proof of execution. |
| `tasks[].protocol_reference.local_protocol` | string | Original archive path of a registered protocol; the protocol file itself is not included in this metadata package. |
| `tasks[].protocol_reference.registered_task_index` | integer | Task position/identifier in the registered protocol; it can differ from later operational numbering. |
| `tasks[].protocol_reference.section` | string | Section, figure, table or location within a supporting source. |
| `tasks[].protocol_reference.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `tasks[].qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `tasks[].ranking` | null / string | Rule used to order participants or methods in the stated task/phase, or its source description. |
| `tasks[].ranking_reference` | object | Supporting source reference for ranking. |
| `tasks[].ranking_reference.local_protocol` | string | Original archive path of a registered protocol; the protocol file itself is not included in this metadata package. |
| `tasks[].ranking_reference.registered_task_index` | integer | Task position/identifier in the registered protocol; it can differ from later operational numbering. |
| `tasks[].ranking_reference.section` | string | Section, figure, table or location within a supporting source. |
| `tasks[].ranking_reference.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `tasks[].registered_metrics_text` | string | Text extracted from the registered metric or ranking description. The unusual original key is retained literally; it is not a separately standardized metric. |
| `tasks[].registered_ranking_text` | string | Text extracted from the registered metric or ranking description. The unusual original key is retained literally; it is not a separately standardized metric. |
| `tasks[].sample_weights` | object | Structured entries for sample weights within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `tasks[].sample_weights.moderate` | integer | Weight/coefficient assigned to the source-defined target or component `moderate` in the enclosing formula. |
| `tasks[].sample_weights.normal_mild` | integer | Weight/coefficient assigned to the source-defined target or component `normal_mild` in the enclosing formula. |
| `tasks[].sample_weights.severe` | integer | Weight/coefficient assigned to the source-defined target or component `severe` in the enclosing formula. |
| `tasks[].specified_hardware` | string | Hardware configuration required or described by the source; retain whether mandatory or advisory. |
| `tasks[].target_weights` | object | Structured entries for target weights within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `tasks[].target_weights.Aneurysm Present` | integer | Weight/coefficient assigned to the source-defined target or component `Aneurysm Present` in the enclosing formula. |
| `tasks[].target_weights.each_location_specific_target` | integer | Weight/coefficient assigned to the source-defined target or component `each_location_specific_target` in the enclosing formula. |
| `tasks[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `tasks[].tolerance` | string | Permitted numerical, spatial or procedural deviation in the enclosing evaluation; use the source's stated unit and threshold meaning. |
| `tasks[].validation_metrics` | array; items: string | Structured entries for validation metrics within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `tasks[].validation_mode` | string | Source-recorded validation mode for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `tasks[].validation_ranking` | string | Source-recorded validation ranking for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `track_note` | string | Qualification or source distinction concerning track. |
| `validation_evaluated` | boolean | Whether the condition “validation evaluated” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `validation_metrics` | array; items: string | Structured entries for validation metrics within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `validation_ranking` | string | Source-recorded validation ranking for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `workflow_evidence` | object | Recorded documentary support for workflow. Preserve the task/phase scope and source qualifications. |
| `workflow_evidence.basis_type` | string | Kind of evidence underlying the enclosing decision, such as public documentation or human confirmation. |
| `workflow_evidence.date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `workflow_evidence.independently_verified_in_this_update` | boolean | Whether the condition “independently verified in this update” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `workflow_evidence.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `workflow_evidence.summary` | string | Concise summary of the enclosing source, review or observation. |

<a id="result-evidence-review"></a>

## `result_evidence_review`

JSON parent path: `challenge.result_evidence_review`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.result_evidence_review`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `access_conclusion` | string | Source-recorded access conclusion for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `final_test` | object | Structured entries for final test within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `final_test.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `final_test.scores` | object | Structured entries for scores within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `final_test.scores.LGE_DSC` | number | Reported value or specification of the source-named metric `LGE_DSC` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `final_test.scores.cine_DSC` | number | Reported value or specification of the source-named metric `cine_DSC` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `final_test.scores.cine_LVEF_PCC` | number | Reported numerical value for cine LVEF PCC within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `final_test.scores.overall` | number | Reported numerical value for overall within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `final_test.scores.scar_mass_vPCC` | number | Reported numerical value for scar mass v PCC within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `final_test.scores.task1_cine` | number | Reported numerical value for task1 cine within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `final_test.scores.task2_lge` | number | Reported numerical value for task2 lge within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `final_test.source` | string | Source identifier, URL, citation, original wording or source object for the enclosing item. |
| `final_test.team` | string | Team identity attached to the stated method, submission, award or result. |
| `final_test.username` | string | Platform account identifier associated with the enclosing entry. |
| `official_final_ranking` | string | Organizer/platform record of final ranking for the stated task/edition scope. |
| `review_date` | string | Date of the review operation described in the enclosing object. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `validation` | object | Validation-stage data, quantities, submissions or results; not automatically final-test evidence. |
| `validation.authors` | array; items: string | Authors credited for the enclosing publication or source. |
| `validation.paper_id` | string | Identifier of a paper within the cited conference, repository or programme. |
| `validation.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `validation.scores` | object | Structured entries for scores within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `validation.scores.EF_PCC` | number | Reported numerical value for EF PCC within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `validation.scores.LGE_DSC` | number | Reported value or specification of the source-named metric `LGE_DSC` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `validation.scores.cine_DSC` | number | Reported value or specification of the source-named metric `cine_DSC` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `validation.scores.overall` | number | Reported numerical value for overall within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `validation.scores.scar_mass_vPCC` | number | Reported numerical value for scar mass v PCC within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `validation.scores.task1_cine` | number | Reported numerical value for task1 cine within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `validation.scores.task2_lge` | number | Reported numerical value for task2 lge within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `validation.source` | string | Source identifier, URL, citation, original wording or source object for the enclosing item. |

[Back to README](../../README.md#variable-dictionary)
