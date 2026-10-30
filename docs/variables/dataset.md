# Datasets, cohorts and quantities

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

Population, splits, acquisition settings, sites, counts and their original units.

## Field groups

- [`challenge.dataset`](#dataset)
- [`challenge.resource_characteristics_review`](#resource-characteristics-review)

<a id="dataset"></a>

## `dataset`

JSON parent path: `challenge.dataset`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.dataset`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `additional_real_world_evaluation` | boolean | Whether the condition “additional real world evaluation” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `annotation_count` | integer | Source-reported quantity or quantity breakdown for annotation count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `anonymized` | null / boolean | Whether anonymization/de-identification is explicitly reported for the dataset. |
| `cancer_type_count` | integer | Source-reported quantity or quantity breakdown for cancer type count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `center_count` | null / integer | Number of acquisition/source centers in the stated data scope; not the number of organizer institutions. |
| `center_scope` | string | Task, phase, cohort or source boundaries of center. |
| `center_type` | null / string | Source-center structure described for the dataset, such as single-center, multicenter or multinational. |
| `class_counts` | array; items: object | Source-reported quantity or quantity breakdown for class counts. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `class_counts[].label` | string | Class label, category name or display label for the enclosing item. |
| `class_counts[].value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `collection_period` | object | Period during which the underlying imaging/data were acquired, distinct from the metadata collection date. |
| `collection_period.end_date` | string | Date associated with end. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `collection_period.end_year` | null / integer | Last year of the enclosing acquisition period or explicitly identified interval. |
| `collection_period.start_date` | string | Date associated with start. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `collection_period.start_year` | null / integer | First year of the enclosing acquisition period or explicitly identified interval. |
| `context_roi_size_pixels` | array; items: integer | Acquisition or sample specification for context roi size pixels; use the unit explicitly named in the key or source, without converting counts or inferring an unstated unit. Unit/format: pixels; denominator/scope follows field name. |
| `contributing_institution_count` | integer | Number of institutions explicitly contributing to the stated data/resource scope. |
| `country_count` | integer | Number of explicitly represented countries in the stated source scope; not a claim of population representativeness. |
| `data_components` | null / array; items: string | Types of images, labels, metadata or outcomes included in the dataset. |
| `dataset_structure` | object | Dataset subset or source-defined breakdown named `dataset_structure`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `dataset_structure.external_validation` | string | Description of an external validation data source or setting; assess source independence from its accompanying evidence. |
| `dataset_structure.training_reference` | string | Supporting source reference for training. |
| `downstream_binary_task_count` | integer | Source-reported quantity or quantity breakdown for downstream binary task count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `downstream_datasets` | array; items: string | Source-reported quantity or quantity breakdown for downstream datasets. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `ethical_approval` | null / boolean | Whether ethics approval is explicitly reported; this field is not an independent assessment of compliance. |
| `evaluation_fps` | integer | Acquisition or sample specification for evaluation frames per second; use the unit explicitly named in the key or source, without converting counts or inferring an unstated unit. Unit/format: frames/second; denominator/scope follows field name. |
| `field_strength_range_tesla` | array; items: number | Acquisition or sample specification for field strength range tesla; use the unit explicitly named in the key or source, without converting counts or inferring an unstated unit. Unit/format: tesla; denominator/scope follows field name. |
| `frame_dimensions` | array; items: integer | Acquisition or sample specification for frame dimensions; use the unit explicitly named in the key or source, without converting counts or inferring an unstated unit. |
| `imaging_device_count` | integer | Source-reported quantity or quantity breakdown for imaging device count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `independence_note` | string | Qualification or source distinction concerning independence. |
| `input_frames_per_case` | integer | Source-reported quantity or quantity breakdown for input frames per case. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `input_volume_size` | array; items: integer | Acquisition or sample specification for input volume size; use the unit explicitly named in the key or source, without converting counts or inferring an unstated unit. |
| `institutions_description` | null / string | Source wording identifying or describing institutions contributing data. |
| `international` | null / boolean | Whether the relevant organizers or dataset sources span countries, according to the enclosing field; not a population-representativeness claim. |
| `labeled_training_tumor_types` | integer | Dataset subset or source-defined breakdown named `labeled_training_tumor_types`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `microns_per_pixel` | number | Acquisition or sample specification for microns per pixel; use the unit explicitly named in the key or source, without converting counts or inferring an unstated unit. Unit/format: micrometers; denominator/scope follows field name. |
| `modalities` | null / array; items: string | Dataset subset or source-defined breakdown named `modalities`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `modality_count_observations` | array; items: object | Source-reported quantity or quantity breakdown for modality count observations. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `modality_count_observations[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `modality_count_observations[].value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `modality_counts` | object | Source-reported quantity or quantity breakdown for modality counts. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `modality_counts.CT_cases` | integer | Source-reported quantity or quantity breakdown for CT cases. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `modality_counts.MRI_scans` | integer | Source-reported quantity or quantity breakdown for MRI scans. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `multi_center` | null / boolean | Whether acquisition at multiple centers is explicitly documented; does not imply institution-held-out testing. |
| `paired_modalities` | boolean | Whether the condition “paired modalities” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `patient_and_followup_separation_across_splits` | null | Source statement on whether patients and their follow-up examinations are separated across dataset splits. |
| `pixel_spacing_mm` | number | Acquisition or sample specification for pixel spacing mm; use the unit explicitly named in the key or source, without converting counts or inferring an unstated unit. Unit/format: mm; denominator/scope follows field name. |
| `population` | null / object | Population-level dataset quantities and characteristics, preserving their stated units. |
| `population.annotated_scan_count` | integer | Source-reported quantity or quantity breakdown for annotated scan count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `population.case_count` | null / integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `population.cell_count` | object | Number of cells in the stated scope, distinct from image or patch counts. Unit/format: cells; stated cohort/split. |
| `population.cell_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `population.cell_count.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `population.cell_count.relation` | string | Relationship between the enclosing observations, datasets or resources. |
| `population.cell_count.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `population.cell_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `population.echocardiogram_count` | integer | Source-reported quantity or quantity breakdown for echocardiogram count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `population.external_validation_case_count` | integer | Source-reported quantity or quantity breakdown for external validation case count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `population.frame_count` | object | Number of video/image frames in the stated scope. Unit/format: frames; stated cohort/split. |
| `population.frame_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `population.frame_count.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `population.frame_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `population.held_out_count` | object | Source-reported quantity or quantity breakdown for held out count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `population.held_out_count.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `population.held_out_count.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `population.held_out_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `population.image_count` | integer / object | Number of images under the source's image definition; do not equate with patients or three-dimensional volumes. Unit/format: images; stated cohort/split. |
| `population.image_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `population.image_count.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `population.image_count.relation` | string | Relationship between the enclosing observations, datasets or resources. |
| `population.image_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `population.image_pair_count` | object | Source-reported quantity or quantity breakdown for image pair count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `population.image_pair_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `population.image_pair_count.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `population.image_pair_count.relation` | string | Relationship between the enclosing observations, datasets or resources. |
| `population.image_pair_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `population.image_series_count` | integer | Number of imaging series, distinct from patients, studies or individual images. |
| `population.nucleus_annotation_count` | object | Source-reported quantity or quantity breakdown for nucleus annotation count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `population.nucleus_annotation_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `population.nucleus_annotation_count.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `population.nucleus_annotation_count.relation` | string | Relationship between the enclosing observations, datasets or resources. |
| `population.nucleus_annotation_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `population.pair_count` | integer | Number of paired data items; the enclosing field identifies what is paired. |
| `population.patient_count` | null / integer | Number of patients in the stated cohort or split; not interchangeable with studies, scans or images. Unit/format: patients; stated cohort/split. |
| `population.preterm_neonate_count` | integer | Source-reported quantity or quantity breakdown for preterm neonate count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `population.pretraining_scan_count` | integer / object | Source-reported quantity or quantity breakdown for pretraining scan count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `population.pretraining_scan_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `population.pretraining_scan_count.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `population.pretraining_scan_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `population.roi_count` | integer | Source-reported quantity or quantity breakdown for roi count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `population.sample_count` | object | Number of source-defined samples; interpret with sample_unit or the original source wording. |
| `population.sample_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `population.sample_count.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `population.sample_count.relation` | string | Relationship between the enclosing observations, datasets or resources. |
| `population.sample_count.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `population.sample_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `population.scan_count` | integer / object | Number of scans in the stated scope, possibly represented as a value/approximation/raw-text object. Unit/format: scans; stated cohort/split. |
| `population.scan_count.approximate` | null / boolean | Whether the enclosing quantity is approximate rather than exact. |
| `population.scan_count.lower_bound` | boolean | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `population.scan_count.raw_text` | null / string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `population.scan_count.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `population.scan_count.value` | null / integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `population.simulated_test_spectrum_count` | integer | Source-reported quantity or quantity breakdown for simulated test spectrum count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `population.simulated_training_spectrum_count` | integer | Source-reported quantity or quantity breakdown for simulated training spectrum count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `population.slide_count` | object | Number of slides in the stated scope; not the number of extracted image patches. Unit/format: slides; stated cohort/split. |
| `population.slide_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `population.slide_count.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `population.slide_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `population.study_count` | null / integer | Number of studies/examinations in the stated cohort or split; a patient may contribute more than one. Unit/format: studys; stated cohort/split. |
| `population.subject_count` | integer | Number of subjects in the stated cohort; preserve whether they are patients, volunteers, animals or other source-defined subjects. Unit/format: subjects; stated cohort/split. |
| `population.test_count` | null / integer / object | Test-set quantity in the unit explicitly specified by the enclosing source. |
| `population.test_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `population.test_count.lower_bound` | boolean | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `population.test_count.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `population.test_count.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `population.test_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `population.train_count` | null / integer / object | Training-set quantity in the unit explicitly specified by the enclosing source. |
| `population.train_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `population.train_count.lower_bound` | boolean / integer | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `population.train_count.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `population.train_count.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `population.train_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `population.validation_count` | null / integer / object | Validation-set quantity in the unit explicitly specified by the enclosing source. |
| `population.validation_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `population.validation_count.lower_bound` | boolean | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `population.validation_count.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `population.validation_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `population.video_count` | integer / object | Number of videos or video samples as defined by the source. Unit/format: videos; stated cohort/split. |
| `population.video_count.lower_bound_exclusive` | integer | Whether the enclosing lower bound is strict, for example more than rather than at least. |
| `population.video_count.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `population.volume_count` | integer | Number of volumetric imaging samples in the stated scope. Unit/format: volumes; stated cohort/split. |
| `population.volume_pair_count` | integer | Source-reported quantity or quantity breakdown for volume pair count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `population.wsi_count` | integer | Number of whole-slide images in the stated scope. Unit/format: whole-slide images; stated cohort/split. |
| `population_description` | string | Textual description of participants, specimens or other entities represented by the cohort. |
| `preliminary_test_count` | integer | Source-reported quantity or quantity breakdown for preliminary test count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `preregistered_splits` | object | Dataset subset or source-defined breakdown named `preregistered_splits`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `preregistered_splits.container_debug` | object | Dataset subset or source-defined breakdown named `container_debug`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `preregistered_splits.container_debug.sequence_count` | integer | Source-reported quantity or quantity breakdown for sequence count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `preregistered_splits.final_test` | object | Dataset subset or source-defined breakdown named `final_test`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `preregistered_splits.final_test.image_count` | integer | Number of images under the source's image definition; do not equate with patients or three-dimensional volumes. Unit/format: images; stated cohort/split. |
| `preregistered_splits.preliminary_test` | object | Dataset subset or source-defined breakdown named `preliminary_test`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `preregistered_splits.preliminary_test.image_count` | integer | Number of images under the source's image definition; do not equate with patients or three-dimensional volumes. Unit/format: images; stated cohort/split. |
| `preregistered_splits.real_qualitative_test` | object | Dataset subset or source-defined breakdown named `real_qualitative_test`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `preregistered_splits.real_qualitative_test.sequence_count` | integer | Source-reported quantity or quantity breakdown for sequence count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `preregistered_splits.synthetic_test` | object | Dataset subset or source-defined breakdown named `synthetic_test`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `preregistered_splits.synthetic_test.sequence_count` | integer | Source-reported quantity or quantity breakdown for sequence count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `preregistered_splits.test` | object | Test-stage subset, quantity, procedure or outcome under the parent field; preserve its recorded unit and phase. |
| `preregistered_splits.test.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `preregistered_splits.train` | object | Dataset subset or source-defined breakdown named `train`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `preregistered_splits.train.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `preregistered_splits.train.sequence_count` | integer | Source-reported quantity or quantity breakdown for sequence count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `preregistered_splits.train.volume_count` | object | Number of volumetric imaging samples in the stated scope. Unit/format: volumes; stated cohort/split. |
| `preregistered_splits.train.volume_count.lower_bound_exclusive` | integer | Whether the enclosing lower bound is strict, for example more than rather than at least. |
| `preregistered_splits.train.volume_count.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `preregistered_splits_per_task` | object | Dataset subset or source-defined breakdown named `preregistered_splits_per_task`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `preregistered_splits_per_task.final_test` | object | Dataset subset or source-defined breakdown named `final_test`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `preregistered_splits_per_task.final_test.patch_count` | integer | Number of extracted image patches in the stated scope. Unit/format: patchs; stated cohort/split. |
| `preregistered_splits_per_task.preliminary_test` | object | Dataset subset or source-defined breakdown named `preliminary_test`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `preregistered_splits_per_task.preliminary_test.patch_count` | integer | Number of extracted image patches in the stated scope. Unit/format: patchs; stated cohort/split. |
| `preregistered_splits_per_task.train` | object | Dataset subset or source-defined breakdown named `train`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `preregistered_splits_per_task.train.patch_count` | integer | Number of extracted image patches in the stated scope. Unit/format: patchs; stated cohort/split. |
| `pretraining_dataset` | string | Data designated for pretraining, distinct from labeled adaptation and evaluation sets. |
| `protocol_reference` | object | Reference to the edition-specific protocol supporting the enclosing field; a protocol describes specification rather than proof of execution. |
| `protocol_reference.local_protocol` | string | Original archive path of a registered protocol; the protocol file itself is not included in this metadata package. |
| `protocol_reference.registered_task_index` | integer | Task position/identifier in the registered protocol; it can differ from later operational numbering. |
| `protocol_reference.section` | string | Section, figure, table or location within a supporting source. |
| `protocol_reference.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `quantity_unit` | string | Unit of the reported dataset/resource quantity. |
| `raw_whole_slide_images_available` | boolean | Source-reported quantity or quantity breakdown for raw whole slide images available. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `reported_quantities` | array; items: object | Dataset subset or source-defined breakdown named `reported_quantities`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `reported_quantities[].phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. |
| `reported_quantities[].raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `reported_quantities[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `reported_quantities[].unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `reported_quantities[].value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `roi_size_pixels` | array; items: integer | Acquisition or sample specification for roi size pixels; use the unit explicitly named in the key or source, without converting counts or inferring an unstated unit. Unit/format: pixels; denominator/scope follows field name. |
| `routine_clinical_practice` | null / boolean | Whether the dataset is explicitly described as originating from routine clinical practice. |
| `scans_per_patient` | integer | Source-reported quantity or quantity breakdown for scans per patient. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `sequences` | array; items: string | Dataset subset or source-defined breakdown named `sequences`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `shared_between_child_tracks` | boolean | Whether the condition “shared between child tracks” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `slide_count_consistency` | string | Source-reported quantity or quantity breakdown for slide count consistency. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `slide_count_observations` | array; items: object | Source-reported quantity or quantity breakdown for slide count observations. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `slide_count_observations[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `slide_count_observations[].value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `source_centers_by_task` | array; items: object | Dataset subset or source-defined breakdown named `source_centers_by_task`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `source_centers_by_task[].center_count` | integer | Number of acquisition/source centers in the stated data scope; not the number of organizer institutions. |
| `source_centers_by_task[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `source_conflicts` | object | Dataset subset or source-defined breakdown named `source_conflicts`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `source_conflicts.xray_images_per_training_ct` | object | Source-reported quantity or quantity breakdown for xray images per training CT. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `source_conflicts.xray_images_per_training_ct.organizer_report` | integer | Quantity for source-defined data subgroup `organizer_report`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `source_conflicts.xray_images_per_training_ct.public_repository` | integer | Quantity for source-defined data subgroup `public_repository`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `source_conflicts.xray_train_image_count` | object | Source-reported quantity or quantity breakdown for xray train image count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `source_conflicts.xray_train_image_count.organizer_report` | integer | Quantity for source-defined data subgroup `organizer_report`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `source_conflicts.xray_train_image_count.public_repository` | integer | Quantity for source-defined data subgroup `public_repository`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `source_database` | object | Dataset subset or source-defined breakdown named `source_database`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `source_database.class_counts` | array; items: object | Source-reported quantity or quantity breakdown for class counts. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `source_database.class_counts[].label` | string | Class label, category name or display label for the enclosing item. |
| `source_database.class_counts[].value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `source_database.name` | string | Name of the enclosing task, institution, dataset, source, method or event; the parent field identifies the entity. |
| `source_database.scan_count` | object | Number of scans in the stated scope, possibly represented as a value/approximation/raw-text object. Unit/format: scans; stated cohort/split. |
| `source_database.scan_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `source_database.scan_count.lower_bound` | boolean | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `source_database.scan_count.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `source_database.scan_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `source_dataset` | string | Dataset subset or source-defined breakdown named `source_dataset`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `source_datasets` | array; items: string | Source-reported quantity or quantity breakdown for source datasets. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `source_reference` | string | Reference to the supporting document or source, possibly with section, URL and archival location. |
| `source_type` | null / string | Kind of data or evidence source. In dataset records this describes cohort origin; in provenance it describes the supporting document or confirmation. |
| `split_details` | object | Details or qualifications concerning dataset partitions, overlap, cohorts and quantity units. |
| `split_details.CBCT_CT_pairs` | string | Source-reported quantity or quantity breakdown for CBCT CT pairs. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.MRI_CT_pairs` | string | Source-reported quantity or quantity breakdown for MRI CT pairs. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.TA36` | string | Source-recorded TA36 for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `split_details.additional_external_test_patients` | integer | Source-reported quantity or quantity breakdown for additional external test patients. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.annotated_training_patches` | integer | Source-reported quantity or quantity breakdown for annotated training patches. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.batch1` | object | Source-defined batch1 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `split_details.batch1.CTA_center4` | integer | Dataset subset or source-defined breakdown named `CTA_center4`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.batch1.MRA_center2` | integer | Dataset subset or source-defined breakdown named `MRA_center2`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.batch2` | object | Source-defined batch2 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `split_details.batch2.CTA_center2` | integer | Dataset subset or source-defined breakdown named `CTA_center2`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.batch2.CTA_center4` | integer | Dataset subset or source-defined breakdown named `CTA_center4`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.batch2.MRA_center1` | integer | Dataset subset or source-defined breakdown named `MRA_center1`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.batch2.MRA_public_center5` | integer | Dataset subset or source-defined breakdown named `MRA_public_center5`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.categories` | array; items: string | One or more classifications or groups used by the enclosing dataset or coding scheme. |
| `split_details.count_unit` | string | Unit to which the reported count refers. |
| `split_details.current_dataset_page_test` | string | Dataset subset or source-defined breakdown named `current_dataset_page_test`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.current_dataset_page_training` | string | Dataset subset or source-defined breakdown named `current_dataset_page_training`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.database_size` | string | Acquisition or sample specification for database size; use the unit explicitly named in the key or source, without converting counts or inferring an unstated unit. |
| `split_details.debug` | string | Source-recorded debug for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `split_details.development` | string | Dataset subset or source-defined breakdown named `development`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.difficult_to_image_cohort` | object | Dataset subset or source-defined breakdown named `difficult_to_image_cohort`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.difficult_to_image_cohort.frames` | integer | Source-reported quantity or quantity breakdown for frames. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.difficult_to_image_cohort.patients` | integer | Source-reported quantity or quantity breakdown for patients. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.easy_to_image_cohort` | object | Dataset subset or source-defined breakdown named `easy_to_image_cohort`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.easy_to_image_cohort.four_chamber_frames` | integer | Source-reported quantity or quantity breakdown for four chamber frames. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.easy_to_image_cohort.patients` | integer | Source-reported quantity or quantity breakdown for patients. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.final_test_cases` | null | Source-reported quantity or quantity breakdown for final test cases. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.fixed_training_unannotated_patches` | string | Source-reported quantity or quantity breakdown for fixed training unannotated patches. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.homepage_expanded_cohort` | string | Dataset subset or source-defined breakdown named `homepage_expanded_cohort`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.labels` | string | Target labels or their source-reported number, according to the recorded value type and context. |
| `split_details.note` | string | Contextual qualification, uncertainty or source distinction for the enclosing item. |
| `split_details.organizer_classifier_testing` | object | Dataset subset or source-defined breakdown named `organizer_classifier_testing`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.organizer_classifier_testing.AD` | integer | Quantity for source-defined data subgroup `AD`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `split_details.organizer_classifier_testing.CN` | integer | Quantity for source-defined data subgroup `CN`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `split_details.organizer_classifier_testing.MCI` | integer | Quantity for source-defined data subgroup `MCI`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `split_details.organizer_classifier_testing.images` | integer | Source-reported quantity or quantity breakdown for images. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.organizer_classifier_training` | object | Dataset subset or source-defined breakdown named `organizer_classifier_training`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.organizer_classifier_training.AD` | integer | Quantity for source-defined data subgroup `AD`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `split_details.organizer_classifier_training.CN` | integer | Quantity for source-defined data subgroup `CN`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `split_details.organizer_classifier_training.MCI` | integer | Quantity for source-defined data subgroup `MCI`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `split_details.organizer_classifier_training.images` | integer | Source-reported quantity or quantity breakdown for images. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.participant_training` | string | Dataset subset or source-defined breakdown named `participant_training`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.per_center_anatomy` | string | Source-recorded per center anatomy for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `split_details.per_task_training` | object | Dataset subset or source-defined breakdown named `per_task_training`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.per_task_training.task1` | object | Source-defined task1 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `split_details.per_task_training.task1.inputs` | integer | Input data types or data objects used by the described task or workflow. |
| `split_details.per_task_training.task1.labels` | integer | Target labels or their source-reported number, according to the recorded value type and context. |
| `split_details.per_task_training.task1.reference_reasoning` | integer | Quantity for source-defined data subgroup `reference_reasoning`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `split_details.per_task_training.task2` | object | Source-defined task2 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `split_details.per_task_training.task2.inputs` | integer | Input data types or data objects used by the described task or workflow. |
| `split_details.per_task_training.task2.labels` | integer | Target labels or their source-reported number, according to the recorded value type and context. |
| `split_details.per_task_training.task2.reference_reasoning` | integer | Quantity for source-defined data subgroup `reference_reasoning`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `split_details.per_task_training.task3` | object | Source-defined task3 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `split_details.per_task_training.task3.inputs` | integer | Input data types or data objects used by the described task or workflow. |
| `split_details.per_task_training.task3.labels` | integer | Target labels or their source-reported number, according to the recorded value type and context. |
| `split_details.per_task_training.task3.reference_reasoning` | integer | Quantity for source-defined data subgroup `reference_reasoning`. The enclosing dataset/split and its unit identify the entity counted; no additional diagnosis or modality is inferred from the code. |
| `split_details.phase1_test_images` | integer | Source-reported quantity or quantity breakdown for phase1 test images. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.phase2_test_images` | integer | Source-reported quantity or quantity breakdown for phase2 test images. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.planned_test_cases` | integer | Source-reported quantity or quantity breakdown for planned test cases. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.preliminary_test` | integer | Dataset subset or source-defined breakdown named `preliminary_test`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.preregistered_clinical_split` | object | Dataset subset or source-defined breakdown named `preregistered_clinical_split`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.preregistered_clinical_split.test` | integer | Test-stage subset, quantity, procedure or outcome under the parent field; preserve its recorded unit and phase. |
| `split_details.preregistered_clinical_split.training` | integer | Training-stage data, quantities, rules or model-use arrangements, according to the parent field. |
| `split_details.preregistered_clinical_split.validation` | integer | Validation-stage data, quantities, submissions or results; not automatically final-test evidence. |
| `split_details.sanity_check` | string | Source-recorded sanity check for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `split_details.simulation` | string | Source-recorded simulation for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `split_details.stated_total_pairs` | integer | Source-reported quantity or quantity breakdown for stated total pairs. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task1` | string / object | Source-defined task1 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `split_details.task1.development` | integer | Dataset subset or source-defined breakdown named `development`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.task1.test` | integer | Test-stage subset, quantity, procedure or outcome under the parent field; preserve its recorded unit and phase. |
| `split_details.task1.test_CBCT_volumes` | integer | Source-reported quantity or quantity breakdown for test CBCT volumes. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task1.test_just_in_time_videos` | integer | Source-reported quantity or quantity breakdown for test just in time videos. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task1.test_regular_videos` | integer | Source-reported quantity or quantity breakdown for test regular videos. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task1.train_CBCT_volumes` | integer | Source-reported quantity or quantity breakdown for train CBCT volumes. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task1.train_annotated` | integer | Dataset subset or source-defined breakdown named `train_annotated`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.task1.train_unannotated` | integer | Dataset subset or source-defined breakdown named `train_unannotated`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.task1.train_videos` | integer | Source-reported quantity or quantity breakdown for train videos. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task1_preliminary_studies` | integer | Source-reported quantity or quantity breakdown for task1 preliminary studies. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task1_test_studies` | integer | Source-reported quantity or quantity breakdown for task1 test studies. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task1_test_subsets` | string | Dataset subset or source-defined breakdown named `task1_test_subsets`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.task1_train` | object | Dataset subset or source-defined breakdown named `task1_train`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.task1_train.FDG_studies` | integer | Source-reported quantity or quantity breakdown for FDG studies. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task1_train.PSMA_studies` | integer | Source-reported quantity or quantity breakdown for PSMA studies. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task1_training` | string | Dataset subset or source-defined breakdown named `task1_training`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.task2` | string / object | Source-defined task2 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `split_details.task2.development` | integer | Dataset subset or source-defined breakdown named `development`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.task2.test` | integer | Test-stage subset, quantity, procedure or outcome under the parent field; preserve its recorded unit and phase. |
| `split_details.task2.test_patient_cases` | integer | Source-reported quantity or quantity breakdown for test patient cases. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task2.test_videos` | integer | Source-reported quantity or quantity breakdown for test videos. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task2.train_annotated` | integer | Dataset subset or source-defined breakdown named `train_annotated`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.task2.train_patient_cases` | integer | Source-reported quantity or quantity breakdown for train patient cases. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task2.train_videos` | integer | Source-reported quantity or quantity breakdown for train videos. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task2_cohort` | string | Dataset subset or source-defined breakdown named `task2_cohort`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.task2_preliminary_studies` | integer | Source-reported quantity or quantity breakdown for task2 preliminary studies. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task2_test_studies` | integer | Source-reported quantity or quantity breakdown for task2 test studies. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task2_test_subsets` | string | Dataset subset or source-defined breakdown named `task2_test_subsets`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.task2_train_patients` | integer | Source-reported quantity or quantity breakdown for task2 train patients. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task2_train_studies` | integer | Source-reported quantity or quantity breakdown for task2 train studies. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task2_train_v2` | integer | Dataset subset or source-defined breakdown named `task2_train_v2`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.task2_training` | string | Dataset subset or source-defined breakdown named `task2_training`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.task3` | object | Source-defined task3 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `split_details.task3.test_frames` | integer | Source-reported quantity or quantity breakdown for test frames. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task3.train_annotated_frames` | integer | Source-reported quantity or quantity breakdown for train annotated frames. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task3_train_v2` | integer | Dataset subset or source-defined breakdown named `task3_train_v2`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.task4` | object | Source-defined task4 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `split_details.task4.test_videos` | integer | Source-reported quantity or quantity breakdown for test videos. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task4.train_videos` | integer | Source-reported quantity or quantity breakdown for train videos. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task5` | object | Source-defined task5 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `split_details.task5.test_frames` | integer | Source-reported quantity or quantity breakdown for test frames. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.task5.train_annotated_question_frames` | integer | Source-reported quantity or quantity breakdown for train annotated question frames. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.test` | string / object | Test-stage subset, quantity, procedure or outcome under the parent field; preserve its recorded unit and phase. |
| `split_details.test.task1` | integer | Source-defined task1 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `split_details.test.task2` | integer | Source-defined task2 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `split_details.test_Instituto_Alexander_Fleming_Argentina` | integer | Dataset subset or source-defined breakdown named `test_Instituto_Alexander_Fleming_Argentina`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.test_Radboud_Netherlands` | integer | Dataset subset or source-defined breakdown named `test_Radboud_Netherlands`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.test_cases` | integer | Source-reported quantity or quantity breakdown for test cases. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.test_external_karolinska_cases` | integer | Source-reported quantity or quantity breakdown for test external karolinska cases. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.test_phase1` | integer | Dataset subset or source-defined breakdown named `test_phase1`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.test_phase2` | integer | Dataset subset or source-defined breakdown named `test_phase2`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.train_unique_patients` | integer | Source-reported quantity or quantity breakdown for train unique patients. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.train_unit` | string | Dataset subset or source-defined breakdown named `train_unit`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.training` | string | Training-stage data, quantities, rules or model-use arrangements, according to the parent field. |
| `split_details.training_ATLAS_v2_train_and_former_validation` | integer | Dataset subset or source-defined breakdown named `training_ATLAS_v2_train_and_former_validation`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.training_FDG_studies` | integer | Source-reported quantity or quantity breakdown for training FDG studies. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.training_PSMA_studies` | integer | Source-reported quantity or quantity breakdown for training PSMA studies. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.training_SOOP` | integer | Dataset subset or source-defined breakdown named `training_SOOP`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.training_abdominal_patients` | integer | Source-reported quantity or quantity breakdown for training abdominal patients. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.training_case_folders` | integer | Dataset subset or source-defined breakdown named `training_case_folders`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.training_new` | integer | Dataset subset or source-defined breakdown named `training_new`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.training_photon_segments` | integer | Source-reported quantity or quantity breakdown for training photon segments. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.training_proton_beamlets` | integer | Source-reported quantity or quantity breakdown for training proton beamlets. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.training_thoracic_patients` | integer | Source-reported quantity or quantity breakdown for training thoracic patients. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `split_details.training_unit` | string | Dataset subset or source-defined breakdown named `training_unit`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `split_details.validation` | string | Validation-stage data, quantities, submissions or results; not automatically final-test evidence. |
| `split_details.validation_cases` | integer | Source-reported quantity or quantity breakdown for validation cases. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits` | object | Dataset partitions and their source-reported quantities or composition. |
| `splits.additional_crown_internal_test` | object | Dataset subset or source-defined breakdown named `additional_crown_internal_test`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.additional_crown_internal_test.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.additional_crown_train` | object | Dataset subset or source-defined breakdown named `additional_crown_train`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.additional_crown_train.MRA_scan_count` | integer | Source-reported quantity or quantity breakdown for MRA scan count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.annotated_finetuning` | object | Dataset subset or source-defined breakdown named `annotated_finetuning`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.annotated_finetuning.neural_activity_patch_count` | integer | Source-reported quantity or quantity breakdown for neural activity patch count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.annotated_finetuning.nucleus_patch_count` | integer | Source-reported quantity or quantity breakdown for nucleus patch count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.annotated_finetuning.plaque_patch_count` | integer | Source-reported quantity or quantity breakdown for plaque patch count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.annotated_finetuning.vessel_patch_count` | integer | Source-reported quantity or quantity breakdown for vessel patch count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.ct_test` | object | Dataset subset or source-defined breakdown named `ct_test`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.ct_test.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.ct_train` | object | Dataset subset or source-defined breakdown named `ct_train`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.ct_train.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.ct_validation` | object | Dataset subset or source-defined breakdown named `ct_validation`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.ct_validation.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.development` | object | Dataset subset or source-defined breakdown named `development`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.development.overlaps_training` | boolean | Dataset subset or source-defined breakdown named `overlaps_training`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.development.patient_count` | integer | Number of patients in the stated cohort or split; not interchangeable with studies, scans or images. Unit/format: patients; stated cohort/split. |
| `splits.final_test` | object | Dataset subset or source-defined breakdown named `final_test`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.final_test.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.final_test.external_center_study_count` | integer | Source-reported quantity or quantity breakdown for external center study count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.final_test.patient_count` | integer | Number of patients in the stated cohort or split; not interchangeable with studies, scans or images. Unit/format: patients; stated cohort/split. |
| `splits.final_test.roi_count` | integer | Source-reported quantity or quantity breakdown for roi count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.final_test.same_center_study_count` | integer | Source-reported quantity or quantity breakdown for same center study count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.final_test.scan_count` | integer | Number of scans in the stated scope, possibly represented as a value/approximation/raw-text object. Unit/format: scans; stated cohort/split. |
| `splits.final_test.study_count` | integer | Number of studies/examinations in the stated cohort or split; a patient may contribute more than one. Unit/format: studys; stated cohort/split. |
| `splits.fully_annotated_test` | object | Dataset subset or source-defined breakdown named `fully_annotated_test`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.fully_annotated_test.image_count` | integer | Number of images under the source's image definition; do not equate with patients or three-dimensional volumes. Unit/format: images; stated cohort/split. |
| `splits.fully_annotated_train` | object | Dataset subset or source-defined breakdown named `fully_annotated_train`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.fully_annotated_train.image_count` | integer | Number of images under the source's image definition; do not equate with patients or three-dimensional volumes. Unit/format: images; stated cohort/split. |
| `splits.fully_annotated_validation` | object | Dataset subset or source-defined breakdown named `fully_annotated_validation`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.fully_annotated_validation.image_count` | integer | Number of images under the source's image definition; do not equate with patients or three-dimensional volumes. Unit/format: images; stated cohort/split. |
| `splits.hidden_generalizability_test` | object | Dataset subset or source-defined breakdown named `hidden_generalizability_test`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.hidden_generalizability_test.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.hidden_test` | object | Dataset subset or source-defined breakdown named `hidden_test`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.hidden_test.case_count` | integer / object | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.hidden_test.case_count.lower_bound_exclusive` | integer | Whether the enclosing lower bound is strict, for example more than rather than at least. |
| `splits.hidden_test.case_count.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `splits.hidden_tuning` | object | Dataset subset or source-defined breakdown named `hidden_tuning`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.hidden_tuning.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.hidden_validation_tuning` | object | Dataset subset or source-defined breakdown named `hidden_validation_tuning`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.hidden_validation_tuning.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.labeled_train` | object | Dataset subset or source-defined breakdown named `labeled_train`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.labeled_train.patient_count` | integer | Number of patients in the stated cohort or split; not interchangeable with studies, scans or images. Unit/format: patients; stated cohort/split. |
| `splits.lesion_test` | object | Dataset subset or source-defined breakdown named `lesion_test`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.lesion_test.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.outcome_test` | object | Dataset subset or source-defined breakdown named `outcome_test`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.outcome_test.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.preliminary_test` | object | Dataset subset or source-defined breakdown named `preliminary_test`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.preliminary_test.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.preliminary_test.patient_count` | integer | Number of patients in the stated cohort or split; not interchangeable with studies, scans or images. Unit/format: patients; stated cohort/split. |
| `splits.preliminary_test.roi_count` | integer | Source-reported quantity or quantity breakdown for roi count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.preliminary_test.scan_count` | integer | Number of scans in the stated scope, possibly represented as a value/approximation/raw-text object. Unit/format: scans; stated cohort/split. |
| `splits.preliminary_test.study_count` | integer | Number of studies/examinations in the stated cohort or split; a patient may contribute more than one. Unit/format: studys; stated cohort/split. |
| `splits.private_train` | object | Dataset subset or source-defined breakdown named `private_train`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.private_train.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.psma_train` | object | Dataset subset or source-defined breakdown named `psma_train`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.psma_train.study_count` | integer | Number of studies/examinations in the stated cohort or split; a patient may contribute more than one. Unit/format: studys; stated cohort/split. |
| `splits.public_test` | object | Dataset subset or source-defined breakdown named `public_test`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.public_test.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.public_train` | object | Dataset subset or source-defined breakdown named `public_train`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.public_train.image_count` | integer | Number of images under the source's image definition; do not equate with patients or three-dimensional volumes. Unit/format: images; stated cohort/split. |
| `splits.public_train.roi_count` | integer | Source-reported quantity or quantity breakdown for roi count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.public_train_development` | object | Dataset subset or source-defined breakdown named `public_train_development`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.public_train_development.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.quadrant_enumeration_training` | object | Dataset subset or source-defined breakdown named `quadrant_enumeration_training`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.quadrant_enumeration_training.image_count` | integer | Number of images under the source's image definition; do not equate with patients or three-dimensional volumes. Unit/format: images; stated cohort/split. |
| `splits.quadrant_only_training` | object | Dataset subset or source-defined breakdown named `quadrant_only_training`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.quadrant_only_training.image_count` | integer | Number of images under the source's image definition; do not equate with patients or three-dimensional volumes. Unit/format: images; stated cohort/split. |
| `splits.reader_study` | object | Dataset subset or source-defined breakdown named `reader_study`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.reader_study.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.reader_study_test_subset` | object | Dataset subset or source-defined breakdown named `reader_study_test_subset`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.reader_study_test_subset.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.sanity_check` | object | Dataset subset or source-defined breakdown named `sanity_check`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.sanity_check.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.sanity_check.overlaps_training` | boolean | Dataset subset or source-defined breakdown named `overlaps_training`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.sanity_check.patient_count` | integer | Number of patients in the stated cohort or split; not interchangeable with studies, scans or images. Unit/format: patients; stated cohort/split. |
| `splits.test` | object | Test-stage subset, quantity, procedure or outcome under the parent field; preserve its recorded unit and phase. |
| `splits.test.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.test.image_count` | integer / object | Number of images under the source's image definition; do not equate with patients or three-dimensional volumes. Unit/format: images; stated cohort/split. |
| `splits.test.image_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `splits.test.image_count.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `splits.test.image_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `splits.test.pair_count` | integer | Number of paired data items; the enclosing field identifies what is paired. |
| `splits.test.patient_count` | integer | Number of patients in the stated cohort or split; not interchangeable with studies, scans or images. Unit/format: patients; stated cohort/split. |
| `splits.test.scan_count` | integer | Number of scans in the stated scope, possibly represented as a value/approximation/raw-text object. Unit/format: scans; stated cohort/split. |
| `splits.test.strata` | array; items: string | Dataset subset or source-defined breakdown named `strata`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.test.video_count` | integer | Number of videos or video samples as defined by the source. Unit/format: videos; stated cohort/split. |
| `splits.train` | object | Dataset subset or source-defined breakdown named `train`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.train.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.train.clip_duration_seconds` | integer | Acquisition or sample specification for clip duration seconds; use the unit explicitly named in the key or source, without converting counts or inferring an unstated unit. Unit/format: seconds; denominator/scope follows field name. |
| `splits.train.frame_count` | object | Number of video/image frames in the stated scope. Unit/format: frames; stated cohort/split. |
| `splits.train.frame_count.lower_bound_exclusive` | integer | Whether the enclosing lower bound is strict, for example more than rather than at least. |
| `splits.train.frame_count.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `splits.train.frame_rate_fps` | integer | Acquisition or sample specification for frame rate frames per second; use the unit explicitly named in the key or source, without converting counts or inferring an unstated unit. Unit/format: frames/second; denominator/scope follows field name. |
| `splits.train.frame_resolution` | array; items: integer | Acquisition or sample specification for frame resolution; use the unit explicitly named in the key or source, without converting counts or inferring an unstated unit. |
| `splits.train.image_count` | integer / object | Number of images under the source's image definition; do not equate with patients or three-dimensional volumes. Unit/format: images; stated cohort/split. |
| `splits.train.image_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `splits.train.image_count.raw_text` | string | Original source wording retained to preserve qualifiers, units, ranges or unresolved interpretation. |
| `splits.train.image_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `splits.train.labeled_case_count` | integer | Source-reported quantity or quantity breakdown for labeled case count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.train.original_image_count` | integer | Source-reported quantity or quantity breakdown for original image count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.train.pair_count` | integer | Number of paired data items; the enclosing field identifies what is paired. |
| `splits.train.patient_count` | integer | Number of patients in the stated cohort or split; not interchangeable with studies, scans or images. Unit/format: patients; stated cohort/split. |
| `splits.train.resolution` | array; items: integer | Resolution of a recorded evidence conflict in review objects, or image/spatial resolution in imaging descriptions; use the parent field to distinguish them. |
| `splits.train.scan_count` | integer | Number of scans in the stated scope, possibly represented as a value/approximation/raw-text object. Unit/format: scans; stated cohort/split. |
| `splits.train.scan_moments_per_patient_range` | array; items: integer | Dataset subset or source-defined breakdown named `scan_moments_per_patient_range`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.train.session_count` | integer | Source-reported quantity or quantity breakdown for session count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.train.study_count` | integer | Number of studies/examinations in the stated cohort or split; a patient may contribute more than one. Unit/format: studys; stated cohort/split. |
| `splits.train.synthetic_image_count` | integer | Source-reported quantity or quantity breakdown for synthetic image count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.train.unlabeled_case_count` | integer | Source-reported quantity or quantity breakdown for unlabeled case count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.train.video_count` | integer | Number of videos or video samples as defined by the source. Unit/format: videos; stated cohort/split. |
| `splits.tuning` | object | Dataset subset or source-defined breakdown named `tuning`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.tuning.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.unannotated_pretraining` | object | Dataset subset or source-defined breakdown named `unannotated_pretraining`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.unannotated_pretraining.neural_activity_brain_count` | integer | Source-reported quantity or quantity breakdown for neural activity brain count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.unannotated_pretraining.nucleus_subregion_count` | integer | Source-reported quantity or quantity breakdown for nucleus subregion count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.unannotated_pretraining.plaque_brain_count` | integer | Source-reported quantity or quantity breakdown for plaque brain count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.unannotated_pretraining.vessel_brain_count` | integer | Source-reported quantity or quantity breakdown for vessel brain count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.unlabeled_pretraining` | object | Dataset subset or source-defined breakdown named `unlabeled_pretraining`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.unlabeled_pretraining.image_count` | integer | Number of images under the source's image definition; do not equate with patients or three-dimensional volumes. Unit/format: images; stated cohort/split. |
| `splits.unlabeled_train` | object | Dataset subset or source-defined breakdown named `unlabeled_train`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.unlabeled_train.patient_count` | integer | Number of patients in the stated cohort or split; not interchangeable with studies, scans or images. Unit/format: patients; stated cohort/split. |
| `splits.validation` | object | Validation-stage data, quantities, submissions or results; not automatically final-test evidence. |
| `splits.validation.case_count` | integer | Number of source-defined cases; case meaning can differ among challenges and must be read with unit/scope. Unit/format: cases; stated cohort/split. |
| `splits.validation.image_count` | integer | Number of images under the source's image definition; do not equate with patients or three-dimensional volumes. Unit/format: images; stated cohort/split. |
| `splits.validation.patient_count` | integer | Number of patients in the stated cohort or split; not interchangeable with studies, scans or images. Unit/format: patients; stated cohort/split. |
| `splits.validation.scan_count` | integer | Number of scans in the stated scope, possibly represented as a value/approximation/raw-text object. Unit/format: scans; stated cohort/split. |
| `splits.validation.video_count` | integer | Number of videos or video samples as defined by the source. Unit/format: videos; stated cohort/split. |
| `splits.xray_test` | object | Dataset subset or source-defined breakdown named `xray_test`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.xray_test.image_count` | integer | Number of images under the source's image definition; do not equate with patients or three-dimensional volumes. Unit/format: images; stated cohort/split. |
| `splits.xray_test.source_ct_count` | integer | Source-reported quantity or quantity breakdown for source CT count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.xray_train` | object | Dataset subset or source-defined breakdown named `xray_train`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.xray_train.image_count` | null | Number of images under the source's image definition; do not equate with patients or three-dimensional volumes. Unit/format: images; stated cohort/split. |
| `splits.xray_train.images_per_ct` | null | Source-reported quantity or quantity breakdown for images per CT. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.xray_train.source_ct_count` | integer | Source-reported quantity or quantity breakdown for source CT count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits.xray_validation` | object | Dataset subset or source-defined breakdown named `xray_validation`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits.xray_validation.image_count` | integer | Number of images under the source's image definition; do not equate with patients or three-dimensional volumes. Unit/format: images; stated cohort/split. |
| `splits.xray_validation.source_ct_count` | integer | Source-reported quantity or quantity breakdown for source CT count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_modality` | object | Dataset partitions stratified by imaging modality; do not infer independence of cohorts. |
| `splits_by_modality.CT` | object | Dataset subset or source-defined breakdown named `CT`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits_by_modality.CT.test_scans` | integer | Source-reported quantity or quantity breakdown for test scans. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_modality.CT.train_scans` | integer | Source-reported quantity or quantity breakdown for train scans. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_modality.CT.validation_scans` | integer | Source-reported quantity or quantity breakdown for validation scans. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_modality.MRI` | object | Dataset subset or source-defined breakdown named `MRI`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits_by_modality.MRI.test_scans` | integer | Source-reported quantity or quantity breakdown for test scans. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_modality.MRI.train_scans` | integer | Source-reported quantity or quantity breakdown for train scans. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_modality.MRI.validation_scans` | integer | Source-reported quantity or quantity breakdown for validation scans. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_task` | object | Task-specific dataset partitions; counts across tasks can overlap. |
| `splits_by_task.arteries` | object | Dataset subset or source-defined breakdown named `arteries`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits_by_task.arteries.test_images` | integer | Source-reported quantity or quantity breakdown for test images. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_task.arteries.train_images` | integer | Source-reported quantity or quantity breakdown for train images. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_task.arteries.validation_images` | integer | Source-reported quantity or quantity breakdown for validation images. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_task.stenosis` | object | Dataset subset or source-defined breakdown named `stenosis`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits_by_task.stenosis.test_images` | integer | Source-reported quantity or quantity breakdown for test images. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_task.stenosis.train_images` | integer | Source-reported quantity or quantity breakdown for train images. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_task.stenosis.validation_images` | integer | Source-reported quantity or quantity breakdown for validation images. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_task.task1` | object | Source-defined task1 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `splits_by_task.task1.source_train` | object | Dataset subset or source-defined breakdown named `source_train`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits_by_task.task1.source_train.contrast` | string | Image contrast, sequence contrast or contrast-agent condition described by the source. |
| `splits_by_task.task1.source_train.scan_count` | integer | Number of scans in the stated scope, possibly represented as a value/approximation/raw-text object. Unit/format: scans; stated cohort/split. |
| `splits_by_task.task1.target_test` | object | Dataset subset or source-defined breakdown named `target_test`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits_by_task.task1.target_test.scan_count` | integer | Number of scans in the stated scope, possibly represented as a value/approximation/raw-text object. Unit/format: scans; stated cohort/split. |
| `splits_by_task.task1.target_train` | object | Dataset subset or source-defined breakdown named `target_train`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits_by_task.task1.target_train.contrast` | string | Image contrast, sequence contrast or contrast-agent condition described by the source. |
| `splits_by_task.task1.target_train.scan_count` | integer | Number of scans in the stated scope, possibly represented as a value/approximation/raw-text object. Unit/format: scans; stated cohort/split. |
| `splits_by_task.task1.target_validation` | object | Dataset subset or source-defined breakdown named `target_validation`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits_by_task.task1.target_validation.scan_count` | integer | Number of scans in the stated scope, possibly represented as a value/approximation/raw-text object. Unit/format: scans; stated cohort/split. |
| `splits_by_task.task1.test_case_count` | integer | Source-reported quantity or quantity breakdown for test case count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_task.task1.test_image_count` | integer | Source-reported quantity or quantity breakdown for test image count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_task.task1.train_case_count` | integer | Source-reported quantity or quantity breakdown for train case count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_task.task1.train_image_count` | integer | Source-reported quantity or quantity breakdown for train image count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_task.task2` | object | Source-defined task2 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `splits_by_task.task2.test_case_count` | integer | Source-reported quantity or quantity breakdown for test case count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_task.task2.test_image_count` | integer | Source-reported quantity or quantity breakdown for test image count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_task.task2.train_case_count` | integer | Source-reported quantity or quantity breakdown for train case count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_task.task2.train_image_count` | integer | Source-reported quantity or quantity breakdown for train image count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_task.task3` | object | Source-defined task3 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `splits_by_task.task3.test_image_count` | integer | Source-reported quantity or quantity breakdown for test image count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_by_task.task3.train_image_count` | integer | Source-reported quantity or quantity breakdown for train image count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_per_species` | object | Dataset subset or source-defined breakdown named `splits_per_species`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits_per_species.test` | object | Test-stage subset, quantity, procedure or outcome under the parent field; preserve its recorded unit and phase. |
| `splits_per_species.test.volume_pair_count` | integer | Source-reported quantity or quantity breakdown for volume pair count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_per_species.train` | object | Dataset subset or source-defined breakdown named `train`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits_per_species.train.volume_pair_count` | integer | Source-reported quantity or quantity breakdown for volume pair count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_per_species.validation` | object | Validation-stage data, quantities, submissions or results; not automatically final-test evidence. |
| `splits_per_species.validation.volume_pair_count` | integer | Source-reported quantity or quantity breakdown for volume pair count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `splits_per_task_per_anatomy` | object | Dataset subset or source-defined breakdown named `splits_per_task_per_anatomy`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits_per_task_per_anatomy.test` | object | Test-stage subset, quantity, procedure or outcome under the parent field; preserve its recorded unit and phase. |
| `splits_per_task_per_anatomy.test.patient_count` | integer | Number of patients in the stated cohort or split; not interchangeable with studies, scans or images. Unit/format: patients; stated cohort/split. |
| `splits_per_task_per_anatomy.train` | object | Dataset subset or source-defined breakdown named `train`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `splits_per_task_per_anatomy.train.patient_count` | integer | Number of patients in the stated cohort or split; not interchangeable with studies, scans or images. Unit/format: patients; stated cohort/split. |
| `splits_per_task_per_anatomy.validation` | object | Validation-stage data, quantities, submissions or results; not automatically final-test evidence. |
| `splits_per_task_per_anatomy.validation.patient_count` | integer | Number of patients in the stated cohort or split; not interchangeable with studies, scans or images. Unit/format: patients; stated cohort/split. |
| `structured_extraction_status` | string | Recorded state of structured extraction. Preserve the task/phase scope and source qualifications. |
| `structured_quantity_extraction_status` | string | Recorded state of structured quantity extraction. Preserve the task/phase scope and source qualifications. |
| `subsets` | array; items: object | Dataset subset or source-defined breakdown named `subsets`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `subsets[].description` | string | Description of the enclosing entity, procedure, data or result as retained from the source or review. |
| `subsets[].subset_id` | string | Dataset subset or source-defined breakdown named `subset_id`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `subsets[].test_case_count` | integer | Source-reported quantity or quantity breakdown for test case count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `subsets[].train_case_count` | integer | Source-reported quantity or quantity breakdown for train case count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `synthetic` | boolean | Whether the condition “synthetic” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `task_anatomy_strata` | array; items: string | Dataset subset or source-defined breakdown named `task_anatomy_strata`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `task_datasets` | array; items: object | Source-reported quantity or quantity breakdown for task datasets. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `task_datasets[].counts_basis` | string | Evidence or reasoning supporting counts. |
| `task_datasets[].evaluation_count` | object | Source-reported quantity or quantity breakdown for evaluation count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `task_datasets[].evaluation_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `task_datasets[].evaluation_count.lower_bound` | boolean | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `task_datasets[].evaluation_count.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `task_datasets[].evaluation_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `task_datasets[].labeled_training_count` | object | Source-reported quantity or quantity breakdown for labeled training count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `task_datasets[].labeled_training_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `task_datasets[].labeled_training_count.lower_bound` | boolean | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `task_datasets[].labeled_training_count.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `task_datasets[].labeled_training_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `task_datasets[].noise_simulation` | string | Procedure or setting used to generate simulated noise in the stated data or evaluation. |
| `task_datasets[].sources` | array; items: string | Sources supporting the enclosing statement or dataset description, preserving document/source type and scope. |
| `task_datasets[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. |
| `task_datasets[].test_count` | null / object | Test-set quantity in the unit explicitly specified by the enclosing source. |
| `task_datasets[].test_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `task_datasets[].test_count.lower_bound` | boolean | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `task_datasets[].test_count.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `task_datasets[].test_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `task_datasets[].test_sources` | array; items: object | Sources supporting test. |
| `task_datasets[].test_sources[].name` | string | Name of the enclosing task, institution, dataset, source, method or event; the parent field identifies the entity. |
| `task_datasets[].test_sources[].subjects` | integer | Source-reported quantity or quantity breakdown for subjects. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `task_datasets[].test_subject_count` | object | Source-reported quantity or quantity breakdown for test subject count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `task_datasets[].test_subject_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `task_datasets[].test_subject_count.lower_bound` | boolean | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `task_datasets[].test_subject_count.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `task_datasets[].test_subject_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `task_datasets[].total_count` | object | Source-reported quantity or quantity breakdown for total count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `task_datasets[].total_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `task_datasets[].total_count.lower_bound` | boolean | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `task_datasets[].total_count.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `task_datasets[].total_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `task_datasets[].train_count` | object | Training-set quantity in the unit explicitly specified by the enclosing source. |
| `task_datasets[].train_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `task_datasets[].train_count.lower_bound` | boolean | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `task_datasets[].train_count.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `task_datasets[].train_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `task_datasets[].training_subject_count` | object | Source-reported quantity or quantity breakdown for training subject count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `task_datasets[].training_subject_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `task_datasets[].training_subject_count.lower_bound` | boolean | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `task_datasets[].training_subject_count.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `task_datasets[].training_subject_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `task_datasets[].unlabeled_training_count` | object | Source-reported quantity or quantity breakdown for unlabeled training count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `task_datasets[].unlabeled_training_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `task_datasets[].unlabeled_training_count.lower_bound` | boolean | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `task_datasets[].unlabeled_training_count.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `task_datasets[].unlabeled_training_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `task_datasets[].validation_count` | object | Validation-set quantity in the unit explicitly specified by the enclosing source. |
| `task_datasets[].validation_count.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `task_datasets[].validation_count.lower_bound` | boolean | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `task_datasets[].validation_count.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `task_datasets[].validation_count.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `test_center_count` | integer | Source-reported quantity or quantity breakdown for test center count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `test_composition` | string | Dataset subset or source-defined breakdown named `test_composition`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `test_description` | string | Source description of test. |
| `test_image_mask_pairs` | object | Source-reported quantity or quantity breakdown for test image mask pairs. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `test_image_mask_pairs.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `test_image_mask_pairs.lower_bound` | boolean | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `test_image_mask_pairs.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `test_image_mask_pairs.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `test_tumor_types` | integer | Dataset subset or source-defined breakdown named `test_tumor_types`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `testing` | object | Testing-stage data, rules or execution arrangements as specified in the enclosing record. |
| `testing.case_types` | array; items: string | Dataset subset or source-defined breakdown named `case_types`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `testing.cases` | integer | Source-reported quantity or quantity breakdown for cases. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `testing.hidden` | boolean | Whether the condition “hidden” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `total_count_basis` | string | Evidence or reasoning supporting total count. |
| `training` | object | Training-stage data, quantities, rules or model-use arrangements, according to the parent field. |
| `training.annotations_provided` | boolean | Source-reported quantity or quantity breakdown for annotations provided. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `training.case_types` | array; items: string | Dataset subset or source-defined breakdown named `case_types`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `training.cases` | integer | Source-reported quantity or quantity breakdown for cases. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `training.postoperative_followup` | string | Source-recorded postoperative followup for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `training_center_count` | integer | Source-reported quantity or quantity breakdown for training center count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `training_data_provided` | boolean | Dataset subset or source-defined breakdown named `training_data_provided`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `training_fps` | integer | Acquisition or sample specification for training frames per second; use the unit explicitly named in the key or source, without converting counts or inferring an unstated unit. Unit/format: frames/second; denominator/scope follows field name. |
| `training_regimes` | array; items: object | Dataset subset or source-defined breakdown named `training_regimes`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `training_regimes[].name` | string | Name of the enclosing task, institution, dataset, source, method or event; the parent field identifies the entity. |
| `training_regimes[].subset_of` | string | Dataset subset or source-defined breakdown named `subset_of`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `training_source_type` | string | Dataset subset or source-defined breakdown named `training_source_type`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `training_tool_class_count` | integer | Source-reported quantity or quantity breakdown for training tool class count. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `training_tumor_types` | integer | Dataset subset or source-defined breakdown named `training_tumor_types`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `unique_patient_total` | null | Number of distinct patients across the stated scope after the source's deduplication; not a sum of overlapping split counts. |
| `upstream_acquisition_note` | string | Qualification or source distinction concerning upstream acquisition. |
| `validation` | object | Validation-stage data, quantities, submissions or results; not automatically final-test evidence. |
| `validation.annotations_provided` | boolean | Source-reported quantity or quantity breakdown for annotations provided. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `validation.case_types` | array; items: string | Dataset subset or source-defined breakdown named `case_types`. Its value/nested fields specify composition or quantity in the enclosing task and split. |
| `validation.cases` | integer | Source-reported quantity or quantity breakdown for cases. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `validation.postoperative_followup` | string | Source-recorded postoperative followup for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `validation_prediction_counts` | object | Source-reported quantity or quantity breakdown for validation prediction counts. The key and enclosing unit/split define what is counted; overlapping cohorts and different units are not pooled. |
| `validation_prediction_counts.task1` | integer | Source-defined task1 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `validation_prediction_counts.task2` | integer | Source-defined task2 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `voxel_size_nm` | array; items: integer | Acquisition or sample specification for voxel size nm; use the unit explicitly named in the key or source, without converting counts or inferring an unstated unit. Unit/format: nm; denominator/scope follows field name. |
| `voxel_spacing_micrometers` | array; items: number | Acquisition or sample specification for voxel spacing micrometers; use the unit explicitly named in the key or source, without converting counts or inferring an unstated unit. Unit/format: micrometers; denominator/scope follows field name. |
| `voxel_spacing_mm` | array; items: integer, number | Acquisition or sample specification for voxel spacing mm; use the unit explicitly named in the key or source, without converting counts or inferring an unstated unit. Unit/format: mm; denominator/scope follows field name. |

<a id="resource-characteristics-review"></a>

## `resource_characteristics_review`

JSON parent path: `challenge.resource_characteristics_review`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.resource_characteristics_review`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `fields` | object | Named variables examined in the enclosing review; child keys identify the individual coding domains. |
| `fields.active_teams` | object | Number of active teams under the source's definition and stated phase. |
| `fields.active_teams.state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. |
| `fields.active_teams.value` | null / object | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.active_teams.value.approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `fields.active_teams.value.comparable` | boolean | Whether the condition “comparable” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `fields.active_teams.value.details` | string | Source-recorded details for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `fields.active_teams.value.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `fields.active_teams.value.unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `fields.active_teams.value.value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.centers` | object | Structured entries for centers within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fields.centers.state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. |
| `fields.centers.value` | null / string | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.geography` | object | Explicit acquisition geography or identifiable source locations, retaining partial coverage and plans. |
| `fields.geography.state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. |
| `fields.geography.value` | object | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.geography.value.countries` | array; items: string | Structured entries for countries within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fields.geography.value.reported_scope` | string | Task, phase, cohort or source boundaries of reported. |
| `fields.post_challenge` | object | Structured entries for post challenge within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fields.post_challenge.state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. |
| `fields.post_challenge.value` | null / string | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.typed_size` | object | Dataset quantity interpreted together with its explicit unit, split and source scope. |
| `fields.typed_size.state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. |
| `fields.typed_size.value` | array; items: object | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.typed_size.value[].approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `fields.typed_size.value[].lower_bound` | boolean | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `fields.typed_size.value[].range` | boolean | Whether the condition “range” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `fields.typed_size.value[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `fields.typed_size.value[].split` | string | Dataset partition to which the enclosing quantity, observation or result applies. |
| `fields.typed_size.value[].unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `fields.typed_size.value[].upper_value` | integer | Upper numerical endpoint of the stated quantity range; preserve whether the bound is inclusive or approximate. |
| `fields.typed_size.value[].value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `review_date` | string | Date of the review operation described in the enclosing object. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `review_note` | string | Qualification or source distinction concerning review. |
| `sources` | array; items: object | Sources supporting the enclosing statement or dataset description, preserving document/source type and scope. |
| `sources[].local_source` | string | Path identifying a source in the original review archive, not a downloadable file inside this release. |
| `sources[].section` | string | Section, figure, table or location within a supporting source. |
| `sources[].url` | string | Web address of the enclosing source, document or resource. |

[Back to README](../../README.md#variable-dictionary)
