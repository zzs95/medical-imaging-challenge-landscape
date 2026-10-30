# Publications and participant-method evidence

[Back to README](../../README.md#variable-dictionary) · [Dictionary index](../DATA_DICTIONARY.md) · [Paths, types and missing values](conventions.md)

Related papers, publication status, literature leads and participant-method sources.

## Field groups

- [`challenge.publication`](#publication)
- [`challenge.literature_followups`](#literature-followups)
- [`challenge.literature_review_leads`](#literature-review-leads)
- [`challenge.participant_method_evidence`](#participant-method-evidence)

<a id="publication"></a>

## `publication`

JSON parent path: `challenge.publication`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.publication`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `challenge_results_manuscript_planned` | null / boolean | Whether organizers state an intention to publish a challenge-results manuscript; a plan is not an available result. |
| `code_release_required` | boolean | Whether the condition “code release required” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `conference_program` | object | Structured entries for conference program within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `conference_program.chair` | string | Person identified as chair of the stated session or event. |
| `conference_program.evidence_ids` | array; items: string | Identifiers of specific evidence items supporting the enclosing interpretation; archival ledgers may be outside this package. |
| `conference_program.listed_presentation_count` | integer | Reported numerical value for listed presentation count within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `conference_program.program_pages` | array; items: integer | Structured entries for program pages within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `conference_program.program_paper_ids` | array; items: string | Structured entries for program paper identifiers within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `conference_program.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `conference_program.room` | string | Room assigned to the challenge event or presentation session. |
| `conference_program.session_date` | string | Date associated with session. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `conference_program.session_time_as_printed` | string | Session time copied from the programme, with its original timezone/precision qualifications. |
| `conference_program.source_snapshot` | string | Identifier or path of the source snapshot in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `conference_program.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `conference_program.title_as_printed` | string | Publication or programme title preserved exactly as printed in the cited source. |
| `dataset_benchmark_paper` | object | Structured entries for dataset benchmark paper within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `dataset_benchmark_paper.arxiv_id` | string | arXiv identifier of the enclosing preprint. |
| `dataset_benchmark_paper.date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `dataset_benchmark_paper.does_not_establish` | string | Claims that the enclosing evidence is explicitly insufficient to support. |
| `dataset_benchmark_paper.doi` | string | Digital Object Identifier assigned to the enclosing publication, protocol or dataset. |
| `dataset_benchmark_paper.first_author` | string | First author credited for the enclosing publication. |
| `dataset_benchmark_paper.supports` | array; items: string | Statements or fields that the source is recorded as supporting, limited by the source's actual task, phase and evidence scope. |
| `dataset_benchmark_paper.title` | string | Title of the enclosing source document, publication, method or programme entry. |
| `dataset_benchmark_paper.type` | string | Type of the enclosing source, document, artifact, observation or event; its vocabulary is specific to that parent context. |
| `dataset_benchmark_paper.url` | string | Web address of the enclosing source, document or resource. |
| `embargo_policy` | string | Permission, restriction or procedural rule governing embargo. |
| `final_competition_report_status` | string | Recorded state of final competition report. Preserve the task/phase scope and source qualifications. |
| `invitation_timeline_note` | object | Qualification or source distinction concerning invitation timeline. |
| `invitation_timeline_note.description` | string | Description of the enclosing entity, procedure, data or result as retained from the source or review. |
| `invitation_timeline_note.source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `invitation_timeline_note.status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `method_description` | string | Source description of method. |
| `method_description_required` | boolean | Whether the condition “method description required” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `optional_workshop_submission` | null / object | Structured entries for optional workshop submission within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `optional_workshop_submission.independent_from_challenge` | null | Whether the enclosing paper/workshop participation is independent of competition participation. |
| `optional_workshop_submission.paper_length_pages` | null | Permitted or stated manuscript length in pages. |
| `optional_workshop_submission.proceedings` | null | Proceedings series or volume associated with the workshop or publication. |
| `optional_workshop_submission.workshop` | null | Associated workshop and the nature of its relationship to the challenge. |
| `organizer_overview_results_paper_status` | string | Recorded state of organizer overview results paper. Preserve the task/phase scope and source qualifications. |
| `organizer_results_paper_status` | string | Recorded state of organizer results paper. Preserve the task/phase scope and source qualifications. |
| `organizer_results_report` | object | Structured entries for organizer results report within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `organizer_results_report.challenge_year` | integer | Calendar year assigned to challenge; preserve whether this concerns an edition, analysis, event or publication. |
| `organizer_results_report.doi` | string | Digital Object Identifier assigned to the enclosing publication, protocol or dataset. |
| `organizer_results_report.publication_year` | integer | Year of publication or posting, separate from the year of the challenge edition. |
| `organizer_results_report.title` | string | Title of the enclosing source document, publication, method or programme entry. |
| `organizer_results_report.url` | string | Web address of the enclosing source, document or resource. |
| `organizer_retrospective_2026_status` | string | Recorded state of organizer retrospective 2026. Preserve the task/phase scope and source qualifications. |
| `participant_method_paper_pages` | integer | Number of participant method paper pages in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `participant_paper_metadata` | array; items: object | Structured entries for participant paper metadata within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `participant_paper_metadata[].authors` | array; items: string | Authors credited for the enclosing publication or source. |
| `participant_paper_metadata[].content_scope` | string | Task, phase, cohort or source boundaries of content. |
| `participant_paper_metadata[].doi` | string | Digital Object Identifier assigned to the enclosing publication, protocol or dataset. |
| `participant_paper_metadata[].full_text_reviewed` | boolean | Whether the condition “full text reviewed” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `participant_paper_metadata[].metadata_verified` | boolean | Whether the condition “metadata verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `participant_paper_metadata[].publication_date` | string | Date associated with publication. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `participant_paper_metadata[].title` | string | Title of the enclosing source document, publication, method or programme entry. |
| `participant_papers` | array; items: object | Structured entries for participant papers within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `participant_papers[].authors` | array; items: string | Authors credited for the enclosing publication or source. |
| `participant_papers[].bibliographic_note` | string | Qualification or source distinction concerning bibliographic. |
| `participant_papers[].challenge_year` | integer | Calendar year assigned to challenge; preserve whether this concerns an edition, analysis, event or publication. |
| `participant_papers[].doi` | null | Digital Object Identifier assigned to the enclosing publication, protocol or dataset. |
| `participant_papers[].evidence_id` | string | Identifier of one supporting evidence item in the review ledger. |
| `participant_papers[].full_text` | string | Availability, location or description of the reviewed full-text source, as stored by the enclosing record. |
| `participant_papers[].full_text_url` | string | Web address for full text. |
| `participant_papers[].openreview` | string | OpenReview record or URL for the enclosing paper/venue. |
| `participant_papers[].openreview_decision` | string | Decision status reported in the cited OpenReview entry; not independently a competition outcome. |
| `participant_papers[].pages` | null | Page range or page information for the enclosing publication. |
| `participant_papers[].paper_id` | string | Identifier of a paper within the cited conference, repository or programme. |
| `participant_papers[].publication_status` | string | Documented publication state, such as planned, in preparation, preprint or published; not itself an evaluation outcome. |
| `participant_papers[].results` | object | Reported findings or results for the enclosing task, phase, method or publication. |
| `participant_papers[].results.field_completion_rate` | number | Reported numerical value for field completion rate within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `participant_papers[].results.mean_rotation_error_degrees` | number | Reported numerical value for mean rotation error degrees within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. Unit/format: degrees; denominator/scope follows field name. |
| `participant_papers[].results.mean_translation_error_mm` | number | Reported numerical value for mean translation error mm within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. Unit/format: mm; denominator/scope follows field name. |
| `participant_papers[].results.output` | string | Prediction, artifact or information produced by the task or model. |
| `participant_papers[].results.phase` | string | Competition or assessment stage associated with the enclosing value, protocol or outcome. |
| `participant_papers[].results.qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `participant_papers[].results.rank` | integer | Reported placement under the stated task, phase and ranking scope. |
| `participant_papers[].results.rank_at_evaluation` | integer | Placement at the date of the cited evaluation snapshot, not necessarily the eventual final ranking. |
| `participant_papers[].results.total_score` | number | Combined score across the components explicitly included in the source's aggregation rule. |
| `participant_papers[].results.weighted_score` | number | Score after applying the source-defined component weights; preserve the formula and task/phase scope. |
| `participant_papers[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `participant_papers[].springer_doi` | null | DOI assigned to the enclosing Springer publication. |
| `participant_papers[].status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `participant_papers[].task` | string | Task name or task-specific result/description associated with the enclosing entry. |
| `participant_papers[].title` | string | Title of the enclosing source document, publication, method or programme entry. |
| `participant_papers[].url` | string | Web address of the enclosing source, document or resource. |
| `participant_papers[].venue` | string | Named venue of an event or publication, according to its enclosing record. |
| `participant_papers[].year` | integer | Publication or posting year of the enclosing document; not the year of the competition edition. |
| `participant_preprints` | array; items: object | Structured entries for participant preprints within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `participant_preprints[].arxiv_id` | string | arXiv identifier of the enclosing preprint. |
| `participant_preprints[].authors` | array; items: string | Authors credited for the enclosing publication or source. |
| `participant_preprints[].evaluation_scope` | string | Task, phase, cohort or source boundaries of evaluation. |
| `participant_preprints[].evidence_id` | string | Identifier of one supporting evidence item in the review ledger. |
| `participant_preprints[].first_posted` | string | Date the preprint or online source was first posted, preserving the source's stated precision. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `participant_preprints[].reported_metrics` | object | Structured entries for reported metrics within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `participant_preprints[].reported_metrics.AUC_DMM` | number | Reported value or specification of the source-named metric `AUC_DMM` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `participant_preprints[].reported_metrics.AUC_Dice` | number | Reported value or specification of the source-named metric `AUC_Dice` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `participant_preprints[].reported_metrics.Dice_after_five_corrections` | number | Reported value or specification of the source-named metric `Dice_after_five_corrections` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `participant_preprints[].reported_metrics.Dice_without_scribbles` | number | Reported value or specification of the source-named metric `Dice_without_scribbles` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `participant_preprints[].reviewed_version` | string | Specific source/document version examined in the review. |
| `participant_preprints[].status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `participant_preprints[].title` | string | Title of the enclosing source document, publication, method or programme entry. |
| `participant_preprints[].url` | string | Web address of the enclosing source, document or resource. |
| `participant_reports` | array; items: object | Structured entries for participant reports within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `participant_reports[].date` | string | Date attached to the enclosing source, event, review or decision; distinguish it from edition and acquisition dates. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `participant_reports[].local_pdf` | string | Identifier or path of the local pdf in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `participant_reports[].publication_status` | string | Documented publication state, such as planned, in preparation, preprint or published; not itself an evaluation outcome. |
| `participant_reports[].title` | string | Title of the enclosing source document, publication, method or programme entry. |
| `participant_reports[].track_scope` | string | Task, phase, cohort or source boundaries of track. |
| `participant_reports[].type` | string | Type of the enclosing source, document, artifact, observation or event; its vocabulary is specific to that parent context. |
| `participant_reports[].url` | string | Web address of the enclosing source, document or resource. |
| `participant_result_sources` | array; items: object | Sources supporting participant result. |
| `participant_result_sources[].evidence_scope` | string | Boundary of what the supporting evidence establishes, including specification versus actual execution. |
| `participant_result_sources[].preprint_first_posted` | string | First public posting date of the preprint, distinct from the challenge edition year. |
| `participant_result_sources[].publication_type` | string | Type of publication or source, such as journal article, proceedings paper, preprint or organizer report. |
| `participant_result_sources[].repository` | string | Repository name or location for the relevant dataset, software, model or source. |
| `participant_result_sources[].scope` | string | Task, phase, cohort, resource or source boundaries to which the enclosing statement applies. |
| `participant_result_sources[].submitted_on` | string | Submission date attached to the enclosing paper or evaluation record. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `participant_result_sources[].title` | string | Title of the enclosing source document, publication, method or programme entry. |
| `participant_result_sources[].url` | string | Web address of the enclosing source, document or resource. |
| `proceedings` | string / object | Proceedings series or volume associated with the workshop or publication. |
| `proceedings.challenge_year` | integer | Calendar year assigned to challenge; preserve whether this concerns an edition, analysis, event or publication. |
| `proceedings.count_scope` | string | Task, phase, cohort or source boundaries of count. |
| `proceedings.doi` | string | Digital Object Identifier assigned to the enclosing publication, protocol or dataset. |
| `proceedings.full_papers` | integer | Reported numerical value for full papers within the enclosing task, phase or source. Use the stated unit/metric; no cross-challenge comparability is implied. |
| `proceedings.paper_submissions` | integer | Number of paper submissions in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |
| `proceedings.publication_year` | integer | Year of publication or posting, separate from the year of the challenge edition. |
| `proceedings.series` | string | Name of the recurring challenge, workshop or publication series in the enclosing record. |
| `proceedings.subtitle` | string | Subtitle of the enclosing document or publication. |
| `proceedings.title` | string | Title of the enclosing source document, publication, method or programme entry. |
| `proceedings.url` | string | Web address of the enclosing source, document or resource. |
| `proceedings.volume` | integer | Publication volume identifier; in dataset quantities use the enclosing field's imaging meaning instead. |
| `publication_evidence_source` | string | Source supporting publication evidence. |
| `publication_status_note` | string | Qualification or source distinction concerning publication status. |
| `published_participant_papers` | boolean | Whether the condition “published participant papers” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `registration_doi` | string | DOI of the registered challenge protocol or registration record. |
| `related_2024_report_warning` | string | Source-recorded related 2024 report warning for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `related_dataset_and_benchmark_paper` | object | Structured entries for related dataset and benchmark paper within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `related_dataset_and_benchmark_paper.article_number` | string | Article identifier used instead of or alongside page numbers. |
| `related_dataset_and_benchmark_paper.authors` | array; items: object | Authors credited for the enclosing publication or source. |
| `related_dataset_and_benchmark_paper.authors[].family` | string | Family/surname component of an author's name when nested in authors; elsewhere the source-defined challenge/model family. |
| `related_dataset_and_benchmark_paper.authors[].given` | string | Given-name component of an author's name. |
| `related_dataset_and_benchmark_paper.doi` | string | Digital Object Identifier assigned to the enclosing publication, protocol or dataset. |
| `related_dataset_and_benchmark_paper.edition_counting_note` | string | Qualification or source distinction concerning edition counting. |
| `related_dataset_and_benchmark_paper.journal` | string | Journal publishing the enclosing article. |
| `related_dataset_and_benchmark_paper.online_date_independently_verified` | boolean | Whether the condition “online date independently verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `related_dataset_and_benchmark_paper.online_date_note` | string | Qualification or source distinction concerning online date. |
| `related_dataset_and_benchmark_paper.online_date_reported_by_user` | string | Source-recorded online date reported by user for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `related_dataset_and_benchmark_paper.pmid` | string | PubMed identifier of the enclosing publication. |
| `related_dataset_and_benchmark_paper.publication_status` | string | Documented publication state, such as planned, in preparation, preprint or published; not itself an evaluation outcome. |
| `related_dataset_and_benchmark_paper.relationship_to_challenge` | string | Source-recorded relationship to challenge for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `related_dataset_and_benchmark_paper.result_scope` | object | Task, phase, cohort or source boundaries of result. |
| `related_dataset_and_benchmark_paper.result_scope.comparison` | string | Comparison described in the source or review, preserving which methods, tasks and phases are compared. |
| `related_dataset_and_benchmark_paper.result_scope.competition_final_result_evidence` | boolean | Recorded documentary support for competition final result. Preserve the task/phase scope and source qualifications. |
| `related_dataset_and_benchmark_paper.result_scope.datasets` | array; items: string | Structured entries for datasets within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `related_dataset_and_benchmark_paper.result_scope.label` | string | Class label, category name or display label for the enclosing item. |
| `related_dataset_and_benchmark_paper.result_scope.table` | string | Table identifier/location within the supporting publication or source. |
| `related_dataset_and_benchmark_paper.reviewed_full_text` | string | Full-text document or review status used to support the enclosing extraction. |
| `related_dataset_and_benchmark_paper.reviewed_manuscript_version` | string | Version of the manuscript actually examined for the recorded evidence. |
| `related_dataset_and_benchmark_paper.reviewed_manuscript_version_date` | string | Date associated with reviewed manuscript version. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `related_dataset_and_benchmark_paper.title` | string | Title of the enclosing source document, publication, method or programme entry. |
| `related_dataset_and_benchmark_paper.url` | string | Web address of the enclosing source, document or resource. |
| `related_dataset_and_benchmark_paper.volume` | string | Publication volume identifier; in dataset quantities use the enclosing field's imaging meaning instead. |
| `related_dataset_and_benchmark_paper.year` | integer | Publication or posting year of the enclosing document; not the year of the competition edition. |
| `related_dataset_paper` | object | Structured entries for related dataset paper within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `related_dataset_paper.doi` | string | Digital Object Identifier assigned to the enclosing publication, protocol or dataset. |
| `related_dataset_paper.publication_date` | string | Date associated with publication. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `related_dataset_paper.title` | string | Title of the enclosing source document, publication, method or programme entry. |
| `related_dataset_paper.type` | string | Type of the enclosing source, document, artifact, observation or event; its vocabulary is specific to that parent context. |
| `related_dataset_paper.url` | string | Web address of the enclosing source, document or resource. |
| `related_preprints` | array; items: object | Structured entries for related preprints within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `related_preprints[].arxiv_id` | string | arXiv identifier of the enclosing preprint. |
| `related_preprints[].authors` | array; items: string | Authors credited for the enclosing publication or source. |
| `related_preprints[].counting_note` | string | Qualification or source distinction concerning counting. |
| `related_preprints[].evidence_ids` | array; items: string | Identifiers of specific evidence items supporting the enclosing interpretation; archival ledgers may be outside this package. |
| `related_preprints[].first_submitted` | string | Date the enclosing manuscript or source was first submitted. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `related_preprints[].ieee_proceedings_doi_status` | string | Recorded state of ieee proceedings DOI. Preserve the task/phase scope and source qualifications. |
| `related_preprints[].program_paper_id` | string | Source-recorded program paper identifier for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `related_preprints[].publication_status` | string | Documented publication state, such as planned, in preparation, preprint or published; not itself an evaluation outcome. |
| `related_preprints[].title` | string | Title of the enclosing source document, publication, method or programme entry. |
| `related_preprints[].url` | string | Web address of the enclosing source, document or resource. |
| `related_publications` | array; items: object | Structured entries for related publications within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `related_publications[].article_number` | string | Article identifier used instead of or alongside page numbers. |
| `related_publications[].challenge_edition_year` | integer | Calendar year assigned to challenge edition; preserve whether this concerns an edition, analysis, event or publication. |
| `related_publications[].doi` | string | Digital Object Identifier assigned to the enclosing publication, protocol or dataset. |
| `related_publications[].electronic_publication_date` | string | Date associated with electronic publication. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `related_publications[].first_author` | string | First author credited for the enclosing publication. |
| `related_publications[].issue` | string | Journal issue identifier. |
| `related_publications[].issue_date` | string | Date associated with issue. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `related_publications[].journal` | string | Journal publishing the enclosing article. |
| `related_publications[].pmcid` | string | PubMed Central identifier of the enclosing full-text article. |
| `related_publications[].pmid` | string | PubMed identifier of the enclosing publication. |
| `related_publications[].qualification` | string | Restriction on what the enclosing evidence or decision can establish. |
| `related_publications[].review_scope` | string | Variables, tasks, phases or source types covered by the recorded review. |
| `related_publications[].role` | string | Role of the enclosing task, source, artifact or person; context determines whether it is scored, auxiliary or supporting. |
| `related_publications[].title` | string | Title of the enclosing source document, publication, method or programme entry. |
| `related_publications[].url` | string | Web address of the enclosing source, document or resource. |
| `related_publications[].venue` | string | Named venue of an event or publication, according to its enclosing record. |
| `related_publications[].volume` | string | Publication volume identifier; in dataset quantities use the enclosing field's imaging meaning instead. |
| `related_publications[].year` | integer | Publication or posting year of the enclosing document; not the year of the competition edition. |
| `results_manuscript_status` | string | Recorded state of results manuscript. Preserve the task/phase scope and source qualifications. |
| `results_manuscript_status_independently_verified` | boolean | Whether the condition “results manuscript status independently verified” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `results_manuscript_status_source` | string | Source supporting results manuscript status. |
| `results_publication_verified` | null | Optional field for results publication verified in the enclosing record. It is unpopulated in this snapshot; neither a value nor a negative finding is established. |
| `reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `separate_participant_publication_allowed_without_embargo` | null / boolean | Whether participants may publish their own methods/results without a specified embargo. |
| `top_teams_invited_to_challenge_manuscript` | null / integer | Whether or how many leading teams are invited to contribute, according to the recorded type and source wording. |
| `verified_participant_papers` | array; items: object | Structured entries for verified participant papers within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `verified_participant_papers[].authors` | array; items: object | Authors credited for the enclosing publication or source. |
| `verified_participant_papers[].authors[].family` | string | Family/surname component of an author's name when nested in authors; elsewhere the source-defined challenge/model family. |
| `verified_participant_papers[].authors[].given` | string | Given-name component of an author's name. |
| `verified_participant_papers[].doi` | string | Digital Object Identifier assigned to the enclosing publication, protocol or dataset. |
| `verified_participant_papers[].evidence_ids` | array; items: string | Identifiers of specific evidence items supporting the enclosing interpretation; archival ledgers may be outside this package. |
| `verified_participant_papers[].final_test_results_verified_by_this_metadata_check` | boolean | Whether the condition “final test results verified by this metadata check” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `verified_participant_papers[].pages` | string | Page range or page information for the enclosing publication. |
| `verified_participant_papers[].proceedings` | string | Proceedings series or volume associated with the workshop or publication. |
| `verified_participant_papers[].program_paper_id` | string | Source-recorded program paper identifier for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `verified_participant_papers[].publication_status` | string | Documented publication state, such as planned, in preparation, preprint or published; not itself an evaluation outcome. |
| `verified_participant_papers[].relationship` | string | Documented relationship between the enclosing entities, preserving affiliation, scope and timing qualifications. |
| `verified_participant_papers[].title` | string | Title of the enclosing source document, publication, method or programme entry. |
| `verified_participant_papers[].url` | string | Web address of the enclosing source, document or resource. |
| `verified_participant_papers[].year` | integer | Publication or posting year of the enclosing document; not the year of the competition edition. |
| `verified_published_participant_paper_count` | integer | Number of verified published participant paper count in the stated phase/source scope. Preserve the entity and success/eligibility definition; submission counts are not independent team counts. |

<a id="literature-followups"></a>

## `literature_followups`

JSON parent path: `challenge.literature_followups`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.literature_followups`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `[].audit_path` | string | Identifier or path of the audit path in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `[].fields` | array; items: string | Named variables examined in the enclosing review; child keys identify the individual coding domains. |
| `[].review_date` | string | Date of the review operation described in the enclosing object. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |

<a id="literature-review-leads"></a>

## `literature_review_leads`

JSON parent path: `challenge.literature_review_leads`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.literature_review_leads`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `[].authors` | array; items: string | Authors credited for the enclosing publication or source. |
| `[].bibliography_status` | string | Recorded state of bibliography. Preserve the task/phase scope and source qualifications. |
| `[].content_status` | string | Recorded state of content. Preserve the task/phase scope and source qualifications. |
| `[].decision` | string | Recorded inclusion, coding or scope decision, with the associated reason and evidence retained. |
| `[].discovery_abstract_url` | string | Web address for discovery abstract. |
| `[].discovery_claim` | string | Source-recorded discovery claim for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `[].doi` | string | Digital Object Identifier assigned to the enclosing publication, protocol or dataset. |
| `[].evidence_level` | string | Scope/level of support supplied by the enclosing source, not a validated numerical evidence-quality scale. |
| `[].final_phase_identification` | string | Source-recorded final phase identification for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `[].final_test_result` | string | Result attributed to the designated final test, preserving the source and task scope. |
| `[].interpretation` | string | Reviewer's scoped interpretation of the recorded source information; not additional organizer evidence. |
| `[].metadata_snapshot` | string | Source-recorded metadata snapshot for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `[].original_paper_followup` | object | Structured entries for original paper followup within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `[].original_paper_followup.local_pdf` | string | Identifier or path of the local pdf in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `[].original_paper_followup.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `[].original_paper_followup.snapshot` | string | Identifier or path of the snapshot in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `[].previous_decision` | string | Earlier/superseded value of decision, preserved to document a revision rather than a current observation. |
| `[].primary_full_text_access` | string | Source-recorded primary full text access for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `[].publication_date` | string | Date associated with publication. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `[].reported_hidden_test_results_unverified` | object | Structured entries for reported hidden test results unverified within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `[].reported_hidden_test_results_unverified.Task 1` | object | Source-defined Task 1 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `[].reported_hidden_test_results_unverified.Task 1.AUC_percent` | number | Reported value or specification of the source-named metric `AUC_percent` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `[].reported_hidden_test_results_unverified.Task 1.F1_percent` | number | Reported value or specification of the source-named metric `F1_percent` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `[].reported_hidden_test_results_unverified.Task 2` | object | Source-defined Task 2 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `[].reported_hidden_test_results_unverified.Task 2.AUC_percent` | number | Reported value or specification of the source-named metric `AUC_percent` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `[].reported_hidden_test_results_unverified.Task 2.F1_percent` | number | Reported value or specification of the source-named metric `F1_percent` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `[].reported_model` | string | Model name or description explicitly reported by the cited source. |
| `[].reported_phase` | string | Phase name or scope explicitly reported by the cited source. |
| `[].reported_task` | string | Task identity/scope explicitly reported by the cited source. |
| `[].reported_task_mapping` | object | Structured entries for reported task mapping within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `[].reported_task_mapping.Task 1` | string | Source-defined Task 1 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `[].reported_task_mapping.Task 2` | string | Source-defined Task 2 branch. Its nested variables retain that task/track/phase scope and do not create an additional analytical edition. |
| `[].reported_validation_metrics` | object | Structured entries for reported validation metrics within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `[].reported_validation_metrics.mean_AUROC` | number | Reported value or specification of the source-named metric `mean_AUROC` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `[].reported_validation_metrics.mean_balanced_accuracy` | number | Reported value or specification of the source-named metric `mean_balanced_accuracy` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `[].requires_original_paper_for_content_verification` | boolean | Whether the condition “requires original paper for content verification” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `[].reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `[].snapshot` | string | Identifier or path of the snapshot in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `[].source_type` | string | Kind of data or evidence source. In dataset records this describes cohort origin; in provenance it describes the supporting document or confirmation. |
| `[].status` | string | Source-specific status of the enclosing item; numeric values in retrieval records can be HTTP response codes rather than scientific evidence states. |
| `[].submission_number` | integer | Submission identifier or ordinal number in the cited venue/platform; not necessarily the number of submissions. |
| `[].subsequent_human_verification` | object | Structured entries for subsequent human verification within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `[].subsequent_human_verification.baseline_separation` | string | Explanation separating organizer/local baseline experiments from competition assessment evidence. |
| `[].subsequent_human_verification.basis` | string | Evidence or reasoning used to support the enclosing classification, count or decision. |
| `[].subsequent_human_verification.caption_competition_assessment` | string | Evidence/status of competitive caption assessment in the specified phase. |
| `[].subsequent_human_verification.declared_captioning_objective` | string | Source-recorded declared captioning objective for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `[].subsequent_human_verification.evidence_state` | string | State of the documentary evidence for the specific field or assessment, retaining ambiguity, missingness and structural non-applicability. |
| `[].subsequent_human_verification.include_in_confirmed_caption_assessment_count` | boolean | Whether the condition “include in confirmed caption assessment count” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `[].subsequent_human_verification.independently_verified_complete_final_rankings` | string | Source-recorded independently verified complete final rankings for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `[].subsequent_human_verification.participant_paper_doi` | string | DOI of the participant publication cited as supporting the enclosing statement. |
| `[].subsequent_human_verification.published_evaluation_protocol` | string | Source-recorded published evaluation protocol for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `[].subsequent_human_verification.published_participant_result` | string | Source-recorded published participant result for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `[].subsequent_human_verification.reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `[].subsequent_human_verification.supersedes` | string | Earlier statement or record that the enclosing revision replaces. |
| `[].subsequent_human_verification.verification_limit` | string | Specific limit on what was verified from the available source. |
| `[].text_input_or_image_language_endpoint` | string | Source-recorded text input or image language endpoint for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `[].title` | string | Title of the enclosing source document, publication, method or programme entry. |
| `[].track_identity` | string | Source-recorded track identity for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `[].user_summary` | string | Source-recorded user summary for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |

<a id="participant-method-evidence"></a>

## `participant_method_evidence`

JSON parent path: `challenge.participant_method_evidence`. Variables in this table are relative to that parent; `[]` denotes an item of an array.

Paths in this table are relative to `challenge.participant_method_evidence`.


| Variable | Observed type | Definition |
| --- | --- | --- |
| `[].authors` | array; items: string | Authors credited for the enclosing publication or source. |
| `[].edition_year` | integer | Calendar year assigned to edition; preserve whether this concerns an edition, analysis, event or publication. |
| `[].evaluated_output` | string | Source-recorded evaluated output for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `[].evaluated_pipeline` | string | Source-recorded evaluated pipeline for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `[].evaluation_phase` | string | Stage to which the evaluation evidence applies, such as validation, preliminary test or final test. |
| `[].final_test_results_reported` | boolean | Whether the condition “final test results reported” holds within the enclosing source/task/phase scope. Null or missing information is distinct from a documented false value. |
| `[].interpretation` | string | Reviewer's scoped interpretation of the recorded source information; not additional organizer evidence. |
| `[].language_use_scope` | string | Task, phase, cohort or source boundaries of language use. |
| `[].limitations` | string | Limitations of the enclosing evidence, procedure or interpretation. |
| `[].local_pdf` | string | Identifier or path of the local pdf in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `[].method` | string | Method or procedure used for the enclosing evaluation, extraction or analysis; preserve whether organizer-defined or reviewer-applied. |
| `[].method_summary` | string | Source-recorded method summary for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `[].model` | string | Model named or described in the enclosing entry; not evidence of the challenge's organizer-defined objective by itself. |
| `[].openreview_identity` | string | Source-recorded openreview identity for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `[].pretraining` | string | Data or procedure used for pretraining before downstream task adaptation. |
| `[].publication_date` | string | Date associated with publication. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `[].reported_cross_validation_metrics` | object | Structured entries for reported cross validation metrics within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `[].reported_cross_validation_metrics.mean_AUROC` | number | Reported value or specification of the source-named metric `mean_AUROC` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `[].reported_cross_validation_metrics.mean_balanced_accuracy` | number | Reported value or specification of the source-named metric `mean_balanced_accuracy` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `[].reported_test_metrics` | object | Structured entries for reported test metrics within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `[].reported_test_metrics.AUROC` | number | Reported value or specification of the source-named metric `AUROC` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `[].reported_test_metrics.balanced_accuracy` | number | Reported value or specification of the source-named metric `balanced_accuracy` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `[].reported_test_metrics.runtime_seconds` | number | Reported or specified method runtime in seconds for the stated processing unit/scope. Unit/format: seconds; denominator/scope follows field name. |
| `[].reported_validation_metrics` | object | Structured entries for reported validation metrics within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `[].reported_validation_metrics.macro_AUROC` | number | Reported value or specification of the source-named metric `macro_AUROC` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `[].reported_validation_metrics.macro_balanced_accuracy` | number | Reported value or specification of the source-named metric `macro_balanced_accuracy` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `[].reported_validation_metrics.mean_AUROC` | number | Reported value or specification of the source-named metric `mean_AUROC` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `[].reported_validation_metrics.mean_balanced_accuracy` | number | Reported value or specification of the source-named metric `mean_balanced_accuracy` for the enclosing task/phase. Preserve the source formula, aggregation and scale; it is not an edition-wide capability score. |
| `[].result_scope` | string | Task, phase, cohort or source boundaries of result. |
| `[].reviewed_on` | string | Date on which the enclosing statement or source was reviewed, as recorded. Unit/format: Date as recorded; retain incomplete dates and timezone qualifications. |
| `[].snapshot` | string | Identifier or path of the snapshot in the original evidence archive. Its presence does not mean that the file is bundled in this release. |
| `[].source_locations` | array; items: string | Structured entries for source locations within the enclosing record. Nested variables define the entities, quantities or source qualifications represented. |
| `[].source_type` | string | Kind of data or evidence source. In dataset records this describes cohort origin; in provenance it describes the supporting document or confirmation. |
| `[].source_url` | string | Public URL cited as supporting the enclosing statement or record. |
| `[].task` | string | Task name or task-specific result/description associated with the enclosing entry. |
| `[].team` | string | Team identity attached to the stated method, submission, award or result. |
| `[].title` | string | Title of the enclosing source document, publication, method or programme entry. |
| `[].track` | string | Track identifier, name or description within the competition. |
| `[].track_identity` | string | Source-recorded track identity for the enclosing item. The exact wording and its surrounding task/phase or provenance context define its scope. |
| `[].validation_instance_scope` | string | Task, phase, cohort or source boundaries of validation instance. |
| `[].vision_language_interpretation` | string | Scoped review interpretation of vision language. |

[Back to README](../../README.md#variable-dictionary)
