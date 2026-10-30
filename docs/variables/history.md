# Historical coding and protocol revisions

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

Superseded classifications, earlier protocols and historical submission arrangements.

## Field groups

- [`challenge.previous_review_coding`](#previous-review-coding)
- [`challenge.protocol_history`](#protocol-history)
- [`challenge.submission_history`](#submission-history)

<a id="previous-review-coding"></a>

## `previous_review_coding`

JSON parent path: `challenge.previous_review_coding`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.previous_review_coding`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. This occurrence is historical and must be interpreted within its enclosing revision. |
| `imaging_eligibility` | string | Source-recorded imaging eligibility for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `imaging_scope` | string | Task, phase, cohort or source boundaries of imaging. |
| `tool_mediated_clinical_workflow` | string | Source-recorded tool mediated clinical workflow for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |

<a id="protocol-history"></a>

## `protocol_history`

JSON parent path: `challenge.protocol_history`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.protocol_history`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `[].evaluation` | object | Assessment metrics, implementation, ranking and results, preserving task and phase distinctions. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].evaluation.cross_task_rule` | null | Rule linking outputs, assessments or rankings across tasks within the competition. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].evaluation.design_document` | string | Registered protocol or other document describing the proposed challenge design. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].evaluation.hidden_test_set` | null | Whether the designated test set or its protected component is described as hidden; read inputs/labels visibility separately. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].evaluation.online_evaluation` | null | Whether an online evaluation process is specified or reported; does not by itself establish automated inference or scoring. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].evaluation.platform` | string | Named service involved in the enclosing data, submission or evaluation operation; service naming alone does not establish the executor. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].evaluation.platform_evidence_stage` | string | Stage represented by the evidence naming the platform, such as registered design versus operational execution. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].evaluation.platform_scope` | string | Task, phase, cohort or source boundaries of platform. |
| `[].evaluation.tasks` | array; items: object | Task-specific objects or descriptions; each has its own scope, inputs, outputs or assessment information where available. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].evaluation.tasks[].design_status` | string | Recorded state of design. Preserve the task/phase scope and source qualifications. |
| `[].evaluation.tasks[].evidence_section` | string | Source-recorded evidence section for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `[].evaluation.tasks[].metrics` | array; items: string | Metrics assigned to the enclosing task or assessment; a metric list alone does not define the ranking formula. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].evaluation.tasks[].ranking` | null | Rule used to order participants or methods in the stated task/phase, or its source description. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].evaluation.tasks[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].recorded_on` | string | Date when the enclosing observation or decision was entered into the record. This occurrence is historical and must be interpreted within its enclosing revision. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].submission` | object | Required artifacts, submission routes, runtime constraints and phase-specific procedures. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].submission.evidence_stage` | string | Stage represented by the evidence, such as registered design, operational instructions or reported execution/results. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].submission.platform` | string | Named service involved in the enclosing data, submission or evaluation operation; service naming alone does not establish the executor. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].submission.runtime_limits` | object | Documented constraints for executing a submitted method, preserving time, host RAM and GPU memory as separate quantities. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].submission.runtime_limits.gpu` | null | GPU model or GPU resource assigned/recommended for the enclosing execution setting; retain whether mandatory or advisory. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].submission.runtime_limits.gpu_vram_gb` | null | GPU video-memory capacity or limit in GB for the stated hardware/rule; hardware capacity and an enforced software ceiling are distinct. This occurrence is historical and must be interpreted within its enclosing revision. Unit/format: GB; denominator/scope follows field name. |
| `[].submission.runtime_limits.max_processing_time_per_case_minutes` | null | Maximum specified processing time for one case, in minutes; check whether this is a declared rule or enforced limit. This occurrence is historical and must be interpreted within its enclosing revision. Unit/format: minutes; denominator/scope follows field name. |
| `[].submission.runtime_limits.max_ram_gb` | null | Maximum specified host/system RAM in GB; not a GPU-memory ceiling. This occurrence is historical and must be interpreted within its enclosing revision. Unit/format: GB; denominator/scope follows field name. |
| `[].submission.runtime_limits.reserved_ram_gb` | null | Host/system RAM reserved for infrastructure or non-method processes, in GB, as stated by the source. This occurrence is historical and must be interpreted within its enclosing revision. Unit/format: GB; denominator/scope follows field name. |
| `[].submission.submission_limits` | object | Limits on the number or timing of submissions, preserving phase, team/user unit and successful/failed-attempt rules. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].submission.submission_limits.additional_distinct_final_algorithms_possible_with_organizer_approval` | null | Whether extra distinct final algorithms may be submitted after organizer approval. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].submission.submission_limits.final_submissions_per_team` | null | Maximum final-stage submissions permitted for one team. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].submission.submission_limits.sanity_check_successful_submissions_per_day` | null | Maximum successful sanity-check submissions per day under the documented counting unit. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].submission.submission_type` | string | Recorded kind of submitted artifact or workflow, such as predictions, code, weights, containers or a platform-executed notebook. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].submission.task_outputs` | null | Source-defined artifact/interface requirement for task outputs. Distinguish scored input/output from supporting code, model files or verification material. |

<a id="submission-history"></a>

## `submission_history`

JSON parent path: `challenge.submission_history`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.submission_history`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `[].record` | object | Nested record preserved in the enclosing source, historical or review object; its status follows the parent context. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].record.additional_materials` | array | Supporting or verification materials supplied in addition to the principal scored artifact. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].record.execution` | string | Description or evidence state of executing the relevant method or assessment. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].record.format_by_task_or_phase` | array; items: object | Source-defined artifact/interface requirement for format by task or phase. Distinguish scored input/output from supporting code, model files or verification material. |
| `[].record.format_by_task_or_phase[].archive` | string | Source-defined artifact/interface requirement for archive. Distinguish scored input/output from supporting code, model files or verification material. |
| `[].record.format_by_task_or_phase[].artifact` | string | Source-defined artifact/interface requirement for artifact. Distinguish scored input/output from supporting code, model files or verification material. |
| `[].record.format_by_task_or_phase[].contents` | array; items: string | Source-defined artifact/interface requirement for contents. Distinguish scored input/output from supporting code, model files or verification material. |
| `[].record.format_by_task_or_phase[].input_format` | string | Source-defined artifact/interface requirement for input format. Distinguish scored input/output from supporting code, model files or verification material. |
| `[].record.format_by_task_or_phase[].max_submissions_per_day` | integer | Specified submission/execution constraint for max submissions per day. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `[].record.format_by_task_or_phase[].outer_packaging` | null | Source-defined artifact/interface requirement for outer packaging. Distinguish scored input/output from supporting code, model files or verification material. |
| `[].record.format_by_task_or_phase[].output_format` | string | Source-defined artifact/interface requirement for output format. Distinguish scored input/output from supporting code, model files or verification material. |
| `[].record.format_by_task_or_phase[].permitted_file_extensions_examples` | array; items: string | Source-defined artifact/interface requirement for permitted file extensions examples. Distinguish scored input/output from supporting code, model files or verification material. |
| `[].record.format_by_task_or_phase[].phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].record.format_by_task_or_phase[].prebuilt_image_required` | boolean | Whether the condition “prebuilt image required” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `[].record.format_by_task_or_phase[].required_files` | array; items: string | Source-defined artifact/interface requirement for required files. Distinguish scored input/output from supporting code, model files or verification material. |
| `[].record.format_by_task_or_phase[].required_materials` | array; items: string | Structured entries for required materials within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `[].record.format_by_task_or_phase[].score_feedback` | string | Scores or other assessment information returned to participants for the stated phase. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].record.format_limitations` | array; items: string | Specified submission/execution constraint for format limitations. Preserve the counting unit, phase, time unit and whether failed attempts are included; a rule is not proof of enforcement. |
| `[].record.platform` | null / string | Named service involved in the enclosing data, submission or evaluation operation; service naming alone does not establish the executor. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].record.portal_review_source` | string | Source supporting portal review. |
| `[].record.primary_artifacts` | array; items: string | Source-defined artifact/interface requirement for primary artifacts. Distinguish scored input/output from supporting code, model files or verification material. |
| `[].record.registered_task_submissions` | array; items: object | Structured entries for registered task submissions within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `[].record.registered_task_submissions[].protocol_description` | string | Source description of protocol. |
| `[].record.registered_task_submissions[].source_reference` | object | Reference to the supporting document or source, possibly with section, URL and archival location. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].record.registered_task_submissions[].source_reference.local_protocol` | string | Original archive path of a registered protocol; the protocol file itself is not included in this metadata package. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].record.registered_task_submissions[].source_reference.registered_task_index` | integer | Task position/identifier in the registered protocol; it can differ from later operational numbering. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].record.registered_task_submissions[].source_reference.section` | string | Section, figure, table or location within a supporting source. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].record.registered_task_submissions[].source_reference.source_url` | string | Public URL cited as supporting the enclosing statement or record. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].record.registered_task_submissions[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].record.review_date` | string | Date of the review operation described in the enclosing object. This occurrence is historical and must be interpreted within its enclosing revision. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `[].record.review_source` | string | Source supporting review. |
| `[].record.runtime_limits` | null | Documented constraints for executing a submitted method, preserving time, host RAM and GPU memory as separate quantities. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].record.source_reference` | string | Reference to the supporting document or source, possibly with section, URL and archival location. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].record.submission_evidence_status` | string | Recorded state of submission evidence. Preserve the task/phase scope and source qualifications. |
| `[].record.submission_limits` | null | Limits on the number or timing of submissions, preserving phase, team/user unit and successful/failed-attempt rules. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].record.submission_type` | string | Recorded kind of submitted artifact or workflow, such as predictions, code, weights, containers or a platform-executed notebook. This occurrence is historical and must be interpreted within its enclosing revision. |
| `[].superseded_on` | string | Date the enclosing older value or decision was superseded. This occurrence is historical and must be interpreted within its enclosing revision. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |

[Back to README](../../README.md#variable-dictionary)
