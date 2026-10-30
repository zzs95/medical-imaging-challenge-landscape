# Labels, targets and reference annotations

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

Target definitions, label mappings and reference-annotation procedures.

## Field groups

- [`challenge.labels_and_targets`](#labels-and-targets)

<a id="labels-and-targets"></a>

## `labels_and_targets`

JSON parent path: `challenge.labels_and_targets`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.labels_and_targets`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `anatomical_location_class_count` | integer | Number of anatomical-location target classes under the stated label definition. |
| `annotation_source` | null / string | Persons, procedures or source material used to construct reference annotations; not the same as expert assessment of model outputs. |
| `auxiliary_labels` | null / object | Additional labels supporting training or analysis that may differ from the principal scored targets. |
| `auxiliary_labels.silver_standard_vessel_masks` | null | Availability or description of automatically generated or otherwise non-gold-standard vessel masks. |
| `auxiliary_labels.training_only` | null | Whether the enclosing labels or information are restricted to training rather than inference or final scoring. |
| `caption_annotation_evidence` | object | Recorded documentary support for caption annotation. Preserve the task/phase scope and source qualifications. |
| `caption_annotation_evidence.description` | string | Description of the enclosing entity, procedure, data or result as retained from the source or review. |
| `caption_annotation_evidence.interpretation` | string | Reviewer's scoped interpretation of the recorded source information; not additional organizer evidence. |
| `caption_annotation_evidence.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `caption_annotation_evidence.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `condition_labels` | array; items: string | Structured entries for condition labels within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fine_grained_anatomy` | null | Whether the target labels distinguish detailed anatomical structures under the source's definition. |
| `label_semantics` | null / string / array / object; items: string | Clinical or technical meaning of the target labels, including any grouping or interpretation restrictions. |
| `label_semantics.LR-1` | string | Meaning assigned by the source to label/code `LR-1` in this mapping; mappings are task-specific. |
| `label_semantics.LR-2` | string | Meaning assigned by the source to label/code `LR-2` in this mapping; mappings are task-specific. |
| `label_semantics.LR-3` | string | Meaning assigned by the source to label/code `LR-3` in this mapping; mappings are task-specific. |
| `label_semantics.LR-4` | string | Meaning assigned by the source to label/code `LR-4` in this mapping; mappings are task-specific. |
| `label_semantics.LR-5` | string | Meaning assigned by the source to label/code `LR-5` in this mapping; mappings are task-specific. |
| `lumbar_levels` | array; items: string | Structured entries for lumbar levels within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `official_description` | null / string | Organizer wording describing labels, targets or another explicitly identified entity. |
| `protocol_reference` | object | Reference to the edition-specific protocol supporting the enclosing field; a protocol describes specification rather than proof of execution. |
| `protocol_reference.local_protocol` | string | Original archive path of a registered protocol; the protocol file itself is not included in this metadata package. |
| `protocol_reference.registered_task_index` | integer | Task position/identifier in the registered protocol; it can differ from later operational numbering. |
| `protocol_reference.section` | string | Section, figure, table or location within a supporting source. |
| `protocol_reference.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `submission_label_specification` | object | Structured entries for submission label specification within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `submission_label_specification.label` | object | Class label, category name or display label for the enclosing item. |
| `submission_label_specification.label.class_names` | null | Names of target classes when explicitly available; not inferred from a class count. |
| `submission_label_specification.label.dtype` | string | Storage data type of the enclosing array, image, label or artifact. |
| `submission_label_specification.label.shape` | array; items: integer | Dimensions or layout of the specified image, mask, vector or submitted array. |
| `submission_label_specification.label.values` | string | Permitted label codes, numerical values or source-defined value semantics for the enclosing field. |
| `submission_label_specification.mask` | object | Structured entries for mask within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `submission_label_specification.mask.dtype` | string | Storage data type of the enclosing array, image, label or artifact. |
| `submission_label_specification.mask.shape` | array; items: integer | Dimensions or layout of the specified image, mask, vector or submitted array. |
| `submission_label_specification.mask.values` | string | Permitted label codes, numerical values or source-defined value semantics for the enclosing field. |
| `submission_label_specification.source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `submission_label_specification.views` | array; items: string | Structured entries for views within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `target_entity` | null / string / array; items: string | Anatomical entity, disease, object or other target that the challenge asks methods to predict or characterize. |
| `target_label_count` | integer | Number of prediction targets/labels in the stated task; distinguish foreground labels from any background code. |
| `task1` | object | Source-defined task1 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `task1.class_count_description` | null | Original wording describing the number or extent of classes, including approximate or open-ended counts. |
| `task1.complete_class_name_list_available_in_this_record` | null | Whether the record contains the complete documented class-name list. |
| `task1.exact_class_count_confirmed` | null | Whether an exact target-class count has been established from the reviewed source. |
| `task1.label_type` | null | Form of the target label, such as a class label, voxel mask, measurement or free text. |
| `task2` | object | Source-defined task2 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `task2.background_included_in_value_range` | null | Whether the stated mask-value range explicitly includes a background label. |
| `task2.exact_number_of_foreground_classes_inferred_from_range` | null | Recorded foreground-class count derived from a range when justified; preserve any null or uncertainty rather than recomputing it automatically. |
| `task2.label_type` | null | Form of the target label, such as a class label, voxel mask, measurement or free text. |
| `task2.mask_datatype` | null | Storage data type required for the segmentation mask. |
| `task2.mask_value_range` | null | Permitted encoded mask values; the range alone need not resolve the number of foreground classes. |
| `tasks` | null / array; items: object | Task-specific objects or descriptions; each has its own scope, inputs, outputs or assessment information where available. |
| `tasks[].class_count` | integer | Number of target classes under the stated task and background convention. |
| `tasks[].classes` | array / object; items: string | Target class names, codes or their mapping within the stated task. |
| `tasks[].classes.0` | string | Meaning assigned by the source to label/code `0` in this mapping; mappings are task-specific. |
| `tasks[].classes.1` | string | Meaning assigned by the source to label/code `1` in this mapping; mappings are task-specific. |
| `tasks[].classes.2` | string | Meaning assigned by the source to label/code `2` in this mapping; mappings are task-specific. |
| `tasks[].classes.3` | string | Meaning assigned by the source to label/code `3` in this mapping; mappings are task-specific. |
| `tasks[].mask_values` | object | Structured entries for mask values within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `tasks[].mask_values.0` | string | Meaning assigned by the source to label/code `0` in this mapping; mappings are task-specific. |
| `tasks[].mask_values.1` | string | Meaning assigned by the source to label/code `1` in this mapping; mappings are task-specific. |
| `tasks[].mask_values.2` | string | Meaning assigned by the source to label/code `2` in this mapping; mappings are task-specific. |
| `tasks[].target` | string | Entity, output or quantity that the enclosing task or assessment concerns. |
| `tasks[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |

[Back to README](../../README.md#variable-dictionary)
