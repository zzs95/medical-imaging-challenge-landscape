# Clinical scope and imaging modalities

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

Anatomy, disease context, acquisition modalities and their harmonized classifications.

## Field groups

- [`challenge.clinical_domain`](#clinical-domain)
- [`challenge.clinical_classification_review`](#clinical-classification-review)
- [`challenge.modality_harmonization_review`](#modality-harmonization-review)

<a id="clinical-domain"></a>

## `clinical_domain`

JSON parent path: `challenge.clinical_domain`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.clinical_domain`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `body_region` | null / array; items: string | Broad anatomical region represented by the task or cohort. |
| `body_region_applicability` | string | Whether human anatomical region coding applies, with non-human, cellular, phantom or procedural contexts kept distinct. |
| `body_region_basis` | string | Evidence or reasoning supporting body region. |
| `clinical_context` | null / string | Clinical, procedural or specimen context in which the task or cohort is described. |
| `disease_evidence_scope` | string | Task, phase, cohort or source boundaries of disease evidence. |
| `diseases` | null / array; items: string | Explicit disease, condition or abnormality targets or cohort diagnoses; not inferred from an organ name alone. |
| `modality` | null / array; items: string | Imaging acquisition category recorded for the challenge; raw labels can differ from harmonized analytical categories. |
| `modality_counting_note` | string | Qualification or source distinction concerning modality counting. |
| `modality_detail` | string | More specific modality description retained alongside the broad category. |
| `modality_evidence_scope` | string | Task, phase, cohort or source boundaries of modality evidence. |
| `organ_system` | null / array; items: string | Review-level anatomical/physiological system grouping associated with the documented targets. |
| `organ_system_basis` | null / string | Evidence or reasoning supporting organ system. |
| `organ_system_coding_scope` | null / string | Which recorded anatomical targets support the organ-system grouping and what that grouping does not imply. |
| `organs_or_structures` | null / array; items: string | Specific organs, structures, specimen types or procedure contexts named by the source. |
| `submodality` | null / array; items: string | More specific acquisition sequence, protocol, tracer or imaging variant within a modality. |
| `submodality_detail` | string | Additional sequence/protocol/tracer details for the stated imaging modality. |

<a id="clinical-classification-review"></a>

## `clinical_classification_review`

JSON parent path: `challenge.clinical_classification_review`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.clinical_classification_review`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `anatomical_scope` | string | Task, phase, cohort or source boundaries of anatomical. |
| `basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `disease_review_note` | string | Qualification or source distinction concerning disease review. |
| `disease_scope_note` | string | Qualification or source distinction concerning disease scope. |
| `fields` | object | Named variables examined in the enclosing review; child keys identify the individual coding domains. |
| `fields.body_region` | object | Broad anatomical region represented by the task or cohort. |
| `fields.body_region.note` | string | Contextual qualification, uncertainty or source distinction for the enclosing item. |
| `fields.body_region.state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. |
| `fields.body_region.value` | array; items: string | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.disease` | object | Structured entries for disease within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fields.disease.note` | string | Contextual qualification, uncertainty or source distinction for the enclosing item. |
| `fields.disease.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `fields.disease.source_urls` | string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `fields.disease.state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. |
| `fields.disease.value` | array; items: string | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `note_zh` | string | Chinese-language qualification or explanation for the enclosing review decision. |
| `organs_or_structures` | array; items: string | Specific organs, structures, specimen types or procedure contexts named by the source. |
| `remaining_detail` | string | Specific detail not established by the available sources. |
| `review_date` | string | Date of the review operation described in the enclosing object. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `review_history` | array; items: object | Earlier review actions and interpretations; not additional current observations. |
| `review_history[].audit` | string | Identifier or path of the audit in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `review_history[].backup` | string | Identifier or path of the backup in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `review_history[].date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `review_history[].field` | string | Name/path of the variable targeted by the enclosing review, source mapping or change record. |
| `review_history[].previous_specific_diseases` | null | Earlier/superseded value of specific diseases, preserved to document a revision rather than a current observation. |
| `review_history[].previous_state` | string | Earlier documentary or classification state, retained before the recorded revision. |
| `review_history[].review_note` | string | Qualification or source distinction concerning review. |
| `review_note` | string | Qualification or source distinction concerning review. |
| `review_scope` | string | Variables, tasks, phases or source types covered by the recorded review. |
| `sources` | array; items: object | Sources supporting the enclosing statement or dataset description, preserving document/source type and scope. |
| `sources[].capture_date` | string | Date associated with capture. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `sources[].local_source` | string | Path identifying a source in the original review archive, not a downloadable file inside this release. |
| `sources[].section` | string | Section, figure, table or location within a supporting source. |
| `sources[].sha256` | string | Cryptographic checksum or revision identifier for the enclosing sha256; used for provenance rather than as a scientific measurement. |
| `sources[].url` | string | Web address of the enclosing source, document or resource. |
| `sources[].verification` | string | Source-recorded verification for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `specific_diseases` | array; items: string | Structured entries for specific diseases within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |

<a id="modality-harmonization-review"></a>

## `modality_harmonization_review`

JSON parent path: `challenge.modality_harmonization_review`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.modality_harmonization_review`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `harmonized_modalities` | array; items: string | Imaging categories harmonized for the review; multiple categories may apply, and video is a format attribute. |
| `note` | string | Contextual qualification, uncertainty or source distinction for the enclosing item. |
| `original_analysis_labels` | array; items: string | Structured entries for original analysis labels within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `review_date` | string | Date of the review operation described in the enclosing object. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `sources` | array; items: object | Sources supporting the enclosing statement or dataset description, preserving document/source type and scope. |
| `sources[].local_source` | string | Path identifying a source in the original review archive, not a downloadable file inside this release. |
| `sources[].url` | string | Web address of the enclosing source, document or resource. |
| `video_format_documented` | boolean | Whether the condition “video format documented” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |

[Back to README](../../README.md#variable-dictionary)
