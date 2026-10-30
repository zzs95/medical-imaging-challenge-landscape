# Analytical-inventory variables

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

These variables occur in `data/analysis_inventory.json`. Use this harmonized export to reproduce the review's descriptive category counts.

| Variable | Observed type | Definition |
| --- | --- | --- |
| `active_submitting_teams_documented` | boolean | Whether a comparable active/submitting-team count met the earlier narrow criterion; distinct from broader reported participation. |
| `challenge_name` | string | Recorded short or customary name of the competition edition. |
| `clinical_extraction_status` | string | Scope or completion status of clinical-context extraction, not a measure of clinical validation. |
| `completion_basis` | string | Type of evidence supporting the edition-level record: public documentary evidence, human confirmation, or an edition-specific programme/protocol. |
| `completion_status` | string | Recorded edition-level conduct or completion status; does not establish execution of every proposed assessment. |
| `conference` | string | Named conference affiliation. Raw records preserve source wording; the analytical inventory contains the harmonized assignment. |
| `conference_group` | string | Broad conference-affiliation group used for the descriptive analysis. |
| `development_access` | string | Classification of competition-time development-data access, preserving public download, registration, individual authorization and unresolved states. |
| `edition_id` | string | Identifier of the analytical edition used to join the index, inventory and individual record. |
| `emerging_objectives` | array; items: string | Overlapping organizer-defined AI objective labels. The six analytical labels are defined below; labels do not prove assessment execution. |
| `evaluation_host` | string | Service or organization recorded as hosting challenge submissions or evaluation; does not alone identify the inference executor. |
| `final_inference_evidence_scope` | string | Whether the final-inference classification is supported by a specified protocol or evidence of execution. |
| `final_inference_execution` | string | Executor of the designated final scored stage: participant-side, organizer/platform-side, track-dependent, or not established. |
| `harmonized_modalities` | array; items: string | Imaging categories harmonized for the review; multiple categories may apply, and video is a format attribute. |
| `harmonized_task_families` | array; items: string | All review-level output/task categories assigned to the edition; each edition counts once per category, regardless of the number of tracks. |
| `host_group` | string | Harmonized grouping of the evaluation-host or submission-service name. |
| `inventory_source_sha256` | string | Source checksum stored in the original analytical CSV, retained separately from the export checksum. |
| `original_edition_id` | string | Edition identifier retained before analytical naming or unit harmonization. |
| `original_sha256` | string | SHA-256 checksum of the original working JSON used to prepare this package. |
| `original_source_path` | string | Venue/year path of the original working record before export. |
| `packaged_sha256` | string | SHA-256 checksum of the exported individual JSON after conservative remark cleanup. |
| `post_challenge_resources_documented` | boolean | Whether post-challenge resource information was classifiable, including scoped policies, plans or observed provision; not proof of unrestricted availability. |
| `post_challenge_statement` | boolean | Whether an explicit post-challenge statement met the earlier narrow coding criterion; separate from the later resource-information coverage flag. |
| `record_path` | string | Relative location of the packaged individual JSON linked to the analytical row. |
| `registered_participants_documented` | boolean / string | Whether the earlier registration-count criterion was documented. The string Not yet extracted remains distinct from true and false. |
| `reported_participation_documented` | boolean | Whether a qualifying reported participation measure was available, retaining its unit, phase and scope; excludes registration-only counts and submission attempts. |
| `resource_extraction_status` | string | Scope and status of the resource-information extraction used by the analytical inventory. |
| `source_centers` | string | Harmonized acquisition-center category; this is not by itself evidence of institution-held-out evaluation. |
| `source_geography_documented` | boolean | Whether acquisition geography was classifiable under the source-scoped review, including qualified source subsets or explicit plans. |
| `source_urls` | array; items: string | One or more supporting public URLs; some legacy fields store a string instead of an array. |
| `submission_mechanisms` | array; items: string | Harmonized categories of submitted artifacts or executable submission arrangements; multiple categories can apply. |
| `terms_documented` | boolean | Whether the review found classifiable data-use or licence terms; false does not prove that no terms existed. |
| `year` | integer | Year assigned to the included annual challenge edition for the current analysis. |

### Emerging-objective label definitions

| Inventory label | Operational meaning |
| --- | --- |
| `Foundation models` | Organizer-defined objective involving large-scale pretraining, reusable representations or adaptation of pretrained/foundation models. A participant's independent choice of a pretrained model is insufficient. |
| `VLM` | Organizer-defined image–language interaction, conditioning, representation assessment or image-grounded generation. |
| `Report generation` | Image-grounded free-text reports, captions or summaries; predefined clinical-field prediction is recorded separately. |
| `Text-conditioned image generation` | Natural-language inputs guide image or volume synthesis. |
| `Clinical Reasoning` | An explicitly evaluated rationale, evidence-linked explanation or structured justification; answer accuracy alone is insufficient. |
| `Agent` | Organizer-defined tools, retrieval, interaction or state-dependent actions; routine container submission alone does not qualify. |

The labels overlap. Report/caption generation and text-conditioned image generation are also included in vision–language objectives. These classifications describe intended objectives and do not by themselves establish complete execution or demonstrated generality.

[Back to README](../../README.md#variable-dictionary)
