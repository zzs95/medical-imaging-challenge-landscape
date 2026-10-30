# Shared-note identifiers

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

`common_note_ids` in an individual record points to the following keys in `docs/common_notes.json`. The applicable note remains part of that record's documentation.

| Identifier | Definition / shared qualification |
| --- | --- |

| `CN01` | Unverified factual fields are null. Snapshot statistics may include post-challenge submissions. |
| `CN02` | Unverified factual fields are null. Information collection date is separate from medical image acquisition dates. |
| `CN03` | Submission descriptions refer to scoring artifacts unless explicitly identified as verification-only material. |
| `CN04` | Uncoded dataset/access/publication quantities remain null; registered protocol text is retained for further extraction. |
| `CN05` | Metric lists can include secondary reporting metrics; no ranking formula is inferred from their presence. |
| `CN06` | Unknown fields remain null; they are not imputed from adjacent annual editions. |
| `CN07` | Null structured fields are retained where detailed extraction has not yet been harmonized. |

[Back to README](../../README.md#variable-dictionary)
