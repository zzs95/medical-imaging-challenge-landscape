# Record-index variables

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

These variables occur in each row of `data/index.json` and `data/index.csv`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `analysis_include` | boolean | Whether this record belongs to the 342-edition primary analytical subset. |
| `challenge_name` | string | Recorded short or customary name of the competition edition. |
| `edition_id` | string | Identifier of the analytical edition used to join the index, inventory and individual record. |
| `exclusion_reason` | null / string | Recorded reason why the edition is outside the primary analytical subset. |
| `original_sha256` | string | SHA-256 checksum of the original working JSON used to prepare this package. |
| `original_source_path` | string | Venue/year path of the original working record before export. |
| `packaged_sha256` | string | SHA-256 checksum of the exported individual JSON after conservative remark cleanup. |
| `path` | string | Relative location of the individual JSON inside this package. |
| `record_group` | string | Membership in the included, excluded or legacy package group. |
| `year` | integer | Challenge edition year from the current manifest, or the stated year of the legacy record. |

[Back to README](../../README.md#variable-dictionary)
