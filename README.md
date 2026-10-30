# Medical Imaging Challenge Metadata, 2022–2026

[中文说明](README_zh.md)

Structured metadata for a landscape review of medical and biomedical imaging challenges. Records describe competition objectives, imaging tasks, clinical context, datasets, access conditions, submission and evaluation procedures, and documentary evidence.

The analytical subset contains **337 challenge editions** from 2022–2026. This repository also preserves 15 records excluded from that subset and one legacy ACROBAT record, with their status made explicit in the index. It accompanies *Medical Imaging Challenges in the Foundation-Model Era: A Landscape Review of Emerging Paradigms and Future Directions*.

**Package snapshot: 30 October 2026.** This is the packaging date, not a new verification date for every source. Collection and review dates remain in individual records. This is a non-exhaustive landscape collection, not a census of all medical imaging competitions.

## Coverage and analytical units

| Record group | Number | Location | Use in the review |
| --- | ---: | --- | --- |
| Included annual editions | 337 | `data/challenges/` | Primary analysis |
| Excluded records in the current manifest | 15 | `data/excluded/` | Selection transparency; exclude from primary totals |
| Legacy ACROBAT 2023 record | 1 | `data/legacy/` | Historical context only; outside the current manifest |
| All individual challenge JSON files | **353** | All three directories | Filter by `analysis_include` before analysis |

The current manifest contains **352 dated records = 337 included + 15 excluded**. The legacy record is additional and must not be counted as another included edition. The manuscript's earlier screening ledger and undated contextual record describe a different stage of selection; this package is not a copy of all 383 screening entries.

| Edition year | 2022 | 2023 | 2024 | 2025 | 2026 | Total |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| Included editions | 57 | 68 | 76 | 67 | 69 | **337** |

An analytical unit is a challenge edition. Repeated annual editions can contribute separate units. Parent competitions and their separately represented constituent challenges are not counted twice. Task families are multi-label **edition-level** counts: an edition contributes once to each applicable family even if several tracks use that output. Track-level descriptions remain in `task_profile.tasks`.

The included set contains 61 editions with at least one emerging AI objective and 93 edition–objective label assignments. The six overlapping labels are:

| Label in the analytical inventory | Editions |
| --- | ---: |
| `Foundation models` | 30 |
| `VLM` | 36 |
| `Report generation` | 17 |
| `Text-conditioned image generation` | 4 |
| `Clinical Reasoning` | 4 |
| `Agent` | 2 |

These labels describe organizer-defined objectives. They do not establish that every associated assessment was executed or that the intended capability was demonstrated.

Data entry points: [record index](data/index.json) for inclusion status and file paths; [analytical inventory](data/analysis_inventory.json) for the 337 included editions. Use the framework mappings and variable dictionary below to interpret the fields.

## Analytical frameworks and supporting variables

The review uses two linked frameworks: the **six collection-wide dimensions in manuscript Table 1** describe all **337 included editions**, and the **seven capability-assessment fields** examine **61 editions with emerging AI objectives**, retaining **93 edition–objective records**. The six dimensions include an *Emerging AI objectives* dimension, whose six overlapping objective labels are listed above. The seven assessment fields apply to the full emerging-objective subset, including vision–language and reasoning objectives, rather than only the thirty foundation-model-oriented editions.

The tables below map the manuscript's concepts to variables used to examine them. **`I.` means a row of `data/analysis_inventory.json`; `C.` means the `challenge` object inside an individual JSON.** These are shorthand prefixes for this documentation. A group name identifies its nested variables as well; `[]` denotes an array item. The mapping identifies supporting fields and their interpretation, not a requirement that every field be populated in every edition. Source records, review decisions and harmonized analytical categories retain their distinct roles.

### Six collection-wide analytical dimensions

| Dimension in Table 1 | Variables examined | Documentary basis and interpretation |
| --- | --- | --- |
| **1. Challenge identity** | `I.edition_id`, `I.year`, `I.conference`, `I.conference_group`, `I.evaluation_host`, `I.host_group`; `C.challenge_id`, `C.challenge_name`, `C.event.series`, `C.event.year`, `C.event.conference`, `C.parent_challenge_id`, `C.record_relationships`, `C.edition_identity_review`, `C.conference_affiliation_review`. | Official programmes and edition websites establish edition identity and affiliation; source-linked identity decisions resolve parent/track overlap and later publications. The current index establishes inclusion. Submission/evaluation service is distinct from conference affiliation and inference execution. [Identity fields](docs/variables/identity-event.md); [edition decisions](docs/variables/edition-decisions.md). |
| **2. Scientific tasks and clinical scope** | `I.harmonized_task_families`, `I.harmonized_modalities`; `C.task_profile.tasks[].task_id`, `C.task_profile.tasks[].input`, `C.task_profile.tasks[].output`, `C.task_profile.tasks[].role`, `C.task_profile.tasks[].granularity`, `C.task_profile.tasks[].clinical_goal`; `C.clinical_domain.modality`, `C.clinical_domain.organs_or_structures`, `C.clinical_domain.body_region`, `C.clinical_domain.diseases`, `C.clinical_domain.disease_evidence_scope`, `C.clinical_classification_review`. | Task descriptions, rules and challenge reports identify required outputs, acquisition modalities and explicitly stated anatomical/disease scope. Count an edition once per applicable task family, including evaluated downstream transfer tasks. Preserve participant, auxiliary and evaluator-only roles; anatomy alone does not establish a disease diagnosis. [Task fields](docs/variables/tasks-objectives.md); [clinical fields](docs/variables/clinical-scope.md). |
| **3. Emerging AI objectives** | `I.emerging_objectives`; `C.task_objective_review.emerging_objectives`, `C.task_objective_review.foundation_model_basis`, `C.task_objective_review.sources`, `C.review_coding.emerging_objectives`, `C.review_coding.task_objective_basis`, `C.review_coding.stage_specific_objectives`, `C.task_profile.tasks[].input`, `C.task_profile.tasks[].output`. | Organizer-defined aims, registered objectives, track rules and assessment reports support the six overlapping labels. Match each label to its task and input/output requirements. A participant's model choice alone does not establish an organizer-defined foundation-model objective; a label does not establish assessed or achieved capability. [Objective definitions](docs/variables/analysis-inventory.md#emerging-objective-label-definitions); [source-level coding](docs/variables/tasks-objectives.md). |
| **4. Data and reference conditions** | `I.development_access`, `I.source_centers`, `I.source_geography_documented`, `I.terms_documented`; `C.dataset.population`, `C.dataset.quantity_unit`, `C.dataset.reported_quantities`, `C.dataset.splits`, `C.dataset.source_datasets`, `C.dataset.center_count`, `C.dataset.independence_note`; `C.labels_and_targets.annotation_source`, `C.data_access`, `C.data_license_review`, `C.resource_characteristics_review.fields.typed_size`, `C.resource_information_review.fields.geography`. | Dataset descriptions, access terms, validation and annotation documentation establish quantities, split scope, acquisition sources, access and reference information. Retain original units and distinguish multicenter acquisition from independent testing. Annotation/adjudication details, where available, provide context; they were **not systematically coded across all editions or included in the quantitative synthesis**. [Dataset fields](docs/variables/dataset.md); [reference labels](docs/variables/labels-targets.md); [access and licences](docs/variables/data-access.md). |
| **5. Competition and evaluation protocols** | `I.submission_mechanisms`, `I.final_inference_execution`, `I.final_inference_evidence_scope`; `C.submission.submission_type`, `C.submission.phase_specific_requirements`, `C.submission.runtime_limits`, `C.data_usage_mode.testing`, `C.data_usage_mode.external_data`, `C.resource_protocol_review`, `C.evaluation.tasks[].metrics`, `C.evaluation.tasks[].ranking`, `C.evaluation.metrics[].role`, `C.evaluation.metrics[].weight`, `C.evaluation.phase_execution_evidence`. | Rules, platform records, reports and confirmations establish artifacts, the final scored stage, resource constraints, scoring and ranking. Separate submission service, model executor and scoring executor; retain task/phase scope and distinguish a stated limit from evidence of enforcement. A reported metric need not contribute to ranking. [Submission fields](docs/variables/submission.md); [execution arrangements](docs/variables/data-execution.md); [evaluation fields](docs/variables/evaluation.md). |
| **6. Outcomes and post-challenge availability** | `I.completion_status`, `I.completion_basis`, `I.reported_participation_documented`, `I.post_challenge_resources_documented`; `C.assessment_evidence`, `C.evaluation.tasks[].competition_outcome`, `C.participation_statistics`, `C.publication`, `C.resource_information_review.fields.reported_participation`, `C.resource_information_review.fields.post_challenge_resources`. | Reports, awards, confirmations and archived resources establish conduct, scoped outcomes, participation, publications and continuing resources. Registrations and submission attempts do not establish active-team counts. Planned releases, access policies and observed availability remain distinct; edition completion does not establish every assessment's execution. [Participation/resources](docs/variables/participation-resources.md); [publications](docs/variables/publications.md); [outcome evidence](docs/variables/assessment-evidence.md). |

The dedicated resource-policy analysis of thirty foundation-model-oriented editions adds a separate coding matrix for checkpoints, common initialization, external data, adaptation, supervision budgets, time and GPU constraints (Supplementary Methods SM8). Those policy variables are distinct from the seven capability-assessment fields below; the complete policy matrix is not distributed in this JSON package.

### Seven capability-assessment fields

These fields follow the manuscript's *Emerging AI objectives and assessment evidence* methods and Supplementary Methods SM7. They connect an intended capability to an assessment and its supporting evidence. They are **analytical fields synthesized across sources**, not seven standardized keys present in every challenge JSON. The JSON paths below identify relevant source-level information; the separate focused-analysis ledgers supply the reconciled objective/component states.

| Assessment field | Variables examined in this package | Evidence needed for the assessment interpretation |
| --- | --- | --- |
| **1. Intended capability** | `I.emerging_objectives`; `C.task_objective_review.emerging_objectives`, `C.task_objective_review.foundation_model_basis`, `C.review_coding.task_objective_basis`, `C.task_profile.tasks[].clinical_goal`, `C.task_profile.tasks[].input`, `C.task_profile.tasks[].output`. | An organizer-stated capability aim linked to an identifiable task, such as representation transfer, image-grounded generation or evidence-linked reasoning. Retain each applicable objective separately within an edition. [Task/objective variables](docs/variables/tasks-objectives.md). |
| **2. Assessment endpoint** | `C.task_profile.tasks[].task_id`, `C.task_profile.tasks[].output`, `C.task_profile.tasks[].endpoint_scope`, `C.evaluation.tasks[].metrics`, `C.evaluation.tasks[].design_status`, `C.evaluation.metrics[].name`, `C.evaluation.metrics[].task`, `C.evaluation.tasks[].ranking`. | A specified output, metric or evaluation procedure tied to that capability and its task/phase. Organizer rules, task descriptions and evaluation code can establish specification without a released score. A parsing or VQA score does not establish assessment of a separately proposed generation or explanation task. [Evaluation variables](docs/variables/evaluation.md). |
| **3. Evidence grounding** | `C.task_profile.tasks[].output`, `C.labels_and_targets.target_entity`, `C.labels_and_targets.annotation_source`, `C.evaluation.tasks[].metrics`, `C.evaluation.metrics[].name`, `C.evaluation.tasks[].evidence_scope`, `C.assessment_evidence`. | Evaluation of the relation between outputs and images, regions or retrieved evidence, established from task/metric descriptions and component results. The metric name alone is insufficient; generic answer accuracy or text similarity does not establish grounding. For example, [REG2's JSON](data/challenges/MICCAI/2026/reg2-2026.json) records a specified visual-grounding metric in `evaluation.tasks[].metrics`; that design field alone does not establish execution. [Targets](docs/variables/labels-targets.md); [assessment evidence](docs/variables/assessment-evidence.md). |
| **4. Clinical assessment** | `C.evaluation.tasks[].metrics`, `C.evaluation.additional_assessments`, `C.evaluation.additional_assessments.expert_radiologist_assessment.declared`, `C.evaluation.additional_assessments.expert_radiologist_assessment.performed`, `C.evaluation.additional_assessments.expert_radiologist_assessment.execution_status`, `C.assessment_evidence`. | Distinguish **human clinical expert assessment of model outputs** from **clinical content/error assessment**, which can be automated. Reviewer qualifications, the assessed outputs, clinical concepts/errors and reported findings establish the scope. Clinician-created reference annotations and LLM judges do not establish human expert output assessment. The expert-radiologist path is an edition-specific example, not a universal field. [Assessment variables](docs/variables/assessment-evidence.md); [additional assessments](docs/variables/evaluation.md). |
| **5. Generalization testing** | `C.dataset.source_datasets`, `C.dataset.downstream_datasets`, `C.dataset.splits`, `C.dataset.center_scope`, `C.dataset.independence_note`, `C.evaluation.additional_assessments.boston_external_testing.declared`, `C.evaluation.additional_assessments.boston_external_testing.performed`, `C.evaluation.additional_assessments.boston_external_testing.execution_status`, `C.assessment_evidence`. | Specify what transfers and which data, sites or domains are withheld from development. The descriptive field includes cross-task transfer and held-out samples; the Figure 7 independent-site/out-of-domain count requires explicit separation from development sources. Multicenter collection or a hidden test set alone is insufficient. The Boston path is a VLM3D-specific example and retains edition/year scope. [Dataset variables](docs/variables/dataset.md); [evaluation variables](docs/variables/evaluation.md). |
| **6. Execution evidence** | `C.assessment_evidence.execution_evidence[].task_id`, `C.assessment_evidence.execution_evidence[].phase`, `C.assessment_evidence.execution_evidence[].status`, `C.assessment_evidence.execution_evidence[].scope`, `C.assessment_evidence.execution_evidence[].source_url`, `C.evaluation.phase_execution_evidence`, `C.evaluation.final_assessment_evidence`. | Organizer or participant accounts, assessment records or explicit confirmations that the **same specified assessment** was performed. Preserve task/phase, qualifications and explicit non-implementation. Neither `I.completion_status` nor a protocol-only `I.final_inference_execution` classification establishes component execution. [Execution/outcome evidence](docs/variables/assessment-evidence.md). |
| **7. Outcome evidence** | `C.assessment_evidence.outcome_evidence`, `C.assessment_evidence.track_results`, `C.assessment_evidence.award_outcomes`, `C.evaluation.tasks[].competition_outcome`, `C.evaluation.tasks[].outcome_evidence_ids`, `C.evaluation.tasks[].qualification`. | Scores, analytical findings, placements, task awards or directly confirmed results linked to the assessment. A combined score can support an explicitly included component without isolating its contribution. Detailed public component results are recorded separately; a paper in preparation or bare event-completion statement is insufficient. [Outcome variables](docs/variables/assessment-evidence.md); [task-level evaluation](docs/variables/evaluation.md). |

### Focused-analysis ledger fields and package coverage

The following files are in the **separate capability-evidence audit**, not in this metadata ZIP. Their names and columns are listed to make the manuscript-to-variable mapping explicit. A missing or empty `C.assessment_evidence` object in an individual JSON does not establish that the focused review found no evidence: that review also used the separate source catalog and ledgers. The exported JSON files alone do not reproduce the complete component-specific evidence counts in Figure 7.

| Audit file and unit | Fields supporting the seven-item framework |
| --- | --- |
| `edition_evidence.csv` — 61 edition rows | `edition_id`, `year`, `objectives`, `intended_capability` document the intended capability; `evidence_scope`, `source_ids`, `review_date` and `review_method` preserve the interpretation and provenance. |
| `objective_evidence.csv` — 93 edition–objective rows | `edition_id` and `objective` identify the linkage; `endpoint_state` and `specified` record assessment specification; `execution_state` and `executed` record execution; `outcome_state` and `outcome_information` record outcomes. `detailed_public_result_state`, `detailed_public_results`, `outcome_information_scope`, `scope` and `source_ids` preserve the narrower results category and evidence boundaries. |
| `component_evidence.csv` — 305 edition–component rows | `assessment_component` identifies objective-linked assessment, grounding, human clinical expert assessment, clinical content/error assessment or independent-site/out-of-domain testing. `specification_state`/`specification_finding`, `execution_state`/`execution_finding` and `outcome_state`/`outcome_finding` record the separate evidence stages. `counted_specified`, `counted_executed`, `counted_outcome_information` and `counted_detailed_public_results` are aggregation flags. `detailed_public_result_state`, `outcome_information_type`, `outcome_information_scope`, `assessment_scope_and_rationale`, `source_ids`, `source_urls` and `review_date` preserve interpretation and source support. |

The **305 rows = 61 editions × five assessment components** are documentary review records, not 305 executed assessments. The seven analytical fields yield five coverage rows in Figure 7: intended capability links the objective to its endpoint; clinical assessment separates into expert review and clinical content/error; execution and outcome evidence become separate stages for every component. Counts require a specified assessment and subsequent evidence for that same assessment, count each edition at most once per component, and do not establish complete coverage of every objective. The four documentary states are documented/classifiable, ambiguous, not established and not applicable; an explicit report of non-implementation is distinguished from missing evidence. These states are not an ordinal quality scale or a checklist required of every competition.

### Tracing a variable to its evidence

For either framework, follow the edition identifier from the index to its individual record, then examine `C.provenance.field_evidence`, `C.provenance.sources[].url`, `C.provenance.sources[].type`, `C.provenance.sources[].supports`, `C.provenance.sources[].reviewed_on` and `C.provenance.sources[].qualification`, together with the relevant task/phase-specific sources and review rationale. `I.source_urls` supplies a compact source list. These fields identify what a source supports and the limits of that support; their presence alone does not establish verification or execution. See the [source and provenance definitions](docs/variables/sources-provenance.md).

For example, [VLM3D 2026](data/challenges/MICCAI/2026/vlm3d-2026.json) retains track-specific outcomes in `assessment_evidence.track_results` while the separate Boston external test and radiologist assessment retain unresolved execution in `evaluation.additional_assessments`. Read these with their edition and review dates. A confirmed track result cannot be transferred automatically to another component, phase or edition, nor does an assessed component necessarily contribute to the final ranking.

## Variable dictionary

Variable definitions are grouped into separate files. Click a group below to view its fields, observed types, meanings and scope. Each page identifies the JSON parent path and links back here. Start with [dictionary conventions](docs/variables/conventions.md) for array paths, units and missing-value interpretation.

The [complete field CSV](docs/field_catalog.csv) also provides all **4,595 observed named property paths** across the records, index, analytical inventory and packaging-review metadata, including definitions, types, units/formats, examples and record-presence counts. These are nested property paths, not 4,595 independent analytical variables. Shared notes and collection-template fields have their own documentation below.

### Individual challenge JSON variables

| Group | Contents |
| --- | --- |
| [Record identity, events and organizers](docs/variables/identity-event.md) | Record wrapper, challenge identity, event affiliations, organizers and related records. |
| [Clinical scope and imaging modalities](docs/variables/clinical-scope.md) | Anatomy, disease context, acquisition modalities and their harmonized classifications. |
| [Tasks, outputs and emerging AI objectives](docs/variables/tasks-objectives.md) | Tasks and tracks, participant outputs, task-family coding and organizer-defined objectives. |
| [Labels, targets and reference annotations](docs/variables/labels-targets.md) | Target definitions, label mappings and reference-annotation procedures. |
| [Datasets, cohorts and quantities](docs/variables/dataset.md) | Population, splits, acquisition settings, sites, counts and their original units. |
| [Data access, licences and permissions](docs/variables/data-access.md) | Access requirements, release conditions, data licences and reuse permissions. |
| [Data flow and execution arrangements](docs/variables/data-execution.md) | Data/model exchange, inference execution and phase-specific access protocols. |
| [Evaluation, metrics, rankings and results](docs/variables/evaluation.md) | Scoring procedures, metrics, ranking rules and source-scoped result evidence. |
| [Capability-assessment evidence](docs/variables/assessment-evidence.md) | Assessment specification, execution, outcomes, grounding, clinical assessment and transfer scope. |
| [Submissions and execution constraints](docs/variables/submission.md) | Artifacts, platforms, final-stage execution, runtime, memory and submission limits. |
| [Schedule and competition phases](docs/variables/schedule.md) | Phase dates, deadlines, revisions, date sources and timezone qualifications. |
| [Publications and participant-method evidence](docs/variables/publications.md) | Related papers, publication status, literature leads and participant-method sources. |
| [Participation and continuing resources](docs/variables/participation-resources.md) | Registrations, teams, submissions, source geography and post-challenge resources. |
| [Sources, provenance and field review](docs/variables/sources-provenance.md) | URLs, evidence records, review dates, field-level support and original archive references. |
| [Edition identity and analytical inclusion](docs/variables/edition-decisions.md) | Edition-level reconciliation, conference affiliation, eligibility and inclusion decisions. |
| [Historical coding and protocol revisions](docs/variables/history.md) | Superseded classifications, earlier protocols and historical submission arrangements. |

### Index, analysis and documentation variables

| Group | Contents |
| --- | --- |
| [Paths, types, units and missing values](docs/variables/conventions.md) | How to read all field definitions. |
| [Record index](docs/variables/index.md) | Inclusion flags, edition identifiers, file paths and checksums. |
| [Analytical inventory](docs/variables/analysis-inventory.md) | Harmonized variables for the 337 included editions and emerging-objective labels. |
| [Shared notes](docs/variables/shared-notes.md) | Definitions of the CN01–CN07 identifiers. |
| [Collection template](docs/variables/collection-template.md) | Original template metadata, instructions and candidate-label fields. |
| [Packaging review](docs/variables/packaging-review.md) | Per-record cleanup variables and audit-summary fields. |

## Sources and citation

Each record links to organizer documentation and related publications, with source dates and review history recorded in the [provenance fields](docs/variables/sources-provenance.md).

Please cite the relevant original sources when using individual records, and the accompanying review when using the collection or its analytical categories. Corrections are welcome; include the edition identifier, field, proposed update and supporting source.
