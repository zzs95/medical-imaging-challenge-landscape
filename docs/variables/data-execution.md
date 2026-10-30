# Data flow and execution arrangements

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

Data/model exchange, inference execution and phase-specific access protocols.

## Field groups

- [`challenge.data_usage_mode`](#data-usage-mode)
- [`challenge.resource_protocol_review`](#resource-protocol-review)

<a id="data-usage-mode"></a>

## `data_usage_mode`

JSON parent path: `challenge.data_usage_mode`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.data_usage_mode`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `evidence_scope` | string | Boundary of what the supporting evidence establishes, including specification versus actual execution. |
| `evidence_stage` | string | Stage represented by the evidence, such as registered design, operational instructions or reported execution/results. |
| `external_data` | object | Policies concerning additional data outside the designated challenge development resources. |
| `external_data.allowed` | null / boolean | Whether the enclosing resource or action is explicitly permitted within its stated task/phase scope. |
| `external_data.disclosure_required` | null / boolean | Whether participants must disclose the enclosing resource, data source or methodological choice. |
| `external_data.policy` | null / string | Source wording describing permission, prohibition or conditions for the enclosing resource or procedure. |
| `external_data.policy_by_task` | array; items: object | Structured entries for policy by task within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `external_data.policy_by_task[].public_external_data_allowed` | boolean | Whether the condition “public external data allowed” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `external_data.policy_by_task[].public_pretrained_models_allowed` | boolean | Whether the condition “public pretrained models allowed” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `external_data.policy_by_task[].restriction` | string | Limitation or prohibition applied to the enclosing data, model or procedure. |
| `external_data.policy_by_task[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `external_data.policy_by_task[].training_data_restricted_to_challenge` | boolean | Whether the condition “training data restricted to challenge” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `external_data.separate_tracks` | object | Structured entries for separate tracks within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `external_data.separate_tracks.Methods` | string | Source-recorded Methods for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `external_data.separate_tracks.Open` | string | Source-recorded Open for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `external_data.topaneu_only_model_required_for_challenge_manuscript_comparison_if_external_data_used` | null | Optional field for topaneu only model required for challenge manuscript comparison if external data used in the enclosing record. It is unpopulated in this snapshot; neither a value nor a negative finding is established. |
| `flow_evidence` | string | Recorded documentary support for flow. Preserve the task/phase scope and source qualifications. |
| `interpretation` | string | Reviewer's scoped interpretation of the recorded source information; not additional organizer evidence. |
| `overall_paradigm` | null / string | Overall data/model-flow description: data-to-model, model-to-data or hybrid, qualified by phase and source scope. |
| `paradigm` | string | Data/model-flow arrangement for the enclosing phase. It is distinct from access licensing and proof of completed execution. |
| `protocol_reference` | object | Reference to the edition-specific protocol supporting the enclosing field; a protocol describes specification rather than proof of execution. |
| `protocol_reference.local_protocol` | string | Original archive path of a registered protocol; the protocol file itself is not included in this metadata package. |
| `protocol_reference.section` | string | Section, figure, table or location within a supporting source. |
| `protocol_reference.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `review_status` | string | Status or scope of the review process, not a direct measure of challenge quality. |
| `testing` | object | Testing-stage data, rules or execution arrangements as specified in the enclosing record. |
| `testing.evidence_scope` | string | Boundary of what the supporting evidence establishes, including specification versus actual execution. |
| `testing.paradigm` | null / string | Data/model-flow arrangement for the enclosing phase. It is distinct from access licensing and proof of completed execution. |
| `testing.policy` | string | Source wording describing permission, prohibition or conditions for the enclosing resource or procedure. |
| `testing.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `testing.server_side_inference` | null / boolean | Whether the model is specified or reported to run on organizer/platform infrastructure; check the evidence scope for execution confirmation. |
| `testing.submission_artifact` | null / string / array; items: string | Artifact submitted for the enclosing phase, distinct from the output later generated by an executed model. |
| `testing.test_data_visible_to_participants` | null / boolean | Whether participants receive or can access test inputs, independently of access to test labels. |
| `testing.test_labels_visible_to_participants` | boolean | Whether the reference test labels are visible to participants. |
| `track_specific_testing` | array; items: object | Structured entries for track specific testing within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `track_specific_testing[].paradigm` | string | Data/model-flow arrangement for the enclosing phase. It is distinct from access licensing and proof of completed execution. |
| `track_specific_testing[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `track_specific_testing[].submission_artifact` | string | Artifact submitted for the enclosing phase, distinct from the output later generated by an executed model. |
| `track_specific_testing[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `track_specific_testing[].test_data_visible_to_participants` | boolean | Whether participants receive or can access test inputs, independently of access to test labels. |
| `training` | object | Training-stage data, quantities, rules or model-use arrangements, according to the parent field. |
| `training.paradigm` | null / string | Data/model-flow arrangement for the enclosing phase. It is distinct from access licensing and proof of completed execution. |
| `training.training_data_downloadable` | null / boolean | Whether participants can download the designated training/development data. |
| `validation` | object | Validation-stage data, quantities, submissions or results; not automatically final-test evidence. |
| `validation.data_visible_to_participants` | boolean | Whether the enclosing phase's input data are available to participants. |
| `validation.evidence_scope` | string | Boundary of what the supporting evidence establishes, including specification versus actual execution. |
| `validation.paradigm` | string | Data/model-flow arrangement for the enclosing phase. It is distinct from access licensing and proof of completed execution. |
| `validation.server_side_inference` | boolean | Whether the model is specified or reported to run on organizer/platform infrastructure; check the evidence scope for execution confirmation. |
| `validation.submission_artifact` | string / array; items: string | Artifact submitted for the enclosing phase, distinct from the output later generated by an executed model. |

<a id="resource-protocol-review"></a>

## `resource_protocol_review`

JSON parent path: `challenge.resource_protocol_review`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.resource_protocol_review`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `access_followup_20261025` | object | Structured entries for access followup 20261025 within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `access_followup_20261025.attempted_sources` | array; items: string | Sources supporting attempted. |
| `access_followup_20261025.decision` | string | Recorded inclusion, coding or scope decision, with the associated reason and evidence retained. |
| `access_followup_20261025.rationale` | string | Explanation of how the supporting evidence leads to the recorded classification or decision. |
| `access_followup_20261025.status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `data_model_flow` | object | Direction of data/model exchange across the competition workflow, preserving phase-specific differences. |
| `data_model_flow.category` | string | Classification assigned within the enclosing coding scheme; schemes differ across variables. |
| `data_model_flow.evidence_basis` | string | Evidence or reasoning supporting evidence. |
| `data_model_flow.phases` | array; items: object | Structured entries for phases within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `data_model_flow.phases[].data_model_flow` | string | Direction of data/model exchange across the competition workflow, preserving phase-specific differences. |
| `data_model_flow.phases[].eligible_participants` | string | Source-recorded eligible participants for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `data_model_flow.phases[].inference_executor` | string | Party executing model inference on the designated evaluation inputs; distinct from the submission service or metric-computation party. |
| `data_model_flow.phases[].phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. |
| `data_model_flow.phases[].scoring_submission` | string | Artifact or submission record used for scoring, distinct from auxiliary verification materials. |
| `data_model_flow.phases[].test_data` | string | Input data provided or withheld for the stated testing stage. |
| `data_model_flow.rationale` | string | Explanation of how the supporting evidence leads to the recorded classification or decision. |
| `data_model_flow.state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. |
| `data_model_flow_history` | array; items: object | Earlier versions or decisions concerning data model flow. |
| `data_model_flow_history[].record` | object | Nested record preserved in the enclosing source, historical or review object; its status follows the parent context. |
| `data_model_flow_history[].record.category` | string | Classification assigned within the enclosing coding scheme; schemes differ across variables. |
| `data_model_flow_history[].record.rationale` | string | Explanation of how the supporting evidence leads to the recorded classification or decision. |
| `data_model_flow_history[].record.state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. |
| `data_model_flow_history[].superseded_on` | string | Date the enclosing older value or decision was superseded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `decision_history` | array; items: string | Dated earlier decisions and revisions retained to show how the current classification was reached. |
| `development_access` | object | Classification of competition-time development-data access, preserving public download, registration, individual authorization and unresolved states. |
| `development_access.access_by_scope` | array; items: object | Access conditions broken down by dataset, task, phase or source scope. |
| `development_access.access_by_scope[].access_steps` | array; items: string | Documented steps needed to obtain the relevant data, such as registration, authorization and download. |
| `development_access.access_by_scope[].category` | string | Classification assigned within the enclosing coding scheme; schemes differ across variables. |
| `development_access.access_by_scope[].manual_review` | null / boolean | Whether the access procedure includes individual/manual approval; null means unresolved. |
| `development_access.access_by_scope[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `development_access.category` | string | Classification assigned within the enclosing coding scheme; schemes differ across variables. |
| `development_access.confidence` | string | Recorded confidence/qualification in a review decision; not a calibrated probability unless explicitly defined by the source. |
| `development_access.evidence_basis` | string | Evidence or reasoning supporting evidence. |
| `development_access.rationale` | string | Explanation of how the supporting evidence leads to the recorded classification or decision. |
| `development_access.review_date` | string | Date of the review operation described in the enclosing object. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `development_access.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `development_access.source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `development_access.state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. |
| `development_access_history` | array; items: object | Superseded development-data access classifications, preserved separately from the current access decision. |
| `development_access_history[].record` | object | Nested record preserved in the enclosing source, historical or review object; its status follows the parent context. This occurrence is historical and must be interpreted within its enclosing revision. |
| `development_access_history[].record.access_by_scope` | array; items: object | Access conditions broken down by dataset, task, phase or source scope. This occurrence is historical and must be interpreted within its enclosing revision. |
| `development_access_history[].record.access_by_scope[].access_steps` | array; items: string | Documented steps needed to obtain the relevant data, such as registration, authorization and download. This occurrence is historical and must be interpreted within its enclosing revision. |
| `development_access_history[].record.access_by_scope[].category` | string | Classification assigned within the enclosing coding scheme; schemes differ across variables. This occurrence is historical and must be interpreted within its enclosing revision. |
| `development_access_history[].record.access_by_scope[].manual_review` | null / boolean | Whether the access procedure includes individual/manual approval; null means unresolved. This occurrence is historical and must be interpreted within its enclosing revision. |
| `development_access_history[].record.access_by_scope[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. This occurrence is historical and must be interpreted within its enclosing revision. |
| `development_access_history[].record.category` | string | Classification assigned within the enclosing coding scheme; schemes differ across variables. This occurrence is historical and must be interpreted within its enclosing revision. |
| `development_access_history[].record.confidence` | string | Recorded confidence/qualification in a review decision; not a calibrated probability unless explicitly defined by the source. This occurrence is historical and must be interpreted within its enclosing revision. |
| `development_access_history[].record.evidence_basis` | string | Evidence or reasoning supporting evidence. |
| `development_access_history[].record.rationale` | string | Explanation of how the supporting evidence leads to the recorded classification or decision. This occurrence is historical and must be interpreted within its enclosing revision. |
| `development_access_history[].record.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. This occurrence is historical and must be interpreted within its enclosing revision. |
| `development_access_history[].record.source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. This occurrence is historical and must be interpreted within its enclosing revision. |
| `development_access_history[].record.state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. This occurrence is historical and must be interpreted within its enclosing revision. |
| `development_access_history[].round` | string | Review or competition round identifier; the parent object determines which kind of round is meant. This occurrence is historical and must be interpreted within its enclosing revision. |
| `development_access_history[].superseded_on` | string | Date the enclosing older value or decision was superseded. This occurrence is historical and must be interpreted within its enclosing revision. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `limitations` | array; items: string | Limitations of the enclosing evidence, procedure or interpretation. |
| `review_date` | string | Date of the review operation described in the enclosing object. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `sources` | array; items: object | Sources supporting the enclosing statement or dataset description, preserving document/source type and scope. |
| `sources[].excerpt` | string | Passage copied or extracted from a supporting source for the enclosing item. |
| `sources[].local_source` | string | Path identifying a source in the original review archive, not a downloadable file inside this release. |
| `sources[].retrieval_url` | string | Web address for retrieval. |
| `sources[].review_date` | string | Date of the review operation described in the enclosing object. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `sources[].section` | string | Section, figure, table or location within a supporting source. |
| `sources[].url` | string | Web address of the enclosing source, document or resource. |

[Back to README](../../README.md#variable-dictionary)
