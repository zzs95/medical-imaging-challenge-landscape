# Submissions and execution constraints

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

Artifacts, platforms, final-stage execution, runtime, memory and submission limits.

## Field groups

- [`challenge.submission`](#submission)

<a id="submission"></a>

## `submission`

JSON parent path: `challenge.submission`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.submission`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `additional_artifacts` | array; items: object | Source-defined artifact/interface requirement for additional artifacts. Distinguish scored input/output from supporting code, model files or verification material. |
| `additional_artifacts[].artifact` | string | Source-defined artifact/interface requirement for artifact. Distinguish scored input/output from supporting code, model files or verification material. |
| `additional_artifacts[].contents` | string | Source-defined artifact/interface requirement for contents. Distinguish scored input/output from supporting code, model files or verification material. |
| `additional_artifacts[].purpose` | string | Stated purpose of the enclosing dataset, artifact, task or review operation. |
| `additional_artifacts[].role` | string | Role of the enclosing task, source, artifact or person; context determines whether it is scored, auxiliary or supporting. |
| `additional_artifacts[].task` | string | Task name or task-specific result/description associated with the enclosing entry. |
| `additional_materials` | array; items: string, object | Supporting or verification materials supplied in addition to the principal scored artifact. |
| `additional_materials[].artifact` | string | Source-defined artifact/interface requirement for artifact. Distinguish scored input/output from supporting code, model files or verification material. |
| `additional_materials[].contents` | string | Source-defined artifact/interface requirement for contents. Distinguish scored input/output from supporting code, model files or verification material. |
| `additional_materials[].execution_mode` | string | How the relevant method or assessment is run, including participant versus organizer/platform execution where specified. |
| `additional_materials[].material` | string | Source-recorded material for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `additional_materials[].phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. |
| `additional_materials[].purpose` | string | Stated purpose of the enclosing dataset, artifact, task or review operation. |
| `additional_materials[].role` | string | Role of the enclosing task, source, artifact or person; context determines whether it is scored, auxiliary or supporting. |
| `additional_materials[].task` | string | Task name or task-specific result/description associated with the enclosing entry. |
| `additional_materials_count_as_primary_scored_artifact` | boolean | Source-defined artifact/interface requirement for additional materials count as primary scored artifact. Distinguish scored input/output from supporting code, model files or verification material. |
| `container_max_size_gb` | integer | Specified submission/execution constraint for container max size GB. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. Unit/format: GB; denominator/scope follows field name. |
| `container_size_recommendation_gb` | integer | Reported numerical value for container size recommendation GB within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. Unit/format: GB; denominator/scope follows field name. |
| `decision_history` | array; items: object | Dated earlier decisions and revisions retained to show how the current classification was reached. |
| `decision_history[].previous_submission_type` | string | Earlier/superseded value of submission type, preserved to document a revision rather than a current observation. |
| `decision_history[].review_date` | string | Date of the review operation described in the enclosing object. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `delivery_evidence_status` | string | Recorded state of delivery evidence. Preserve the task/phase scope and source qualifications. |
| `delivery_review` | object | Source-linked review of delivery. |
| `delivery_review.actual_execution_record_status` | string | Recorded state of actual execution record. Preserve the task/phase scope and source qualifications. |
| `delivery_review.endpoint_status` | string | Recorded state of endpoint. Preserve the task/phase scope and source qualifications. |
| `delivery_review.excluded_inferences` | array; items: string | Structured entries for excluded inferences within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `delivery_review.execution_infrastructure_status` | string | Recorded state of execution infrastructure. Preserve the task/phase scope and source qualifications. |
| `delivery_review.format_status` | string | Recorded state of format. Preserve the task/phase scope and source qualifications. |
| `delivery_review.local_source` | string | Path identifying a source in the original review archive, not a downloadable file inside this release. |
| `delivery_review.source_type` | string | Kind of data or evidence source. In dataset records this describes cohort origin; in provenance it describes the supporting document or confirmation. |
| `development_artifact` | string | Source-defined artifact/interface requirement for development artifact. Distinguish scored input/output from supporting code, model files or verification material. |
| `editorial_phase_source_review` | object | Source-linked review of editorial phase source. |
| `editorial_phase_source_review.phases` | array; items: object | Structured entries for phases within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `editorial_phase_source_review.phases[].artifact` | string | Source-defined artifact/interface requirement for artifact. Distinguish scored input/output from supporting code, model files or verification material. |
| `editorial_phase_source_review.phases[].delivery` | string | Description or classification of how participants receive data or deliver submissions in the stated workflow. |
| `editorial_phase_source_review.phases[].phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. |
| `editorial_phase_source_review.phases[].source_section` | string | Section or location within the supporting source. |
| `editorial_phase_source_review.phases[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `editorial_phase_source_review.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `evaluation_operator` | string | Party responsible for the evaluation procedure described in the enclosing record. |
| `evidence_basis` | string | Evidence or reasoning supporting evidence. |
| `evidence_stage` | string | Stage represented by the evidence, such as registered design, operational instructions or reported execution/results. |
| `execution` | string | Description or evidence state of executing the relevant method or assessment. |
| `execution_mode` | null / string | How the relevant method or assessment is run, including participant versus organizer/platform execution where specified. |
| `final_artifact` | string | Source-defined artifact/interface requirement for final artifact. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase` | array; items: object | Source-defined artifact/interface requirement for format by task or phase. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].JSONL_fields` | array; items: string | Source-defined artifact/interface requirement for JSONL fields. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].archive` | string | Source-defined artifact/interface requirement for archive. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].archive_examples` | array; items: string | Source-defined artifact/interface requirement for archive examples. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].artifact` | string | Source-defined artifact/interface requirement for artifact. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].class_confidences_per_study` | integer | Source-defined artifact/interface requirement for class confidences per study. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].column_order` | string | Source-defined artifact/interface requirement for column order. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].column_template` | null | Source-defined artifact/interface requirement for column template. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].columns` | string / array; items: string | Source-defined artifact/interface requirement for columns. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].confirmation_basis` | string | Evidence or reasoning supporting confirmation. |
| `format_by_task_or_phase[].container_technology` | string | Container technology specified for packaging or running the method, such as Docker or Singularity. |
| `format_by_task_or_phase[].contents` | array; items: string | Source-defined artifact/interface requirement for contents. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].delimiter` | string | Specified submission/execution constraint for delimiter. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `format_by_task_or_phase[].delivery` | string | Description or classification of how participants receive data or deliver submissions in the stated workflow. |
| `format_by_task_or_phase[].detailed_instructions` | string | Source-recorded detailed instructions for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `format_by_task_or_phase[].directories` | object | Structured entries for directories within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `format_by_task_or_phase[].directories.data/` | string | Source-recorded data/ for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `format_by_task_or_phase[].directories.mappings/` | array; items: string | Structured entries for mappings/ within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `format_by_task_or_phase[].example_filename` | string | Source-defined artifact/interface requirement for example filename. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].execution` | string | Description or evidence state of executing the relevant method or assessment. |
| `format_by_task_or_phase[].file` | string | Source-defined artifact/interface requirement for file. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].file_extension` | null | Source-defined artifact/interface requirement for file extension. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].filename` | string | Source-defined artifact/interface requirement for filename. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].format` | string | Required encoding/file format of the enclosing input, output or submitted artifact. |
| `format_by_task_or_phase[].generated_output` | string | Source-defined artifact/interface requirement for generated output. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].header` | boolean | Whether the condition “header” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `format_by_task_or_phase[].identifier` | string | Identifier retained for the enclosing entity, preserving the original source namespace. |
| `format_by_task_or_phase[].images` | object | Structured entries for images within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `format_by_task_or_phase[].images.channels` | string | Input/output channels described for the enclosing image, model interface or submitted artifact. |
| `format_by_task_or_phase[].images.count` | integer | Number of the entity identified by unit, source_term and the enclosing task/phase. |
| `format_by_task_or_phase[].images.format` | string | Required encoding/file format of the enclosing input, output or submitted artifact. |
| `format_by_task_or_phase[].images.size` | array; items: integer | Structured entries for size within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `format_by_task_or_phase[].implementation_confirmed` | boolean | Whether the condition “implementation confirmed” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `format_by_task_or_phase[].index_base` | integer | Indexing origin used by the enclosing source list, for example zero-based or one-based indexing. |
| `format_by_task_or_phase[].input_format` | string | Source-defined artifact/interface requirement for input format. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].labels` | array; items: string | Target labels or their source-reported number, according to the recorded value type and context. |
| `format_by_task_or_phase[].mapping` | string | Correspondence between the source-defined entities, labels, task names or variables specified by the parent object. |
| `format_by_task_or_phase[].mapping_headers` | array; items: string | Structured entries for mapping headers within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `format_by_task_or_phase[].max_submissions_per_day` | integer | Specified submission/execution constraint for max submissions per day. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `format_by_task_or_phase[].method_description` | string | Source description of method. |
| `format_by_task_or_phase[].model_repository` | string | Source-recorded model repository for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `format_by_task_or_phase[].multiple_CUI_separator` | string | Source-defined artifact/interface requirement for multiple CUI separator. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].observed_filename` | string | Source-defined artifact/interface requirement for observed filename. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].optional_dependency_file` | string | Source-defined artifact/interface requirement for optional dependency file. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].optional_directory` | string | Source-defined artifact/interface requirement for optional directory. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].outer_packaging` | null | Source-defined artifact/interface requirement for outer packaging. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].output` | string | Prediction, artifact or information produced by the task or model. |
| `format_by_task_or_phase[].output_format` | string | Source-defined artifact/interface requirement for output format. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].per_run` | array; items: string | Specified submission/execution constraint for per run. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `format_by_task_or_phase[].permitted_file_extensions_examples` | array; items: string | Source-defined artifact/interface requirement for permitted file extensions examples. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. |
| `format_by_task_or_phase[].prebuilt_image_required` | boolean | Whether the condition “prebuilt image required” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `format_by_task_or_phase[].prediction_pattern` | string | Source-defined artifact/interface requirement for prediction pattern. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].prediction_values_per_image` | integer | Specified submission/execution constraint for prediction values per image. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `format_by_task_or_phase[].probability_range` | array; items: integer | Structured entries for probability range within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `format_by_task_or_phase[].python_file_role` | string | Source-defined artifact/interface requirement for python file role. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].registration` | string | Task flag for estimating spatial correspondence or alignment between images or representations. |
| `format_by_task_or_phase[].registration_command` | string | Source-recorded registration command for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `format_by_task_or_phase[].required_class` | string | Source-defined artifact/interface requirement for required class. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].required_file` | string | Source-defined artifact/interface requirement for required file. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].required_files` | array; items: string | Source-defined artifact/interface requirement for required files. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].required_materials` | array; items: string | Structured entries for required materials within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `format_by_task_or_phase[].root_script` | string | Source-defined artifact/interface requirement for root script. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].row_unit` | string | Entity represented by one row in the submitted table or reported data, such as a case, image or class. |
| `format_by_task_or_phase[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `format_by_task_or_phase[].score_feedback` | string | Scores or other assessment information returned to participants for the stated phase. |
| `format_by_task_or_phase[].score_range` | array; items: integer | Structured entries for score range within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `format_by_task_or_phase[].scores_per_case` | integer | Specified submission/execution constraint for scores per case. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `format_by_task_or_phase[].sole_file` | string | Source-defined artifact/interface requirement for sole file. Distinguish scored input/output from supporting code, model files or verification material. |
| `format_by_task_or_phase[].task` | string | Task name or task-specific result/description associated with the enclosing entry. |
| `format_by_task_or_phase[].tasks` | array; items: string | Task-specific objects or descriptions; each has its own scope, inputs, outputs or assessment information where available. |
| `format_by_task_or_phase[].unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `format_by_task_or_phase[].value` | string | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `format_limitations` | array; items: string | Specified submission/execution constraint for format limitations. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `generated_output` | object | Source-defined artifact/interface requirement for generated output. Distinguish scored input/output from supporting code, model files or verification material. |
| `generated_output.columns` | null / array; items: string | Source-defined artifact/interface requirement for columns. Distinguish scored input/output from supporting code, model files or verification material. |
| `generated_output.filename` | string | Source-defined artifact/interface requirement for filename. Distinguish scored input/output from supporting code, model files or verification material. |
| `implementation_verified_for_all_tracks` | boolean | Whether the condition “implementation verified for all tracks” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `independent_source_check` | object | Structured entries for independent source check within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `independent_source_check.checked_on` | string | Date of the documented check of the enclosing source or field. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `independent_source_check.finding` | string | Specific documentary or analytical observation recorded from the source or review. |
| `independent_source_check.url` | string | Web address of the enclosing source, document or resource. |
| `maximum_submissions_per_team_per_phase` | integer | Specified submission/execution constraint for maximum submissions per team per phase. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `maximum_test_submissions_per_team` | integer | Specified submission/execution constraint for maximum test submissions per team. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `mechanism` | string | Submission or execution mechanism described for the enclosing task or phase. |
| `method_report` | string | Source-recorded method report for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `official_guide_evidence` | object | Recorded documentary support for official guide. Preserve the task/phase scope and source qualifications. |
| `official_guide_evidence.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `official_guide_evidence.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `official_guide_evidence.source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `one_shot_submission` | object | Structured entries for one shot submission within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `one_shot_submission.inference_execution` | string | Description/classification of where and by whom inference is performed in the stated evaluation scope. |
| `one_shot_submission.labels` | object | Target labels or their source-reported number, according to the recorded value type and context. |
| `one_shot_submission.labels.0` | string | Value associated with source-defined code/key `0` in the enclosing mapping; the same code can have a different meaning in another task. |
| `one_shot_submission.labels.1` | string | Value associated with source-defined code/key `1` in the enclosing mapping; the same code can have a different meaning in another task. |
| `one_shot_submission.note` | string | Contextual qualification, uncertainty or source distinction for the enclosing item. |
| `one_shot_submission.prediction_column` | string | Source-defined artifact/interface requirement for prediction column. Distinguish scored input/output from supporting code, model files or verification material. |
| `one_shot_submission.provided_template` | string | Source-recorded provided template for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `one_shot_submission.submission_format` | string | Required file/packaging format for the stated scored or auxiliary submission. |
| `one_shot_submission.test_input_format` | string | Source-defined artifact/interface requirement for test input format. Distinguish scored input/output from supporting code, model files or verification material. |
| `output_resolution` | array; items: integer | Source-defined artifact/interface requirement for output resolution. Distinguish scored input/output from supporting code, model files or verification material. |
| `phase_attribution` | string | Assignment of the source or requirement to a specific competition phase, with ambiguity preserved. |
| `phase_specific_requirements` | array; items: object | Structured entries for phase specific requirements within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `phase_specific_requirements[].annotations_visible_to_participants` | boolean | Whether the condition “annotations visible to participants” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `phase_specific_requirements[].data_visible_to_participants` | boolean | Whether the enclosing phase's input data are available to participants. |
| `phase_specific_requirements[].evaluation_operator` | string | Party responsible for the evaluation procedure described in the enclosing record. |
| `phase_specific_requirements[].evidence_scope` | string | Boundary of what the supporting evidence establishes, including specification versus actual execution. |
| `phase_specific_requirements[].format` | string | Required encoding/file format of the enclosing input, output or submitted artifact. |
| `phase_specific_requirements[].image_count` | integer | Number of images under the source's image definition; do not equate with patients or three-dimensional volumes. Unit/format: images; stated cohort/split. |
| `phase_specific_requirements[].phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. |
| `phase_specific_requirements[].source_sections` | array; items: string | Structured entries for source sections within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `phase_specific_requirements[].submission_type` | string | Recorded kind of submitted artifact or workflow, such as predictions, code, weights, containers or a platform-executed notebook. |
| `phases` | array; items: object | Structured entries for phases within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `phases[].artifact` | string | Source-defined artifact/interface requirement for artifact. Distinguish scored input/output from supporting code, model files or verification material. |
| `phases[].automated_image_retrieval_and_execution_documented` | boolean | Whether the condition “automated image retrieval and execution documented” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `phases[].competition_id` | integer | Identifier of the competition on its hosting platform, not its analytical edition count. |
| `phases[].data_model_flow` | string | Direction of data/model exchange across the competition workflow, preserving phase-specific differences. |
| `phases[].eligible_participants` | string | Source-recorded eligible participants for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `phases[].evaluation_status` | string | Recorded state of evaluation. Preserve the task/phase scope and source qualifications. |
| `phases[].execution_evidence` | string | Evidence that the specified assessment or execution actually occurred within the recorded task and phase. |
| `phases[].execution_mode` | string | How the relevant method or assessment is run, including participant versus organizer/platform execution where specified. |
| `phases[].format` | string | Required encoding/file format of the enclosing input, output or submitted artifact. |
| `phases[].inference_executor` | string | Party executing model inference on the designated evaluation inputs; distinct from the submission service or metric-computation party. |
| `phases[].model_executed_by_evaluation_system` | boolean | Whether the condition “model executed by evaluation system” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `phases[].operational_execution_independently_verified` | boolean | Whether the condition “operational execution independently verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `phases[].output` | string | Prediction, artifact or information produced by the task or model. |
| `phases[].phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. |
| `phases[].platform` | string | Named service involved in the enclosing data, submission or evaluation operation; service naming alone does not establish the executor. |
| `phases[].runtime_scored` | boolean | Whether the condition “runtime scored” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `phases[].scoring_automatically_triggered` | null | Whether scoring is automatically initiated by the stated submission/workflow event, according to the source. |
| `phases[].scoring_submission` | string | Artifact or submission record used for scoring, distinct from auxiliary verification materials. |
| `phases[].server_architecture` | string | Source-recorded server architecture for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `phases[].service` | string | Named technical service associated with the enclosing delivery, submission or scoring operation. |
| `phases[].source` | string | Source identifier, URL, citation, original wording or source object for the enclosing item. |
| `phases[].submission_entry` | string | Source-defined artifact/interface requirement for submission entry. Distinguish scored input/output from supporting code, model files or verification material. |
| `phases[].submission_format` | null / string | Required file/packaging format for the stated scored or auxiliary submission. |
| `phases[].submission_type` | string | Recorded kind of submitted artifact or workflow, such as predictions, code, weights, containers or a platform-executed notebook. |
| `phases[].submitted_artifact` | string | Source-defined artifact/interface requirement for submitted artifact. Distinguish scored input/output from supporting code, model files or verification material. |
| `phases[].test_data` | string | Input data provided or withheld for the stated testing stage. |
| `platform` | null / string | Named service involved in the enclosing data, submission or evaluation operation; service naming alone does not establish the executor. |
| `platform_qualification` | string | Restriction on interpreting the recorded platform name or attributing a function to it. |
| `platform_scope` | string | Task, phase, cohort or source boundaries of platform. |
| `platform_url` | string | Web address for platform. |
| `portal_review_source` | string | Source supporting portal review. |
| `portal_url` | string | Web address for portal. |
| `preregistered_artifact` | string | Source-defined artifact/interface requirement for preregistered artifact. Distinguish scored input/output from supporting code, model files or verification material. |
| `preregistered_submission_limits` | object | Specified submission/execution constraint for preregistered submission limits. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `preregistered_submission_limits.container_debug` | integer | Reported numerical value for container debug within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `preregistered_submission_limits.final` | integer | Reported numerical value for final within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `preregistered_submission_limits.preliminary` | integer | Reported numerical value for preliminary within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `preregistered_submission_limits.preliminary_per_week` | integer | Specified submission/execution constraint for preliminary per week. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `previous_recorded_design` | object | Earlier/superseded value of recorded design, preserved to document a revision rather than a current observation. |
| `previous_recorded_design.qualification` | string | Restriction on what the enclosing evidence or decision can establish. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_recorded_design.submission_type` | string | Recorded kind of submitted artifact or workflow, such as predictions, code, weights, containers or a platform-executed notebook. This occurrence is historical and must be interpreted within its enclosing revision. |
| `primary_artifacts` | array; items: string | Source-defined artifact/interface requirement for primary artifacts. Distinguish scored input/output from supporting code, model files or verification material. |
| `protocol_source` | string | Source supporting protocol. |
| `qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `reconstruction_submission_specification` | object | Structured entries for reconstruction submission specification within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `reconstruction_submission_specification.archive_format` | string | Source-defined artifact/interface requirement for archive format. Distinguish scored input/output from supporting code, model files or verification material. |
| `reconstruction_submission_specification.archive_name_template` | string | Source-defined artifact/interface requirement for archive name template. Distinguish scored input/output from supporting code, model files or verification material. |
| `reconstruction_submission_specification.array_dimensions` | integer | Dimensions or number of axes of the specified array, as represented by the source value. |
| `reconstruction_submission_specification.array_shape` | null | Source-defined artifact/interface requirement for array shape. Distinguish scored input/output from supporting code, model files or verification material. |
| `reconstruction_submission_specification.axis_order` | null | Order of spatial, channel or other axes in the specified array/output format. |
| `reconstruction_submission_specification.directories` | object | Structured entries for directories within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `reconstruction_submission_specification.directories.ID_results` | object | Structured entries for identifier results within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `reconstruction_submission_specification.directories.ID_results.examples` | array; items: string | Structured entries for examples within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `reconstruction_submission_specification.directories.ID_results.filename_pattern` | string | Source-defined artifact/interface requirement for filename pattern. Distinguish scored input/output from supporting code, model files or verification material. |
| `reconstruction_submission_specification.directories.OOD_results` | object | Structured entries for OOD results within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `reconstruction_submission_specification.directories.OOD_results.examples` | array; items: string | Structured entries for examples within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `reconstruction_submission_specification.directories.OOD_results.filename_pattern` | string | Source-defined artifact/interface requirement for filename pattern. Distinguish scored input/output from supporting code, model files or verification material. |
| `reconstruction_submission_specification.format_basis` | string | Evidence or reasoning supporting format. |
| `reconstruction_submission_specification.prediction_format` | string | Source-defined artifact/interface requirement for prediction format. Distinguish scored input/output from supporting code, model files or verification material. |
| `reconstruction_submission_specification.quantization_policy` | string | Permission, restriction or procedural rule governing quantization. |
| `reconstruction_submission_specification.storage_dtype` | string | Storage data type used for the enclosing array or output file. |
| `reconstruction_submission_specification.value_range` | array; items: integer | Structured entries for value range within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `reconstruction_submission_specification.value_semantics` | string | Meaning of the values encoded in the enclosing prediction/label field, distinct from their storage type. |
| `registered_design_submission_type` | string | Source-recorded registered design submission type for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `registered_task_submissions` | array; items: object | Structured entries for registered task submissions within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `registered_task_submissions[].protocol_description` | string | Source description of protocol. |
| `registered_task_submissions[].source_reference` | object | Reference to the supporting document or source, possibly with section, URL and archival location. |
| `registered_task_submissions[].source_reference.local_protocol` | string | Original archive path of a registered protocol; the protocol file itself is not included in this metadata package. |
| `registered_task_submissions[].source_reference.registered_task_index` | integer | Task position/identifier in the registered protocol; it can differ from later operational numbering. |
| `registered_task_submissions[].source_reference.section` | string | Section, figure, table or location within a supporting source. |
| `registered_task_submissions[].source_reference.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `registered_task_submissions[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `repository_output_format_evidence` | object | Recorded documentary support for repository output format. Preserve the task/phase scope and source qualifications. |
| `repository_output_format_evidence.completed_final_assessment` | string | Source-recorded completed final assessment for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `repository_output_format_evidence.date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `repository_output_format_evidence.documented_output_format` | string | Source-defined artifact/interface requirement for documented output format. Distinguish scored input/output from supporting code, model files or verification material. |
| `repository_output_format_evidence.finding` | string | Specific documentary or analytical observation recorded from the source or review. |
| `repository_output_format_evidence.limits` | string | Set of limits applied to the enclosing resources or procedures. |
| `repository_output_format_evidence.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `repository_output_format_evidence.results_file_caution` | string | Source-defined artifact/interface requirement for results file caution. Distinguish scored input/output from supporting code, model files or verification material. |
| `repository_output_format_evidence.scoring_execution_platform` | null | Platform/environment on which metric computation occurs, where established. |
| `repository_output_format_evidence.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `repository_output_format_evidence.submission_service` | null | Service receiving the scored submission, distinct from inference and scoring execution. |
| `repository_output_format_evidence.tree_sha` | string | Cryptographic checksum or revision identifier for the enclosing tree; used for provenance rather than as a scientific measurement. |
| `required_artifacts` | array; items: string | Files, models, code or other artifacts explicitly required by the stated submission procedure. |
| `required_prediction_columns` | array; items: string | Source-defined artifact/interface requirement for required prediction columns. Distinguish scored input/output from supporting code, model files or verification material. |
| `review_date` | string | Date of the review operation described in the enclosing object. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `review_source` | string | Source supporting review. |
| `reviewed_phase_submissions` | array; items: object | Structured entries for reviewed phase submissions within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `reviewed_phase_submissions[].artifact` | string | Source-defined artifact/interface requirement for artifact. Distinguish scored input/output from supporting code, model files or verification material. |
| `reviewed_phase_submissions[].inference_execution` | string | Description/classification of where and by whom inference is performed in the stated evaluation scope. |
| `reviewed_phase_submissions[].phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. |
| `reviewed_phase_submissions[].scoring_service` | string | Service used to compute or deliver evaluation scores. |
| `reviewed_phase_submissions[].submission_type` | string | Recorded kind of submitted artifact or workflow, such as predictions, code, weights, containers or a platform-executed notebook. |
| `rule_version_review` | object | Source-linked review of rule version. |
| `rule_version_review.implemented_submission` | object | Structured entries for implemented submission within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `rule_version_review.implemented_submission.evidence_ids` | array; items: string | Identifiers of specific evidence items supporting the enclosing interpretation; archival ledgers may be outside this package. |
| `rule_version_review.implemented_submission.model_interface` | array; items: string | Structured entries for model interface within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `rule_version_review.implemented_submission.submission_type` | string | Recorded kind of submitted artifact or workflow, such as predictions, code, weights, containers or a platform-executed notebook. |
| `rule_version_review.note` | string | Contextual qualification, uncertainty or source distinction for the enclosing item. |
| `rule_version_review.registered_design` | object | Structured entries for registered design within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `rule_version_review.registered_design.source` | string | Source identifier, URL, citation, original wording or source object for the enclosing item. |
| `rule_version_review.registered_design.submission_type` | string | Recorded kind of submitted artifact or workflow, such as predictions, code, weights, containers or a platform-executed notebook. |
| `rule_version_review.registered_design.test_submission_limit` | integer | Specified submission/execution constraint for test submission limit. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `rule_version_review.registered_design.validation_successful_submission_limit` | integer | Specified submission/execution constraint for validation successful submission limit. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `rule_version_review.retrospective_limits_reported_by_user` | object | Specified submission/execution constraint for retrospective limits reported by user. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `rule_version_review.retrospective_limits_reported_by_user.independently_verified_in_this_update` | boolean | Whether the condition “independently verified in this update” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `rule_version_review.retrospective_limits_reported_by_user.source` | string | Source identifier, URL, citation, original wording or source object for the enclosing item. |
| `rule_version_review.retrospective_limits_reported_by_user.test` | integer | Test-stage subset, quantity, procedure or outcome under the parent field; preserve its recorded unit and phase. |
| `rule_version_review.retrospective_limits_reported_by_user.validation` | string | Validation-stage data, quantities, submissions or results; not automatically final-test evidence. |
| `runtime_limits` | null / object | Documented constraints for executing a submitted method, preserving time, host RAM and GPU memory as separate quantities. |
| `runtime_limits.average_execution_time_per_submission_minutes` | integer | Number of average execution time per submission minutes in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. Unit/format: minutes; denominator/scope follows field name. |
| `runtime_limits.average_processing_time_minutes` | integer | Reported numerical value for average processing time minutes within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. Unit/format: minutes; denominator/scope follows field name. |
| `runtime_limits.cpu` | string | CPU hardware description for the stated execution setting. |
| `runtime_limits.cpu_cores` | integer | Number of CPU cores specified for the stated execution setting. |
| `runtime_limits.cpu_count` | integer | Number of CPUs/CPU units as explicitly described by the source; do not assume equivalence to core count. |
| `runtime_limits.gpu` | null / string | GPU model or GPU resource assigned/recommended for the enclosing execution setting; retain whether mandatory or advisory. |
| `runtime_limits.gpu_options` | array; items: string | Structured entries for GPU options within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `runtime_limits.gpu_vram_gb` | null / integer | GPU video-memory capacity or limit in GB for the stated hardware/rule; hardware capacity and an enforced software ceiling are distinct. Unit/format: GB; denominator/scope follows field name. |
| `runtime_limits.max_container_size_gb` | integer | Specified submission/execution constraint for max container size GB. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. Unit/format: GB; denominator/scope follows field name. |
| `runtime_limits.max_gpus` | integer | Specified submission/execution constraint for max gpus. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `runtime_limits.max_inference_seconds_per_frame` | integer | Specified submission/execution constraint for max inference seconds per frame. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. Unit/format: seconds; denominator/scope follows field name. |
| `runtime_limits.max_processing_time_per_algorithm_job_minutes` | integer | Specified submission/execution constraint for max processing time per algorithm job minutes. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. Unit/format: minutes; denominator/scope follows field name. |
| `runtime_limits.max_processing_time_per_batch_minutes` | integer | Specified submission/execution constraint for max processing time per batch minutes. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. Unit/format: minutes; denominator/scope follows field name. |
| `runtime_limits.max_processing_time_per_case_minutes` | null / integer | Maximum specified processing time for one case, in minutes; check whether this is a declared rule or enforced limit. Unit/format: minutes; denominator/scope follows field name. |
| `runtime_limits.max_processing_time_per_case_seconds` | integer | Specified submission/execution constraint for max processing time per case seconds. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. Unit/format: seconds; denominator/scope follows field name. |
| `runtime_limits.max_processing_time_per_class_seconds` | integer | Specified submission/execution constraint for max processing time per class seconds. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. Unit/format: seconds; denominator/scope follows field name. |
| `runtime_limits.max_processing_time_per_image_seconds` | integer | Specified submission/execution constraint for max processing time per image seconds. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. Unit/format: seconds; denominator/scope follows field name. |
| `runtime_limits.max_processing_time_per_sample_ms` | integer | Specified submission/execution constraint for max processing time per sample milliseconds. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. Unit/format: milliseconds; denominator/scope follows field name. |
| `runtime_limits.max_processing_time_total_hours` | integer | Specified submission/execution constraint for max processing time total hours. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. Unit/format: hours; denominator/scope follows field name. |
| `runtime_limits.max_processing_time_validation_set_hours` | integer | Specified submission/execution constraint for max processing time validation set hours. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. Unit/format: hours; denominator/scope follows field name. |
| `runtime_limits.max_ram_gb` | null / integer | Maximum specified host/system RAM in GB; not a GPU-memory ceiling. Unit/format: GB; denominator/scope follows field name. |
| `runtime_limits.max_studies_per_batch` | integer | Specified submission/execution constraint for max studies per batch. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `runtime_limits.maximum_full_test_processing_minutes` | integer | Specified submission/execution constraint for maximum full test processing minutes. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. Unit/format: minutes; denominator/scope follows field name. |
| `runtime_limits.maximum_processing_minutes_per_100_images` | integer | Specified submission/execution constraint for maximum processing minutes per 100 images. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. Unit/format: minutes; denominator/scope follows field name. |
| `runtime_limits.ram_options_gb` | array; items: integer | Structured entries for host RAM options GB within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. Unit/format: GB; denominator/scope follows field name. |
| `runtime_limits.reserved_ram_gb` | null / integer | Host/system RAM reserved for infrastructure or non-method processes, in GB, as stated by the source. Unit/format: GB; denominator/scope follows field name. |
| `runtime_limits.runtime_limit_scope` | string | Task, phase, cohort or source boundaries of runtime limit. |
| `runtime_limits_by_task` | array; items: object | Specified submission/execution constraint for runtime limits by task. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `runtime_limits_by_task[].cpu_only` | boolean | Whether the condition “cpu only” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `runtime_limits_by_task[].gpu_required` | boolean | Whether the condition “GPU required” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `runtime_limits_by_task[].max_ram_gb` | integer | Maximum specified host/system RAM in GB; not a GPU-memory ceiling. Unit/format: GB; denominator/scope follows field name. |
| `runtime_limits_by_task[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `scope_note` | string | Qualification or source distinction concerning scope. |
| `scoring_submission_review` | object | Source-linked review of scoring submission. |
| `scoring_submission_review.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `scoring_submission_review.date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `scoring_submission_review.local_source` | string | Path identifying a source in the original review archive, not a downloadable file inside this release. |
| `scoring_submission_review.source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `source_code_requirement` | object | Structured entries for source code requirement within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `source_code_requirement.hosting` | string | Service hosting the relevant dataset or download resources. |
| `source_code_requirement.license` | string | Licence designation attached to the enclosing data, software or publication resource; those resource types are distinct. |
| `source_code_requirement.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `source_reference` | string | Reference to the supporting document or source, possibly with section, URL and archival location. |
| `source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `submission_archive_contents` | array; items: object | Source-defined artifact/interface requirement for submission archive contents. Distinguish scored input/output from supporting code, model files or verification material. |
| `submission_archive_contents[].content` | string | Information that the enclosing file or artifact must contain. |
| `submission_archive_contents[].count` | null / integer | Number of the entity identified by unit, source_term and the enclosing task/phase. |
| `submission_archive_contents[].format` | string | Required encoding/file format of the enclosing input, output or submitted artifact. |
| `submission_artifact` | string | Artifact submitted for the enclosing phase, distinct from the output later generated by an executed model. |
| `submission_contact` | string | Source-recorded submission contact for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `submission_entry` | string | Source-defined artifact/interface requirement for submission entry. Distinguish scored input/output from supporting code, model files or verification material. |
| `submission_entry_evidence` | string | Recorded documentary support for submission entry. Preserve the task/phase scope and source qualifications. |
| `submission_evidence_status` | string | Recorded state of submission evidence. Preserve the task/phase scope and source qualifications. |
| `submission_format` | string | Required file/packaging format for the stated scored or auxiliary submission. |
| `submission_limits` | null / object | Limits on the number or timing of submissions, preserving phase, team/user unit and successful/failed-attempt rules. |
| `submission_limits.additional_distinct_final_algorithms_possible_with_organizer_approval` | null | Whether extra distinct final algorithms may be submitted after organizer approval. |
| `submission_limits.debug_upload_attempts` | integer | Number of debug upload attempts in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `submission_limits.development_submissions` | integer | Number of development submissions in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `submission_limits.development_submissions_per_participant_per_track` | integer | Specified submission/execution constraint for development submissions per participant per track. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.development_submissions_per_task` | integer | Specified submission/execution constraint for development submissions per task. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.development_submissions_per_team` | integer | Specified submission/execution constraint for development submissions per team. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.development_submissions_per_team_per_week` | integer | Specified submission/execution constraint for development submissions per team per week. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.development_submissions_per_week` | integer | Specified submission/execution constraint for development submissions per week. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.development_submissions_total` | integer | Number of development submissions total in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `submission_limits.distinct_extra_algorithms` | string | Source-recorded distinct extra algorithms for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `submission_limits.evaluation_submissions_per_person_per_track` | integer | Number of evaluation submissions per person per track in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `submission_limits.evaluation_uploads` | integer | Number of evaluation uploads in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `submission_limits.final_algorithms_per_task` | integer | Specified submission/execution constraint for final algorithms per task. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.final_submissions` | integer | Number of final submissions in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `submission_limits.final_submissions_per_task` | integer | Specified submission/execution constraint for final submissions per task. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.final_submissions_per_team` | null / integer | Maximum final-stage submissions permitted for one team. |
| `submission_limits.final_submissions_per_team_across_categories` | integer | Specified submission/execution constraint for final submissions per team across categories. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.final_submissions_per_team_per_phase` | integer | Specified submission/execution constraint for final submissions per team per phase. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.final_submissions_per_team_per_task` | integer | Specified submission/execution constraint for final submissions per team per task. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.final_submissions_per_track_per_task` | integer | Specified submission/execution constraint for final submissions per track per task. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.final_successful_submissions` | integer | Number of final successful submissions in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `submission_limits.final_successful_submissions_per_track` | integer | Number of final successful submissions per track in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `submission_limits.final_test_submissions_total` | integer | Number of final test submissions total in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `submission_limits.final_valid_submissions_per_task` | integer | Specified submission/execution constraint for final valid submissions per task. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.last_final_submission_counts` | boolean | Whether the condition “last final submission counts” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `submission_limits.max_submissions_per_team` | integer | Specified submission/execution constraint for max submissions per team. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.max_team_members` | integer | Specified submission/execution constraint for max team members. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.max_teams_per_organization` | integer | Specified submission/execution constraint for max teams per organization. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.phase1_runs_per_team` | integer | Specified submission/execution constraint for phase1 runs per team. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.phase2_runs_per_team` | integer | Specified submission/execution constraint for phase2 runs per team. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.pre_evaluation_submissions` | integer | Number of pre evaluation submissions in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `submission_limits.preliminary_phase2_submissions` | integer | Number of preliminary phase2 submissions in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `submission_limits.preliminary_submissions` | integer | Number of preliminary submissions in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `submission_limits.preliminary_submissions_per_task` | integer | Specified submission/execution constraint for preliminary submissions per task. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.preliminary_submissions_per_team` | integer | Specified submission/execution constraint for preliminary submissions per team. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.preliminary_submissions_per_team_per_day` | integer | Specified submission/execution constraint for preliminary submissions per team per day. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.preliminary_submissions_per_team_per_week` | integer | Specified submission/execution constraint for preliminary submissions per team per week. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.preliminary_submissions_per_user_per_task` | integer | Specified submission/execution constraint for preliminary submissions per user per task. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.preliminary_submissions_per_week` | integer | Specified submission/execution constraint for preliminary submissions per week. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.preliminary_test_submissions_total` | integer | Number of preliminary test submissions total in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `submission_limits.preliminary_valid_submissions_per_task` | integer | Specified submission/execution constraint for preliminary valid submissions per task. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.qualification_test_submissions` | integer | Number of qualification test submissions in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `submission_limits.qualification_validation_submissions` | integer | Number of qualification validation submissions in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `submission_limits.sanity_check_max_attempts_per_team` | integer | Specified submission/execution constraint for sanity check max attempts per team. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.sanity_check_submissions_per_team_per_week` | integer | Specified submission/execution constraint for sanity check submissions per team per week. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.sanity_check_successful_submissions_per_day` | null / integer | Maximum successful sanity-check submissions per day under the documented counting unit. |
| `submission_limits.selected_submission` | string | Submission chosen for scoring/ranking under the source's selection rule. |
| `submission_limits.submissions_per_day` | integer | Specified submission/execution constraint for submissions per day. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.submissions_per_team` | integer | Specified submission/execution constraint for submissions per team. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.submissions_per_week` | integer | Specified submission/execution constraint for submissions per week. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.testing_submissions_including_failures` | integer | Number of testing submissions including failures in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `submission_limits.total_submissions_per_participant` | integer | Specified submission/execution constraint for total submissions per participant. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.training_phase_submissions` | integer | Number of training phase submissions in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `submission_limits.validation_submissions` | integer | Number of validation submissions in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `submission_limits.validation_submissions_per_day` | integer | Specified submission/execution constraint for validation submissions per day. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.validation_submissions_per_team` | integer | Specified submission/execution constraint for validation submissions per team. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_limits.validation_submissions_per_week` | integer | Specified submission/execution constraint for validation submissions per week. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `submission_platform` | string | Platform receiving the submission; its name alone does not establish execution location. |
| `submission_status` | string | Recorded state of submission. Preserve the task/phase scope and source qualifications. |
| `submission_type` | null / string / array; items: string | Recorded kind of submitted artifact or workflow, such as predictions, code, weights, containers or a platform-executed notebook. |
| `submission_type_scope` | string | Task, phase, cohort or source boundaries of submission type. |
| `submission_url` | null | Web address for submission. |
| `submission_workflow_review` | object | Source-linked review of submission workflow. |
| `submission_workflow_review.basis_type` | string | Kind of evidence underlying the enclosing decision, such as public documentation or human confirmation. |
| `submission_workflow_review.date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `submission_workflow_review.directly_retrieved_protocol_snapshots` | array; items: string | Identifier or path of the directly retrieved protocol snapshots in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `submission_workflow_review.evidence_ids` | array; items: string | Identifiers of specific evidence items supporting the enclosing interpretation; archival ledgers may be outside this package. |
| `submission_workflow_review.independently_verified_in_this_update` | boolean | Whether the condition “independently verified in this update” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `submission_workflow_review.instruction` | string | Instruction recorded for the enclosing procedure or decision; distinguish organizer instructions from historical author/reviewer requests. |
| `submission_workflow_review.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `submission_workflow_review.quoted_instruction` | string | Source instruction retained verbatim to document the applicable rule or interface. |
| `submission_workflow_review.source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `submission_workflow_review.summary` | string | Concise summary of the enclosing source, review or observation. |
| `submission_workflow_review.user_material` | null / string | Source-recorded user material for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `task_outputs` | null / array / object; items: string, object | Source-defined artifact/interface requirement for task outputs. Distinguish scored input/output from supporting code, model files or verification material. |
| `task_outputs.Caption` | string | Source-recorded Caption for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `task_outputs.MES` | string | Source-recorded MES for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `task_outputs.UCEIS` | string | Source-recorded UCEIS for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `task_outputs[].content` | string | Information that the enclosing file or artifact must contain. |
| `task_outputs[].datatype` | string | Storage data type of the enclosing output or artifact. |
| `task_outputs[].dtype` | string | Storage data type of the enclosing array, image, label or artifact. |
| `task_outputs[].format` | null / string | Required encoding/file format of the enclosing input, output or submitted artifact. |
| `task_outputs[].key` | string | Lookup key used to identify the enclosing variable, source or entry. |
| `task_outputs[].shape` | array; items: integer | Dimensions or layout of the specified image, mask, vector or submitted array. |
| `task_outputs[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `task_outputs.nuclei` | string | Source-recorded nuclei for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `task_outputs.synthesis` | string | Task flag for generating images or other specified imaging outputs from source data. |
| `task_outputs.tissue` | string | Source-recorded tissue for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `task_phase_review` | array; items: object | Source-linked review of task phase. |
| `task_phase_review[].actual_run_logs_verified` | boolean | Whether the condition “actual run logs verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `task_phase_review[].artifact` | string | Source-defined artifact/interface requirement for artifact. Distinguish scored input/output from supporting code, model files or verification material. |
| `task_phase_review[].branch` | string | Source-recorded branch for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `task_phase_review[].execution_mode` | string | How the relevant method or assessment is run, including participant versus organizer/platform execution where specified. |
| `task_phase_review[].filenames` | array; items: string | Source-defined artifact/interface requirement for filenames. Distinguish scored input/output from supporting code, model files or verification material. |
| `task_phase_review[].phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. |
| `task_phase_review[].qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `task_phase_review[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `task_phase_review[].source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `task_phase_review[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `task_submission_review` | array; items: object | Source-linked review of task submission. |
| `task_submission_review[].actual_portal_artifact` | null | Source-defined artifact/interface requirement for actual portal artifact. Distinguish scored input/output from supporting code, model files or verification material. |
| `task_submission_review[].additional_user_review` | object | Source-linked review of additional user. |
| `task_submission_review[].additional_user_review.baseline` | string | Reference method or baseline result, distinguished from final competitive participant outcomes. |
| `task_submission_review[].additional_user_review.output` | string | Prediction, artifact or information produced by the task or model. |
| `task_submission_review[].additional_user_review.portal` | string | Submission portal/interface identified by the organizer or source. |
| `task_submission_review[].additional_user_review.sample_input_phase` | string | Source-defined artifact/interface requirement for sample input phase. Distinguish scored input/output from supporting code, model files or verification material. |
| `task_submission_review[].additional_user_review.verification` | string | Source-recorded verification for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `task_submission_review[].container_implementation_evidence` | string | Recorded documentary support for container implementation. Preserve the task/phase scope and source qualifications. |
| `task_submission_review[].final_automated_execution_independently_verified` | boolean | Whether the condition “final automated execution independently verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `task_submission_review[].registered_artifact` | string | Source-defined artifact/interface requirement for registered artifact. Distinguish scored input/output from supporting code, model files or verification material. |
| `task_submission_review[].registered_artifact_source` | string | Source supporting registered artifact. |
| `task_submission_review[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `technical_error_resubmission_allowed` | boolean | Whether the condition “technical error resubmission allowed” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `track_specific_documentation` | array; items: object | Structured entries for track specific documentation within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `track_specific_documentation[].artifact` | string | Source-defined artifact/interface requirement for artifact. Distinguish scored input/output from supporting code, model files or verification material. |
| `track_specific_documentation[].local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `track_specific_documentation[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `track_specific_documentation[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `updated_official_protocol_url` | string | Web address for updated official protocol. |
| `validation_artifact` | string | Source-defined artifact/interface requirement for validation artifact. Distinguish scored input/output from supporting code, model files or verification material. |
| `validation_submission_artifact` | string | Source-defined artifact/interface requirement for validation submission artifact. Distinguish scored input/output from supporting code, model files or verification material. |
| `validation_submission_type` | string | Source-recorded validation submission type for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `workflow_review` | object | Source-linked review of workflow. |
| `workflow_review.basis_type` | string | Kind of evidence underlying the enclosing decision, such as public documentation or human confirmation. |
| `workflow_review.date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `workflow_review.independently_verified_in_this_update` | boolean | Whether the condition “independently verified in this update” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `workflow_review.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `workflow_review.summary` | string | Concise summary of the enclosing source, review or observation. |

[Back to README](../../README.md#variable-dictionary)
