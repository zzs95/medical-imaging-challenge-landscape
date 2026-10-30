# Dictionary conventions: paths, types and missing values

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md)

The grouped dictionary covers every named property path found in the exported individual records, the index, the analytical inventory and the packaging-review metadata. Array elements are represented by `[]`; a path such as `tasks[].task_id` refers to the identifier inside each task object. Shared variables are repeated under their actual parent paths so that source, task, phase and historical scope remain visible. Not all fields occur in every record.

**Types are observed representations in this snapshot, not a mandatory schema.** `string` is text, `integer` is a whole number, `number` is a numeric value, `boolean` is true/false, `array` is a list, `object` contains named fields, and `null` means that no populated value was recorded. An array's item types are shown where observed. CSV cells are stored as text even when they represent counts.

| Value or evidence condition | Interpretation |
| --- | --- |
| `null` or an absent field | Information was not populated or established at that location. It does not show that the practice did not occur. |
| `false` in a factual Boolean | Preserve the explicit source/coding meaning; do not substitute false for missing information. |
| `false` in an inventory documentation flag | The corresponding documentation criterion was not met, not proof that the underlying practice was absent. |
| `Not yet extracted` | A retained legacy extraction state; it is neither true nor false. It occurs for 122 `registered_participants_documented` entries. |
| Empty array | Interpret with the specific field. In inventory objective labels it means no assigned label; raw historical arrays do not all share one missingness convention. |
| Documented and classifiable | Available information supports the variable's stated classification within its source scope. |
| Ambiguous | Available information does not uniquely resolve the classification. |
| Not established | The reviewed evidence does not establish the value or assessment state. |
| Not applicable | Structural non-applicability under the coding rules, not simply a missing source. |
| Explicit non-implementation | A source states that a proposed assessment was not performed; distinct from missing execution evidence. |
| Specified protocol | A described design or requirement; it does not itself establish that the assessment or limit was executed/enforced. |

Dataset counts retain their original units and split scope. Patients, studies, scans, images, volumes, slides, patches, cells and videos are not interchangeable. Registered users, active teams, finalists and submission attempts are also distinct. A publication year is not an edition year, and a metadata-review date is not an acquisition date.

Fields named after a specific task, split, metric or class retain their source-defined meaning. A named branch such as `task1` is a scope container, not a new universal analytical dimension. For unusual one-off fields, the source label and enclosing object provide the applicable scope; no unreported metric formula, unit or verification outcome is inferred.

The [CSV dictionary](../field_catalog.csv) supplies complete paths and illustrative observed values. Those examples are not an exhaustive set of permitted values. `file_family` identifies the containing file type; the initial `record`, `index`, `inventory`, `record_review` or `review_summary` in `variable_path` is a documentation prefix, not an extra JSON property. `json_pointer_pattern` omits that prefix; `[]` denotes array items, and `~1`/`~0` escape literal slashes/tildes in field names. `record_count` counts records containing the field, including nulls; it is not a verified-evidence count.

[Back to README](../../README.md#variable-dictionary)
