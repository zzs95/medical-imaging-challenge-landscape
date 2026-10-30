# Capability-assessment evidence

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

Assessment specification, execution, outcomes, grounding, clinical assessment and transfer scope.

## Field groups

- [`challenge.assessment_evidence`](#assessment-evidence)

<a id="assessment-evidence"></a>

## `assessment_evidence`

JSON parent path: `challenge.assessment_evidence`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.assessment_evidence`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `all_four_declared_tracks_have_documented_competition_outcomes` | boolean | Whether the condition “all four declared tracks have documented competition outcomes” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `all_six_current_active_tracks_have_documented_competition_outcomes` | boolean | Whether the condition “all six current active tracks have documented competition outcomes” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `any_executed_assessment_status` | string | Recorded state of any executed assessment. Preserve the task/phase scope and source qualifications. |
| `as_of_date` | string | Reference date for the stated documentary/evaluation status. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `audit_record` | string | Identifier/path of an internal review record; not necessarily present in this package. |
| `award_claims` | object | Structured entries for award claims within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `award_claims.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `award_claims.source_snapshot` | string | Identifier or path of the source snapshot in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `award_claims.status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `award_evidence` | object | Recorded documentary support for award. Preserve the task/phase scope and source qualifications. |
| `award_evidence.award_rank` | integer | Placement or award position for the stated task and phase. |
| `award_evidence.award_task` | null | Task to which the reported award applies. |
| `award_evidence.full_rankings` | string | Source-recorded full rankings for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `award_evidence.hidden_test_assessment` | string | Source-recorded hidden test assessment for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `award_evidence.participants` | array; items: string | Structured entries for participants within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `award_outcomes` | array; items: object | Structured entries for award outcomes within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `award_outcomes[].certificate_date` | string | Date associated with certificate. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `award_outcomes[].evidence_type` | string | Kind of supporting evidence, preserving protocol, report, result and confirmation distinctions. |
| `award_outcomes[].independently_inspected` | boolean | Whether the condition “independently inspected” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `award_outcomes[].institution` | string | Named institution in the enclosing organizer, data-source or participant context. |
| `award_outcomes[].institutions` | array; items: string | Named organizing or contributing institutions; organizer institutions do not establish acquisition-center diversity. |
| `award_outcomes[].members` | array; items: string | Structured entries for members within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `award_outcomes[].publication_date` | string | Date associated with publication. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `award_outcomes[].rank` | integer | Reported placement under the stated task, phase and ranking scope. |
| `award_outcomes[].retrieval_scope` | string | Task, phase, cohort or source boundaries of retrieval. |
| `award_outcomes[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `award_outcomes[].source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `award_outcomes[].task_id` | null | Identifier of a task within its challenge or source-specific numbering scheme. |
| `basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `benchmark_assessment` | object | Structured entries for benchmark assessment within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `benchmark_assessment.competition_final_assessment` | string | Source-recorded competition final assessment for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `benchmark_assessment.evidence_ids` | array; items: string | Identifiers of specific evidence items supporting the enclosing interpretation; archival ledgers may be outside this package. |
| `benchmark_assessment.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `benchmark_assessment.value` | string | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `caption_assessment_review` | object | Source-linked review of caption assessment. |
| `caption_assessment_review.baseline_separation` | string | Explanation separating organizer/local baseline experiments from competition assessment evidence. |
| `caption_assessment_review.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `caption_assessment_review.caption_competition_assessment` | string | Evidence/status of competitive caption assessment in the specified phase. |
| `caption_assessment_review.declared_captioning_objective` | string | Source-recorded declared captioning objective for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `caption_assessment_review.evidence_state` | string | State of the documentary evidence for the specific field or assessment, retaining ambiguity, missingness and structural non-applicability. |
| `caption_assessment_review.include_in_confirmed_caption_assessment_count` | boolean | Whether the condition “include in confirmed caption assessment count” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `caption_assessment_review.independently_verified_complete_final_rankings` | string | Source-recorded independently verified complete final rankings for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `caption_assessment_review.participant_paper_doi` | string | DOI of the participant publication cited as supporting the enclosing statement. |
| `caption_assessment_review.published_evaluation_protocol` | string | Source-recorded published evaluation protocol for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `caption_assessment_review.published_participant_result` | string | Source-recorded published participant result for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `caption_assessment_review.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `caption_assessment_review.supersedes` | string | Earlier statement or record that the enclosing revision replaces. |
| `caption_assessment_review.verification_limit` | string | Specific limit on what was verified from the available source. |
| `caption_baseline_assessment_status` | string | Recorded state of caption baseline assessment. Preserve the task/phase scope and source qualifications. |
| `caption_competition_assessment_status` | string | Recorded state of caption competition assessment. Preserve the task/phase scope and source qualifications. |
| `caption_final_rankings_independently_verified` | boolean | Whether the condition “caption final rankings independently verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `caption_review_history` | array; items: object | Earlier versions or decisions concerning caption review. |
| `caption_review_history[].additional_evidence` | string | Recorded documentary support for additional. Preserve the task/phase scope and source qualifications. |
| `caption_review_history[].caption_specific_final_assessment` | string | Source-recorded caption specific final assessment for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `caption_review_history[].decision_basis` | string | Evidence or reasoning supporting decision. |
| `caption_review_history[].edition_completion` | string | Source-recorded edition completion for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `caption_review_history[].include_in_confirmed_caption_assessment_count` | boolean | Whether the condition “include in confirmed caption assessment count” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `caption_review_history[].qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `caption_review_history[].retain_declared_caption_generation_objective` | boolean | Whether the condition “retain declared caption generation objective” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `caption_review_history[].retain_edition` | boolean | Whether the condition “retain edition” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `caption_review_history[].reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `combined_record_assessment` | object | Structured entries for combined record assessment within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `combined_record_assessment.evidence_ids` | array; items: string | Identifiers of specific evidence items supporting the enclosing interpretation; archival ledgers may be outside this package. |
| `combined_record_assessment.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `combined_record_assessment.value` | string | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `complete_codalab_final_leaderboard_verified` | boolean | Whether the condition “complete codalab final leaderboard verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `complete_official_leaderboard_independently_verified` | boolean | Whether the condition “complete official leaderboard independently verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `completion_adjudication` | object | Structured entries for completion adjudication within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `completion_adjudication.analysis_id` | string | Identifier assigned to a review-defined analytical unit; historical combined-unit identifiers can be superseded. |
| `completion_adjudication.analysis_year` | integer | Calendar year assigned to analysis; preserve whether this concerns an edition, analysis, event or publication. |
| `completion_adjudication.authorized_by` | string | Person or role recorded as authorizing the enclosing decision; not evidence of organizer execution. |
| `completion_adjudication.basis_type` | string | Kind of evidence underlying the enclosing decision, such as public documentation or human confirmation. |
| `completion_adjudication.completion_for_analysis` | string | Source-recorded completion for analysis for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `completion_adjudication.completion_status` | string | Recorded edition-level conduct or completion status; does not establish execution of every proposed assessment. |
| `completion_adjudication.date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `completion_adjudication.decision_id` | string | Identifier of a review or adjudication decision. |
| `completion_adjudication.edition_year` | integer | Calendar year assigned to edition; preserve whether this concerns an edition, analysis, event or publication. |
| `completion_adjudication.exact_completion_date` | null | Date associated with exact completion. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `completion_adjudication.include_in_2026_scope` | boolean | Task, phase, cohort or source boundaries of include in 2026. |
| `completion_adjudication.independently_verified_final_completion` | boolean | Whether the condition “independently verified final completion” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `completion_adjudication.independently_verified_final_completion_by_this_update` | boolean | Whether the condition “independently verified final completion by this update” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `completion_adjudication.independently_verified_v2_final_completion` | boolean | Whether the condition “independently verified v2 final completion” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `completion_adjudication.instruction` | string | Instruction recorded for the enclosing procedure or decision; distinguish organizer instructions from historical author/reviewer requests. |
| `completion_adjudication.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `completion_basis` | string | Type of evidence supporting the edition-level record: public documentary evidence, human confirmation, or an edition-specific programme/protocol. |
| `completion_status` | string | Recorded edition-level conduct or completion status; does not establish execution of every proposed assessment. |
| `conference_programme_entry` | boolean | Whether the condition “conference programme entry” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `confirmation_basis` | string | Evidence or reasoning supporting confirmation. |
| `confirmed_completed_downstream_task_count` | null | Number or recorded confirmation state of downstream tasks whose completion is supported; preserve an unresolved string instead of inferring a number. |
| `counting_note` | string | Qualification or source distinction concerning counting. |
| `documentary_final_assessment_status_before_adjudication` | string | Source-recorded documentary final assessment status before adjudication for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `documentary_final_assessment_status_before_human_confirmation` | string | Source-recorded documentary final assessment status before human confirmation for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `edition_level_actual_assessment` | boolean | Whether the condition “edition level actual assessment” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `event_state` | string | Documentary coding state of event. Preserve the task/phase scope and source qualifications. |
| `evidence_source_url` | string | Public URL supporting evidence. |
| `evidence_sources` | array; items: string | Sources supporting evidence. |
| `evidence_type` | string | Kind of supporting evidence, preserving protocol, report, result and confirmation distinctions. |
| `evidence_urls` | array; items: string | Structured entries for evidence URLs within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `excluded_cross_year_evidence` | array; items: object | Recorded documentary support for excluded cross year. Preserve the task/phase scope and source qualifications. |
| `excluded_cross_year_evidence[].reason` | string | Reason for the enclosing decision, revision, exclusion or qualification. |
| `excluded_cross_year_evidence[].url` | string | Web address of the enclosing source, document or resource. |
| `excluded_cross_year_evidence[].verification_scope` | string | Task, phase, cohort or source boundaries of verification. |
| `execution_evidence` | array; items: object | Evidence that the specified assessment or execution actually occurred within the recorded task and phase. |
| `execution_evidence[].branch` | string | Source-recorded branch for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `execution_evidence[].phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. |
| `execution_evidence[].qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `execution_evidence[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `execution_evidence[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `execution_evidence[].status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `execution_evidence[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `final_assessment_status` | string | Recorded state of final assessment. Preserve the task/phase scope and source qualifications. |
| `final_category_results` | object | Structured entries for final category results within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `final_category_results.clinician_driven_interaction` | object | Structured entries for clinician driven interaction within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `final_category_results.clinician_driven_interaction.column_order` | array; items: string | Structured entries for column order within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `final_category_results.clinician_driven_interaction.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `final_category_results.clinician_driven_interaction.rows` | array; items: array | Structured entries for rows within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `final_category_results.simulated_interaction` | object | Structured entries for simulated interaction within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `final_category_results.simulated_interaction.column_order` | array; items: string | Structured entries for column order within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `final_category_results.simulated_interaction.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `final_category_results.simulated_interaction.rows` | array; items: array | Structured entries for rows within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `followup` | object | Structured entries for followup within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `followup.automatic_monitoring_scheduled` | boolean | Whether the condition “automatic monitoring scheduled” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `followup.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `followup.scheduled_awards_date` | string | Date associated with scheduled awards. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `followup.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `followup.status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `followup.suggested_recheck_on_or_after` | string | Suggested date for a future source recheck; not evidence that a subsequent check occurred. |
| `followup.time_local` | string | Source-recorded time local for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `followup.timezone` | string | Timezone specified for the enclosing schedule or observation; null means it was not established. |
| `followup.trigger` | string | Source-recorded trigger for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `foundation_model_specific_assessment` | string | Source-recorded foundation model specific assessment for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `full_challenge_programme_completed` | boolean | Whether the condition “full challenge programme completed” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `historical_submission_policy` | object | Permission, restriction or procedural rule governing historical submission. |
| `historical_submission_policy.evidence_scope` | string | Boundary of what the supporting evidence establishes, including specification versus actual execution. |
| `historical_submission_policy.policy` | string | Source wording describing permission, prohibition or conditions for the enclosing resource or procedure. |
| `historical_submission_policy.source_snapshot` | string | Identifier or path of the source snapshot in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `identity_status` | string | Recorded state of identity. Preserve the task/phase scope and source qualifications. |
| `latest_documentary_followup` | object | Structured entries for latest documentary followup within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `latest_documentary_followup.basis_type` | string | Kind of evidence underlying the enclosing decision, such as public documentation or human confirmation. |
| `latest_documentary_followup.details` | object | Structured entries for details within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `latest_documentary_followup.details.Learn2Breath` | object | Structured entries for Learn2Breath within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `latest_documentary_followup.details.Learn2Breath.participant_reported_rank` | integer | Rank reported by a participant source, retaining its phase and independent-verification qualifications. |
| `latest_documentary_followup.details.Learn2Breath.source` | string | Source identifier, URL, citation, original wording or source object for the enclosing item. |
| `latest_documentary_followup.details.PSMAReg` | object | Structured entries for PSMAReg within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `latest_documentary_followup.details.PSMAReg.test_rank` | integer | Placement for the stated test phase; check whether that phase is final. |
| `latest_documentary_followup.details.PSMAReg.validation_rank` | integer | Placement on the validation evaluation, distinct from final-test ranking. |
| `latest_documentary_followup.details.Task2` | object | Source-defined Task2 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `latest_documentary_followup.details.Task2.assessment` | string | Assessment procedure or scoped assessment-status entry for the enclosing capability or task. |
| `latest_documentary_followup.details.Task2.participants` | array; items: string | Structured entries for participants within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `latest_documentary_followup.details.Task2.rank` | integer | Reported placement under the stated task, phase and ranking scope. |
| `latest_documentary_followup.details.award` | string | Award or recognition identified for the specified task, method, participant or edition. |
| `latest_documentary_followup.details.award_date` | string | Date associated with award. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `latest_documentary_followup.details.award_rank` | integer | Placement or award position for the stated task and phase. |
| `latest_documentary_followup.details.correction_to_user_review` | string | Source-linked review of correction to user. |
| `latest_documentary_followup.details.count_definition` | string | Definition of what is counted, including unit, eligible entries and phase/task scope. |
| `latest_documentary_followup.details.evidence_type` | string | Kind of supporting evidence, preserving protocol, report, result and confirmation distinctions. |
| `latest_documentary_followup.details.final_combined_score` | number | Composite score for the designated final ranking under the stated included phases/components. |
| `latest_documentary_followup.details.final_test_macro_F1_percent` | number | Reported value or specification of the source-named metric `final_test_macro_F1_percent` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `latest_documentary_followup.details.full_numerical_leaderboard_independently_verified` | boolean | Whether the condition “full numerical leaderboard independently verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `latest_documentary_followup.details.independent_award` | string | Source-recorded independent award for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `latest_documentary_followup.details.independent_corrobation` | string | Source-recorded independent corrobation for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `latest_documentary_followup.details.manuscript` | string | Source-recorded manuscript for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `latest_documentary_followup.details.organizer_winner_announcement` | string | Source-recorded organizer winner announcement for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `latest_documentary_followup.details.overall_first_place` | string | Source-recorded overall first place for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `latest_documentary_followup.details.overall_rank` | integer | Overall placement under the stated competition/phase ranking rules. |
| `latest_documentary_followup.details.participant` | string | Participant identity or description attached to the stated method, submission or result. |
| `latest_documentary_followup.details.participant_hidden_test` | object | Structured entries for participant hidden test within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `latest_documentary_followup.details.participant_hidden_test.ASSD_mm` | number | Reported value or specification of the source-named metric `ASSD_mm` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. Unit/format: mm; denominator/scope follows field name. |
| `latest_documentary_followup.details.participant_hidden_test.Dice` | number | Reported value or specification of the source-named metric `Dice` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `latest_documentary_followup.details.participant_hidden_test.HD95_mm` | number | Reported value or specification of the source-named metric `HD95_mm` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. Unit/format: mm; denominator/scope follows field name. |
| `latest_documentary_followup.details.participant_hidden_test.population` | string | Population-level dataset quantities and characteristics, preserving their stated units. |
| `latest_documentary_followup.details.participant_hidden_test.rank` | integer | Reported placement under the stated task, phase and ranking scope. |
| `latest_documentary_followup.details.participant_reported_team_count` | integer | Number of participant reported team count in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `latest_documentary_followup.details.participants` | array; items: string | Structured entries for participants within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `latest_documentary_followup.details.platform_username` | string | Platform account name associated with the captured submission or evaluation record. |
| `latest_documentary_followup.details.previous_third_place_scope` | string | Earlier/superseded value of third place scope, preserved to document a revision rather than a current observation. |
| `latest_documentary_followup.details.publication_date` | string | Date associated with publication. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `latest_documentary_followup.details.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `latest_documentary_followup.details.quantitative_score` | null | Numerical score explicitly reported for the stated metric, task and phase. |
| `latest_documentary_followup.details.rank` | integer / string | Reported placement under the stated task, phase and ranking scope. |
| `latest_documentary_followup.details.score_scope` | string | Task, phase, cohort or source boundaries of score. |
| `latest_documentary_followup.details.segmentation_competition_assessment` | string | Source-recorded segmentation competition assessment for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `latest_documentary_followup.details.task_id` | null | Identifier of a task within its challenge or source-specific numbering scheme. |
| `latest_documentary_followup.details.team` | string | Team identity attached to the stated method, submission, award or result. |
| `latest_documentary_followup.details.test_metrics` | object | Structured entries for test metrics within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `latest_documentary_followup.details.test_metrics.N_stage_balanced_accuracy` | number | Reported value or specification of the source-named metric `N_stage_balanced_accuracy` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `latest_documentary_followup.details.test_metrics.RFS_C_index` | number | Reported value or specification of the source-named metric `RFS_C_index` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `latest_documentary_followup.details.test_metrics.T_stage_balanced_accuracy` | number | Reported value or specification of the source-named metric `T_stage_balanced_accuracy` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `latest_documentary_followup.details.test_metrics.mean_Dice` | number | Reported value or specification of the source-named metric `mean_Dice` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `latest_documentary_followup.details.test_metrics.weighted_score` | number | Score after applying the source-defined component weights; preserve the formula and task/phase scope. |
| `latest_documentary_followup.evidence_ids` | array; items: string | Identifiers of specific evidence items supporting the enclosing interpretation; archival ledgers may be outside this package. |
| `latest_documentary_followup.propagation_status` | string | Recorded state of propagation. Preserve the task/phase scope and source qualifications. |
| `latest_documentary_followup.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `latest_documentary_followup.source_snapshot` | string | Identifier or path of the source snapshot in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `latest_documentary_followup.source_type` | string | Kind of data or evidence source. In dataset records this describes cohort origin; in provenance it describes the supporting document or confirmation. |
| `latest_documentary_followup.source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `latest_documentary_followup.summary` | string | Concise summary of the enclosing source, review or observation. |
| `latest_documentary_followup.user_instruction` | string | Source-recorded user instruction for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `latest_documentary_followup.user_material` | string | Source-recorded user material for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `objective_assessment` | array; items: object | Structured entries for objective assessment within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `objective_assessment[].confirmed_scope` | string | Task, phase, cohort or source boundaries of confirmed. |
| `objective_assessment[].declared` | boolean | Whether the condition “declared” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `objective_assessment[].evidence_ids` | array; items: string | Identifiers of specific evidence items supporting the enclosing interpretation; archival ledgers may be outside this package. |
| `objective_assessment[].final_assessment_status` | string | Recorded state of final assessment. Preserve the task/phase scope and source qualifications. |
| `objective_assessment[].objective` | string | Organizer-defined AI objective linked to the enclosing task or assessment record. |
| `objective_assessment[].reason` | string | Reason for the enclosing decision, revision, exclusion or qualification. |
| `objective_assessment[].validation_assessment_status` | string | Recorded state of validation assessment. Preserve the task/phase scope and source qualifications. |
| `objective_assessment[].value` | string | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `optional_documentary_limitations` | array; items: string | Structured entries for optional documentary limitations within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `organizer_final_category_rankings_independently_verified` | boolean | Whether the condition “organizer final category rankings independently verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `organizer_final_overview_paper_located` | boolean | Whether the condition “organizer final overview paper located” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `organizer_full_rankings_independently_verified` | boolean | Whether the condition “organizer full rankings independently verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `outcome` | object | Structured entries for outcome within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `outcome.award_rank` | integer | Placement or award position for the stated task and phase. |
| `outcome.final_combined_score` | number | Composite score for the designated final ranking under the stated included phases/components. |
| `outcome.platform_username` | string | Platform account name associated with the captured submission or evaluation record. |
| `outcome.publication_date` | string | Date associated with publication. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `outcome.quantitative_score` | null | Numerical score explicitly reported for the stated metric, task and phase. |
| `outcome.score_scope` | string | Task, phase, cohort or source boundaries of score. |
| `outcome.team` | string | Team identity attached to the stated method, submission, award or result. |
| `outcome_evidence` | null / string | Evidence of reported scores, analytical findings, awards, placements or confirmed results within the stated scope. |
| `participant_hidden_test_paper_verified` | boolean | Whether the condition “participant hidden test paper verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `participant_leaderboard_result` | object | Structured entries for participant leaderboard result within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `participant_leaderboard_result.executed_competition_assessment` | string | Source-recorded executed competition assessment for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `participant_leaderboard_result.final_test_status` | string | Recorded state of final test. Preserve the task/phase scope and source qualifications. |
| `participant_leaderboard_result.metrics` | object | Metrics assigned to the enclosing task or assessment; a metric list alone does not define the ranking formula. |
| `participant_leaderboard_result.metrics.DSC_percent` | number | Reported value or specification of the source-named metric `DSC_percent` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `participant_leaderboard_result.metrics.F1_percent` | number | Reported value or specification of the source-named metric `F1_percent` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `participant_leaderboard_result.metrics.NSD_percent` | number | Reported value or specification of the source-named metric `NSD_percent` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `participant_leaderboard_result.metrics.overall_score` | number | Overall score within the source-defined aggregation scope, not a general clinical capability measure. |
| `participant_leaderboard_result.phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. |
| `participant_leaderboard_result.rank` | null | Reported placement under the stated task, phase and ranking scope. |
| `participant_leaderboard_result.runtime_score_included` | string | Source-recorded runtime score included for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `participant_method_result` | object | Structured entries for participant method result within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `participant_method_result.foundation_model_downstream_method_test` | string | Source-recorded foundation model downstream method test for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `participant_method_result.foundation_model_generality_assessment` | string | Source-recorded foundation model generality assessment for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `participant_method_result.participant_method` | string | Source-recorded participant method for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `participant_method_result.pretrained_model` | string | Model/checkpoint pretrained before the challenge-specific development or assessment stage. |
| `participant_method_result.test_Dice` | object | Reported value or specification of the source-named metric `test_Dice` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `participant_method_result.test_Dice.GED4` | number | Reported value or specification of the source-named metric `GED4` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `participant_method_result.test_Dice.T1` | number | Reported numerical value for T1 within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `participant_method_result.track` | string | Track identifier, name or description within the competition. |
| `phase1` | object | Source-defined phase1 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `phase1.count_scope` | string | Task, phase, cohort or source boundaries of count. |
| `phase1.example` | object | Structured entries for example within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `phase1.example.algorithm` | string | Algorithm or executable method named in the enclosing submission or evaluation record. |
| `phase1.example.evaluation_url` | string | Web address for evaluation. |
| `phase1.example.result_date` | string | Date associated with result. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `phase1.example.score` | number | Reported score for the enclosing task, phase, metric or evaluation record; not automatically an overall final result. |
| `phase1.example.status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `phase1.example.submission_date` | string | Date associated with submission. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `phase1.example.user` | string | Account or reviewer identity as recorded by the enclosing source; not a count of independent teams. |
| `phase1.executed_assessment_status` | string | Recorded state of executed assessment. Preserve the task/phase scope and source qualifications. |
| `phase1.public_leaderboard_rows` | integer | Reported numerical value for public leaderboard rows within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `phase1.submission_count` | integer | Number of submission count in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `phase2` | object | Source-defined phase2 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `phase2.eligible_competitive_final_scoring_status` | string | Recorded state of eligible competitive final scoring. Preserve the task/phase scope and source qualifications. |
| `phase2.example` | object | Structured entries for example within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `phase2.example.algorithm` | string | Algorithm or executable method named in the enclosing submission or evaluation record. |
| `phase2.example.evaluation_url` | string | Web address for evaluation. |
| `phase2.example.result_date` | string | Date associated with result. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `phase2.example.score` | number | Reported score for the enclosing task, phase, metric or evaluation record; not automatically an overall final result. |
| `phase2.example.status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `phase2.example.submission_date` | string | Date associated with submission. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `phase2.example.user` | string | Account or reviewer identity as recorded by the enclosing source; not a count of independent teams. |
| `phase2.final_ranking_status` | string | Recorded state of final ranking. Preserve the task/phase scope and source qualifications. |
| `phase2.public_leaderboard_rows` | integer | Reported numerical value for public leaderboard rows within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `phase2.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `phase2.submission_count` | integer | Number of submission count in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `phase2.successful_scoring_record_exists` | boolean | Whether the condition “successful scoring record exists” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `phase2.winner_announcement_status` | string | Recorded state of winner announcement. Preserve the task/phase scope and source qualifications. |
| `phase_assessment` | object | Structured entries for phase assessment within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `phase_assessment.final_hidden_test` | object | Structured entries for final hidden test within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `phase_assessment.final_hidden_test.status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `phase_assessment.validation` | object | Validation-stage data, quantities, submissions or results; not automatically final-test evidence. |
| `phase_assessment.validation.participant_results` | array; items: object | Structured entries for participant results within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `phase_assessment.validation.participant_results[].authors` | array; items: string | Authors credited for the enclosing publication or source. |
| `phase_assessment.validation.participant_results[].bibliographic_note` | string | Qualification or source distinction concerning bibliographic. |
| `phase_assessment.validation.participant_results[].challenge_year` | integer | Calendar year assigned to challenge; preserve whether this concerns an edition, analysis, event or publication. |
| `phase_assessment.validation.participant_results[].evidence_id` | string | Identifier of one supporting evidence item in the review ledger. |
| `phase_assessment.validation.participant_results[].full_text_url` | string | Web address for full text. |
| `phase_assessment.validation.participant_results[].pages` | null | Page range or page information for the enclosing publication. |
| `phase_assessment.validation.participant_results[].publication_status` | string | Documented publication state, such as planned, in preparation, preprint or published; not itself an evaluation outcome. |
| `phase_assessment.validation.participant_results[].results` | object | Reported findings or results for the enclosing task, phase, method or publication. |
| `phase_assessment.validation.participant_results[].results.field_completion_rate` | number | Reported numerical value for field completion rate within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `phase_assessment.validation.participant_results[].results.mean_rotation_error_degrees` | number | Reported numerical value for mean rotation error degrees within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. Unit/format: degrees; denominator/scope follows field name. |
| `phase_assessment.validation.participant_results[].results.mean_translation_error_mm` | number | Reported numerical value for mean translation error mm within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. Unit/format: mm; denominator/scope follows field name. |
| `phase_assessment.validation.participant_results[].results.output` | string | Prediction, artifact or information produced by the task or model. |
| `phase_assessment.validation.participant_results[].results.phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. |
| `phase_assessment.validation.participant_results[].results.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `phase_assessment.validation.participant_results[].results.rank` | integer | Reported placement under the stated task, phase and ranking scope. |
| `phase_assessment.validation.participant_results[].results.rank_at_evaluation` | integer | Placement at the date of the cited evaluation snapshot, not necessarily the eventual final ranking. |
| `phase_assessment.validation.participant_results[].results.total_score` | number | Combined score across the components explicitly included in the source's aggregation rule. |
| `phase_assessment.validation.participant_results[].results.weighted_score` | number | Score after applying the source-defined component weights; preserve the formula and task/phase scope. |
| `phase_assessment.validation.participant_results[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `phase_assessment.validation.participant_results[].springer_doi` | null | DOI assigned to the enclosing Springer publication. |
| `phase_assessment.validation.participant_results[].task` | string | Task name or task-specific result/description associated with the enclosing entry. |
| `phase_assessment.validation.participant_results[].title` | string | Title of the enclosing source document, publication, method or programme entry. |
| `phase_assessment.validation.status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `planned_downstream_task_count` | integer | Number of downstream tasks proposed in the design; distinct from confirmed completed tasks. |
| `programme_status` | string | Recorded state of programme. Preserve the task/phase scope and source qualifications. |
| `protocol_review` | object | Source-linked review of protocol. |
| `protocol_review.date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `protocol_review.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `protocol_review.source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `protocol_review.status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `public_final_results_independently_verified` | boolean | Whether the condition “public final results independently verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `quantitative_final_test_scores_verified` | boolean | Whether the condition “quantitative final test scores verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `remaining_questions` | array; items: string | Structured entries for remaining questions within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `schedule_year_audit` | object | Structured entries for schedule year audit within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `schedule_year_audit.interpretation` | string | Reviewer's scoped interpretation of the recorded source information; not additional organizer evidence. |
| `schedule_year_audit.official_page_heading` | string | Source-recorded official page heading for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `schedule_year_audit.page_mixes_years` | boolean | Whether the condition “page mixes years” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `schedule_year_audit.result_announcement_status_on_page` | string | Source-recorded result announcement status on page for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `schedule_year_audit.stale_content` | string | Source-recorded stale content for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `segmentation_result_evidence` | object | Recorded documentary support for segmentation result. Preserve the task/phase scope and source qualifications. |
| `segmentation_result_evidence.award_rank` | integer | Placement or award position for the stated task and phase. |
| `segmentation_result_evidence.count_definition` | string | Definition of what is counted, including unit, eligible entries and phase/task scope. |
| `segmentation_result_evidence.independent_corrobation` | string | Source-recorded independent corrobation for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `segmentation_result_evidence.participant` | string | Participant identity or description attached to the stated method, submission or result. |
| `segmentation_result_evidence.participant_reported_team_count` | integer | Number of participant reported team count in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `segmentation_result_evidence.segmentation_competition_assessment` | string | Source-recorded segmentation competition assessment for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `segmentation_result_evidence.task_id` | null | Identifier of a task within its challenge or source-specific numbering scheme. |
| `subtask_assessment` | array; items: object | Structured entries for subtask assessment within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `subtask_assessment[].branch` | string | Source-recorded branch for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `subtask_assessment[].evidence_type` | string | Kind of supporting evidence, preserving protocol, report, result and confirmation distinctions. |
| `subtask_assessment[].final_assessment_status` | string | Recorded state of final assessment. Preserve the task/phase scope and source qualifications. |
| `subtask_assessment[].independently_verified_official_leaderboard` | boolean | Whether the condition “independently verified official leaderboard” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `subtask_assessment[].metric` | string | Name or definition of the evaluation metric used for the stated task/component. |
| `subtask_assessment[].phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. |
| `subtask_assessment[].qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `subtask_assessment[].reported_validation_cases` | integer | Reported numerical value for reported validation cases within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `subtask_assessment[].score` | number | Reported score for the enclosing task, phase, metric or evaluation record; not automatically an overall final result. |
| `subtask_assessment[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `subtask_assessment[].source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `subtask_assessment[].subtask` | string | Subtask identifier or description within a larger task. |
| `subtask_assessment[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `subtask_assessment[].validation_results` | array; items: object | Structured entries for validation results within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `subtask_assessment[].validation_results[].metric` | string | Name or definition of the evaluation metric used for the stated task/component. |
| `subtask_assessment[].validation_results[].phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. |
| `subtask_assessment[].validation_results[].score` | number | Reported score for the enclosing task, phase, metric or evaluation record; not automatically an overall final result. |
| `subtask_assessment[].validation_results[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `subtask_assessment[].validation_results[].team` | string | Team identity attached to the stated method, submission, award or result. |
| `ta36_snapshot` | string | Source-recorded ta36 snapshot for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `ta36_snapshot_date` | string | Date associated with ta36 snapshot. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `task_award_evidence` | object | Recorded documentary support for task award. Preserve the task/phase scope and source qualifications. |
| `task_award_evidence.Task2` | object | Source-defined Task2 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `task_award_evidence.Task2.assessment` | string | Assessment procedure or scoped assessment-status entry for the enclosing capability or task. |
| `task_award_evidence.Task2.participants` | array; items: string | Structured entries for participants within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `task_award_evidence.Task2.rank` | integer | Reported placement under the stated task, phase and ranking scope. |
| `task_award_evidence.full_numerical_leaderboard_independently_verified` | boolean | Whether the condition “full numerical leaderboard independently verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `task_award_evidence.organizer_winner_announcement` | string | Source-recorded organizer winner announcement for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `task_award_evidence.overall_first_place` | string | Source-recorded overall first place for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `task_award_evidence.previous_third_place_scope` | string | Earlier/superseded value of third place scope, preserved to document a revision rather than a current observation. |
| `task_result_evidence` | array / object; items: object | Recorded documentary support for task result. Preserve the task/phase scope and source qualifications. |
| `task_result_evidence.VQA_accuracy_percent` | number | Reported numerical value for visual question answering accuracy percent within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `task_result_evidence[].award` | string | Award or recognition identified for the specified task, method, participant or edition. |
| `task_result_evidence[].award_source` | string | Source supporting award. |
| `task_result_evidence[].final_assessment` | string | Evidence/status of the designated final scored assessment in the stated task or edition scope. |
| `task_result_evidence[].final_award_claim` | string | Source-recorded final award claim for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `task_result_evidence[].metrics` | object | Metrics assigned to the enclosing task or assessment; a metric list alone does not define the ranking formula. |
| `task_result_evidence[].metrics.DSC_percent` | number | Reported value or specification of the source-named metric `DSC_percent` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `task_result_evidence[].metrics.NSD_percent` | number | Reported value or specification of the source-named metric `NSD_percent` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `task_result_evidence[].objective_specific_final_assessment` | string | Source-recorded objective specific final assessment for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `task_result_evidence[].report_generation_scope` | string | Task, phase, cohort or source boundaries of report generation. |
| `task_result_evidence[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `task_result_evidence[].status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `task_result_evidence[].subtask` | string | Subtask identifier or description within a larger task. |
| `task_result_evidence[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `task_result_evidence.action_anticipation_top1_percent` | number | Reported numerical value for action anticipation top1 percent within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `task_result_evidence.action_recognition_top1_percent` | number | Reported numerical value for action recognition top1 percent within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `task_result_evidence.activity_recognition` | string | Source-recorded activity recognition for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `task_result_evidence.all_tasks_evaluated` | boolean | Whether the condition “all tasks evaluated” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `task_result_evidence.challenge_year` | integer | Calendar year assigned to challenge; preserve whether this concerns an edition, analysis, event or publication. |
| `task_result_evidence.doi` | string | Digital Object Identifier assigned to the enclosing publication, protocol or dataset. |
| `task_result_evidence.publication_year` | integer | Year of publication or posting, separate from the year of the challenge edition. |
| `task_specific_final_results` | array; items: object | Structured entries for task specific final results within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `task_specific_final_results[].reason` | string | Reason for the enclosing decision, revision, exclusion or qualification. |
| `task_specific_final_results[].status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `task_specific_final_results[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `topbrainv2_final_assessment_status` | string | Recorded state of topbrainv2 final assessment. Preserve the task/phase scope and source qualifications. |
| `topbrainv2_final_phase` | object | Structured entries for topbrainv2 final phase within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `topbrainv2_final_phase.phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. |
| `topbrainv2_final_phase.planned_opening_date` | string | Date associated with planned opening. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `topbrainv2_final_phase.planned_opening_time_displayed` | string | Source-recorded planned opening time displayed for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `topbrainv2_final_phase.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `topbrainv2_final_phase.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `topbrainv2_final_phase.status_as_of_review` | string | Source-linked review of status as of. |
| `topbrainv2_final_phase.timezone` | null | Timezone specified for the enclosing schedule or observation; null means it was not established. |
| `topbrainv2_final_phase.verified_on` | string | Date of the specific verification described in the enclosing record. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `topbrainv2_quantitative_final_results_verified` | boolean | Whether the condition “topbrainv2 quantitative final results verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `track_results` | array; items: object | Structured entries for track results within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `track_results[].awards` | array; items: object | Structured entries for awards within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `track_results[].awards[].institution` | string | Named institution in the enclosing organizer, data-source or participant context. |
| `track_results[].awards[].method` | string | Method or procedure used for the enclosing evaluation, extraction or analysis; preserve whether organizer-defined or reviewer-applied. |
| `track_results[].awards[].rank` | integer | Reported placement under the stated task, phase and ranking scope. |
| `track_results[].awards[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `track_results[].awards[].team` | string | Team identity attached to the stated method, submission, award or result. |
| `track_results[].awards[].team_or_institution` | string | Source-recorded team or institution for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `track_results[].competition_outcome` | string | Source-recorded competition outcome for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `track_results[].complete_numerical_final_leaderboard_verified` | boolean | Whether the condition “complete numerical final leaderboard verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `track_results[].complete_official_numerical_final_ranking_verified` | boolean | Whether the condition “complete official numerical final ranking verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `track_results[].evidence_ids` | array; items: string | Identifiers of specific evidence items supporting the enclosing interpretation; archival ledgers may be outside this package. |
| `track_results[].evidence_type` | string | Kind of supporting evidence, preserving protocol, report, result and confirmation distinctions. |
| `track_results[].hidden_test_scores_verified` | boolean | Whether the condition “hidden test scores verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `track_results[].hidden_test_source_url` | string | Public URL supporting hidden test. |
| `track_results[].historical_leaderboard_url` | string | Web address for historical leaderboard. |
| `track_results[].modality` | string | Imaging acquisition category recorded for the challenge; raw labels can differ from harmonized analytical categories. |
| `track_results[].name` | string | Name of the enclosing task, institution, dataset, source, method or event; the parent field identifies the entity. |
| `track_results[].snapshot` | string | Identifier or path of the snapshot in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `track_results[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `track_results[].task_family` | string | Broad category of task output or operation for the specific task. |
| `track_results[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `track_results[].tie_qualification` | string | Source-recorded tie qualification for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `track_results[].track_id` | string | Identifier of a competition track; a track is not automatically a separate analytical edition. |

[Back to README](../../README.md#variable-dictionary)
