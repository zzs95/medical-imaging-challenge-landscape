# Tasks, outputs and emerging AI objectives

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

Tasks and tracks, participant outputs, task-family coding and organizer-defined objectives.

## Field groups

- [`challenge.task_profile`](#task-profile)
- [`challenge.task_taxonomy`](#task-taxonomy)
- [`challenge.review_coding`](#review-coding)
- [`challenge.task_objective_review`](#task-objective-review)
- [`challenge.current_output_classification`](#current-output-classification)
- [`challenge.registered_task_taxonomy`](#registered-task-taxonomy)

<a id="task-profile"></a>

## `task_profile`

JSON parent path: `challenge.task_profile`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.task_profile`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `classification_basis` | string | Evidence or reasoning supporting classification. |
| `coding` | string | Source-recorded coding for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `coding_note` | string | Qualification or source distinction concerning coding. |
| `competition_tracks` | array; items: string | Structured entries for competition tracks within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `counting_note` | string | Qualification or source distinction concerning counting. |
| `declared_main_task_count` | integer | Number of main tasks declared in the cited competition design, not proof that all were executed. |
| `declared_vision_language_objective` | boolean | Whether the condition “declared vision language objective” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `declared_vs_implemented_review` | object | Source-linked review of declared vs implemented. |
| `declared_vs_implemented_review.blocks_completion_confirmation` | boolean | Whether the condition “blocks completion confirmation” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `declared_vs_implemented_review.blocks_edition_inclusion` | boolean | Whether the condition “blocks edition inclusion” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `declared_vs_implemented_review.declaration_source` | string | Source supporting declaration. |
| `declared_vs_implemented_review.declared_foundation_model_transfer_objective` | boolean | Whether the condition “declared foundation model transfer objective” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `declared_vs_implemented_review.foundation_model_specific_assessment` | string | Source-recorded foundation model specific assessment for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `declared_vs_implemented_review.implemented_unified_cardiac_segmentation_assessment` | string | Source-recorded implemented unified cardiac segmentation assessment for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `declared_vs_implemented_review.interpretation` | string | Reviewer's scoped interpretation of the recorded source information; not additional organizer evidence. |
| `declared_vs_implemented_review.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `evaluation_tracks` | array; items: object | Structured entries for evaluation tracks within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `evaluation_tracks[].final_assessment_status` | string | Recorded state of final assessment. Preserve the task/phase scope and source qualifications. |
| `evaluation_tracks[].label_count` | integer | Number of labels in the enclosing target or dataset definition. |
| `evaluation_tracks[].label_scope` | string | Task, phase, cohort or source boundaries of label. |
| `evaluation_tracks[].name` | string | Name of the enclosing task, institution, dataset, source, method or event; the parent field identifies the entity. |
| `evaluation_tracks[].phases` | array; items: string | Structured entries for phases within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `evaluation_tracks[].result_source` | string | Source supporting result. |
| `evaluation_tracks[].scheduled_opening` | object | Structured entries for scheduled opening within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `evaluation_tracks[].scheduled_opening.phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. |
| `evaluation_tracks[].scheduled_opening.planned_opening_date` | string | Date associated with planned opening. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `evaluation_tracks[].scheduled_opening.planned_opening_time_displayed` | string | Source-recorded planned opening time displayed for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `evaluation_tracks[].scheduled_opening.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `evaluation_tracks[].scheduled_opening.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `evaluation_tracks[].scheduled_opening.status_as_of_review` | string | Source-linked review of status as of. |
| `evaluation_tracks[].scheduled_opening.timezone` | null | Timezone specified for the enclosing schedule or observation; null means it was not established. |
| `evaluation_tracks[].scheduled_opening.verified_on` | string | Date of the specific verification described in the enclosing record. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `evaluation_tracks[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `evaluation_tracks[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `evaluation_tracks[].track_id` | string | Identifier of a competition track; a track is not automatically a separate analytical edition. |
| `evidence_stage` | string | Stage represented by the evidence, such as registered design, operational instructions or reported execution/results. |
| `executed_task_families` | array; items: string | Structured entries for executed task families within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `implemented_tracks` | array; items: object | Structured entries for implemented tracks within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `implemented_tracks[].independent_edition` | boolean | Whether the condition “independent edition” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `implemented_tracks[].modalities` | array; items: string | Structured entries for modalities within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `implemented_tracks[].official_name` | string | Task or entity name as used in organizer documentation. |
| `implemented_tracks[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `implemented_tracks[].subtasks` | array; items: string | Structured entries for subtasks within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `implemented_tracks[].task_description` | string | Source description of the task and the behavior expected from a participating method. |
| `implemented_tracks[].task_family` | string | Broad category of task output or operation for the specific task. |
| `implemented_tracks[].track_id` | string | Identifier of a competition track; a track is not automatically a separate analytical edition. |
| `learning_paradigms` | array; items: string | Structured entries for learning paradigms within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `objective_execution_status` | string | Recorded state of objective execution. Preserve the task/phase scope and source qualifications. |
| `official_downstream_task_count` | integer | Number of downstream tasks specified in the organizer source, with that source's phase and execution qualification. |
| `previous_primary_task_family` | string | Earlier/superseded value of primary task family, preserved to document a revision rather than a current observation. |
| `primary_output_coding` | string | Source-recorded primary output coding for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `primary_task_family` | null / string | Single primary task label in the source record; insufficient for reconstructing all multi-label task counts. |
| `program_declared_tasks` | array; items: object | Structured entries for program declared tasks within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `program_declared_tasks[].clinical_goal` | null | Clinical question or intended clinical use motivating the task, not evidence of demonstrated clinical benefit. |
| `program_declared_tasks[].granularity` | string | Level at which a prediction or target is defined, such as pixel, voxel, lesion, study, patient or report. |
| `program_declared_tasks[].input` | array; items: string | Data or information supplied to the model for the described task. |
| `program_declared_tasks[].official_name` | string | Task or entity name as used in organizer documentation. |
| `program_declared_tasks[].optional_training_input` | null | Additional input information permitted or supplied during training, distinct from required inference inputs. |
| `program_declared_tasks[].output` | array; items: string | Prediction, artifact or information produced by the task or model. |
| `program_declared_tasks[].task_family` | string | Broad category of task output or operation for the specific task. |
| `program_declared_tasks[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `program_declared_tasks[].task_subtype` | null / string | More specific task formulation, such as multi-label classification or instance segmentation. |
| `registered_design_tasks` | array; items: object | Structured entries for registered design tasks within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `registered_design_tasks[].clinical_goal` | null | Clinical question or intended clinical use motivating the task, not evidence of demonstrated clinical benefit. |
| `registered_design_tasks[].granularity` | null | Level at which a prediction or target is defined, such as pixel, voxel, lesion, study, patient or report. |
| `registered_design_tasks[].input` | array; items: string | Data or information supplied to the model for the described task. |
| `registered_design_tasks[].official_name` | string | Task or entity name as used in organizer documentation. |
| `registered_design_tasks[].optional_training_input` | null | Additional input information permitted or supplied during training, distinct from required inference inputs. |
| `registered_design_tasks[].output` | array; items: string | Prediction, artifact or information produced by the task or model. |
| `registered_design_tasks[].task_family` | string | Broad category of task output or operation for the specific task. |
| `registered_design_tasks[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `registered_design_tasks[].task_subtype` | null | More specific task formulation, such as multi-label classification or instance segmentation. |
| `registered_only_unverified_execution_task_families` | array; items: string | Structured entries for registered only unverified execution task families within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `registered_related_task_families` | array; items: string | Structured entries for registered related task families within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `registered_tasks` | array; items: object | Structured entries for registered tasks within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `registered_tasks[].clinical_goal` | null | Clinical question or intended clinical use motivating the task, not evidence of demonstrated clinical benefit. |
| `registered_tasks[].evidence_scope` | string | Boundary of what the supporting evidence establishes, including specification versus actual execution. |
| `registered_tasks[].granularity` | null | Level at which a prediction or target is defined, such as pixel, voxel, lesion, study, patient or report. |
| `registered_tasks[].input` | null | Data or information supplied to the model for the described task. |
| `registered_tasks[].official_name` | string | Task or entity name as used in organizer documentation. |
| `registered_tasks[].optional_training_input` | null | Additional input information permitted or supplied during training, distinct from required inference inputs. |
| `registered_tasks[].output` | null | Prediction, artifact or information produced by the task or model. |
| `registered_tasks[].task_family` | string | Broad category of task output or operation for the specific task. |
| `registered_tasks[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `registered_tasks[].task_subtype` | null | More specific task formulation, such as multi-label classification or instance segmentation. |
| `related_task_families` | array; items: string | Structured entries for related task families within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `secondary_task_families` | null / array; items: string | Other task families associated with the edition in the source record. |
| `submission_tasks` | array; items: object | Structured entries for submission tasks within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `submission_tasks[].official_output` | string | Output explicitly required for the specified task by the organizer. |
| `submission_tasks[].submission_task_id` | string | Task identifier used in the submission instructions or interface. |
| `submission_tasks[].task_family` | string | Broad category of task output or operation for the specific task. |
| `task_extension_evidence` | string | Recorded documentary support for task extension. Preserve the task/phase scope and source qualifications. |
| `task_families` | array; items: string | Set of task/output families assigned in the enclosing review or task description. |
| `task_numbering_history` | array; items: object | Earlier versions or decisions concerning task numbering. |
| `task_numbering_history[].effect_on_caption_completion` | string | Source-recorded effect on caption completion for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `task_numbering_history[].official_website_task2` | string | Source-recorded official website task2 for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `task_numbering_history[].participant_paper_task2_as_reported_in_user_summary` | string | Source-recorded participant paper task2 as reported in user summary for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `task_numbering_history[].reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `task_numbering_history[].status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `task_numbering_note` | object | Qualification or source distinction concerning task numbering. |
| `task_numbering_note.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `task_numbering_note.official_submission_guides` | object | Structured entries for official submission guides within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `task_numbering_note.official_submission_guides.Task 1` | string | Source-defined Task 1 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `task_numbering_note.official_submission_guides.Task 2` | string | Source-defined Task 2 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `task_numbering_note.official_submission_guides.Task 3` | string | Source-defined Task 3 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `task_numbering_note.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `task_numbering_note.source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `task_numbering_note.status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `task_numbering_note.website_overview` | object | Structured entries for website overview within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `task_numbering_note.website_overview.Task I` | string | Source-defined Task I branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `task_numbering_note.website_overview.Task II` | string | Source-defined Task II branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `task_numbering_note.website_overview.Task III` | string | Source-defined Task III branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `task_role_scope` | object | Task, phase, cohort or source boundaries of task role. |
| `task_role_scope.Biomarker discovery / prediction` | string | Role of the `Biomarker discovery / prediction` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_role_scope.Classification` | string | Role of the `Classification` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_role_scope.Clinical reasoning` | string | Role of the `Clinical reasoning` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_role_scope.Detection` | string | Role of the `Detection` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_role_scope.Explanation` | string | Role of the `Explanation` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_role_scope.Localization` | string | Role of the `Localization` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_role_scope.Named entity extraction` | string | Role of the `Named entity extraction` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_role_scope.Prognosis` | string | Role of the `Prognosis` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_role_scope.Prompt generation` | string | Role of the `Prompt generation` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_role_scope.Quality / suitability assessment` | string | Role of the `Quality / suitability assessment` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_role_scope.Quantification / measurement` | string | Role of the `Quantification / measurement` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_role_scope.Question generation` | string | Role of the `Question generation` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_role_scope.Reconstruction` | string | Role of the `Reconstruction` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_role_scope.Registration` | string | Role of the `Registration` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_role_scope.Report generation` | string | Role of the `Report generation` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_role_scope.Representation / model artifacts` | string | Role of the `Representation / model artifacts` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_role_scope.Retrieval` | string | Role of the `Retrieval` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_role_scope.Segmentation` | string | Role of the `Segmentation` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_role_scope.Structured clinical field prediction` | string | Role of the `Structured clinical field prediction` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_role_scope.Synthesis` | string | Role of the `Synthesis` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_role_scope.VQA / multimodal QA` | string | Role of the `VQA / multimodal QA` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_scope_review` | object | Source-linked review of task scope. |
| `task_scope_review.aggregate_status` | string | Recorded state of aggregate. Preserve the task/phase scope and source qualifications. |
| `task_scope_review.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `task_scope_review.dialogue` | boolean | Whether the condition “dialogue” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `task_scope_review.evaluation_methods` | array; items: string | Structured entries for evaluation methods within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `task_scope_review.foundation_model_objective` | string | Whether the organizer's stated objective concerns large-scale pretraining, reusable representations or adaptation of a pretrained/foundation model. |
| `task_scope_review.image_text_generation` | boolean | Whether the condition “image text generation” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `task_scope_review.nonblocking_evidence_gap` | string | Unresolved documentary detail retained without changing the stated inclusion/coding decision. |
| `task_scope_review.primary_task` | string | Principal task description in the enclosing source or review; not necessarily all task families. |
| `task_scope_review.report_generation` | boolean | Task/objective flag for generating image-grounded free-text reports or captions; structured field prediction is separate. |
| `task_scope_review.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `task_scope_review.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `task_scope_review.source_snapshot` | string | Identifier or path of the source snapshot in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `task_scope_review.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `task_scope_review.status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `task_scope_review.vision_language_model_adaptation_track` | boolean | Whether the condition “vision language model adaptation track” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `task_scope_review.visual_question_answering` | boolean | Task flag for answering questions using image or video content together with language. |
| `tasks` | array; items: object | Task-specific objects or descriptions; each has its own scope, inputs, outputs or assessment information where available. |
| `tasks[].clinical_goal` | null | Clinical question or intended clinical use motivating the task, not evidence of demonstrated clinical benefit. |
| `tasks[].competition_outcome` | string | Source-recorded competition outcome for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `tasks[].endpoint_scope` | string | Task, phase, cohort or source boundaries of endpoint. |
| `tasks[].evidence_scope` | string | Boundary of what the supporting evidence establishes, including specification versus actual execution. |
| `tasks[].granularity` | null / string | Level at which a prediction or target is defined, such as pixel, voxel, lesion, study, patient or report. |
| `tasks[].granularity_by_input` | array; items: string | Structured entries for granularity by input within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `tasks[].input` | null / string / array; items: string | Data or information supplied to the model for the described task. |
| `tasks[].modality` | string | Imaging acquisition category recorded for the challenge; raw labels can differ from harmonized analytical categories. |
| `tasks[].modality_group` | string | Broad imaging category used for harmonized display or analysis. |
| `tasks[].official_name` | string | Task or entity name as used in organizer documentation. |
| `tasks[].optional_training_input` | null / array; items: string | Additional input information permitted or supplied during training, distinct from required inference inputs. |
| `tasks[].output` | null / string / array; items: string | Prediction, artifact or information produced by the task or model. |
| `tasks[].protocol_reference` | object | Reference to the edition-specific protocol supporting the enclosing field; a protocol describes specification rather than proof of execution. |
| `tasks[].protocol_reference.local_protocol` | string | Original archive path of a registered protocol; the protocol file itself is not included in this metadata package. |
| `tasks[].protocol_reference.registered_task_index` | integer | Task position/identifier in the registered protocol; it can differ from later operational numbering. |
| `tasks[].protocol_reference.section` | string | Section, figure, table or location within a supporting source. |
| `tasks[].protocol_reference.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `tasks[].role` | string | Role of the enclosing task, source, artifact or person; context determines whether it is scored, auxiliary or supporting. |
| `tasks[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `tasks[].subtasks` | array; items: object | Structured entries for subtasks within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `tasks[].subtasks[].evidence_scope` | string | Boundary of what the supporting evidence establishes, including specification versus actual execution. |
| `tasks[].subtasks[].name` | string | Name of the enclosing task, institution, dataset, source, method or event; the parent field identifies the entity. |
| `tasks[].subtasks[].outputs` | array; items: string | Set of prediction outputs or artifacts specified for the enclosing task. |
| `tasks[].subtasks[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `tasks[].subtasks[].source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `tasks[].task_families` | array; items: string | Set of task/output families assigned in the enclosing review or task description. |
| `tasks[].task_family` | string | Broad category of task output or operation for the specific task. |
| `tasks[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `tasks[].task_subtype` | null / string | More specific task formulation, such as multi-label classification or instance segmentation. |
| `track_hierarchy_review` | object | Source-linked review of track hierarchy. |
| `track_hierarchy_review.award_category_count` | integer | Number of award categories; these can differ from the number of major tracks or analytical editions. |
| `track_hierarchy_review.interpretation` | string | Reviewer's scoped interpretation of the recorded source information; not additional organizer evidence. |
| `track_hierarchy_review.major_track_count` | integer | Number of major competition tracks explicitly distinguished in the associated hierarchy review. |
| `track_hierarchy_review.registered_to_implemented_task_mapping` | string | Source-recorded registered to implemented task mapping for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `track_hierarchy_review.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `track_relationship` | object | Structured entries for track relationship within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `track_relationship.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `track_relationship.combined_final_ranking_rule` | null | Optional field for combined final ranking rule in the enclosing record. It is unpopulated in this snapshot; neither a value nor a negative finding is established. |
| `track_relationship.counting_note` | string | Qualification or source distinction concerning counting. |
| `track_relationship.independent_award_structure` | null | Optional field for independent award structure in the enclosing record. It is unpopulated in this snapshot; neither a value nor a negative finding is established. |
| `track_relationship.separate_phases_and_leaderboards` | boolean | Whether the condition “separate phases and leaderboards” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `track_relationship.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `track_relationship.ta36_is_only_a_validation_stage_of_v2` | boolean | Whether the condition “ta36 is only a validation stage of v2” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `training_and_testing_note` | string | Qualification or source distinction concerning training and testing. |
| `training_data_note` | string | Qualification or source distinction concerning training data. |
| `vision_language_scope_review` | object | Source-linked review of vision language scope. |
| `vision_language_scope_review.declared_direction` | string | Source-recorded declared direction for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `vision_language_scope_review.final_track_assessment` | string | Evidence/status of final assessment for the specified track, without extending it to other tracks. |
| `vision_language_scope_review.participant_method_evidence` | string | Recorded documentary support for participant method. Preserve the task/phase scope and source qualifications. |
| `vision_language_scope_review.remaining_check` | string | Unresolved verification question retained after the current review. |
| `vision_language_scope_review.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `vision_language_scope_review.separate_capability_question` | string | Source-recorded separate capability question for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `vision_language_scope_review.statistics_scope` | string | Task, phase, cohort or source boundaries of statistics. |

<a id="task-taxonomy"></a>

## `task_taxonomy`

JSON parent path: `challenge.task_taxonomy`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.task_taxonomy`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `agent` | null / boolean | Task/objective flag for organizer-defined tools, retrieval, interaction or state-dependent actions; routine container execution alone does not qualify. |
| `classification` | null / boolean | Task flag for predicting categorical labels at the specified granularity. |
| `detection` | null / boolean | Task flag for identifying the presence and location of target entities or events. |
| `dialogue` | boolean | Whether the condition “dialogue” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `enhancement` | null / boolean | Task flag for improving image quality or restoring degraded imaging information. |
| `image_text_generation` | boolean | Whether the condition “image text generation” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `localization` | null / boolean | Task flag for locating target positions, landmarks, regions or image-grounded findings. |
| `prognosis` | null / boolean | Task flag for predicting a future clinical outcome or course. |
| `reasoning` | null | Task/objective flag for an explicitly evaluated rationale, evidence-linked explanation or structured justification. |
| `reconstruction` | null / boolean | Task flag for recovering an image or imaging representation from measured, sampled or degraded data. |
| `registration` | null / boolean | Task flag for estimating spatial correspondence or alignment between images or representations. |
| `report_generation` | null / boolean | Task/objective flag for generating image-grounded free-text reports or captions; structured field prediction is separate. |
| `segmentation` | null / boolean | Task flag for assigning labels or masks to spatial image elements or instances within the stated task scope. |
| `synthesis` | null / boolean | Task flag for generating images or other specified imaging outputs from source data. |
| `visual_question_answering` | null / boolean | Task flag for answering questions using image or video content together with language. |

<a id="review-coding"></a>

## `review_coding`

JSON parent path: `challenge.review_coding`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.review_coding`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `caption_generation_objective_assessed` | string | Recorded assessment status for image-grounded caption generation, separate from parsing or other language tasks. |
| `data_model_flow` | string | Direction of data/model exchange across the competition workflow, preserving phase-specific differences. |
| `development_access` | string | Classification of competition-time development-data access, preserving public download, registration, individual authorization and unresolved states. |
| `emerging_objectives` | null / array; items: string | Overlapping organizer-defined AI objective labels. The six analytical labels are defined below; labels do not prove assessment execution. |
| `foundation_model_objective` | string | Whether the organizer's stated objective concerns large-scale pretraining, reusable representations or adaptation of a pretrained/foundation model. |
| `foundation_model_objective_assessed` | string | Recorded assessment status for the foundation-model objective; does not automatically apply to every other objective in that edition. |
| `imaging_eligibility` | string | Source-recorded imaging eligibility for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `report_generation_label` | string | Source-recorded report generation label for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `stage_specific_objectives` | object | Structured entries for stage specific objectives within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `stage_specific_objectives.VQA` | boolean | Whether the condition “visual question answering” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `stage_specific_objectives.image_text_retrieval` | boolean | Whether the condition “image text retrieval” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `stage_specific_objectives.report_generation` | boolean | Task/objective flag for generating image-grounded free-text reports or captions; structured field prediction is separate. |
| `stage_specific_objectives.test` | string | Test-stage subset, quantity, procedure or outcome under the parent field; preserve its recorded unit and phase. |
| `stage_specific_objectives.training` | string | Training-stage data, quantities, rules or model-use arrangements, according to the parent field. |
| `supersedes` | string | Earlier statement or record that the enclosing revision replaces. |
| `task_families` | array; items: string | Set of task/output families assigned in the enclosing review or task description. |
| `task_objective_basis` | string | Evidence or reasoning supporting task objective. |
| `training_objectives` | array; items: string | Structured entries for training objectives within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `vision_language_objective` | string | Whether the organizer's objective involves image–language interaction, conditioning, generation or representation assessment. |
| `vision_language_objective_assessed` | string | Recorded assessment status for the vision–language objective within the named task and phase. |

<a id="task-objective-review"></a>

## `task_objective_review`

JSON parent path: `challenge.task_objective_review`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.task_objective_review`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `emerging_objectives` | array; items: string | Overlapping organizer-defined AI objective labels. The six analytical labels are defined below; labels do not prove assessment execution. |
| `foundation_model_basis` | string | Evidence or reasoning supporting foundation model. |
| `note_zh` | string | Chinese-language qualification or explanation for the enclosing review decision. |
| `previous_emerging_objectives` | array; items: string | Earlier/superseded value of emerging objectives, preserved to document a revision rather than a current observation. |
| `previous_task_families` | array; items: string | Earlier/superseded value of task families, preserved to document a revision rather than a current observation. |
| `review_date` | string | Date of the review operation described in the enclosing object. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `six_category_update` | object | Structured entries for six category update within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `six_category_update.added_objective` | string | Objective label added by the documented review decision, with the source and date retained. |
| `six_category_update.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `six_category_update.definition` | string | Operational or source definition of the enclosing variable, count or category. |
| `six_category_update.review_date` | string | Date of the review operation described in the enclosing object. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `sources` | array; items: object | Sources supporting the enclosing statement or dataset description, preserving document/source type and scope. |
| `sources[].local_source` | string | Path identifying a source in the original review archive, not a downloadable file inside this release. |
| `sources[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `sources[].section` | string | Section, figure, table or location within a supporting source. |
| `sources[].sha256` | string | Cryptographic checksum or revision identifier for the enclosing sha256; used for provenance rather than as a scientific measurement. |
| `sources[].url` | string | Web address of the enclosing source, document or resource. |
| `task_families` | array; items: string | Set of task/output families assigned in the enclosing review or task description. |
| `task_roles` | object | Structured entries for task roles within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `task_roles.Biomarker discovery / prediction` | string | Role of the `Biomarker discovery / prediction` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.Classification` | string | Role of the `Classification` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.Clinical reasoning` | string | Role of the `Clinical reasoning` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.Detection` | string | Role of the `Detection` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.Explanation` | string | Role of the `Explanation` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.Localization` | string | Role of the `Localization` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.Named entity extraction` | string | Role of the `Named entity extraction` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.Prognosis` | string | Role of the `Prognosis` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.Prompt generation` | string | Role of the `Prompt generation` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.Quality / suitability assessment` | string | Role of the `Quality / suitability assessment` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.Quantification / measurement` | string | Role of the `Quantification / measurement` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.Question generation` | string | Role of the `Question generation` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.Reconstruction` | string | Role of the `Reconstruction` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.Registration` | string | Role of the `Registration` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.Report generation` | string | Role of the `Report generation` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.Representation / model artifacts` | string | Role of the `Representation / model artifacts` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.Retrieval` | string | Role of the `Retrieval` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.Segmentation` | string | Role of the `Segmentation` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.Structured clinical field prediction` | string | Role of the `Structured clinical field prediction` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.Synthesis` | string | Role of the `Synthesis` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.Tracking` | string | Role of the `Tracking` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `task_roles.VQA / multimodal QA` | string | Role of the `VQA / multimodal QA` task family in this edition, such as participant output, downstream assessment or auxiliary task. |
| `text_output_rule` | string | Source-recorded text output rule for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |

<a id="current-output-classification"></a>

## `current_output_classification`

JSON parent path: `challenge.current_output_classification`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.current_output_classification`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `reason` | string | Reason for the enclosing decision, revision, exclusion or qualification. |
| `report_caption_generation` | boolean | Whether the condition “report caption generation” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `review_date` | string | Date of the review operation described in the enclosing object. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `structured_clinical_field_prediction` | boolean | Whether the condition “structured clinical field prediction” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `vision_language` | boolean | Whether the condition “vision language” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |

<a id="registered-task-taxonomy"></a>

## `registered_task_taxonomy`

JSON parent path: `challenge.registered_task_taxonomy`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.registered_task_taxonomy`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `agent` | null | Task/objective flag for organizer-defined tools, retrieval, interaction or state-dependent actions; routine container execution alone does not qualify. |
| `classification` | null | Task flag for predicting categorical labels at the specified granularity. |
| `detection` | boolean | Task flag for identifying the presence and location of target entities or events. |
| `enhancement` | null | Task flag for improving image quality or restoring degraded imaging information. |
| `localization` | boolean | Task flag for locating target positions, landmarks, regions or image-grounded findings. |
| `prognosis` | null | Task flag for predicting a future clinical outcome or course. |
| `reasoning` | null | Task/objective flag for an explicitly evaluated rationale, evidence-linked explanation or structured justification. |
| `reconstruction` | null | Task flag for recovering an image or imaging representation from measured, sampled or degraded data. |
| `registration` | null | Task flag for estimating spatial correspondence or alignment between images or representations. |
| `report_generation` | null | Task/objective flag for generating image-grounded free-text reports or captions; structured field prediction is separate. |
| `segmentation` | boolean | Task flag for assigning labels or masks to spatial image elements or instances within the stated task scope. |
| `synthesis` | null | Task flag for generating images or other specified imaging outputs from source data. |
| `visual_question_answering` | null | Task flag for answering questions using image or video content together with language. |

[Back to README](../../README.md#variable-dictionary)
