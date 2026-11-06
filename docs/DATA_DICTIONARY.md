# Variable dictionary index

[Back to README](../README.md#variable-dictionary)

For the manuscript-level mapping, see [the six analytical dimensions and seven capability-assessment fields](../README.md#analytical-frameworks-and-supporting-variables), including the supporting JSON variables and the scope of the separate evidence ledgers.

Definitions are organized into the following thematic files. Each file preserves complete nested field definitions within its group.

### Individual challenge JSON variables

| Group | Contents |
| --- | --- |
| [Record identity, events and organizers](variables/identity-event.md) | Record wrapper, challenge identity, event affiliations, organizers and related records. |
| [Clinical scope and imaging modalities](variables/clinical-scope.md) | Anatomy, disease context, acquisition modalities and their harmonized classifications. |
| [Tasks, outputs and emerging AI objectives](variables/tasks-objectives.md) | Tasks and tracks, participant outputs, task-family coding and organizer-defined objectives. |
| [Labels, targets and reference annotations](variables/labels-targets.md) | Target definitions, label mappings and reference-annotation procedures. |
| [Datasets, cohorts and quantities](variables/dataset.md) | Population, splits, acquisition settings, sites, counts and their original units. |
| [Data access, licences and permissions](variables/data-access.md) | Access requirements, release conditions, data licences and reuse permissions. |
| [Data flow and execution arrangements](variables/data-execution.md) | Data/model exchange, inference execution and phase-specific access protocols. |
| [Evaluation, metrics, rankings and results](variables/evaluation.md) | Scoring procedures, metrics, ranking rules and source-scoped result evidence. |
| [Capability-assessment evidence](variables/assessment-evidence.md) | Assessment specification, execution, outcomes, grounding, clinical assessment and transfer scope. |
| [Submissions and execution constraints](variables/submission.md) | Artifacts, platforms, final-stage execution, runtime, memory and submission limits. |
| [Schedule and competition phases](variables/schedule.md) | Phase dates, deadlines, revisions, date sources and timezone qualifications. |
| [Publications and participant-method evidence](variables/publications.md) | Related papers, publication status, literature leads and participant-method sources. |
| [Participation and continuing resources](variables/participation-resources.md) | Registrations, teams, submissions, source geography and post-challenge resources. |
| [Sources, provenance and field review](variables/sources-provenance.md) | URLs, evidence records, review dates, field-level support and original archive references. |
| [Edition identity and analytical inclusion](variables/edition-decisions.md) | Edition-level reconciliation, conference affiliation, eligibility and inclusion decisions. |
| [Historical coding and protocol revisions](variables/history.md) | Superseded classifications, earlier protocols and historical submission arrangements. |

### Index, analysis and documentation variables

| Group | Contents |
| --- | --- |
| [Paths, types, units and missing values](variables/conventions.md) | How to read all field definitions. |
| [Record index](variables/index.md) | Inclusion flags, edition identifiers, file paths and checksums. |
| [Analytical inventory](variables/analysis-inventory.md) | Harmonized variables for the 342 included editions and emerging-objective labels. |
| [Shared notes](variables/shared-notes.md) | Definitions of the CN01–CN07 identifiers. |
| [Collection template](variables/collection-template.md) | Original template metadata, instructions and candidate-label fields. |
| [Packaging review](variables/packaging-review.md) | Per-record cleanup variables and audit-summary fields. |

## Complete field CSV

[field_catalog.csv](field_catalog.csv) contains the path-specific dictionary in tabular form. Its columns are:

| Column | Definition |
| --- | --- |
| `file_family` | File group: individual record, index, analytical inventory, per-record audit or audit summary. |
| `variable_path` | Full documentation path with a file-family prefix; `[]` represents a list item. |
| `json_pointer_pattern` | Pointer-like path inside that file family; `[]` represents list items, `~1` escapes a literal slash and `~0` a literal tilde. |
| `observed_types` | Value types actually present in this snapshot, including array-item types where observed. |
| `definition` | Meaning of the field, its scope and relevant interpretation limits. |
| `unit_or_format` | Unit or format supported by the field name or definition; no unstated unit is inferred. |
| `observed_examples` | Illustrative short values found in the data, not an exhaustive allowed-value set. |
| `record_count` | Number of records containing this path in the indicated file family, including null values; not a count of verified evidence. |

The dictionary describes the exported data after remark cleanup. Historical and challenge-specific fields remain visible; their presence does not make them universal analytical variables.
