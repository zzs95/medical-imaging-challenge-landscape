# Data access, licences and permissions

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

Access requirements, release conditions, data licences and reuse permissions.

## Field groups

- [`challenge.data_access`](#data-access)
- [`challenge.data_license_review`](#data-license-review)

<a id="data-access"></a>

## `data_access`

JSON parent path: `challenge.data_access`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.data_access`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `access_after_challenge` | null / boolean / string | Statement about continued or later access after the challenge, retaining plans versus observed availability. |
| `access_by_scope` | array; items: object | Access conditions broken down by dataset, task, phase or source scope. |
| `access_by_scope[].access_steps` | array; items: string | Documented steps needed to obtain the relevant data, such as registration, authorization and download. |
| `access_by_scope[].category` | string | Classification assigned within the enclosing coding scheme; schemes differ across variables. |
| `access_by_scope[].manual_review` | null / boolean | Whether the access procedure includes individual/manual approval; null means unresolved. |
| `access_by_scope[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `access_evidence` | string | Recorded documentary support for access. Preserve the task/phase scope and source qualifications. |
| `access_scope` | null / string | Task, phase, cohort or source boundaries of access. |
| `access_status` | null / string | Source-recorded access category, including public, registration, authorization, restricted or unavailable arrangements. |
| `attribution_required` | null / boolean | Whether the source expressly requires acknowledgement or attribution when using the data. |
| `commercial_permission_required` | null / boolean | Whether separate permission is explicitly required for commercial use. |
| `commercial_use_allowed_without_permission` | null / boolean | Whether commercial use is explicitly allowed without additional permission. |
| `dua_required` | null / boolean | Whether a data-use agreement is explicitly required for the relevant data scope. |
| `hosting` | null / string | Service hosting the relevant dataset or download resources. |
| `is_public` | null / boolean | Whether external researchers can obtain the relevant data under the documented conditions; not merely whether a webpage is public. |
| `license_conflict` | string | Description of inconsistent licence statements across sources or versions. |
| `license_evidence` | string | Recorded documentary support for license. Preserve the task/phase scope and source qualifications. |
| `license_or_terms` | null / string | Recorded licence or use-agreement wording and its applicable data/task/phase scope. |
| `license_review_resolution` | string | Source-supported resolution of an earlier licence inconsistency, with resource and edition scope retained. |
| `license_review_status` | string | Recorded state of license review. Preserve the task/phase scope and source qualifications. |
| `open_use` | null | Source-recorded statement about open use of the data; interpret together with the actual licence and restrictions. |
| `post_challenge_public_release` | object | Structured entries for post challenge public release within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `post_challenge_public_release.dataset_name` | string | Name of the dataset or release to which the enclosing metadata apply. |
| `post_challenge_public_release.doi` | string | Digital Object Identifier assigned to the enclosing publication, protocol or dataset. |
| `post_challenge_public_release.download_url` | string | Web address for download. |
| `post_challenge_public_release.file_id` | integer | Identifier assigned to a hosted file by its repository/service; not a file count. |
| `post_challenge_public_release.file_name` | string | Filename assigned to the cited data, source or submission artifact. |
| `post_challenge_public_release.license` | string | Licence designation attached to the enclosing data, software or publication resource; those resource types are distinct. |
| `post_challenge_public_release.public_release_date` | string | Date associated with public release. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `post_challenge_public_release.repository` | string | Repository name or location for the relevant dataset, software, model or source. |
| `post_challenge_public_release.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `post_challenge_public_release.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `post_challenge_public_release.status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `post_challenge_public_release.verified_on` | string | Date of the specific verification described in the enclosing record. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `preregistered_data_license` | string | Licence or data-use condition stated in the preregistered protocol, separate from later release terms. |
| `protocol_reference` | object | Reference to the edition-specific protocol supporting the enclosing field; a protocol describes specification rather than proof of execution. |
| `protocol_reference.local_protocol` | string | Original archive path of a registered protocol; the protocol file itself is not included in this metadata package. |
| `protocol_reference.registered_task_index` | integer | Task position/identifier in the registered protocol; it can differ from later operational numbering. |
| `protocol_reference.section` | string | Section, figure, table or location within a supporting source. |
| `protocol_reference.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `public_download` | null / boolean | Whether a public download route is explicitly documented, subject to the recorded scope and terms. |
| `redistribution_allowed` | null / boolean | Whether redistribution is explicitly permitted by the applicable source terms; null is not permission. |
| `registration_required_for_challenge_participation` | null / boolean | Whether registration is required to participate; this alone does not establish data authorization requirements. |
| `review_status` | string | Status or scope of the review process, not a direct measure of challenge quality. |
| `verified_grand_challenge_account_required_for_challenge` | null | Whether a verified Grand Challenge account is explicitly required for participation. |
| `versioned_access` | array; items: object | Structured entries for versioned access within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `versioned_access[].access_status` | string | Source-recorded access category, including public, registration, authorization, restricted or unavailable arrangements. |
| `versioned_access[].license` | string | Licence designation attached to the enclosing data, software or publication resource; those resource types are distinct. |
| `versioned_access[].reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `versioned_access[].subject_count` | integer | Number of subjects in the stated cohort; preserve whether they are patients, volunteers, animals or other source-defined subjects. Unit/format: subjects; stated cohort/split. |
| `versioned_access[].url` | string | Web address of the enclosing source, document or resource. |
| `versioned_access[].version` | string | Version of the enclosing dataset, protocol, software, manuscript or source document. |

<a id="data-license-review"></a>

## `data_license_review`

JSON parent path: `challenge.data_license_review`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.data_license_review`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `agreement_acceptance_scope` | string | Task, phase, cohort or source boundaries of agreement acceptance. |
| `agreement_end_date` | string | Date associated with agreement end. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `agreement_full_text_verified` | string | Source-recorded agreement full text verified for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `agreement_required` | null / boolean | Whether a signed or accepted agreement is required, retaining the source's unresolved or qualified state. |
| `confidence` | string | Recorded confidence/qualification in a review decision; not a calibrated probability unless explicitly defined by the source. |
| `dataset_scope_verified` | string | Source-recorded dataset scope verified for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `detail_level` | string | Level of detail provided by the supporting source, such as a result summary versus component-specific findings. |
| `effective_date` | string | Date associated with effective. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `evidence_basis` | string | Evidence or reasoning supporting evidence. |
| `followup_review` | string | Source-linked review of followup. |
| `licence_names` | array; items: string | Structured entries for licence names within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `not_inferred` | string | Information deliberately left unresolved rather than inferred from related fields or sources. |
| `previous_review` | object | Earlier review object preserved to document superseded evidence or classification. |
| `previous_review.agreement_required` | null | Whether a signed or accepted agreement is required, retaining the source's unresolved or qualified state. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.detail_level` | string | Level of detail provided by the supporting source, such as a result summary versus component-specific findings. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.licence_names` | array | Structured entries for licence names within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `previous_review.not_inferred` | string | Information deliberately left unresolved rather than inferred from related fields or sources. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.qualifications` | array | Structured entries for qualifications within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `previous_review.review_cohort` | string | Subset of records targeted by the described review operation. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.review_date` | string | Date of the review operation described in the enclosing object. This occurrence is historical and must be interpreted within its enclosing revision. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `previous_review.review_population` | string | Records or variables eligible for the described review operation, not a patient population. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.scoped_terms` | array; items: object | Structured entries for scoped terms within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `previous_review.scoped_terms[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.scoped_terms[].source` | object | Source identifier, URL, citation, original wording or source object for the enclosing item. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.scoped_terms[].source.local_source` | string | Path identifying a source in the original review archive, not a downloadable file inside this release. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.scoped_terms[].source.url` | string | Web address of the enclosing source, document or resource. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.scoped_terms[].text` | string | Text retained in the enclosing source, explanation or review entry. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.search_attempts` | array; items: object | Recorded attempts to retrieve relevant sources, including unsuccessful searches; retrieval success is not factual confirmation. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.search_attempts[].error` | null | Error reported during retrieval, extraction or execution; the parent field identifies which process failed. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.search_attempts[].local_source` | string | Path identifying a source in the original review archive, not a downloadable file inside this release. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.search_attempts[].status` | null / integer | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.search_attempts[].url` | string | Web address of the enclosing source, document or resource. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.sources` | array; items: object | Sources supporting the enclosing statement or dataset description, preserving document/source type and scope. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.sources[].local_source` | string | Path identifying a source in the original review archive, not a downloadable file inside this release. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.sources[].url` | string | Web address of the enclosing source, document or resource. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.substantive_terms_documented` | boolean | Whether the condition “substantive terms documented” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `previous_review.summary_zh` | string | Chinese-language summary of the enclosing review, source or interpretation. This occurrence is historical and must be interpreted within its enclosing revision. |
| `previous_review.terms_documented` | boolean | Whether the review found classifiable data-use or licence terms; false does not prove that no terms existed. This occurrence is historical and must be interpreted within its enclosing revision. |
| `qualifications` | array; items: string | Structured entries for qualifications within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `reuse_terms_verified` | string | Recorded verification status of reuse terms for the specified resource; not blanket permission for unrelated data/software. |
| `review_cohort` | string | Subset of records targeted by the described review operation. |
| `review_date` | string | Date of the review operation described in the enclosing object. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `review_population` | string | Records or variables eligible for the described review operation, not a patient population. |
| `scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `scoped_terms` | array; items: object | Structured entries for scoped terms within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `scoped_terms[].agreement_effective_date` | string | Date associated with agreement effective. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `scoped_terms[].applicability` | string | Whether the enclosing variable applies structurally to this challenge/task; distinct from a missing source. |
| `scoped_terms[].document_status` | string | Recorded state of document. Preserve the task/phase scope and source qualifications. |
| `scoped_terms[].end_date` | string | Date associated with end. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `scoped_terms[].evidence_section` | string | Source-recorded evidence section for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `scoped_terms[].licence_name` | string | Name/designation of the applicable licence, preserving which resource it covers. |
| `scoped_terms[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `scoped_terms[].source` | object | Source identifier, URL, citation, original wording or source object for the enclosing item. |
| `scoped_terms[].source.evidence_type` | string | Kind of supporting evidence, preserving protocol, report, result and confirmation distinctions. |
| `scoped_terms[].source.local_source` | string | Path identifying a source in the original review archive, not a downloadable file inside this release. |
| `scoped_terms[].source.sha256` | string | Cryptographic checksum or revision identifier for the enclosing sha256; used for provenance rather than as a scientific measurement. |
| `scoped_terms[].source.url` | string | Web address of the enclosing source, document or resource. |
| `scoped_terms[].text` | string | Text retained in the enclosing source, explanation or review entry. |
| `scoped_terms[].text_type` | string | Kind of text required or assessed, such as a free-text report or structured fields. |
| `scoped_terms[].verification` | string | Source-recorded verification for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `search_attempts` | array; items: object | Recorded attempts to retrieve relevant sources, including unsuccessful searches; retrieval success is not factual confirmation. |
| `search_attempts[].error` | null / string | Error reported during retrieval, extraction or execution; the parent field identifies which process failed. |
| `search_attempts[].local_source` | string | Path identifying a source in the original review archive, not a downloadable file inside this release. |
| `search_attempts[].status` | null / integer | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `search_attempts[].url` | string | Web address of the enclosing source, document or resource. |
| `sources` | array; items: object | Sources supporting the enclosing statement or dataset description, preserving document/source type and scope. |
| `sources[].capture_date` | string | Date associated with capture. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `sources[].evidence_type` | string | Kind of supporting evidence, preserving protocol, report, result and confirmation distinctions. |
| `sources[].local_source` | string | Path identifying a source in the original review archive, not a downloadable file inside this release. |
| `sources[].provenance` | string | Source references, observation dates, field-level supporting evidence and review history. |
| `sources[].sha256` | string | Cryptographic checksum or revision identifier for the enclosing sha256; used for provenance rather than as a scientific measurement. |
| `sources[].url` | string | Web address of the enclosing source, document or resource. |
| `sources[].verification` | string | Source-recorded verification for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `state` | string | Documentary coding state for the enclosing item; not an ordinal quality score. |
| `substantive_terms_documented` | boolean | Whether the condition “substantive terms documented” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `summary_zh` | string | Chinese-language summary of the enclosing review, source or interpretation. |
| `supplemental_user_review` | string | Source-linked review of supplemental user. |
| `terms_documented` | boolean | Whether the review found classifiable data-use or licence terms; false does not prove that no terms existed. |
| `training_licence_applicability` | string | Source-recorded training licence applicability for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |

[Back to README](../../README.md#variable-dictionary)
