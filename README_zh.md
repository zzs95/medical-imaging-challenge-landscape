# 医学影像比赛元数据，2022–2026

[English README](README.md)

本数据包为医学及生物医学影像比赛的全景综述提供结构化元数据，记录比赛目标、影像任务、临床背景、数据集、访问条件、提交与评估流程，以及相关文档证据。

分析子集包含 2022–2026 年的 **337 届比赛**。本仓库还保留了 15 条未纳入该子集的记录，以及 1 条 ACROBAT 历史记录，具体状态见索引。本数据包对应论文 *Medical Imaging Challenges in the Foundation-Model Era: A Landscape Review of Emerging Paradigms and Future Directions*。

**数据包快照：2026 年 10 月 30 日。** 这是打包日期；各来源的采集和审查日期保留在对应记录中，并不因本次打包而更新。本数据集属于非穷尽的全景性收集，并非所有医学影像比赛的完整普查。

## 数据范围与分析单位

| 记录类别 | 数量 | 位置 | 在综述中的用途 |
| --- | ---: | --- | --- |
| 纳入分析的年度比赛 | 337 | `data/challenges/` | 主要分析 |
| 当前清单中排除的记录 | 15 | `data/excluded/` | 保留筛选依据，不计入主要分析总数 |
| ACROBAT 2023 历史记录 | 1 | `data/legacy/` | 历史背景，位于当前清单之外 |
| 全部独立比赛 JSON 文件 | **353** | 上述三个目录 | 分析前按 `analysis_include` 筛选 |

当前清单包含 **352 条有明确年份的记录 = 337 条纳入 + 15 条排除**。额外保留的历史记录不能作为另一届纳入比赛计数。论文早期筛选台账及其中未注明年份的背景记录属于另一个筛选阶段；本包并非全部 383 条筛选记录的副本。

| 届次年份 | 2022 | 2023 | 2024 | 2025 | 2026 | 合计 |
| --- | ---: | ---: | ---: | ---: | ---: | ---: |
| 纳入届数 | 57 | 68 | 76 | 67 | 69 | **337** |

分析单位为一届比赛，同一系列不同年度可分别计数。父比赛与单独列出的子比赛避免重复计数。任务族采用多标签的**届次级**统计：即使同一届有多个赛道产生相同输出，该届在相应任务族中也只计一次。赛道级描述保留在 `task_profile.tasks` 中。

纳入子集中，61 届至少具有一个新兴 AI 目标，共形成 93 条届次—目标标签记录。六个可重叠的标签如下：

| 分析清单中的标签 | 届数 |
| --- | ---: |
| `Foundation models` | 30 |
| `VLM` | 36 |
| `Report generation` | 17 |
| `Text-conditioned image generation` | 4 |
| `Clinical Reasoning` | 4 |
| `Agent` | 2 |

这些标签描述组织者定义的目标，不代表每项相关评估都已执行或预期能力已得到证明。

数据入口：[记录索引](data/index.json)提供纳入状态和文件路径；[分析清单](data/analysis_inventory.json)提供 337 届纳入比赛的统一分析变量。字段解释见下方框架对应表和变量字典。

## 论文分析框架与变量考证依据
论文使用两个相互衔接的框架：Table 1 的**六类全局分析维度**覆盖全部 **337 届**；**七项能力评估条目**用于具有新兴 AI 目标的 **61 届**，保留 **93 条届次—目标记录**。六类全局维度中的“新兴 AI 目标”本身又包含六个可重叠的目标标签，见上表。七项条目覆盖基础模型、视觉—语言、推理等目标，并非仅针对 30 届基础模型导向比赛。

以下用 **`I.` 表示 `data/analysis_inventory.json` 中的一行，`C.` 表示单个比赛 JSON 内的 `challenge` 对象**。两者仅为说明中的缩写，不是额外 JSON 键。组名涵盖其嵌套字段，`[]` 表示列表元素。表中列出考证时使用的字段及解释规则，不要求每届比赛都有全部字段；原始信息、审查决策与统一分析标签分别解释。

### 六类全局分析维度

| 论文维度 | 纳入考证的变量 | 证据依据与解释范围 |
| --- | --- | --- |
| **1. 比赛身份（Challenge identity）** | `I.edition_id`、`I.year`、`I.conference`、`I.conference_group`、`I.evaluation_host`、`I.host_group`；`C.challenge_id`、`C.challenge_name`、`C.event.series`、`C.event.year`、`C.event.conference`、`C.parent_challenge_id`、`C.record_relationships`、`C.edition_identity_review`、`C.conference_affiliation_review`。 | 官方会议日程和届次网站支持身份、年份与归属；审查记录处理父比赛、赛道及后续出版物的关系。当前索引确定分析纳入。会议归属、提交或评估服务、推理执行方分别解释。[身份字段](docs/variables/identity-event.md)；[届次决策](docs/variables/edition-decisions.md)。 |
| **2. 科学任务与临床范围（Scientific tasks and clinical scope）** | `I.harmonized_task_families`、`I.harmonized_modalities`；`C.task_profile.tasks[].task_id`、`C.task_profile.tasks[].input`、`C.task_profile.tasks[].output`、`C.task_profile.tasks[].role`、`C.task_profile.tasks[].granularity`、`C.task_profile.tasks[].clinical_goal`；`C.clinical_domain.modality`、`C.clinical_domain.organs_or_structures`、`C.clinical_domain.body_region`、`C.clinical_domain.diseases`、`C.clinical_domain.disease_evidence_scope`、`C.clinical_classification_review`。 | 从任务说明、规则及报告核对输入输出、任务角色、模态和明确陈述的解剖/疾病范围。同一届在每个任务族中只计一次，包含明确评估的下游迁移任务；区分参赛输出、辅助任务和评估器代理模型。不能由器官直接推断疾病。[任务字段](docs/variables/tasks-objectives.md)；[临床字段](docs/variables/clinical-scope.md)。 |
| **3. 新兴 AI 目标（Emerging AI objectives）** | `I.emerging_objectives`；`C.task_objective_review.emerging_objectives`、`C.task_objective_review.foundation_model_basis`、`C.task_objective_review.sources`、`C.review_coding.emerging_objectives`、`C.review_coding.task_objective_basis`、`C.review_coding.stage_specific_objectives`、`C.task_profile.tasks[].input`、`C.task_profile.tasks[].output`。 | 依据组织者明确目标、注册方案、赛道规则和评估报告编码六个重叠目标。标签需对应具体任务要求；参赛者自行使用预训练模型不直接建立比赛的基础模型目标，目标标签也不证明能力已经评估或实现。[目标定义](docs/variables/analysis-inventory.md#emerging-objective-label-definitions)；[原始编码](docs/variables/tasks-objectives.md)。 |
| **4. 数据与参考条件（Data and reference conditions）** | `I.development_access`、`I.source_centers`、`I.source_geography_documented`、`I.terms_documented`；`C.dataset.population`、`C.dataset.quantity_unit`、`C.dataset.reported_quantities`、`C.dataset.splits`、`C.dataset.source_datasets`、`C.dataset.center_count`、`C.dataset.independence_note`；`C.labels_and_targets.annotation_source`、`C.data_access`、`C.data_license_review`、`C.resource_characteristics_review.fields.typed_size`、`C.resource_information_review.fields.geography`。 | 数据集说明、访问条款、验证及标注文档支持数量、单位、划分、来源、访问方式与参考信息。多中心采集与独立测试分别判断。可获得的标注/裁决过程用于背景解释，**并未在全部比赛中系统编码，也未纳入定量综合**。[数据集](docs/variables/dataset.md)；[参考标注](docs/variables/labels-targets.md)；[访问许可](docs/variables/data-access.md)。 |
| **5. 比赛与评估协议（Competition and evaluation protocols）** | `I.submission_mechanisms`、`I.final_inference_execution`、`I.final_inference_evidence_scope`；`C.submission.submission_type`、`C.submission.phase_specific_requirements`、`C.submission.runtime_limits`、`C.data_usage_mode.testing`、`C.data_usage_mode.external_data`、`C.resource_protocol_review`、`C.evaluation.tasks[].metrics`、`C.evaluation.tasks[].ranking`、`C.evaluation.metrics[].role`、`C.evaluation.metrics[].weight`、`C.evaluation.phase_execution_evidence`。 | 规则、平台记录、报告及确认信息支持提交物、最终计分阶段、资源条件、指标与排名。区分提交服务、模型执行方、指标计算方；保留任务和阶段。规定限制不等于已确认执行，报告某个指标不等于它进入最终排名。[提交规范](docs/variables/submission.md)；[执行方式](docs/variables/data-execution.md)；[评估字段](docs/variables/evaluation.md)。 |
| **6. 结果与赛后可用性（Outcomes and post-challenge availability）** | `I.completion_status`、`I.completion_basis`、`I.reported_participation_documented`、`I.post_challenge_resources_documented`；`C.assessment_evidence`、`C.evaluation.tasks[].competition_outcome`、`C.participation_statistics`、`C.publication`、`C.resource_information_review.fields.reported_participation`、`C.resource_information_review.fields.post_challenge_resources`。 | 报告、奖项、确认信息和归档资源支持比赛开展、结果、参与、出版物及持续资源。注册数和提交尝试不直接作为活跃团队数；计划发布、访问政策与实际可用性分别记录。赛事完成不代表全部组件均完成评估。[参与与资源](docs/variables/participation-resources.md)；[出版物](docs/variables/publications.md)；[结果证据](docs/variables/assessment-evidence.md)。 |

30 届基础模型导向比赛另有资源政策矩阵，记录共享权重、共同初始化、外部数据、参数适配、监督预算、时间和 GPU 约束（SM8）。这些政策变量与下述七项能力评估条目分别编码；完整政策矩阵未包含在本 JSON 包内。

### 七项能力评估条目

本框架对应论文“Emerging AI objectives and assessment evidence”方法部分及补充方法 SM7。七项是跨来源综合得到的**分析条目**，不代表每个比赛 JSON 都有七个同名标准键。下表列出原始 JSON 的考证入口，专项账本则保留综合后的目标级和组件级状态。

| 条目 | 纳入考证的包内变量 | 判断所需证据 |
| --- | --- | --- |
| **1. 预期能力（Intended capability）** | `I.emerging_objectives`；`C.task_objective_review.emerging_objectives`、`C.task_objective_review.foundation_model_basis`、`C.review_coding.task_objective_basis`、`C.task_profile.tasks[].clinical_goal`、`C.task_profile.tasks[].input`、`C.task_profile.tasks[].output`。 | 组织者提出的能力目标，且能关联到具体任务，如表征迁移、图像支撑的生成或证据关联推理。同一届多个目标分别保留。[任务与目标](docs/variables/tasks-objectives.md)。 |
| **2. 评估终点（Assessment endpoint）** | `C.task_profile.tasks[].task_id`、`C.task_profile.tasks[].output`、`C.task_profile.tasks[].endpoint_scope`、`C.evaluation.tasks[].metrics`、`C.evaluation.tasks[].design_status`、`C.evaluation.metrics[].name`、`C.evaluation.metrics[].task`、`C.evaluation.tasks[].ranking`。 | 能力对应的输出、指标或评估程序，以及任务/阶段。规则、任务说明和评估代码可以建立“已规定”，不要求已有分数。解析或 VQA 结果不能证明另外提出的生成或解释任务已经评估。[评估字段](docs/variables/evaluation.md)。 |
| **3. 证据定位与关联（Evidence grounding）** | `C.task_profile.tasks[].output`、`C.labels_and_targets.target_entity`、`C.labels_and_targets.annotation_source`、`C.evaluation.tasks[].metrics`、`C.evaluation.metrics[].name`、`C.evaluation.tasks[].evidence_scope`、`C.assessment_evidence`。 | 从任务/指标定义和组件结果确认输出是否与图像、区域或检索证据建立了被评估的联系；不能只看指标名，普通答案准确率或文本相似度不足以证明 grounding。[REG2 JSON](data/challenges/MICCAI/2026/reg2-2026.json) 中的视觉 grounding 指标记录了评估设计，该字段本身不证明已执行。[标签目标](docs/variables/labels-targets.md)；[评估证据](docs/variables/assessment-evidence.md)。 |
| **4. 临床评估（Clinical assessment）** | `C.evaluation.tasks[].metrics`、`C.evaluation.additional_assessments`、`C.evaluation.additional_assessments.expert_radiologist_assessment.declared`、`C.evaluation.additional_assessments.expert_radiologist_assessment.performed`、`C.evaluation.additional_assessments.expert_radiologist_assessment.execution_status`、`C.assessment_evidence`。 | 分开判断“临床专家对模型输出的评价”和“临床内容/错误评价”；后者可以自动化。核对评审者资格、受评输出、概念/错误类型和结果。临床参考标注或 LLM 评分不能替代人工临床专家评价。radiologist 路径是个别比赛的实际字段，不是全体通用键。[评估证据](docs/variables/assessment-evidence.md)；[附加评估](docs/variables/evaluation.md)。 |
| **5. 泛化测试（Generalization testing）** | `C.dataset.source_datasets`、`C.dataset.downstream_datasets`、`C.dataset.splits`、`C.dataset.center_scope`、`C.dataset.independence_note`、`C.evaluation.additional_assessments.boston_external_testing.declared`、`C.evaluation.additional_assessments.boston_external_testing.performed`、`C.evaluation.additional_assessments.boston_external_testing.execution_status`、`C.assessment_evidence`。 | 明确迁移对象及开发阶段未见的数据、机构或域。描述性条目可包含跨任务迁移和留出样本；Figure 7 的独立机构/域外统计要求与开发来源明确分离。多中心或隐藏测试集本身不足以建立独立测试。Boston 字段是 VLM3D 专用示例，须保留届次范围。[数据集](docs/variables/dataset.md)；[评估](docs/variables/evaluation.md)。 |
| **6. 执行证据（Execution evidence）** | `C.assessment_evidence.execution_evidence[].task_id`、`C.assessment_evidence.execution_evidence[].phase`、`C.assessment_evidence.execution_evidence[].status`、`C.assessment_evidence.execution_evidence[].scope`、`C.assessment_evidence.execution_evidence[].source_url`、`C.evaluation.phase_execution_evidence`、`C.evaluation.final_assessment_evidence`。 | 组织者或参赛者报告、评估记录或明确确认，须支持**同一已规定评估**实际执行。保留任务、阶段及限定，明确未执行与证据缺失分别记录。`I.completion_status` 全局完成状态或仅有方案依据的 `I.final_inference_execution` 最终推理分类不能替代组件执行证据。[执行与结果](docs/variables/assessment-evidence.md)。 |
| **7. 结果证据（Outcome evidence）** | `C.assessment_evidence.outcome_evidence`、`C.assessment_evidence.track_results`、`C.assessment_evidence.award_outcomes`、`C.evaluation.tasks[].competition_outcome`、`C.evaluation.tasks[].outcome_evidence_ids`、`C.evaluation.tasks[].qualification`。 | 与该评估对应的分数、分析发现、名次、任务奖项或直接确认结果。组合分数可支持明确包含的组件，但不分离组件贡献；详细公开结果另行记录。论文筹备状态或笼统的比赛结束陈述不构成结果证据。[结果字段](docs/variables/assessment-evidence.md)；[任务级评估](docs/variables/evaluation.md)。 |

### 专项账本字段与本包覆盖范围

以下文件属于**独立的能力评估审查账本，未包含在本 ZIP 中**，在此列出列名用于说明论文框架的实际编码依据。单个 JSON 中 `C.assessment_evidence` 缺失或为空，不意味着专项审查没有找到证据；专项分析还使用单独的来源目录和账本。因此，仅靠本包 JSON 不能完整复现 Figure 7 的组件证据计数。

| 专项文件与分析单位 | 对应字段 |
| --- | --- |
| `edition_evidence.csv`：61 条届次记录 | `edition_id`、`year`、`objectives`、`intended_capability`描述预期能力；`evidence_scope`、`source_ids`、`review_date`、`review_method`记录范围、来源和审查方法。 |
| `objective_evidence.csv`：93 条届次—目标记录 | `edition_id`、`objective`建立目标关联；`endpoint_state`、`specified`表示评估规定；`execution_state`、`executed`表示执行；`outcome_state`、`outcome_information`表示结果。`detailed_public_result_state`、`detailed_public_results`、`outcome_information_scope`、`scope`、`source_ids`保留公开详细结果和证据范围。 |
| `component_evidence.csv`：305 条届次—组件记录 | `assessment_component`标识目标相关、grounding、临床专家、临床内容/错误、独立机构/域外五类组件。`specification_state`/`specification_finding`、`execution_state`/`execution_finding`、`outcome_state`/`outcome_finding`分开记录三个证据阶段；`counted_specified`、`counted_executed`、`counted_outcome_information`、`counted_detailed_public_results`是汇总标志。`detailed_public_result_state`、`outcome_information_type`、`outcome_information_scope`、`assessment_scope_and_rationale`、`source_ids`、`source_urls`、`review_date`保留结果类别、判断理由及来源。 |

**305 = 61 届 × 5 类组件**，表示文档审查记录数，不是执行了 305 次评估。七项条目对应 Figure 7 的五行覆盖统计：预期能力关联目标和终点，临床评估拆为人工专家与临床内容/错误，执行及结果作为每个组件的独立阶段。同一行须先有明确评估规定，后续证据须对应同一评估；每届在每个组件中最多计一次，不意味着其全部目标都已评估。四类文档状态为“已记录且可分类、含糊、未建立、不适用”；明确未执行与缺失证据分别记录。这些状态不构成质量等级，也不是每场比赛都必须具备的检查清单。

### 如何追溯考证依据

从索引中的届次标识进入单个记录，再结合 `C.provenance.field_evidence`、`C.provenance.sources[].url`、`C.provenance.sources[].type`、`C.provenance.sources[].supports`、`C.provenance.sources[].reviewed_on`、`C.provenance.sources[].qualification`以及具体任务/阶段的来源和判断理由核对。`I.source_urls`提供精简来源列表。这些字段说明来源支持哪些陈述及其限制，字段存在本身不证明已经核实或实际执行。[来源与溯源说明](docs/variables/sources-provenance.md)。

例如，[VLM3D 2026](data/challenges/MICCAI/2026/vlm3d-2026.json) 的 `assessment_evidence.track_results`保留赛道结果，而 `evaluation.additional_assessments` 中 Boston 外部测试和放射科专家评价仍保留未确认执行状态。需连同届次和审查日期解读，不能将赛道结果直接推广到另一个组件、阶段或年份；组件被评估与其是否进入最终排名也要分别判断。

## 变量字典

变量定义已按主题拆分为独立文件。点击下列分类可查看字段、实际类型、含义和适用范围。各页面标明 JSON 父路径，并提供返回 README 的链接。建议先查看[字典阅读规则](docs/variables/conventions.md)，了解列表路径、单位与缺失值的解释方式。

[完整字段 CSV](docs/field_catalog.csv)包含独立比赛记录、索引、分析清单和打包审查元数据中 **4,595 个实际命名字段路径**的定义、类型、单位或格式、示例及记录出现次数。这些是嵌套字段路径，并非 4,595 个独立分析变量。公共备注和采集模板字段另有下方对应文档。

### 比赛 JSON 变量

| 分组 | 内容 |
| --- | --- |
| [记录身份、会议与组织者](docs/variables/identity-event.md) | 记录顶层结构、比赛身份、会议归属、组织者与关联记录。 |
| [临床范围与影像模态](docs/variables/clinical-scope.md) | 解剖范围、疾病背景、影像采集模态及统一分类。 |
| [任务、输出与新兴 AI 目标](docs/variables/tasks-objectives.md) | 任务与赛道、参赛输出、任务族编码及组织者定义的目标。 |
| [标签、目标与参考标注](docs/variables/labels-targets.md) | 目标定义、标签映射与参考标注流程。 |
| [数据集、队列与数量](docs/variables/dataset.md) | 人群、数据划分、采集条件、机构、数量及其原始单位。 |
| [数据访问、许可与使用权限](docs/variables/data-access.md) | 访问要求、发布条件、数据许可与复用权限。 |
| [数据流转与执行方式](docs/variables/data-execution.md) | 数据与模型交换、推理执行以及分阶段访问协议。 |
| [评估、指标、排名与结果](docs/variables/evaluation.md) | 评分程序、指标、排名规则及保留来源范围的结果证据。 |
| [能力评估证据](docs/variables/assessment-evidence.md) | 评估规定、执行、结果、证据定位与关联、临床评估及迁移范围。 |
| [提交规范与运行限制](docs/variables/submission.md) | 提交物、平台、最终阶段执行、运行时间、内存和提交限制。 |
| [日程与比赛阶段](docs/variables/schedule.md) | 阶段日期、截止时间、修订、日期来源及时区说明。 |
| [出版物与参赛方法证据](docs/variables/publications.md) | 相关论文、出版状态、文献线索与参赛方法来源。 |
| [参与情况与后续资源](docs/variables/participation-resources.md) | 注册数、团队、提交次数、来源地理信息及赛后资源。 |
| [来源、溯源与字段审查](docs/variables/sources-provenance.md) | 网址、证据记录、审查日期、字段级依据与原始档案引用。 |
| [届次认定与分析纳入](docs/variables/edition-decisions.md) | 届次记录协调、会议归属、资格与纳入决策。 |
| [历史分类与方案修订](docs/variables/history.md) | 已替代的分类、早期方案与历史提交安排。 |

### 索引、分析与文档变量

| 分组 | 内容 |
| --- | --- |
| [路径、类型、单位与缺失值](docs/variables/conventions.md) | 各类字段定义的阅读规则。 |
| [记录索引](docs/variables/index.md) | 纳入标志、届次标识、文件路径与校验值。 |
| [统一分析变量](docs/variables/analysis-inventory.md) | 337 届纳入比赛的统一分析变量及新兴目标标签。 |
| [公共备注](docs/variables/shared-notes.md) | CN01–CN07 标识对应的定义。 |
| [共用采集规则](docs/variables/collection-template.md) | 原始模板元数据、填写规则及候选标签字段。 |
| [打包审查变量](docs/variables/packaging-review.md) | 逐记录清理变量和审查汇总字段。 |

## 来源与引用

每条记录提供组织者文档和相关出版物的链接，来源日期与审查历史保留在[溯源字段](docs/variables/sources-provenance.md)中。

使用单条记录时，请引用对应的原始来源；使用整个数据集或其分析分类时，请同时引用相关综述。欢迎提交更正，并附上届次标识、字段、建议修改及支持来源。
