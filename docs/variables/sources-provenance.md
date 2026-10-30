# Sources, provenance and field review

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

URLs, evidence records, review dates, field-level support and original archive references.

## Field groups

- [`challenge.links`](#links)
- [`challenge.provenance`](#provenance)
- [`challenge.record_field_review`](#record-field-review)

<a id="links"></a>

## `links`

JSON parent path: `challenge.links`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.links`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `challenge_paper` | null / string | Public link to the challenge paper resource associated with the edition; availability is specific to the recorded observation. |
| `dataset` | null / string | Source cohorts, quantities, splits, acquisition conditions and associated data characteristics. |
| `dataset_paper` | string | Public link to the dataset paper resource associated with the edition; availability is specific to the recorded observation. |
| `docker_template` | string | Public link to the docker template resource associated with the edition; availability is specific to the recorded observation. |
| `github` | null / string | Public link to the github resource associated with the edition; availability is specific to the recorded observation. |
| `grand_challenge` | null / string | Public link to the grand challenge resource associated with the edition; availability is specific to the recorded observation. |
| `official` | string | Public link to the official resource associated with the edition; availability is specific to the recorded observation. |
| `official_conference_programme` | null / string | Public link to the official conference programme resource associated with the edition; availability is specific to the recorded observation. |
| `official_registry` | string | Public link to the official registry resource associated with the edition; availability is specific to the recorded observation. |
| `official_website` | null / string | Public link to the official website resource associated with the edition; availability is specific to the recorded observation. |
| `platform` | null / string | Named service involved in the enclosing data, submission or evaluation operation; service naming alone does not establish the executor. |
| `platform_scope` | string | Task, phase, cohort or source boundaries of platform. |
| `registration` | string | Task flag for estimating spatial correspondence or alignment between images or representations. |
| `related_parent` | string | Public link to the related parent resource associated with the edition; availability is specific to the recorded observation. |
| `supporting_sources` | array; items: string | Sources supporting supporting. |
| `task2_platform` | string | Public link to the task2 platform resource associated with the edition; availability is specific to the recorded observation. |

<a id="provenance"></a>

## `provenance`

JSON parent path: `challenge.provenance`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.provenance`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `collection_batch` | string | Source-recorded collection batch for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `collection_date` | string | Date when challenge metadata were collected, not when the underlying medical images were acquired. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `collection_date_definition` | string | Explanation distinguishing metadata collection dates from underlying data acquisition dates. |
| `collection_date_description` | string | Source description of collection date. |
| `collection_date_format` | string | Format used to encode metadata collection dates. |
| `collection_status` | string | Recorded completeness/verification status of the metadata collection. |
| `curation_input` | string | Source-recorded curation input for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `field_evidence` | object | Supporting evidence indexed by target field name; the child keys identify the fields being justified. |
| `field_evidence.assessment_evidence` | object | Evidence entry supporting the target field `assessment_evidence`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.assessment_evidence.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.assessment_evidence.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.assessment_evidence.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.assessment_evidence.source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `field_evidence.assessment_evidence.status` | object | Evidence entry supporting the target field `assessment_evidence.status`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.assessment_evidence.status.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.assessment_evidence.status.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.assessment_evidence.status.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.assessment_evidence.track_results` | object | Evidence entry supporting the target field `assessment_evidence.track_results`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.assessment_evidence.track_results.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.assessment_evidence.track_results.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.assessment_evidence.track_results.source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `field_evidence.clinical_domain.body_region` | object | Evidence entry supporting the target field `clinical_domain.body_region`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.clinical_domain.body_region.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.clinical_domain.body_region.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.clinical_domain.body_region.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.clinical_domain.body_region.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.clinical_domain.body_region_basis` | object | Evidence entry supporting the target field `clinical_domain.body_region_basis`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.clinical_domain.body_region_basis.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.clinical_domain.body_region_basis.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.clinical_domain.body_region_basis.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.clinical_domain.body_region_basis.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.clinical_domain.clinical_context` | object | Evidence entry supporting the target field `clinical_domain.clinical_context`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.clinical_domain.clinical_context.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.clinical_domain.clinical_context.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.clinical_domain.clinical_context.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.clinical_domain.clinical_context.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.clinical_domain.disease_evidence_scope` | object | Evidence entry supporting the target field `clinical_domain.disease_evidence_scope`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.clinical_domain.disease_evidence_scope.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.clinical_domain.disease_evidence_scope.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.clinical_domain.disease_evidence_scope.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.clinical_domain.disease_evidence_scope.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.clinical_domain.diseases` | object | Evidence entry supporting the target field `clinical_domain.diseases`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.clinical_domain.diseases.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.clinical_domain.diseases.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.clinical_domain.diseases.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.clinical_domain.diseases.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.clinical_domain.organ_system` | object | Evidence entry supporting the target field `clinical_domain.organ_system`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.clinical_domain.organ_system.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.clinical_domain.organ_system.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.clinical_domain.organ_system.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.clinical_domain.organ_system.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.clinical_domain.organ_system_basis` | object | Evidence entry supporting the target field `clinical_domain.organ_system_basis`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.clinical_domain.organ_system_basis.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.clinical_domain.organ_system_basis.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.clinical_domain.organ_system_basis.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.clinical_domain.organ_system_basis.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.clinical_domain.organ_system_coding_scope` | object | Evidence entry supporting the target field `clinical_domain.organ_system_coding_scope`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.clinical_domain.organ_system_coding_scope.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.clinical_domain.organ_system_coding_scope.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.clinical_domain.organ_system_coding_scope.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.clinical_domain.organ_system_coding_scope.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.data_access.access_after_challenge` | object | Evidence entry supporting the target field `data_access.access_after_challenge`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.data_access.access_after_challenge.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.data_access.access_after_challenge.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.data_access.access_after_challenge.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.data_access.access_after_challenge.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.data_access.access_scope` | object | Evidence entry supporting the target field `data_access.access_scope`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.data_access.access_scope.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.data_access.access_scope.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.data_access.access_scope.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.data_access.access_scope.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.data_access.access_status` | object | Evidence entry supporting the target field `data_access.access_status`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.data_access.access_status.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.data_access.access_status.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.data_access.access_status.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.data_access.access_status.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.data_access.dua_required` | object | Evidence entry supporting the target field `data_access.dua_required`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.data_access.dua_required.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.data_access.dua_required.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.data_access.dua_required.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.data_access.dua_required.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.data_access.is_public` | object | Evidence entry supporting the target field `data_access.is_public`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.data_access.is_public.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.data_access.is_public.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.data_access.is_public.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.data_access.is_public.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.data_access.license_conflict` | object | Evidence entry supporting the target field `data_access.license_conflict`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.data_access.license_conflict.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.data_access.license_conflict.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.data_access.license_conflict.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.data_access.license_conflict.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.data_access.license_or_terms` | object | Evidence entry supporting the target field `data_access.license_or_terms`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.data_access.license_or_terms.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.data_access.license_or_terms.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.data_access.license_or_terms.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.data_access.license_or_terms.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.data_access.license_review_resolution` | object | Evidence entry supporting the target field `data_access.license_review_resolution`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.data_access.license_review_resolution.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.data_access.license_review_resolution.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.data_access.license_review_resolution.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.data_access.license_review_resolution.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.data_access.license_review_status` | object | Evidence entry supporting the target field `data_access.license_review_status`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.data_access.license_review_status.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.data_access.license_review_status.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.data_access.license_review_status.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.data_access.license_review_status.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.data_access.public_download` | object | Evidence entry supporting the target field `data_access.public_download`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.data_access.public_download.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.data_access.public_download.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.data_access.public_download.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.data_access.public_download.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.data_access.versioned_access` | object | Evidence entry supporting the target field `data_access.versioned_access`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.data_access.versioned_access.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.data_access.versioned_access.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.data_access.versioned_access.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.data_access.versioned_access.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.data_usage_mode` | object | Evidence entry supporting the target field `data_usage_mode`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.data_usage_mode.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.data_usage_mode.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.data_usage_mode.source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `field_evidence.data_usage_mode.evidence_stage` | object | Evidence entry supporting the target field `data_usage_mode.evidence_stage`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.data_usage_mode.evidence_stage.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.data_usage_mode.evidence_stage.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.data_usage_mode.evidence_stage.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.data_usage_mode.evidence_stage.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.data_usage_mode.interpretation` | object | Evidence entry supporting the target field `data_usage_mode.interpretation`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.data_usage_mode.interpretation.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.data_usage_mode.interpretation.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.data_usage_mode.interpretation.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.data_usage_mode.interpretation.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.data_usage_mode.overall_paradigm` | object | Evidence entry supporting the target field `data_usage_mode.overall_paradigm`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.data_usage_mode.overall_paradigm.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.data_usage_mode.overall_paradigm.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.data_usage_mode.overall_paradigm.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.data_usage_mode.overall_paradigm.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.data_usage_mode.testing.paradigm` | object | Evidence entry supporting the target field `data_usage_mode.testing.paradigm`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.data_usage_mode.testing.paradigm.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.data_usage_mode.testing.paradigm.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.data_usage_mode.testing.paradigm.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.data_usage_mode.testing.paradigm.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.data_usage_mode.testing.server_side_inference` | object | Evidence entry supporting the target field `data_usage_mode.testing.server_side_inference`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.data_usage_mode.testing.server_side_inference.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.data_usage_mode.testing.server_side_inference.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.data_usage_mode.testing.server_side_inference.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.data_usage_mode.testing.server_side_inference.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.data_usage_mode.testing.test_data_visible_to_participants` | object | Evidence entry supporting the target field `data_usage_mode.testing.test_data_visible_to_participants`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.data_usage_mode.testing.test_data_visible_to_participants.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.data_usage_mode.testing.test_data_visible_to_participants.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.data_usage_mode.testing.test_data_visible_to_participants.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.data_usage_mode.testing.test_data_visible_to_participants.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.data_usage_mode.training.paradigm` | object | Evidence entry supporting the target field `data_usage_mode.training.paradigm`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.data_usage_mode.training.paradigm.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.data_usage_mode.training.paradigm.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.data_usage_mode.training.paradigm.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.data_usage_mode.training.paradigm.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.data_usage_mode.training.training_data_downloadable` | object | Evidence entry supporting the target field `data_usage_mode.training.training_data_downloadable`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.data_usage_mode.training.training_data_downloadable.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.data_usage_mode.training.training_data_downloadable.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.data_usage_mode.training.training_data_downloadable.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.data_usage_mode.training.training_data_downloadable.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.dataset.center_count` | object | Evidence entry supporting the target field `dataset.center_count`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.dataset.center_count.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.dataset.center_count.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.dataset.center_count.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.dataset.center_count.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.dataset.center_scope` | object | Evidence entry supporting the target field `dataset.center_scope`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.dataset.center_scope.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.dataset.center_scope.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.dataset.center_scope.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.dataset.center_scope.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.dataset.center_type` | object | Evidence entry supporting the target field `dataset.center_type`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.dataset.center_type.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.dataset.center_type.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.dataset.center_type.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.dataset.center_type.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.dataset.institutions_description` | object | Evidence entry supporting the target field `dataset.institutions_description`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.dataset.institutions_description.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.dataset.institutions_description.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.dataset.institutions_description.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.dataset.institutions_description.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.dataset.multi_center` | object | Evidence entry supporting the target field `dataset.multi_center`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.dataset.multi_center.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.dataset.multi_center.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.dataset.multi_center.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.dataset.multi_center.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.dataset.population.image_count` | object | Evidence entry supporting the target field `dataset.population.image_count`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.dataset.population.image_count.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.dataset.population.image_count.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.dataset.population.image_count.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.dataset.population.image_count.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.dataset.population.patient_count` | object | Evidence entry supporting the target field `dataset.population.patient_count`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.dataset.population.patient_count.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.dataset.population.patient_count.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.dataset.population.patient_count.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.dataset.population.patient_count.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.dataset.splits.test.case_count` | object | Evidence entry supporting the target field `dataset.splits.test.case_count`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.dataset.splits.test.case_count.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.dataset.splits.test.case_count.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.dataset.splits.test.case_count.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.dataset.splits.test.case_count.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.dataset.splits.test.patient_count` | object | Evidence entry supporting the target field `dataset.splits.test.patient_count`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.dataset.splits.test.patient_count.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.dataset.splits.test.patient_count.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.dataset.splits.test.patient_count.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.dataset.splits.test.patient_count.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.dataset.splits.test.scan_count` | object | Evidence entry supporting the target field `dataset.splits.test.scan_count`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.dataset.splits.test.scan_count.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.dataset.splits.test.scan_count.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.dataset.splits.test.scan_count.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.dataset.splits.test.scan_count.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.dataset.splits.train.case_count` | object | Evidence entry supporting the target field `dataset.splits.train.case_count`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.dataset.splits.train.case_count.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.dataset.splits.train.case_count.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.dataset.splits.train.case_count.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.dataset.splits.train.case_count.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.dataset.splits.train.patient_count` | object | Evidence entry supporting the target field `dataset.splits.train.patient_count`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.dataset.splits.train.patient_count.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.dataset.splits.train.patient_count.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.dataset.splits.train.patient_count.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.dataset.splits.train.patient_count.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.dataset.splits.train.scan_count` | object | Evidence entry supporting the target field `dataset.splits.train.scan_count`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.dataset.splits.train.scan_count.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.dataset.splits.train.scan_count.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.dataset.splits.train.scan_count.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.dataset.splits.train.scan_count.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.evaluation` | object | Evidence entry supporting the target field `evaluation`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.evaluation.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.evaluation.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.evaluation.source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `field_evidence.evaluation.executed_2025_scope` | object | Evidence entry supporting the target field `evaluation.executed_2025_scope`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.evaluation.executed_2025_scope.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.evaluation.executed_2025_scope.location` | string | Location relevant to the enclosing event, source or execution description; not automatically an image-acquisition site. |
| `field_evidence.evaluation.executed_2025_scope.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.evaluation.executed_2025_scope.supports` | string | Statements or fields that the source is recorded as supporting, limited by the source's actual task, phase and evidence scope. |
| `field_evidence.evaluation.executed_2025_scope.url` | string | Web address of the enclosing source, document or resource. |
| `field_evidence.evaluation.final_test_evaluated` | object | Evidence entry supporting the target field `evaluation.final_test_evaluated`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.evaluation.final_test_evaluated.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.evaluation.final_test_evaluated.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.evaluation.final_test_evaluated.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.evaluation.final_test_evaluated.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.evaluation.hidden_test_set` | object | Evidence entry supporting the target field `evaluation.hidden_test_set`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.evaluation.hidden_test_set.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.evaluation.hidden_test_set.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.evaluation.hidden_test_set.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.evaluation.hidden_test_set.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.evaluation.platform` | object | Evidence entry supporting the target field `evaluation.platform`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.evaluation.platform.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.evaluation.platform.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.evaluation.platform.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.evaluation.platform.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.evaluation.platform.source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `field_evidence.evaluation.platform_evidence_stage` | object | Evidence entry supporting the target field `evaluation.platform_evidence_stage`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.evaluation.platform_evidence_stage.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.evaluation.platform_evidence_stage.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.evaluation.platform_evidence_stage.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.evaluation.platform_evidence_stage.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.evaluation.platform_scope` | object | Evidence entry supporting the target field `evaluation.platform_scope`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.evaluation.platform_scope.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.evaluation.platform_scope.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.evaluation.platform_scope.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.evaluation.platform_scope.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.event.conference` | object | Evidence entry supporting the target field `event.conference`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.event.conference.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.event.conference.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.event.conference.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.links.challenge_paper` | object | Evidence entry supporting the target field `links.challenge_paper`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.links.challenge_paper.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.links.challenge_paper.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.links.challenge_paper.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.links.challenge_paper.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.links.dataset_paper` | object | Evidence entry supporting the target field `links.dataset_paper`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.links.dataset_paper.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.links.dataset_paper.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.links.dataset_paper.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.links.dataset_paper.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.participation_statistics.evaluated_algorithms` | object | Evidence entry supporting the target field `participation_statistics.evaluated_algorithms`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.participation_statistics.evaluated_algorithms.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.participation_statistics.evaluated_algorithms.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.participation_statistics.evaluated_algorithms.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.participation_statistics.evaluated_algorithms.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.participation_statistics.finalist_teams` | object | Evidence entry supporting the target field `participation_statistics.finalist_teams`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.participation_statistics.finalist_teams.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.participation_statistics.finalist_teams.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.participation_statistics.finalist_teams.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.participation_statistics.finalist_teams.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.participation_statistics.registered_teams` | object | Evidence entry supporting the target field `participation_statistics.registered_teams`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.participation_statistics.registered_teams.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.participation_statistics.registered_teams.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.participation_statistics.registered_teams.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.participation_statistics.registered_teams.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.participation_statistics.teams_with_submission` | object | Evidence entry supporting the target field `participation_statistics.teams_with_submission`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.participation_statistics.teams_with_submission.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.participation_statistics.teams_with_submission.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.participation_statistics.teams_with_submission.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.participation_statistics.teams_with_submission.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.schedule.topbrainv2_final_test` | object | Evidence entry supporting the target field `schedule.topbrainv2_final_test`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.schedule.topbrainv2_final_test.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.schedule.topbrainv2_final_test.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.schedule.topbrainv2_final_test.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.submission` | object | Evidence entry supporting the target field `submission`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.submission.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.submission.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.submission.source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `field_evidence.submission.evidence_stage` | object | Evidence entry supporting the target field `submission.evidence_stage`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.submission.evidence_stage.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.submission.evidence_stage.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.submission.evidence_stage.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.submission.evidence_stage.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.submission.platform` | object | Evidence entry supporting the target field `submission.platform`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.submission.platform.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.submission.platform.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.submission.platform.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.submission.platform.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.submission.platform_scope` | object | Evidence entry supporting the target field `submission.platform_scope`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.submission.platform_scope.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.submission.platform_scope.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.submission.platform_scope.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.submission.platform_scope.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.submission.submission_type` | object | Evidence entry supporting the target field `submission.submission_type`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.submission.submission_type.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.submission.submission_type.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.submission.submission_type.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.submission.submission_type.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.submission.submission_type.source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `field_evidence.task_profile` | object | Evidence entry supporting the target field `task_profile`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.task_profile.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.task_profile.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.task_profile.source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `field_evidence.task_profile.tasks` | object | Evidence entry supporting the target field `task_profile.tasks`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.task_profile.tasks.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.task_profile.tasks.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.task_profile.tasks.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence.task_taxonomy.language_task_absence` | object | Evidence entry supporting the target field `task_taxonomy.language_task_absence`; its nested source, date and basis identify the support and its limits. |
| `field_evidence.task_taxonomy.language_task_absence.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence.task_taxonomy.language_task_absence.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence.task_taxonomy.language_task_absence.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence.task_taxonomy.language_task_absence.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence_history` | array; items: object | Earlier versions or decisions concerning field evidence. |
| `field_evidence_history[].records` | object | Structured entries for records within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `field_evidence_history[].records.evaluation.platform` | object | Structured entries for evaluation.platform within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `field_evidence_history[].records.evaluation.platform.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence_history[].records.evaluation.platform.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence_history[].records.evaluation.platform.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence_history[].records.evaluation.platform.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence_history[].records.evaluation.platform_evidence_stage` | object | Structured entries for evaluation.platform evidence stage within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `field_evidence_history[].records.evaluation.platform_evidence_stage.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence_history[].records.evaluation.platform_evidence_stage.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence_history[].records.evaluation.platform_evidence_stage.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence_history[].records.evaluation.platform_evidence_stage.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence_history[].records.evaluation.platform_scope` | object | Task, phase, cohort or source boundaries of evaluation.platform. |
| `field_evidence_history[].records.evaluation.platform_scope.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence_history[].records.evaluation.platform_scope.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence_history[].records.evaluation.platform_scope.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence_history[].records.evaluation.platform_scope.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence_history[].records.submission.evidence_stage` | object | Structured entries for submission.evidence stage within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `field_evidence_history[].records.submission.evidence_stage.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence_history[].records.submission.evidence_stage.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence_history[].records.submission.evidence_stage.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence_history[].records.submission.evidence_stage.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence_history[].records.submission.submission_type` | object | Structured entries for submission.submission type within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `field_evidence_history[].records.submission.submission_type.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `field_evidence_history[].records.submission.submission_type.local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `field_evidence_history[].records.submission.submission_type.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `field_evidence_history[].records.submission.submission_type.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `field_evidence_history[].superseded_on` | string | Date the enclosing older value or decision was superseded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `gbms_archive_review` | object | Source-linked review of gbms archive. |
| `gbms_archive_review.archive_dates` | array; items: string | Structured entries for archive dates within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `gbms_archive_review.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `gbms_archive_review.independent_archive_access_this_turn` | boolean | Whether the condition “independent archive access this turn” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `gbms_archive_review.local_review` | string | Source-linked review of local. |
| `gbms_archive_review.review_date` | string | Date of the review operation described in the enclosing object. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `gbms_archive_review.versions_consistent` | string | Source-recorded versions consistent for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `last_searched` | string | Date of the most recent source search recorded for the enclosing item. |
| `last_updated` | string | Date the relevant metadata or source record was last updated as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `last_verified` | string | Date of the recorded verification event; not a guarantee that every field was independently reverified on that date. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `legacy_candidate_id` | string | Source-recorded legacy candidate identifier for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `manual_review_disposition` | object | Structured entries for manual review disposition within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `manual_review_disposition.confirmation_evidence_id` | string | Source-recorded confirmation evidence identifier for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `manual_review_disposition.date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `manual_review_disposition.review_status` | string | Status or scope of the review process, not a direct measure of challenge quality. |
| `manual_review_disposition.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `manual_review_disposition.supersedes` | string | Earlier statement or record that the enclosing revision replaces. |
| `missing_information_review` | object | Source-linked review of missing information. |
| `missing_information_review.fields_added` | array; items: string | Structured entries for fields added within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `missing_information_review.literature_search_snapshots` | array; items: string | Identifier or path of the literature search snapshots in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `missing_information_review.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `missing_information_review.remaining_core_fields` | array; items: string | Structured entries for remaining core fields within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `missing_information_review.report` | string | Identifier or path of the report in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `missing_information_review.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `missing_information_review.status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `portal_classification_review` | object | Source-linked review of portal classification. |
| `portal_classification_review.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `portal_classification_review.date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `portal_classification_review.independent_full_text_access_this_turn` | boolean | Whether the condition “independent full text access this turn” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `portal_classification_review.journal_pages` | array; items: integer | Structured entries for journal pages within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `portal_classification_review.local_review` | string | Source-linked review of local. |
| `portal_classification_review.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `portal_classification_review.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `portal_classification_review.sections` | array; items: string | Structured entries for sections within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `protocol_extraction_path` | string | Identifier or path of the protocol extraction path in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `record_created` | string | Date or description of creation of the metadata record. |
| `revision_history` | array; items: object | Earlier record versions or field changes retained for provenance. |
| `revision_history[].backup` | string | Identifier or path of the backup in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `revision_history[].date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. This occurrence is historical and must be interpreted within its enclosing revision. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `revision_history[].previous_challenge_name` | string | Earlier/superseded value of challenge name, preserved to document a revision rather than a current observation. |
| `revision_history[].previous_evaluation` | object | Earlier/superseded value of evaluation, preserved to document a revision rather than a current observation. |
| `revision_history[].previous_evaluation.cross_task_rule` | null | Rule linking outputs, assessments or rankings across tasks within the competition. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_evaluation.hidden_test_set` | null | Whether the designated test set or its protected component is described as hidden; read inputs/labels visibility separately. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_evaluation.online_evaluation` | null | Whether an online evaluation process is specified or reported; does not by itself establish automated inference or scoring. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_evaluation.platform` | null | Named service involved in the enclosing data, submission or evaluation operation; service naming alone does not establish the executor. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_evaluation.tasks` | array; items: object | Task-specific objects or descriptions; each has its own scope, inputs, outputs or assessment information where available. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_evaluation.tasks[].metrics` | null | Metrics assigned to the enclosing task or assessment; a metric list alone does not define the ranking formula. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_evaluation.tasks[].ranking` | null | Rule used to order participants or methods in the stated task/phase, or its source description. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_evaluation.tasks[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_primary_task_family` | string | Earlier/superseded value of primary task family, preserved to document a revision rather than a current observation. |
| `revision_history[].previous_schedule` | object | Earlier/superseded value of schedule, preserved to document a revision rather than a current observation. |
| `revision_history[].previous_schedule.vein_stenosis_activity_period` | string | Source-recorded vein stenosis activity period for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `revision_history[].previous_submission` | object | Earlier/superseded value of submission, preserved to document a revision rather than a current observation. |
| `revision_history[].previous_submission.evidence_stage` | string | Stage represented by the evidence, such as registered design, operational instructions or reported execution/results. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_submission.platform` | null | Named service involved in the enclosing data, submission or evaluation operation; service naming alone does not establish the executor. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_submission.runtime_limits` | object | Documented constraints for executing a submitted method, preserving time, host RAM and GPU memory as separate quantities. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_submission.runtime_limits.gpu` | null | GPU model or GPU resource assigned/recommended for the enclosing execution setting; retain whether mandatory or advisory. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_submission.runtime_limits.gpu_vram_gb` | null | GPU video-memory capacity or limit in GB for the stated hardware/rule; hardware capacity and an enforced software ceiling are distinct. This occurrence is historical and must be interpreted within its enclosing revision. Unit/format: GB; denominator/scope follows field name. |
| `revision_history[].previous_submission.runtime_limits.max_processing_time_per_case_minutes` | null | Maximum specified processing time for one case, in minutes; check whether this is a declared rule or enforced limit. This occurrence is historical and must be interpreted within its enclosing revision. Unit/format: minutes; denominator/scope follows field name. |
| `revision_history[].previous_submission.runtime_limits.max_ram_gb` | null | Maximum specified host/system RAM in GB; not a GPU-memory ceiling. This occurrence is historical and must be interpreted within its enclosing revision. Unit/format: GB; denominator/scope follows field name. |
| `revision_history[].previous_submission.runtime_limits.reserved_ram_gb` | null | Host/system RAM reserved for infrastructure or non-method processes, in GB, as stated by the source. This occurrence is historical and must be interpreted within its enclosing revision. Unit/format: GB; denominator/scope follows field name. |
| `revision_history[].previous_submission.submission_limits` | object | Limits on the number or timing of submissions, preserving phase, team/user unit and successful/failed-attempt rules. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_submission.submission_limits.additional_distinct_final_algorithms_possible_with_organizer_approval` | null | Whether extra distinct final algorithms may be submitted after organizer approval. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_submission.submission_limits.final_submissions_per_team` | null | Maximum final-stage submissions permitted for one team. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_submission.submission_limits.sanity_check_successful_submissions_per_day` | null | Maximum successful sanity-check submissions per day under the documented counting unit. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_submission.submission_type` | null / string | Recorded kind of submitted artifact or workflow, such as predictions, code, weights, containers or a platform-executed notebook. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_submission.task_outputs` | null | Optional field for task outputs in the enclosing record. It is unpopulated in this snapshot; neither a value nor a negative finding is established. |
| `revision_history[].previous_task_profile` | object | Earlier/superseded value of task profile, preserved to document a revision rather than a current observation. |
| `revision_history[].previous_task_profile.primary_task_family` | null / string | Single primary task label in the source record; insufficient for reconstructing all multi-label task counts. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_task_profile.related_task_families` | array; items: string | Structured entries for related task families within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `revision_history[].previous_task_profile.secondary_task_families` | null / array; items: string | Other task families associated with the edition in the source record. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_task_profile.tasks` | array; items: object | Task-specific objects or descriptions; each has its own scope, inputs, outputs or assessment information where available. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_task_profile.tasks[].clinical_goal` | null | Clinical question or intended clinical use motivating the task, not evidence of demonstrated clinical benefit. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_task_profile.tasks[].granularity` | null / string | Level at which a prediction or target is defined, such as pixel, voxel, lesion, study, patient or report. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_task_profile.tasks[].input` | null / array; items: string | Data or information supplied to the model for the described task. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_task_profile.tasks[].official_name` | string | Task or entity name as used in organizer documentation. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_task_profile.tasks[].optional_training_input` | null | Additional input information permitted or supplied during training, distinct from required inference inputs. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_task_profile.tasks[].output` | null / array; items: string | Prediction, artifact or information produced by the task or model. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_task_profile.tasks[].task_family` | string | Broad category of task output or operation for the specific task. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_task_profile.tasks[].task_id` | string | Identifier of a task within its challenge or source-specific numbering scheme. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].previous_task_profile.tasks[].task_subtype` | null / string | More specific task formulation, such as multi-label classification or instance segmentation. This occurrence is historical and must be interpreted within its enclosing revision. |
| `revision_history[].reason` | string | Reason for the enclosing decision, revision, exclusion or qualification. This occurrence is historical and must be interpreted within its enclosing revision. |
| `source_index` | null / integer | Position or indexing convention in the original source-discovery list; not an analytical count. |
| `source_list` | string | Identifier or path of the source list in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `source_list_index` | integer | Position or indexing convention in the original source-discovery list; not an analytical count. |
| `source_list_index_base` | integer | Position or indexing convention in the original source-discovery list; not an analytical count. |
| `source_snapshots` | array; items: string | Structured entries for source snapshots within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `sources` | array; items: object | Sources supporting the enclosing statement or dataset description, preserving document/source type and scope. |
| `sources[].basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `sources[].blob_sha` | null / string | Cryptographic checksum or revision identifier for the enclosing blob; used for provenance rather than as a scientific measurement. |
| `sources[].browser_verification` | string | Source-recorded browser verification for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `sources[].commit` | string | Source-recorded commit for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `sources[].competition_year` | integer | Calendar year assigned to competition; preserve whether this concerns an edition, analysis, event or publication. |
| `sources[].doi` | string | Digital Object Identifier assigned to the enclosing publication, protocol or dataset. |
| `sources[].http_status` | null / integer | Recorded state of http. Preserve the task/phase scope and source qualifications. |
| `sources[].journal_pages` | array; items: integer | Structured entries for journal pages within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `sources[].limits` | string | Set of limits applied to the enclosing resources or procedures. |
| `sources[].local_document` | string | Path or identifier of a document in the original review archive; not bundled here unless explicitly listed. |
| `sources[].local_file` | string | Path or identifier of a file in the original review archive. |
| `sources[].local_pdf` | string | Identifier or path of the local pdf in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `sources[].local_snapshot` | null / string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `sources[].location` | string | Location relevant to the enclosing event, source or execution description; not automatically an image-acquisition site. |
| `sources[].locations` | string | Source-recorded locations for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `sources[].propagated_on` | string | Date an existing review decision/evidence item was copied into the canonical record; not a new external verification date. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `sources[].publication_year` | integer | Year of publication or posting, separate from the year of the challenge edition. |
| `sources[].qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `sources[].received_on` | string | Date of receipt of the enclosing source material or confirmation. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `sources[].registered_task_indices` | array; items: integer | Structured entries for registered task indices within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `sources[].resolved_record_id` | integer | Identifier of the source/ledger record selected after resolving the referenced item. |
| `sources[].retrieval_scope` | string | Task, phase, cohort or source boundaries of retrieval. |
| `sources[].retrieved_on` | string | Date when the cited source was retrieved or captured. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `sources[].review_record` | string | Identifier/path of the corresponding review entry or ledger; it may refer to an unbundled archive. |
| `sources[].reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `sources[].sections` | array; items: string | Structured entries for sections within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `sources[].snapshot_sha256` | string | Cryptographic checksum or revision identifier for the enclosing snapshot; used for provenance rather than as a scientific measurement. |
| `sources[].source_accessible` | boolean | Whether the condition “source accessible” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `sources[].source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `sources[].supports` | string / array; items: string | Statements or fields that the source is recorded as supporting, limited by the source's actual task, phase and evidence scope. |
| `sources[].text_snapshot` | string | Original archive path to an extracted text snapshot of the source. |
| `sources[].title` | string | Title of the enclosing source document, publication, method or programme entry. |
| `sources[].type` | string | Type of the enclosing source, document, artifact, observation or event; its vocabulary is specific to that parent context. |
| `sources[].url` | null / string | Web address of the enclosing source, document or resource. |
| `sources[].verification_notes` | string | Qualifications and source distinctions concerning verification. |
| `submission_human_review` | object | Source-linked review of submission human. |
| `submission_human_review.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `submission_human_review.independent_full_text_access_this_turn` | boolean | Whether the condition “independent full text access this turn” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `submission_human_review.journal_pages` | array; items: integer | Structured entries for journal pages within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `submission_human_review.local_review` | string | Source-linked review of local. |
| `submission_human_review.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `submission_human_review.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `submission_human_review.sections` | array; items: string | Structured entries for sections within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `supersedes_analytical_unit` | string | Source-recorded supersedes analytical unit for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `targeted_review_history` | array; items: object | History of focused source checks or decisions on particular fields. |
| `targeted_review_history[].action` | string | Source-recorded action for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `targeted_review_history[].aggregate_rebuilt` | boolean | Whether the condition “aggregate rebuilt” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `targeted_review_history[].aggregate_status` | string | Recorded state of aggregate. Preserve the task/phase scope and source qualifications. |
| `targeted_review_history[].backup` | string | Identifier or path of the backup in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `targeted_review_history[].baseline_separation` | string | Explanation separating organizer/local baseline experiments from competition assessment evidence. |
| `targeted_review_history[].basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `targeted_review_history[].basis_type` | string | Kind of evidence underlying the enclosing decision, such as public documentation or human confirmation. |
| `targeted_review_history[].caption_competition_assessment` | string | Evidence/status of competitive caption assessment in the specified phase. |
| `targeted_review_history[].caption_specific_final_assessment` | string | Source-recorded caption specific final assessment for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `targeted_review_history[].changes` | array; items: string | Structured entries for changes within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `targeted_review_history[].comparison_file` | string | Source-recorded comparison file for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `targeted_review_history[].comparison_result` | string | Source-recorded comparison result for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `targeted_review_history[].date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `targeted_review_history[].decision_basis` | string | Evidence or reasoning supporting decision. |
| `targeted_review_history[].declared_captioning_objective` | string | Source-recorded declared captioning objective for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `targeted_review_history[].dialogue` | boolean | Whether the condition “dialogue” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `targeted_review_history[].directly_retrieved_protocol_snapshots` | array; items: string | Identifier or path of the directly retrieved protocol snapshots in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `targeted_review_history[].edition_completion` | string | Source-recorded edition completion for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `targeted_review_history[].evaluation_methods` | array; items: string | Structured entries for evaluation methods within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `targeted_review_history[].evidence_ids` | array; items: string | Identifiers of specific evidence items supporting the enclosing interpretation; archival ledgers may be outside this package. |
| `targeted_review_history[].evidence_state` | string | State of the documentary evidence for the specific field or assessment, retaining ambiguity, missingness and structural non-applicability. |
| `targeted_review_history[].fields_updated` | array; items: string | Structured entries for fields updated within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `targeted_review_history[].foundation_model_objective` | string | Whether the organizer's stated objective concerns large-scale pretraining, reusable representations or adaptation of a pretrained/foundation model. |
| `targeted_review_history[].human_review_scope` | string | Task, phase, cohort or source boundaries of human review. |
| `targeted_review_history[].image_text_generation` | boolean | Whether the condition “image text generation” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `targeted_review_history[].include_in_confirmed_caption_assessment_count` | boolean | Whether the condition “include in confirmed caption assessment count” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `targeted_review_history[].independently_verified_complete_final_rankings` | string | Source-recorded independently verified complete final rankings for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `targeted_review_history[].independently_verified_in_this_update` | boolean | Whether the condition “independently verified in this update” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `targeted_review_history[].instruction` | string | Instruction recorded for the enclosing procedure or decision; distinguish organizer instructions from historical author/reviewer requests. |
| `targeted_review_history[].new_external_search` | boolean | Whether the condition “new external search” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `targeted_review_history[].nonblocking_evidence_gap` | string | Unresolved documentary detail retained without changing the stated inclusion/coding decision. |
| `targeted_review_history[].note` | string | Contextual qualification, uncertainty or source distinction for the enclosing item. |
| `targeted_review_history[].participant_paper_doi` | string | DOI of the participant publication cited as supporting the enclosing statement. |
| `targeted_review_history[].previous_affiliation_review` | object | Earlier/superseded value of affiliation review, preserved to document a revision rather than a current observation. |
| `targeted_review_history[].previous_affiliation_review.conference_assignment` | null | Decision assigning the edition to a conference group, with supporting scope and qualifications. This occurrence is historical and must be interpreted within its enclosing revision. |
| `targeted_review_history[].previous_affiliation_review.current_inventory_year` | integer | Calendar year assigned to current inventory; preserve whether this concerns an edition, analysis, event or publication. |
| `targeted_review_history[].previous_affiliation_review.note_zh` | string | Chinese-language qualification or explanation for the enclosing review decision. This occurrence is historical and must be interpreted within its enclosing revision. |
| `targeted_review_history[].previous_affiliation_review.relationship` | string | Documented relationship between the enclosing entities, preserving affiliation, scope and timing qualifications. This occurrence is historical and must be interpreted within its enclosing revision. |
| `targeted_review_history[].previous_affiliation_review.review_date` | string | Date of the review operation described in the enclosing object. This occurrence is historical and must be interpreted within its enclosing revision. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `targeted_review_history[].previous_affiliation_review.source_url` | string | Public URL cited as supporting the enclosing statement or record. This occurrence is historical and must be interpreted within its enclosing revision. |
| `targeted_review_history[].previous_affiliation_review.status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. This occurrence is historical and must be interpreted within its enclosing revision. |
| `targeted_review_history[].previous_assessment` | object | Earlier/superseded value of assessment, preserved to document a revision rather than a current observation. |
| `targeted_review_history[].previous_assessment.event_state` | string | Documentary coding state of event. Preserve the task/phase scope and source qualifications. |
| `targeted_review_history[].previous_assessment.evidence_ids` | array; items: string | Identifiers of specific evidence items supporting the enclosing interpretation; archival ledgers may be outside this package. This occurrence is historical and must be interpreted within its enclosing revision. |
| `targeted_review_history[].previous_assessment.evidence_state` | string | State of the documentary evidence for the specific field or assessment, retaining ambiguity, missingness and structural non-applicability. This occurrence is historical and must be interpreted within its enclosing revision. |
| `targeted_review_history[].previous_assessment.full_challenge_programme_completed` | boolean | Whether the condition “full challenge programme completed” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `targeted_review_history[].previous_assessment.reason` | string | Reason for the enclosing decision, revision, exclusion or qualification. This occurrence is historical and must be interpreted within its enclosing revision. |
| `targeted_review_history[].previous_assessment.value` | string | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. This occurrence is historical and must be interpreted within its enclosing revision. |
| `targeted_review_history[].previous_record_backup` | string | Earlier/superseded value of record backup, preserved to document a revision rather than a current observation. |
| `targeted_review_history[].previous_relationship` | object | Earlier/superseded value of relationship, preserved to document a revision rather than a current observation. |
| `targeted_review_history[].previous_relationship.conference_assignment` | string | Decision assigning the edition to a conference group, with supporting scope and qualifications. This occurrence is historical and must be interpreted within its enclosing revision. |
| `targeted_review_history[].previous_relationship.current_inventory_year` | integer | Calendar year assigned to current inventory; preserve whether this concerns an edition, analysis, event or publication. |
| `targeted_review_history[].previous_relationship.existing_record` | string | Source-recorded existing record for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `targeted_review_history[].previous_relationship.note_zh` | string | Chinese-language qualification or explanation for the enclosing review decision. This occurrence is historical and must be interpreted within its enclosing revision. |
| `targeted_review_history[].previous_relationship.relationship` | string | Documented relationship between the enclosing entities, preserving affiliation, scope and timing qualifications. This occurrence is historical and must be interpreted within its enclosing revision. |
| `targeted_review_history[].previous_relationship.source_url` | string | Public URL cited as supporting the enclosing statement or record. This occurrence is historical and must be interpreted within its enclosing revision. |
| `targeted_review_history[].previous_relationship.status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. This occurrence is historical and must be interpreted within its enclosing revision. |
| `targeted_review_history[].previous_schedule` | object | Earlier/superseded value of schedule, preserved to document a revision rather than a current observation. |
| `targeted_review_history[].previous_schedule.challenge_event` | string | Source-recorded challenge event for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `targeted_review_history[].previous_schedule.evaluation_setup_end` | string | Source-recorded evaluation setup end for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `targeted_review_history[].previous_schedule.evaluation_setup_start` | string | Source-recorded evaluation setup start for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `targeted_review_history[].previous_schedule.model_submission_end` | string | Source-recorded model submission end for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `targeted_review_history[].previous_schedule.registration_end` | string | Source-recorded registration end for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `targeted_review_history[].previous_schedule.testing_end` | string | Source-recorded testing end for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `targeted_review_history[].previous_schedule.testing_start` | string | Source-recorded testing start for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `targeted_review_history[].previous_sha256` | string | Earlier/superseded value of sha256, preserved to document a revision rather than a current observation. |
| `targeted_review_history[].primary_task` | string | Principal task description in the enclosing source or review; not necessarily all task families. |
| `targeted_review_history[].published_evaluation_protocol` | string | Source-recorded published evaluation protocol for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `targeted_review_history[].published_participant_result` | string | Source-recorded published participant result for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `targeted_review_history[].qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `targeted_review_history[].quoted_instruction` | string | Source instruction retained verbatim to document the applicable rule or interface. |
| `targeted_review_history[].report_generation` | boolean | Task/objective flag for generating image-grounded free-text reports or captions; structured field prediction is separate. |
| `targeted_review_history[].result` | string | Reported finding, score, placement or scoped outcome description associated with the enclosing evidence item. |
| `targeted_review_history[].retain_declared_caption_generation_objective` | boolean | Whether the condition “retain declared caption generation objective” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `targeted_review_history[].retain_edition` | boolean | Whether the condition “retain edition” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `targeted_review_history[].review_record` | string | Identifier/path of the corresponding review entry or ledger; it may refer to an unbundled archive. |
| `targeted_review_history[].reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `targeted_review_history[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `targeted_review_history[].sha256` | string | Cryptographic checksum or revision identifier for the enclosing sha256; used for provenance rather than as a scientific measurement. |
| `targeted_review_history[].source_file` | string | Identifier or path of the source file in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `targeted_review_history[].source_material` | string | Identifier or path of the source material in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `targeted_review_history[].source_snapshot` | string | Identifier or path of the source snapshot in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `targeted_review_history[].source_type` | string | Kind of data or evidence source. In dataset records this describes cohort origin; in provenance it describes the supporting document or confirmation. |
| `targeted_review_history[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `targeted_review_history[].source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `targeted_review_history[].status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `targeted_review_history[].summary` | string | Concise summary of the enclosing source, review or observation. |
| `targeted_review_history[].supersedes` | string | Earlier statement or record that the enclosing revision replaces. |
| `targeted_review_history[].user_confirmation_scope` | string | Task, phase, cohort or source boundaries of user confirmation. |
| `targeted_review_history[].user_material` | null / string | Source-recorded user material for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `targeted_review_history[].verification_limit` | string | Specific limit on what was verified from the available source. |
| `targeted_review_history[].vision_language_model_adaptation_track` | boolean | Whether the condition “vision language model adaptation track” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `targeted_review_history[].visual_question_answering` | boolean | Task flag for answering questions using image or video content together with language. |
| `unresolved_fields` | array; items: string | Fields or interpretive questions not resolved by the documented review. |
| `verification_policy` | string | Permission, restriction or procedural rule governing verification. |

<a id="record-field-review"></a>

## `record_field_review`

JSON parent path: `challenge.record_field_review`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.record_field_review`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `fields` | object | Named variables examined in the enclosing review; child keys identify the individual coding domains. |
| `fields.centers` | object | Structured entries for centers within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fields.centers.evidence_path` | string | Source-recorded evidence path for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `fields.centers.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `fields.centers.section` | string | Section, figure, table or location within a supporting source. |
| `fields.centers.source_urls` | string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `fields.centers.state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. |
| `fields.centers.value` | string | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.final_inference` | object | Structured entries for final inference within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fields.final_inference.coding_basis` | string | Evidence or reasoning supporting coding. |
| `fields.final_inference.completed_execution_claim` | string | Source-recorded completed execution claim for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `fields.final_inference.evidence_excerpt` | string | Source passage retained as support for the enclosing classification or observation. |
| `fields.final_inference.evidence_path` | string | Source-recorded evidence path for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `fields.final_inference.evidence_scope` | string | Boundary of what the supporting evidence establishes, including specification versus actual execution. |
| `fields.final_inference.final_inference_execution` | string | Executor of the designated final scored stage: participant-side, organizer/platform-side, track-dependent, or not established. |
| `fields.final_inference.final_stage` | string | Source-recorded final stage for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `fields.final_inference.rationale` | string | Explanation of how the supporting evidence leads to the recorded classification or decision. |
| `fields.final_inference.review_date` | string | Date of the review operation described in the enclosing object. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `fields.final_inference.source_section` | string | Section or location within the supporting source. |
| `fields.final_inference.source_urls` | string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `fields.geography` | object | Explicit acquisition geography or identifiable source locations, retaining partial coverage and plans. |
| `fields.geography.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `fields.geography.evidence` | array; items: object | Source-linked observations supporting the enclosing variable or assessment; preserve type, scope and date. |
| `fields.geography.evidence[].kind` | string | Type of observation or evidence item used in the enclosing review. |
| `fields.geography.evidence[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `fields.geography.evidence[].section` | string | Section, figure, table or location within a supporting source. |
| `fields.geography.evidence[].source_path` | string | Path of the original source or evidence record; archive paths may refer to files not included in this package. |
| `fields.geography.evidence[].url` | string | Web address of the enclosing source, document or resource. |
| `fields.geography.evidence[].value` | string / object | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.geography.evidence[].value.country` | string | Country of the enclosing event or acquisition source; organizer country must not be substituted for dataset geography. |
| `fields.geography.evidence[].value.named_acquisition_site` | string | Institution or location explicitly identified as a data-acquisition source, not inferred from author affiliation. |
| `fields.geography.evidence[].value.named_site` | string | Acquisition/source site explicitly named by the supporting document. |
| `fields.geography.evidence[].value.real_EndoMapper_source` | string | Source supporting real Endo Mapper. |
| `fields.geography.evidence[].value.subset` | string | Subset of the source dataset or analysis population to which the enclosing observation applies. |
| `fields.geography.evidence[].value.synthetic_anatomy_CT_source` | string | Source supporting synthetic anatomy CT. |
| `fields.geography.source_urls` | string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `fields.geography.state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. |
| `fields.post_challenge_resources` | object | Continuing data, code or evaluation resources, policies or plans identified for the edition; these evidence types remain distinct. |
| `fields.post_challenge_resources.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `fields.post_challenge_resources.evidence` | array; items: object | Source-linked observations supporting the enclosing variable or assessment; preserve type, scope and date. |
| `fields.post_challenge_resources.evidence[].kind` | string | Type of observation or evidence item used in the enclosing review. |
| `fields.post_challenge_resources.evidence[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `fields.post_challenge_resources.evidence[].section` | string | Section, figure, table or location within a supporting source. |
| `fields.post_challenge_resources.evidence[].source_path` | string | Path of the original source or evidence record; archive paths may refer to files not included in this package. |
| `fields.post_challenge_resources.evidence[].url` | string | Web address of the enclosing source, document or resource. |
| `fields.post_challenge_resources.evidence[].value` | object | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.post_challenge_resources.evidence[].value.code` | string | Code/software artifact, repository reference or source-defined code value identified by the enclosing record. |
| `fields.post_challenge_resources.evidence[].value.dataset` | string | Source cohorts, quantities, splits, acquisition conditions and associated data characteristics. |
| `fields.post_challenge_resources.evidence[].value.dataset_and_submission_service` | string | Source-recorded dataset and submission service for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `fields.post_challenge_resources.evidence[].value.participant_code` | array; items: string | Structured entries for participant code within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fields.post_challenge_resources.evidence[].value.post_challenge_activity` | string | Source-recorded post challenge activity for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `fields.post_challenge_resources.evidence[].value.post_challenge_deadline` | string | Source-recorded post challenge deadline for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `fields.post_challenge_resources.evidence[].value.release_date` | string | Date associated with release. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `fields.post_challenge_resources.evidence[].value.released` | string | Source-recorded released for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `fields.post_challenge_resources.evidence[].value.released_data` | string | Source-recorded released data for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `fields.post_challenge_resources.evidence[].value.released_resources` | string | Source-recorded released resources for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `fields.post_challenge_resources.evidence[].value.resources` | string | Source-recorded resources for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `fields.post_challenge_resources.evidence[].value.software_integration` | string | Source-recorded software integration for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `fields.post_challenge_resources.evidence[].value.team_model_weights` | string | Source-recorded team model weights for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `fields.post_challenge_resources.evidence[].value.test_data` | string | Input data provided or withheld for the stated testing stage. |
| `fields.post_challenge_resources.evidence[].value.test_ground_truth` | string | Reference labels/targets used to score test predictions, including any access restriction. |
| `fields.post_challenge_resources.evidence[].value.training_data` | string | Data supplied or allowed for the stated model-development stage. |
| `fields.post_challenge_resources.source_urls` | string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `fields.post_challenge_resources.state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. |
| `fields.reported_participation` | object | Reported team/person participation observations with original units and task/phase scope. |
| `fields.reported_participation.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `fields.reported_participation.evidence` | array; items: object | Source-linked observations supporting the enclosing variable or assessment; preserve type, scope and date. |
| `fields.reported_participation.evidence[].kind` | string | Type of observation or evidence item used in the enclosing review. |
| `fields.reported_participation.evidence[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `fields.reported_participation.evidence[].section` | string | Section, figure, table or location within a supporting source. |
| `fields.reported_participation.evidence[].source_path` | string | Path of the original source or evidence record; archive paths may refer to files not included in this package. |
| `fields.reported_participation.evidence[].url` | string | Web address of the enclosing source, document or resource. |
| `fields.reported_participation.evidence[].value` | object | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.reported_participation.evidence[].value.additional_failed_test_teams` | integer | Number of additional failed test teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.final_IQA_teams` | integer | Number of final IQA teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.final_RCS_teams` | integer | Number of final RCS teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.final_submitting_teams` | integer | Number of final submitting teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.late_valid_teams` | integer | Number of late valid teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.named_ranked_team_entries` | integer | Number of named ranked team entries in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.participating_teams` | integer | Number of participating teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.phase1_teams` | integer | Number of phase1 teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.phase2_teams` | integer | Number of phase2 teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.phase3_finalists` | integer | Reported numerical value for phase3 finalists within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `fields.reported_participation.evidence[].value.preliminary_submitting_teams` | integer | Number of preliminary submitting teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.submissions` | integer | Submission-count information grouped by phase, task or platform scope. |
| `fields.reported_participation.evidence[].value.successful_test_teams` | integer | Number of successful test teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.task1_listed_teams` | integer | Number of task1 listed teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.task1_ranked_offline_teams` | integer | Number of task1 ranked offline teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.task1_teams` | integer | Number of task1 teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.task1_validation_teams` | integer | Number of task1 validation teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.task2_listed_teams` | integer | Number of task2 listed teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.task2_methods_in_report` | integer | Reported numerical value for task2 methods in report within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `fields.reported_participation.evidence[].value.task2_teams` | integer | Number of task2 teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.task2_validation_teams` | integer | Number of task2 validation teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.task3_teams` | integer | Number of task3 teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.teams_contributing_source_code` | integer | Number of teams contributing source code in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.teams_progressing_beyond_validation` | integer | Number of teams progressing beyond validation in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.valid_teams_before_deadline` | integer | Number of valid teams before deadline in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.evidence[].value.validation_teams` | integer | Number of validation teams in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `fields.reported_participation.source_urls` | string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `fields.reported_participation.state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. |
| `fields.typed_size` | object | Dataset quantity interpreted together with its explicit unit, split and source scope. |
| `fields.typed_size.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `fields.typed_size.source_refs` | array; items: object | Structured entries for source refs within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `fields.typed_size.source_refs[].local_snapshot` | string | Original local archive identifier/path for a captured source; the referenced archive file is not bundled here. |
| `fields.typed_size.source_refs[].retrieved_on` | string | Date when the cited source was retrieved or captured. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `fields.typed_size.source_refs[].section` | string | Section, figure, table or location within a supporting source. |
| `fields.typed_size.source_refs[].supports` | array; items: string | Statements or fields that the source is recorded as supporting, limited by the source's actual task, phase and evidence scope. |
| `fields.typed_size.source_refs[].type` | string | Type of the enclosing source, document, artifact, observation or event; its vocabulary is specific to that parent context. |
| `fields.typed_size.source_refs[].url` | string | Web address of the enclosing source, document or resource. |
| `fields.typed_size.source_urls` | string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `fields.typed_size.state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. |
| `fields.typed_size.value` | array; items: object | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `fields.typed_size.value[].approximate` | boolean | Whether the enclosing quantity is approximate rather than exact. |
| `fields.typed_size.value[].canonical_field` | string | Field in the canonical challenge record to which the enclosing evidence or review decision applies. |
| `fields.typed_size.value[].evidence_path` | string | Source-recorded evidence path for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `fields.typed_size.value[].lower_bound` | boolean | A lower-bound qualifier when Boolean, or the numerical lower bound when numeric; use the stored type and source wording. |
| `fields.typed_size.value[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `fields.typed_size.value[].split` | string | Dataset partition to which the enclosing quantity, observation or result applies. |
| `fields.typed_size.value[].unit` | string | Unit of the enclosing quantity or measure as recorded by the source. |
| `fields.typed_size.value[].value` | integer | Recorded value of the enclosing measure or decision; its meaning and unit are defined by the parent field and scope. |
| `method` | string | Method or procedure used for the enclosing evaluation, extraction or analysis; preserve whether organizer-defined or reviewer-applied. |
| `review_date` | string | Date of the review operation described in the enclosing object. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |

[Back to README](../../README.md#variable-dictionary)
