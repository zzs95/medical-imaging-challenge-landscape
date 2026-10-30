# Collection-template variables

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

`docs/collection_rules_v1.2.json` preserves the original shared instructions. Its candidate labels are collection aids; they are not proof that every candidate occurred or the final analytical vocabulary.

| Variable | Definition |
| --- | --- |
| `schema_info.schema_name` | Name of the original collection template. |
| `schema_info.schema_version` | Version of that template. |
| `schema_info.language` | Intended language of the original template; actual free-text notes can also be in Chinese. |
| `schema_info.purpose` | Intended use and coverage of the original collection template. |
| `filling_rules.general_rules.rules[]` | General source, missingness, counting and provenance instructions. |
| `filling_rules.<domain>.rules[]` | Collection instructions specific to the named domain. |
| `filling_rules.<domain>.candidate_labels.<field>[]` | Candidate labels suggested for the named field during initial collection; later harmonization may use different analytical labels. |

The named template domains are event, clinical_domain, task_profile, labels_and_targets, dataset, data_access, data_usage_mode, evaluation, submission, methodological_category, publication, provenance and participation_statistics. The corresponding actual record variables are defined in the thematic files linked from the README. For example, video can appear in the original template vocabulary while the current review treats it as a format attribute.

[Back to README](../../README.md#variable-dictionary)
