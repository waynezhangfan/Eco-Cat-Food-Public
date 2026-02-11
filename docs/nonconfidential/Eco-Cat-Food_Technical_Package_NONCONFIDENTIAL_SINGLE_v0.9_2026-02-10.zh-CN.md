# Eco‑Cat‑Food — 非保密技术包

> 语言：中文 | English: [`Eco-Cat-Food_Technical_Package_NONCONFIDENTIAL_SINGLE_v0.9_2026-02-10.en-US.md`](Eco-Cat-Food_Technical_Package_NONCONFIDENTIAL_SINGLE_v0.9_2026-02-10.en-US.md)

版本：v0.9‑ZH

日期：2026-02-10

受众：技术尽调/科研合作方（技术团队 / 投资方技术顾问）

保密级别：**非保密（NON‑CONFIDENTIAL）— 可对外分享**

联系人：[Wayne Zhang](https://www.linkedin.com/in/waynezhangfan)

---

**重要声明（请先读）**

- 本项目当前处于**纯理论/规划阶段**：截至本文档日期，我们**尚未获得任何体外或体内实证数据**；路线科学可行性与安全性均**未知**。
- 本非保密技术包仅用于展示我们如何把研发拆解为**可审计的 Gate 流程与交付物**（“治理与审计成熟度”），并明确哪些关键科学问题仍为“零数据待验证”。
- 本文件**不构成**任何关于**有效性、安全性、跨物种选择性、可逆性、外场可行性**的证明或暗示；对外沟通必须遵守第 8 节的 Evidence & Claims Policy。
- **版本一致性要求**：引用/转述本文件时必须同时给出 **版本号 + 日期**。

本文件覆盖的非保密内容（不含任何阈值数字）：
- 可审计的阶段闸门（Gate）研发流程；
- 明确的交付物结构与验收口径（以模板/字段级形式表达，而非口号式描述）；
- 对“不可控摄入（不限量投喂）”与“非目标暴露”的结构性风险治理口径；
- 对外主张的证据分级与变更控制；
- Gate 4/6 的对外交付包结构与字段模板、P0 风险最小证伪表、追溯 ID/变更控制模板与流程图（均不含结构/合成/配方/阈值数字）。

## 本文件**不包含**且不会对外分发：

- 化学结构/SMILES、SAR 图谱、命中化合物清单、合成路线与工艺细节；
- 配方与含量规格、投喂/剂量指令、任何可直接执行的外场投喂操作细节；
- 原始实验数据集、完整统计分析输出、CRO SOW/报价、供应商与具体场地信息；
- 全文论文/PDF、截图、抽取图表（对外仅提供 DOI 元数据与公开可核查来源）。

---

## 目录
- 0. 非保密可核查的清单
     * 版本与变更记录（非保密）
- 1. 项目概述（非保密）
     * 当前成熟度（双轴：治理成熟度 vs 科学证据成熟度）
- 2. 研发流程总览：Phase 0–7（可审计 Gate 地图）
- 3. Process specifics：Freeze→Run→Review→Audit（标准化闭环）
- 4. Gate 1（体外闭环）— 交付物、字段字典、验收口径（非保密）
- 5. 不可控摄入与“场景所需安全窗”（Dose/Exposure Model）
- 6. B 标准（健康/行为不变）治理：端点框架、停线逻辑、审计要点
- 7. 以猫为目标物种（target species）/非目标影响最小化治理：功能选择性 + 最坏暴露
- 8. 证据与对外主张政策（Evidence & Claims Policy）
- 9. 监管与伦理路径假设（非保密）
- 10. 可在 NDA 下提供的补充包（范围说明）
- 11. 参考文献（仅 DOI 元数据）
- 附录 A：Gate 1 标准化结果表（TSV）模板（字段级）
- 附录 B：Gate 决策备忘录模板（对外可审计结构）
- 附录 C：外场摄入/体重 pilot 数据表模板（字段级）
- 附录 D：第三方 30 分钟快速审计清单（非保密）
- 附录 E：Gate 4（暴露与摄入校准）交付包结构 + Dose Model 输入表模板（字段级）
- 附录 F：Gate 6（受控喂食 B 标准）交付包结构 + AE/SAE 与行为评分模板（字段级）
- 附录 G：追溯 ID 与变更控制模板（非保密）
- 附录 H：Claims Register（主张登记册）模板（字段级）
- 附录 I：DOI 元数据核验记录模板（字段级）

---

# 0. 非保密可核查的清单

本项目目前处于理论/规划阶段；主要体现为：**可执行、可审计的研发治理与交付体系**（而非实验结果）。

## 0.1 版本与变更记录（非保密）

为保证对外引用一致性，本文件提供最小可审计的变更记录（不包含任何保密细节）：

| change_id | from_version | to_version | date | 变更摘要（非保密） | affected_clm_ids | owner |
|---|---|---|---|---|---|---|
| CHG‑NC‑20260209‑001 | v0.4‑ZH | v0.5‑ZH | 2026-02-10 | 增补零数据硬限定语与成熟度双轴；补齐跨物种可比性最低判据、外场 pilot 可审计性最低口径、K_required 形式化定义、B 标准审计级定义、REG‑Gate；修正文献表占位题名。 | policy‑level（全局口径/模板） | CTO |
| CHG‑NC‑20260210‑001 | v0.5‑ZH | v0.6‑ZH | 2026-02-10 | 增补 Claims Register 模板；冻结 K_required 的主判据暴露指标选择规则；补齐桥接对照最低类别要求与 Gate 1 排假阳性强制项清单；补齐 B 标准最小时间窗结构；新增 DOI 元数据核验流程与记录模板；补充法域选择原则（类别级）；将“猫靶向”对外措辞改为“目标物种为猫（target species）+ 非目标治理”。 | policy‑level（全局口径/模板） | CTO |
| CHG‑NC‑20260210‑002 | v0.6‑ZH | v0.7‑ZH | 2026-02-10 | 将审计规则同步落到字段字典：结果表新增可比性/桥接/假阳性 flags；冻结 Dose Model 输入依赖结构与主判据分位集合；补齐 Claims Register 审批链条字段。 | policy‑level（全局口径/模板） | CTO |
| CHG‑NC‑20260210‑003 | v0.7‑ZH | v0.8‑ZH | 2026-02-10 | 为避免执行阶段口径漂移：补齐 flags 字段受控词表（controlled vocabulary）；新增 `bridging_level` 字段并将桥接强弱分级落到结果表；消除 p99 “示例措辞”与“主判据固定 p99”的文字冲突；审计清单去除“非目标无影响”措辞。 | policy‑level（全局口径/模板） | CTO |
| CHG‑NC‑20260210‑004 | v0.8‑ZH | v0.9‑ZH | 2026-02-10 | 执行发布前 DOI 元数据核验并落盘核验记录（Crossref 公开来源）；同步修正 References 的题名/年份与核验来源一致。 | EVD‑NC‑001~013 | CTO |

在非保密范围内，我们已经形成/冻结了：

- **阶段闸门（Gate）地图**：Phase 0–7 的目的、关键输出、主要停线类别（第 2 节）。
- **标准化闭环流程**：Freeze→Run→Review→Audit 的统一口径与变更控制要求（第 3 节）。
- **Gate 1 交付物结构**：数据包目录结构与“必须交付原始数据+元数据”的硬要求（第 4.2 节）。
- **Gate 1 结果表字段字典**：用于跨批次/跨 CRO 汇总的字段集合（第 4.3 节 + 附录 A）。
- **Gate 决策备忘录模板**：确保结论、不可外推边界、后续补证与停线理由可审计（附录 B）。
- **不限量投喂的校准思路**：外场 pilot 的输出目标（分位数）与升级规则（第 5.2 节 + 附录 C）。
- **Gate 4 交付包结构（暴露/摄入校准）**：交付包目录结构与 Dose Model 输入表模板（第 5.4 节 + 附录 E）。
- **Gate 6 交付包结构（受控喂食）**：AE/SAE 事件日志与行为评分模板（第 6.5 节 + 附录 F）。
- **追溯 ID 与变更控制模板**：对外主张/证据/Gate 决策之间的可追溯关联规则（第 8.5 节 + 附录 G）。
- **B 标准治理框架**：端点类别、AE/SAE 与停线规则“先冻结、后执行”的原则（第 6 节）。
- **目标物种为猫（target species）/非目标治理口径**：跨物种功能选择性 + 最坏暴露框架 + 对外主张纪律（第 7 节）。
- **证据分级与对外主张政策**：不虚构、不外推、证据等级与主张分类（第 8 节）。
- **Claims Register（主张登记册）模板**：对外表述的可执行载体（第 8.6 节 + 附录 H）。
- **DOI 元数据核验流程与记录模板**：对外引用可核查留痕（第 8.7 节 + 附录 I）。

---

# 1. 项目概述

Eco Cat Food 是一个研发项目，探索通过 **FSHR（促卵泡激素受体）小分子拮抗**实现猫避孕，并考虑以猫粮作为递送载体。

当前状态：**纯理论/规划阶段**。

本非保密技术包不包含任何实验数据集，也不对外宣称已验证有效性/安全性。

我们把三个难点作为必须被流程化治理的工程约束：
1) **不可控摄入**：个体摄食量/体重差异导致暴露跨度大；
2) **B 标准共主要**：避孕效果必须与“无临床显著健康/行为不良信号”同时满足；
3) **目标物种为猫（target species）/非目标暴露**：投喂方式导致雄猫与非目标物种暴露不可完全避免，因此必须尽早量化跨物种功能选择性，并以最坏暴露做安全治理。

## 1.1 当前成熟度（双轴：治理成熟度 vs 科学证据成熟度）

为避免外界把“流程成熟”误读为“科学已验证”，我们把项目成熟度拆成两条互相独立的轴：

- **治理/审计成熟度（G‑Maturity）**：Gate 地图、交付物结构、字段字典、证据分级、变更控制与审计闭环是否已成体系、可执行到文档层面。
- **科学证据成熟度（S‑Maturity）**：是否已获得可复核的体外/体内数据来支持有效性、安全性、跨物种选择性、可逆性与外场可行性等关键结论。

我们在非保密范围内公开的结论仅限于：**G‑Maturity 方面已具备可审计的设计与模板**；而 **S‑Maturity 目前为“零数据待验证”**。

当前状态（截至 2026-02-10）：
- G‑Maturity：已形成 Gate 0–7 的治理框架与关键交付物模板（本文件 + 附录）。
- S‑Maturity：**0（零实验数据）**。任何科学结论只能作为待检验假设陈述，不对外暗示“已验证/接近落地”。

---

# 2. 研发流程总览：Phase 0–7（可审计 Gate 地图）

我们采用“里程碑冻结（Freeze the rules first）+ 阶段闸门评审（Gate review）”的方式推进。

本对外版本仅用**类别口径**描述推进/停线逻辑；涉及具体数字阈值的内容仅在 NDA 包中提供。

## 2.1 Gate 地图（非保密版）

| Phase | 目的 | 关键输出 | 主要停线理由（类别） |
|---|---|---|---|
| 0 治理/审计 | 防止口径漂移与数据不可审计 | 证据等级与主张分类；数据交付规范；变更控制 | 无法提供原始数据/不可复核交付 |
| 1 文献骨架 | 把“主张”改写成“可检验假设” | DOI 元数据清单；假设→最小补证映射 | 高风险主张被当作结论对外传播 |
| 2 Gate 1 执行包冻结（理论） | 避免“先做化学再找读数” | Gate 1 问题清单；交付物结构；QC 类别；推进/停线规则（类别） | Gate 1 无法形成闭环（效力/机制/选择性/排假阳性） |
| 3 Gate 1 体外数据 | 建立可审计体外闭环 | 功能拮抗、机制分类、跨物种功能选择性、假阳性过滤的数据包 | 信号不可复现；疑似假阳性；跨物种分离不足 |
| 4 暴露与摄入校准 | 把“不限量投喂”变成可计算约束 | 摄入/体重分布（分位数）；混饲暴露校准；场景所需安全窗（K_required） | 场景所需安全窗远超可实现范围 |
| 5 Hit→Lead/优化 | 用数据驱动化学迭代 | 迭代回路（目标函数/停线规则）；候选优先级 | 达不到进入更高风险阶段所需的选择性/稳健性 |
| 6 受控小样本喂食 | 验证 B 标准与可逆性假设 | 受控喂食安全/行为包设计与审计结果 | B 标准出现不可接受不良信号 |
| 7 外场试点 | 验证场景可行性与可审计性 | 外场试点设计、污染/缺失治理、结果可审计报告 | 外场推断不可审计/污染严重 |


## 2.2 P0 风险与最小证伪（非保密）

下表把最关键的结构性风险（P0）与最小证伪/补证动作绑定，目的是尽早判断该路线在不限量投喂与非目标暴露约束下是否值得继续投入。

| 风险（P0） | 为什么是 P0 | 最小证伪/补证（类别） | 触发停线/升级条件（类别） |
|---|---|---|---|
| 不可控摄入导致 K_required 过大 | 可能结构性不可行 | 外场 pilot 产出 intake/BW 分位数并回灌 Dose Model 做情景分析 | 若 K_required 明显超出可实现范围：停线或必须改变场景约束 |
| 跨物种功能选择性不足 | 非目标误食/接触链难闭合 | cat/dog/human FSHR 同平台功能读数 + 相关受体 counterscreen | 若在可比体系下无法形成稳定分离：停线或转入更严格验证/替代策略 |
| B 标准被击穿（健康/行为） | 共同主要（co‑primary）失败即 NoGo | 受控喂食小样本：AE/SAE + 行为评分（盲法优先） | 若出现临床显著不良信号：停线或回到机制/暴露控制 |
| 特殊人群暴露风险（幼猫/孕/哺乳） | 外场难以排除暴露 | 将相关表述严格降级为假设；在进入外场前冻结监测/停线与最小补证路径 | 若无法给出可审计的风险治理与补证路径：不得进入外场 |
| 可逆性/停喂恢复不达标 | 决定产品画像与合规风险 | 预先定义可逆性判据（类别）并在受控喂食阶段验证 | 若无法满足预先定义口径：调整目标或停线 |
| 外场推断不可审计（缺失/污染/识别） | 做了也难形成可信结论 | pilot 演练识别/失访/污染治理 + 冻结缺失处理与污染规则 | 若缺失/污染无法在审计意义上控制：不得进入外场 |
| 含量波动/稳定性导致暴露尖峰 | 放大最坏暴露风险 | 质量/均匀性/稳定性验证方案与放行规则（类别） | 若无法形成可审计的质量控制窗口：不得进入外场 |

注：P0 风险对应的详细字段模板见附录 C/E/F；具体阈值数字仅在 NDA 包中提供。


---

# 3. Process specifics：Freeze→Run→Review→Audit（标准化闭环）

外部所说的 “process” 往往包含三类流程：研发流程、投喂/暴露治理流程、证据与审计流程。我们用同一套四步闭环把它们固化下来：

## 3.1 Freeze（先冻结规则）
在每个 Gate 开始前冻结：
- **问题清单**：本阶段必须回答什么；
- **交付物结构**：交付包的目录/表格/字段（便于审计与外包验收）；
- **QC 与数据合格口径**：哪些数据只能探索性参考，哪些可用于 go/no‑go 决策；
- **推进/停线类别逻辑**：触发停线/补做/重复/升级验证的条件类别；
- **变更控制**：任何变更必须记录“变更原因、影响评估、批准人、版本号”。

## 3.2 Run（按冻结方案执行）
执行阶段的硬要求（第三方可审计的设计原则）：
- **原始数据必交付**：例如 plate 原始读数、plate map、时间戳、分析软件版本与拟合参数；
- **可重复性设计**：包含独立实验日/重复批次的验证思路；
- **对照与反筛**：并行设计假阳性过滤与相关受体/通路干扰检查；
- **跨物种可比性**：跨物种功能比较尽量采用可比实验格式，减少“不可比带来的假选择性”。

## 3.3 Review（标准化 Gate 评审输出）
每个 Gate 的评审输出固定为三类之一：
- **通过（Pass）**：进入下一 Gate；
- **条件通过（Conditional Pass）**：完成预先定义的补证/重复/机制澄清后再推进；
- **停线（Stop）**：停止投入，原因必须能映射到冻结的停线类别。

评审记录必须包含：
- 本阶段结论（pass/conditional/stop）与证据等级；
- 不可外推点（不能从这些数据推到哪些结论）；
- 下一阶段最小前置条件（最小补证）。

## 3.4 Audit（第三方如何复核）
对第三方复核最友好的最小要求：
- 交付包中有 `README`（数据字典、版本、生成步骤）；
- 关键表格使用可 diff 的 TSV/CSV；
- 数据与结论之间存在可追溯链接（例如结果表字段→QC→决策备忘录）。


## 3.5 流程图（文本版）

每个 Gate 都按 Freeze→Run→Review→Audit 的闭环执行：

Freeze（冻结问题清单/交付物结构/QC 与停线逻辑）
  → Run（生成原始数据 + 元数据，形成标准化结果表）
  → Review（形成 Gate 决策备忘录：Pass / Conditional Pass / Stop）
  → Audit（第三方可复核：数据字典、版本、可追溯链接、变更控制）

Phase/Gate 的关系（高层级）：

- Phase 0/1：治理与证据体系（对外主张纪律）
- Gate 1：体外闭环（效力/机制/选择性/排假阳性）
- Gate 4：摄入/体重与暴露校准 → K_required（场景约束）
- Gate 6：受控喂食验证 B 标准与可逆性（在数据支持后启动）
- Gate 7：外场试点（以可审计性为前提）

---

# 4. Gate 1（体外闭环）— 交付物、字段字典、验收口径（非保密）

Gate 1 的目标是建立最小、可审计的体外闭环，防止“没有可复现读数就开始化学优化”。

## 4.1 Gate 1 必须回答的四类问题
1) **效力**：猫 FSHR 上是否存在可复现的功能拮抗信号？
2) **机制**：能否区分竞争/正构位点 vs 别构/非竞争等机制类型？
3) **跨物种功能选择性**：猫 vs 非目标物种（至少犬/人）的功能分离是否存在并可重复？
4) **排假阳性**：毒性/检测干扰/通路干扰等是否被系统性排除？

## 4.1.1 跨物种“可比性”的最低冻结判据（类别级｜非保密）

为避免出现“体系不可比导致假选择性”，凡用于对外或 Gate 决策的跨物种功能比较，必须满足以下**方法学类别**要求（不含任何数值阈值）：

- **同平台/同主读数**：猫/犬/人采用同一类功能读数平台（例如同类 cAMP 读数），并共享同一数据处理与曲线拟合流程。
- **刺激条件冻结**：刺激配体/剂量设定原则必须冻结；若因物种差异必须使用不同配体或不同激动强度，需提供**桥接对照**来证明可比性（否则该比较不得用于选择性主张）。
- **表达与系统记录**：记录受体构建体、表达系统、表达水平的类别信息；避免仅因过表达/系统差异导致的表观选择性。
- **板内/批间桥接对照**：每批次包含可比的阳性/阴性对照与参考化合物（用于漂移监控与批间桥接）。
- **一致的 QC 分级**：跨物种数据的 QC 口径一致；任何未达成“决策级数据”的结果不得用于选择性结论。
- **偏差处理**：若存在关键偏差（平台、刺激、系统、分析流程不一致），必须在结果表中标记为 `qc_grade != decision‑grade` 或 `comparability_flag = not_comparable`（字段名可在 NDA 包中细化），并触发升级验证而非直接推进。

## 4.1.2 桥接对照（bridging controls）的最低类别要求（非保密）

跨物种可比性必须通过“桥接对照”落到可审计的执行层。非保密范围内冻结最低要求（类别级）：

- **参考化合物桥接**：设置至少 1 个“跨物种共享的参考化合物”（reference compound），用于监控体系漂移与批间/板间桥接（不要求对外公开该化合物身份）。
- **对照桥接**：每批次至少包含阳性/阴性对照与参考化合物的关键浓度点/曲线（类别级），用于判断“该批次数据是否可用于跨物种比较”。
- **桥接方式分级**（从强到弱）：
  1) 同日/同板跨物种桥接（理想，漂移最小）；
  2) 同日跨板桥接（需记录板间校准与批次信息）；
  3) 不同日桥接（仅在有稳定参考与 QC 记录时允许，且必须保守解读）。
- **not comparable 的强制判定条件（类别级）**：出现以下任一情况时，该批次跨物种比较必须标记为 `not_comparable`，不得用于“选择性”主张：
  - 缺失桥接对照（参考化合物或关键对照缺失）；
  - 桥接对照未达成冻结的 QC 类别要求；
  - 刺激条件/分析流程发生关键偏差且无有效桥接证明可比。

## 4.1.3 Gate 1 排假阳性强制项清单（类别级｜非保密）

为避免“看起来有效但其实是体系假象”的误推进，Gate 1 的排假阳性至少包含以下**强制检查类别**（不含具体阈值与操作细节）：

- **细胞/体系毒性与活性下降趋势**（与主读数同体系或可桥接体系）；
- **检测体系干扰**（例如发光/荧光/报告基因/读板干扰等类别）；
- **样品物性问题**（溶解性、沉淀/析出、聚集体/胶束等可能导致假信号的类别）；
- **非特异通路扰动/膜破坏类效应**（导致表观拮抗的类别风险）；
- **化学警戒结构类别**（反应性/假阳性富集片段等；仅做类别标注与处置原则，不在非保密版列出具体结构规则）。

触发升级/停线的冻结口径（类别级）：
- 任一强制项出现“高风险信号” → 该数据不得作为决策级依据，必须触发第二读数/正交验证或停线；
- 无法通过升级验证澄清 → 标记为 `invalid` 并停线或回到化学与体系层面重构。

## 4.2 Gate 1 交付包

对外不提供数据，但可明确交付包结构（用于外包验收与审计）：

- `Gate1_Deliverable_Package/`
  - `README.md`（版本、实验批次、数据字典、生成步骤）
  - `Protocols/`（简版：实验概述、对照设置、QC 指标类别；详细数字阈值在 NDA 版）
  - `RawData/`（原始每孔读数、plate map、时间戳；可为导出表或受控格式）
  - `Analysis/`（曲线拟合参数、软件版本、拟合策略说明）
  - `QC/`（QC 汇总表：哪些数据是决策级，哪些仅探索级）
  - `Results/`（标准化结果 TSV：化合物 × 实验 × 物种/受体/读数）
  - `Decision/`（Gate 1 决策备忘录：pass/conditional/stop 与原因）

## 4.3 标准化结果表（TSV/CSV）字段示例（非保密）
为保证跨批次/跨 CRO 可汇总，结果表至少包含的字段（不含化合物结构）：
- `compound_id`：化合物编号（去敏化 ID）
- `batch_id`：批次/来源（可匿名）
- `assay_id`：实验编号
- `species`：cat/dog/human/other
- `target`：FSHR/LHR/TSHR/…
- `cell_system`：体系简述（类别即可）
- `readout`：主要读数类型（例如 cAMP/其他）
- `mode`：antagonism / counterscreen / toxicity / interference
- `concentration_unit`：浓度单位
- `ic50` / `pIC50`：效力指标（若数据合格）
- `e_max`、`hill_slope`：曲线参数（若合格）
- `fit_quality`：拟合质量类别（例如 good/acceptable/poor）
- `qc_grade`：数据合格等级（例如 decision‑grade / exploratory / invalid）
- `replicate_n`、`independent_day_n`：重复信息
- `comparability_flag`：跨物种可比性标记（comparable / partial / not_comparable）
- `bridging_control_present_yes_no`：是否具备桥接对照（Y/N）
- `bridging_level`：桥接强度等级（1/2/3/NA；定义见附录 A）
- `bridging_qc_grade`：桥接对照 QC 类别（good / acceptable / poor / missing）
- `interference_flag`：检测干扰风险标记（none / suspected / confirmed / not_assessed；见附录 A）
- `aggregation_flag`：聚集体/物性假阳性风险标记（none / suspected / confirmed / not_assessed；见附录 A）
- `cytotoxicity_flag`：细胞毒性/活性下降趋势标记（none / suspected / confirmed / not_assessed；见附录 A）
- `notes`：异常说明（例如疑似干扰/细胞毒性趋势）

## 4.4 机制分类与“第二读数”触发（非保密口径）

- 若证据提示存在别构/非竞争机制或偏向性信号风险，则要求增加**第二类读数**（非 cAMP）以降低单一读数误推进的概率。
- 第二读数的选择与阈值在 NDA 版冻结；对外仅承诺“存在触发与升级验证路径”。

## 4.5 Gate 1 的停线类别（非保密）
- 不可复现：多批次/多天无法重复得到一致拮抗信号；
- 假阳性风险高：毒性/干扰/通路非特异扰动无法排除；
- 跨物种分离不足：在可比格式下猫 vs 非目标物种无法形成足够分离（早期可探索，但进入更高风险阶段前必须达到更严格标准）；
- 机制风险：机制指向更高系统性风险且无法通过升级验证降风险。

## 4.6 Gate 1 的 QC 指标类别（指标名称公开；阈值 NDA）
- **实验窗口类**：Z' factor（或等价指标）、信号窗/信噪（S/B、S/N）、对照稳定性；
- **重复性类**：对照与关键点位的变异性（CV 类指标）、独立实验日一致性；
- **曲线质量类**：拟合收敛、平台/斜率合理性、是否存在系统性偏差；
- **假阳性过滤类**：细胞毒性/活性下降趋势、检测体系干扰（例如发光/荧光/报告基因干扰的排查路径）、非特异通路扰动；
- **样品质量类**：溶解性/沉淀/聚集倾向的记录与处置（类别口径）。

---

# 5. 不可控摄入与“场景所需安全窗”（Dose/Exposure Model）

## 5.1 为什么必须先建模
不限量投喂意味着个体暴露取决于：
- 摄食量分布（同一站点内也可能跨度很大）；
- 体重分布；
- 猫粮中有效成分含量波动；
- 吸收/清除的个体差异（PK 变异）。

因此我们不把“平均摄入”当作可接受的安全依据，而以高端摄入者（分位数）驱动“场景所需安全窗”。

## 5.2 最小外场 pilot（非保密框架）
目的不是证明有效性，而是校准输入分布，使模型可计算：
- 输出：摄食量与体重的分布特征（建议至少 p10/p50/p90/p99），并记录站点差异与不确定性；
- 质量要求：方法可重复、数据可审计、对缺失与误差有明确处理；
- 升级规则：若无法稳定得到高端分位数，自动升级测量方案（例如从站点级走向个体级粗估）。

### 5.2.1 外场 pilot 的可审计性最低冻结口径（类别级｜非保密）

外场 pilot 的目标是“校准分布”，因此必须优先保证可审计性（否则输出的分位数不可信、无法回灌模型）。在非保密范围内，我们冻结以下最低规则类别：

- **个体识别/重复计量方法分级**：站点级计数只能作为粗校准；若不能产出冻结的高端分位数（p99）或无法解释站点差异，必须升级到可重复识别个体的方案（视频识别/标记等属于可选类别），否则该 pilot 输出不得用于 Gate 决策。
- **缺失与误差的预定义处理**：缺失原因与机制必须分类记录（例如设备/观察缺失、不可识别个体、异常天气等类别），并冻结敏感性分析的类别策略，避免“做完再挑解释”。
- **污染（contamination）事件记录**：任何可能导致个体暴露不可归因的事件类别（例如跨站点迁移、外来投喂、干预中断等）必须记录并进入审计链条；污染严重时应触发升级或停止，而不是事后忽略。
- **版本化与留痕**：测量流程、识别方法、数据处理脚本/规则必须版本化；关键版本变更必须走变更控制并说明对分位数可比性的影响。

## 5.3 “场景所需安全窗（K_required）”的对外定义
- **目的**：把“不限量投喂”的工程约束转化为一个可计算、可审计的“**最低所需安全窗**”要求，用于早期 go/no‑go（而不是靠平均值叙事）。
- **输入（分布/不确定性）**：
  - 体外效力（作为目标暴露/目标占位的起点，含“有效倍数因子”的先验范围）；
  - 摄食量与体重的分布（至少到高端分位数）；
  - 猫粮中有效成分含量波动（批内/批间）；
  - PK 关键参数的变异（吸收/清除/蛋白结合等，按先验分布表达）。
- **形式化定义（不含数字）**：
  - 定义一个“有效暴露目标” `C_target`（例如与体外功能拮抗相关的目标自由浓度；具体倍数仅在 NDA 包中给出）。
  - 在给定投喂场景与输入分布下，模型产生暴露分布 `C`（或 `C_avg`/`C_max` 等，按冻结口径选其一或同时输出）。
  - **K_required** 定义为：为了使高端暴露者仍处于可治理范围，候选分子必须具备的最低安全窗倍数需求。对外采用两种等价输出口径之一（两者都可审计）：
    1) **分位数口径**：`K_required(p) = Q_p(C) / C_target`（`p` 为冻结的高端分位：本文件冻结 Gate 4 主判据为 `p99`，并要求至少同时报告 `p90` 作为敏感性；同时冻结“用哪个 C 指标”）。
    2) **最坏组合口径**：`K_required^WC = max(C | 关键输入取保守上界组合)`，再归一化为 `K_required^WC / C_target`（用于给出上界警戒线）。
- **主判据暴露指标选择规则（类别级｜冻结以防选择性报告）**：
  - 必须同时计算并报告至少两类暴露指标的 `K_required`：基于 `C_avg`（或 AUC 等时间积分指标）与基于 `C_max`（峰值指标）。
  - Gate 4 的决策主判据默认取两者中**更保守（更大）**者，避免“有利就选 C_avg、不利就选 C_max”的选择性报告。
  - 若因机制/风险研判需要指定单一主指标（例如明确为峰值驱动或时间积分驱动），必须在 Freeze 阶段以变更控制方式写清触发条件类别，并在决策备忘录中记录 `change_id` 与影响评估。
- **输入依赖结构/相关性处理冻结口径（类别级｜防止模型“想怎么假设都行”）**：
  - 默认规则：若外场 pilot 与 PK 数据支持“同一只个体的成对观测”（paired observations），则优先采用**数据估计的相关性/依赖结构**（在输出中记录方法版本与不确定性）。
  - 若仅有边缘分布（marginals）而缺少成对观测，则必须同时给出：
    1) **独立性假设**（independent）下的结果（作为基线）；
    2) **保守依赖假设**（conservative dependence）下的结果（作为上界敏感性），并在 Gate 决策中默认取更保守者。
  - 触发升级条件（类别级）：一旦独立性与保守依赖的差异导致 Gate 结论敏感（例如决策在两者之间发生翻转），则必须升级为“成对观测/数据估计依赖结构”的采集方案，否则不得进入更高阶段。
- **主判据分位集合冻结（类别级｜避免事后挑分位）**：
  - Gate 4 必须在冻结的高端分位集合上报告 `K_required(p)`（至少包含 `p90` 与 `p99`），并同时报告 `K_required^WC`（最坏组合口径）。
  - Gate 4 的主判据默认使用 `p99`（并结合 `C_avg` 与 `C_max` 两套口径取更保守者）；`p90` 作为情景敏感性与沟通辅助，不作为主判据替代。
  - 若无法在审计意义上稳定估计 `p99`（样本/识别不足），则按 5.2 的升级规则提升测量方案；在未满足前不得以较低分位替代主判据推进。
- **输出应包含**：`K_required`（按冻结口径）、关键输入的敏感度排序、以及“结构性不可行/需改变场景约束”的判定说明（类别级）。

若 K_required 显著超出候选分子在生物学与药代层面可合理期待的安全窗范围，则结论不是“再做更大试验”，而是**结构性停线或必须改变场景约束**（例如改变暴露分布、改变递送控制能力等）。


## 5.4 Gate 4 交付包结构（暴露与摄入校准｜非保密）

Gate 4 的目的：将“不限量投喂”约束显式化，并产出可用于更新 Dose/Exposure Model 的输入分布与情景分析结果结构（对外不披露具体数值）。

对外可描述的交付包结构：

- `Gate4_Deliverable_Package/`
  - `README.md`（版本、数据字典、生成步骤）
  - `Intake_BW_Pilot/`（方法概述、分位数输出、缺失/误差处理；模板见附录 C）
  - `Exposure_Calibration/`（混饲暴露校准设计概述、样本清单模板；模板见附录 E）
  - `DoseModel/`（输入表模板、情景定义、敏感度分析输出结构；模板见附录 E）
  - `QC/`（数据合格与审计要点）
  - `Decision/`（Gate 4 决策备忘录；模板见附录 B）

Gate 4 的关键输出之一是 K_required（场景所需安全窗需求量级），用于决定是否允许进入更高成本阶段或外场。

---

# 6. B 标准（健康/行为不变）治理：端点框架、停线逻辑、审计要点

B 标准被定义为与有效性并列的共同主要要求：
- **有效性（降低生育力）** 与 **B 标准（无临床显著健康/行为不良信号）** 必须同时满足。

## 6.1 B 标准端点框架（非保密）
- 健康端点（类别）：体重/体况、食欲与饮水、精神状态、常规体征、可观察不适/疼痛信号；
- 行为端点（类别）：活动/探索、攻击/领地相关行为、社交回避/应激、睡眠与异常行为；
- 生殖相关端点（类别）：发情相关行为表型、可逆性观察窗口（作为产品表型的一部分）。

## 6.2 AE/SAE 与停线逻辑（非保密）
- 预先定义 AE/SAE 分级与升级路径；
- 停线规则在执行前冻结，执行中不可事后修改；
- 条件通过与补证必须有明确清单（例如重复、机制澄清、额外监测）。

## 6.3 “允许某些激素变化”的边界口径（非保密）
- 我们不把“激素完全不变”当作前提。
- 例如黄体期/孕酮模式改变在机制上可能发生；是否可接受取决于是否引入**系统性不良后果**，并必须通过预先冻结的监测与停线治理。

## 6.4 B 标准的“审计级定义”（非保密）

B 标准对外可承诺的是“**方法学与治理**”，而不是“结果一定不变”。因此我们把 B 标准的最低可审计定义冻结为以下类别要素（不含任何阈值数字）：

- **行为评分工具版本化**：采用明确的 ethogram/量表（版本号、训练材料、评分说明）并固化到 Protocol 与数据字典；任何版本变更必须走变更控制并评估对历史可比性的影响。
- **观察者训练与一致性**：在正式评分前进行训练与一致性抽样（inter‑rater reliability 的类别判据与复训触发条件冻结）；评分中持续抽样复核，防止漂移。
- **盲法优先**：行为评分与关键判读尽可能采用盲法（至少盲化分组信息）；若无法盲化，必须记录原因并增加独立复核与偏倚控制措施。
- **AE/SAE Dictionary 与归因流程**：预先维护 AE/SAE 事件字典、分级口径与升级路径；建立“报告→分级→归因→裁决→行动（停线/补证/继续）”的审计链条，并记录裁决者角色与版本。
- **“临床显著”的判定流程**：不依赖事后解释；以冻结的判定流程（触发条件类别 + 复核机制 + 决策记录模板）保证结论可复核。
- **数据留痕与可复核性**：行为原始材料（例如视频/时间戳/元数据）与评分表的对应关系可追溯；缺失与异常必须按冻结口径分类与说明。

### 6.4.1 最小时间窗结构（类别级｜非保密）

为避免“可逆性/恢复”被叙事化，B 标准相关的受控研究必须冻结最小时间结构（不含天数，仅冻结结构与原则）：

- **基线期（Baseline）**：干预前的健康与行为基线采集（同一量表/同一观察流程），用于后续对比与个体内变化判读。
- **干预期（Intervention）**：在受控条件下执行干预并持续监测 AE/SAE 与行为端点；任何偏差进入 deviation log。
- **停止后随访/恢复期（Follow‑up / Recovery）**：停止干预后，按预先冻结的观察点类别持续追踪恢复趋势与潜在延迟性不良信号；作为“可逆性假设”是否仍成立的审计基础。

规则：若因现实条件需要改变时间结构或观察点类别，必须在 Freeze 阶段通过变更控制，且在 Gate 决策备忘录中记录 `change_id` 与对可比性的影响评估。


## 6.5 Gate 6 交付包结构（受控喂食：B 标准与可逆性｜非保密）

Gate 6 的目的：在受控条件下验证 B 标准治理框架与可逆性假设，形成可审计的安全/行为数据包（对外不公开原始数据）。

对外可描述的交付包结构：

- `Gate6_Deliverable_Package/`
  - `README.md`（版本、数据字典、生成步骤）
  - `Protocol_Summary/`（终点类别、盲法/随机化原则、AE/SAE 分级与停线类别）
  - `Event_Log/`（AE/SAE 事件日志模板；见附录 F）
  - `Behavior_Scoring/`（行为评分表模板与一致性评估口径；见附录 F）
  - `Lab_Observations/`（健康指标类别清单与观测记录模板，非保密口径）
  - `QC/`（数据合格与偏差记录）
  - `Decision/`（Gate 6 决策备忘录；模板见附录 B）

---

# 7. 以猫为目标物种（target species）/非目标影响最小化治理：功能选择性 + 最坏暴露

由于投喂方式难以隔离性别与非目标摄入，我们把“目标物种为猫（target species）”理解为**可检验要求**，并把“非目标无影响”视为**禁止外推的高风险主张**（除非有强证据闭环）。
- **跨物种功能选择性**：猫 vs 非目标物种的功能分离要在可比实验格式下尽早量化；
- **最坏暴露治理**：不以平均暴露作为安全依据，而以高端暴露者与误食场景做约束；
- **对外主张纪律**：在证据不足时不宣称“对其他物种无影响”，而是明确其为待验证假设。

---

# 8. 证据与对外主张政策（Evidence & Claims Policy）

## 8.1 核心规则
- **不虚构**：不把假设/推理当作测量结果。
- **不外推**：任何关键表述必须同时写清“证据等级 + 不可外推边界”。

## 8.2 证据等级（对外口径）
- **强**：直接相关、可复现、外推边界清晰；
- **中**：来源可核查但存在物种/机制/场景差异；
- **弱**：背景性/综述性，不用于关键 go/no‑go。

## 8.3 主张分类（对外必须标注）
- **结论**：在边界内有强证据支持；
- **假设**：合理但未证实；必须配套“最小补证”；
- **目标**：期望画像，不等同于现实陈述。

## 8.4 对外红线（示例）
以下表述在无强证据前作为假设：
- “不影响行为/健康”
- “对幼猫/孕猫/哺乳猫安全”
- “对其他物种无影响”


## 8.5 追溯 ID 与变更控制（非保密）

- `CLM-###`：关键对外表述（结论/假设/目标）ID
- `EVD-###`：证据项 ID（可与 DOI 元数据关联）
- `GATE{n}-DM-YYYYMMDD-###`：Gate 决策备忘录 ID
- `TPL-###`：模板/字段字典版本 ID（例如附录 A/C/E/F/G）
- `RISK-P0-###`：P0 风险项 ID（见第 2.2 节）

## 8.6 Claims Register（主张登记册｜非保密）

仅有 CLM/EVD 编号规则仍不足以保证“对外红线”在 PPT/邮件/会议纪要中不失控；因此我们要求以**主张登记册（Claims Register）**作为可执行载体来管理对外表述。

非保密范围内可公开的是**登记册结构与字段**（不含任何保密结论/数据）：
- 最低字段模板见：附录 H
- 规则：任何对外表述必须在登记册中有对应 `clm_id`，并明确其 `claim_type`（结论/假设/目标）、证据等级、不可外推边界与禁止外推点；否则不得对外传播。
- 审批链条（非保密可审计要素）：将主张状态置为 `approved_for_external` 前，必须填写 `approved_by_role`、`approved_at`，并引用 `review_checklist_version`（用于证明按冻结清单完成复核，而非口头决定）。

## 8.7 DOI 元数据核验流程（非保密）

为满足“仅 DOI 元数据、公开可核查来源”的审计要求，我们在对外发布前执行最低核验流程（不含论文全文）：

- **核验对象**：本文件第 11 节与 `04-References.NC.tsv/.csv` 中出现的每一个 DOI。
- **核验人**：非作者本人（角色可为项目成员/法务/外部顾问；记录其角色即可）。
- **核验来源**：Crossref 或出版社落地页（任一即可，但必须记录来源 URL）。
- **核验输出**：记录 `doi / title / venue / year` 是否一致；不一致则修正或移除；并写入核验记录表（见附录 I）。
- **本版本执行情况**：v0.9 已执行上述核验流程，并将核验记录落盘为 `05-DOI-Verification.NC.tsv/.csv`（对外目录同名）；汇总见附录 I。

---

# 9. 监管与伦理路径假设（非保密）

本项目的设想（以猫粮作为递送载体的 FSHR 小分子拮抗避孕）在多数法域都可能触及多重监管边界。由于我们目前为零实验数据阶段，本节只给出**非保密的路径假设与闸门化治理口径**，不涉及任何可操作投喂细节。

## 9.1 为什么必须前置
- **产品监管分类可能决定“科学上可行但监管上死路”**：例如兽药/含药饲料/药饵等不同路径对数据包与流通控制要求差异巨大。
- **非目标暴露与人类接触链是结构性约束**：不限量投喂意味着无法完全避免雄猫与非目标动物暴露；监管评估通常要求对非目标与环境风险有可审计论证。

## 9.2 非保密的“合规闸门（REG‑Gate）”冻结口径
在进入任何外场试点（Gate 7）之前，必须形成并冻结以下**最小合规包**（类别级，不含具体机构/阈值）：

1) **目标法域与候选监管路径**：明确首发法域（国家/地区）与候选监管分类（例如动物用药/含药饲料/其他），并记录选择理由与替代路径。
2) **非目标与环境风险模块**：
   - 非目标物种暴露场景枚举（伴侣动物/野生动物/人类接触链等）；
   - 风险控制假设（例如包装/流通限制/使用场景约束的类别口径）；
   - 与 Gate 1/4 证据的绑定：跨物种功能选择性数据与最坏暴露治理（K_required）必须作为前置输入，而不是后置补写。
3) **动物福利与伦理治理**：受控研究的伦理审批路径、AE/SAE 监测与上报机制、停线与救治原则（类别级）必须在执行前冻结。
4) **数据完整性与可审计性**：原始数据留存、偏差管理（deviation log）、变更控制与第三方复核接口必须可执行。

## 9.3 停线规则（监管/伦理维度）
若无法在目标法域下形成可审计的监管/伦理路径假设，或无法把“非目标/环境风险”与 Gate 数据闭环绑定，则结论不是“先做外场再说”，而是：**不得进入外场阶段（Gate 7）**，并需要回到场景约束/递送控制策略进行重构。

## 9.4 首发法域选择原则与重置条件（类别级｜非保密）

为避免“先选法域、后补理由”的事后叙事，我们冻结首发法域选择的类别级原则（不公开具体国家/地区，仅公开决策逻辑框架）：

| 决策维度 | 选择原则（类别级） | 不满足时的处置（类别级） |
|---|---|---|
| 监管分类清晰度 | 候选路径（动物用药/含药饲料/其他）在该法域有清晰定义与可执行先例/指南 | 分类长期不明确 → 暂停外场相关计划，转为先完成 Gate 1/4 的证据闭环并重新评估 |
| 流通与使用场景可控性 | 能在审计意义上实现“流通控制/标签/使用边界”的治理假设（哪怕是类别级） | 无法提出可控假设 → 该法域不作为首发，或必须重构递送/场景约束 |
| 非目标/环境风险要求强度 | 要求强度与项目可承受的证据路径匹配，并能把需求映射到 Gate 1/4/6 交付包 | 无法映射或成本不可承受 → 更换路径或停线 |
| 动物福利/伦理可执行性 | 伦理审批与 AE/SAE 治理链条可落地并可审计 | 无法形成可审计伦理路径 → 不得进入任何涉及外场/受控研究的阶段 |
| 数据完整性与第三方复核接口 | 可满足原始数据留存/审计/第三方复核的基本要求 | 无法满足 → 不进入高成本阶段（尤其是外场） |

重置（Reset）条件示例（类别级）：
- 首发法域候选路径发生根本性变化（分类从 A 变为 B）；
- 外部审计认为“流通控制/非目标风险治理假设不可审计”；
- Gate 4 输出显示 K_required 结构性不可行，导致监管路径前提不成立。

---

# 10. 可在 NDA 下提供的补充包（范围说明）
在签署 NDA 后，我们可提供更细的“可执行/可审计”材料，包括：
- Gate 1/2/… 的具体数字阈值、QC 门槛与停线规则；
- 更详细的实验 SOP、质量体系与外包验收标准；
- 结构/系列层面的 SAR 与化学迭代策略；
- Dose/Exposure Model 的具体输入表与输出、敏感度与情景分析；
- 外场/受控喂食研究的详细执行与动物福利/伦理合规模块。

---

# 11. 参考文献（仅 DOI 元数据）

| DOI | 标题（原文） | 年份 | 期刊/会议 | 证据等级 | 备注（非保密） |
|---|---|---:|---|---|---|
| 10.1016/j.theriogenology.2024.06.005 | Antibody fragments targeting the extracellular domain of follicular stimulating hormone receptor for contraception in male dogs and cats | 2024 | Theriogenology | 中 | 物种特异性结合的先例（不等同于小分子有效性证明）。 |
| 10.1021/jm049676l | Identification of substituted 6-amino-4-phenyltetrahydroquinoline derivatives: potent antagonists for the follicle-stimulating hormone receptor | 2005 | Journal of Medicinal Chemistry | 中 | 小分子 FSHR 拮抗的先例（scaffold 级锚点）。 |
| 10.1210/en.2018-00317 | Allosteric Regulation of the Follicle-Stimulating Hormone Receptor | 2018 | Endocrinology | 中 | 别构调控/偏向性信号的考虑。 |
| 10.3389/fendo.2018.00757 | Small Molecule Follicle-Stimulating Hormone Receptor Agonists and Antagonists | 2019 | Frontiers in Endocrinology | 中 | 小分子调节剂综述与方法学约束。 |
| 10.1016/j.mce.2016.07.013 | Profiling of FSHR Negative Allosteric Modulators on LH/CGR Reveals Biased Antagonism with Implications in Steroidogenesis | 2016 | Molecular and Cellular Endocrinology | 中 | 偏向性拮抗与跨受体谱系评估原则。 |
| 10.1016/j.mce.2010.12.023 | A negative allosteric modulator demonstrates biased antagonism of the follicle stimulating hormone receptor | 2011 | Molecular and Cellular Endocrinology | 中 | 偏向性拮抗/读数依赖性：支持“至少两类功能读数 + 跨受体谱系”作为硬要求。 |
| 10.1095/biolreprod.113.109397 | Inhibition of Follicle-Stimulating Hormone-Induced Preovulatory Follicles in Rats Treated with a Nonsteroidal Negative Allosteric Modulator of Follicle-Stimulating Hormone Receptor | 2014 | Biology of Reproduction | 中 | 体内内分泌/卵巢终点背景锚点（非猫；方式不同），用于提示“机制‑表型耦合”的风险边界。 |
| 10.1038/s41467-023-38721-0 | Durable contraception in the female domestic cat using viral-vectored delivery of a feline anti-Müllerian hormone transgene | 2023 | Nature Communications | 中 | 猫相关的长期随访与终点/监测参考（方式不同）。 |
| 10.1002/vms3.552 | Vaginal stimulation enhances ovulation of queen ovaries treated using a combination of eCG and hCG | 2021 | Veterinary Medicine and Science | 中 | 猫繁殖生理与终点表述背景（非猫粮递送研究）。 |
| 10.1177/1098612X18791872 | Hybrid model intermediate between a laboratory and field study: A humane paradigm shift in feline research | 2018 | Journal of Feline Medicine and Surgery | 中 | 外场/伦理方法学框架参考。 |
| 10.1186/s13620-021-00189-z | Development of an ethogram/guide for identifying feline emotions | 2021 | Irish Veterinary Journal | 弱 | 训练/背景用途；不足以单独作为关键终点定义。 |
| 10.3390/ani11010020 | Comparison of the Morphology and Developmental Potential of Oocytes Obtained from Prepubertal and Adult Domestic and Wild Cats | 2020 | Animals | 弱 | 幼龄繁殖生物学背景（非安全性证明）。 |
| 10.1016/j.theriogenology.2010.01.010 | The GnRH antagonist acyline prevented ovulation, but did not affect ovarian follicular development or gestational corpora lutea in the domestic cat | 2010 | Theriogenology | 中 | 表型边界类比（GnRH 轴；非 FSHR）。 |

---

# 附录 A：Gate 1 标准化结果表（TSV）模板（字段级）

下表是一个“空模板”（无任何实验数据），用于说明我们如何将 Gate 1 结果结构化为可审计、可汇总的 TSV。

```tsv
compound_id	batch_id	assay_id	species	target	cell_system	readout	mode	concentration_unit	ic50	pIC50	e_max	hill_slope	fit_quality	qc_grade	replicate_n	independent_day_n	comparability_flag	bridging_control_present_yes_no	bridging_level	bridging_qc_grade	interference_flag	aggregation_flag	cytotoxicity_flag	notes
```

## A.1 字段取值枚举（controlled vocabulary｜非保密冻结）

为保证跨批次/跨 CRO 的可比性，以下字段在非保密范围内冻结其“允许取值集合”（不含阈值）：

- `comparability_flag`：`comparable` / `partial` / `not_comparable`
- `bridging_control_present_yes_no`：`Y` / `N`
- `bridging_level`：`1` / `2` / `3` / `NA`
  - `1`：同日同板跨物种桥接（最强）
  - `2`：同日跨板桥接
  - `3`：不同日桥接（最弱；需保守解读）
  - `NA`：不适用（例如未进行跨物种比较）
- `bridging_qc_grade`：`good` / `acceptable` / `poor` / `missing`
- `interference_flag`：`none` / `suspected` / `confirmed` / `not_assessed`
- `aggregation_flag`：`none` / `suspected` / `confirmed` / `not_assessed`
- `cytotoxicity_flag`：`none` / `suspected` / `confirmed` / `not_assessed`

注：若任一 flag 为 `confirmed`（或桥接为 `poor/missing`、或 `comparability_flag=not_comparable`），则对应记录不得被标记为 `qc_grade=decision‑grade`；具体处置与阈值在 NDA 版冻结。

---

# 附录 B：Gate 决策备忘录模板（对外可审计结构）

同样为“空模板”，用于说明 Gate 评审的最小审计结构：

- 标题：Gate X 决策备忘录（版本/日期/负责人）
- 冻结的评审问题清单（引用 Freeze 版本号）
- 执行摘要（pass / conditional pass / stop）
- 数据包清单（目录结构 + 数据字典版本）
- QC 总结（哪些为决策级、哪些为探索级、哪些无效）
- 主要发现（按问题清单逐条回答）
- 不可外推边界（明确“不能从这些数据推出什么结论”）
- 偏差/异常与处置（deviation log）
- 风险更新（P0/P1 风险项是否变化）
- 结论与下一步（最小补证清单/停线理由映射到类别）

---

# 附录 C：外场摄入/体重 pilot 数据表模板（字段级）

该模板用于把外场 pilot 的最小输入“结构化”为可回灌 Dose/Exposure Model 的形式（不包含具体站点信息）。

```tsv
site_id_anonymized	date	feed_mass_in_g	feed_mass_out_g	feeding_window_hours	cat_count_estimate	id_method	bw_sample_n	bw_p10_kg	bw_p50_kg	bw_p90_kg	bw_p99_kg	intake_p10_g_day	intake_p50_g_day	intake_p90_g_day	intake_p99_g_day	missingness_notes	qa_notes
```

---

# 附录 D：第三方 30 分钟快速审计清单（非保密）

第三方若希望快速判断我们是否“流程真实存在、且可审计”，可按以下问题核查：

1) 是否存在明确的 Gate 地图（Phase 0–7）及每个 Gate 的停线类别？
2) 是否存在统一的 Freeze→Run→Review→Audit 流程描述，并包含变更控制？
3) 是否明确要求原始数据 + 元数据交付（而不是仅截图/汇总）？
4) Gate 1 是否明确包含：效力、机制、跨物种选择性、排假阳性四类问题？
5) Gate 1 交付包是否给出目录结构与标准化结果表字段字典？
6) 是否明确“不可控摄入”要通过分位数校准与模型约束来治理，而不是假设平均摄入？
7) 是否明确 B 标准作为共同主要要求，并有 AE/SAE 与停线逻辑（至少类别口径）？
8) 是否把“目标物种为猫（target species）/非目标影响最小化与风险治理（不得外推‘无影响’）”明确为待验证要求，并有跨物种功能数据与最坏暴露治理框架？
9) 是否有证据等级与对外主张纪律（不虚构、不外推、不可外推边界）？
10) 是否清晰区分：非保密可公开的内容 vs NDA 才可提供的内容？
11) 是否提供 Gate 4/6 的交付包结构与字段模板（可审计但不泄密）？
12) 是否提供可公开的追溯 ID 与变更控制模板，使口径演进可复核？
13) 是否把 P0 风险与最小证伪动作绑定，并能映射到停线类别？


---

# 附录 E：Gate 4（暴露与摄入校准）交付包结构 + Dose Model 输入表模板（字段级）

本附录不包含任何数值，只提供对外可公开的交付结构与字段模板，用于第三方理解与审计。

## E.1 Gate 4 交付包目录结构（示例）
- `Gate4_Deliverable_Package/`
  - `README.md`
  - `Intake_BW_Pilot/`（与附录 C 对应）
  - `Exposure_Calibration/`（样本清单模板见 E.3）
  - `DoseModel/`（输入表模板见 E.2；情景表模板见 E.4）
  - `QC/`
  - `Decision/`

## E.2 Dose/Exposure Model 输入表模板（TSV｜字段级）
```tsv
parameter_id\tparameter_name\tsymbol\tunit\tvalue_type\tp10\tp50\tp90\tp99\tsource_type\tevidence_level\tassumption_rationale\tversion\tnotes
```

字段说明（非保密）：
- `value_type`：fixed / range / distribution
- `source_type`：literature / internal / assumption
- `assumption_rationale`：若为假设输入，必须写清理由与可证伪路径（类别）

## E.3 混饲/暴露校准样本清单模板（TSV｜字段级）
```tsv
study_id\tsample_id\tmatrix\ttimepoint_label\tcollection_window\tanalysis_method\tqc_status\tnotes
```

## E.4 情景（Scenario）定义表模板（TSV｜字段级）
```tsv
scenario_id\tdescription\tintake_quantile\tbw_quantile\tfood_concentration_quantile\tpk_assumption\tdependence_assumption\toutput_metrics\tpass_fail_category\tnotes
```

---

# 附录 F：Gate 6（受控喂食 B 标准）交付包结构 + AE/SAE 与行为评分模板（字段级）

本附录不包含任何给药/剂量/配方信息；仅提供对外可公开的审计结构与字段模板。

## F.1 Gate 6 交付包目录结构（示例）
- `Gate6_Deliverable_Package/`
  - `README.md`
  - `Protocol_Summary/`（终点类别、盲法/随机化原则、停线类别）
  - `Event_Log/`（模板见 F.2）
  - `Behavior_Scoring/`（模板见 F.3）
  - `Lab_Observations/`
  - `QC/`
  - `Decision/`

## F.2 AE/SAE 事件日志模板（TSV｜字段级）
```tsv
subject_id_anonymized\tdate\tevent_term\tevent_type\tseverity_grade\tseriousness\toutcome\trelationship_assessment\taction_taken\tfollow_up_needed\tnotes
```

## F.3 行为评分记录模板（TSV｜字段级）
```tsv
subject_id_anonymized\tdate\tobserver_id\tethogram_version\tdomain\tscore\tcontext_notes\tblinded_yes_no\tinterrater_check\tnotes
```

字段说明（非保密）：
- `domain`：activity / aggression_territorial / stress_anxiety / social_withdrawal / sleep_abnormal / other
- `interrater_check`：是否纳入一致性抽样（例如双评/复评；具体门槛 NDA）

---

# 附录 G：追溯 ID 与变更控制模板（非保密）

本附录提供对外可公开的追溯与变更控制模板，便于第三方在不接触内部目录与商业秘密的前提下复核口径演进。

## G.1 追溯 ID 规则（建议）
- `CLM-###`：关键对外表述 ID
- `EVD-###`：证据项 ID（可关联 DOI）
- `GATE{n}-DM-YYYYMMDD-###`：Gate 决策备忘录 ID
- `TPL-###`：模板版本 ID
- `RISK-P0-###`：P0 风险项 ID

## G.2 变更记录模板（TSV｜字段级）
```tsv
change_id\tdate\tdocument_id\tfrom_version\tto_version\tchange_summary\taffected_clm_ids\tevidence_level_change\tapprover_role\tnotes
```

## G.3 措辞变更说明模板（Markdown｜结构）
- 变更摘要：
- 影响范围：CLM‑xxx / CLM‑yyy
- 变更原因：
- 证据等级变化：无 / 上调 / 下调（下调需说明风险与临时替代口径）
- 不可外推边界是否变化：
- 批准角色与日期：

---

# 附录 H：Claims Register（主张登记册）模板（字段级）

本附录提供“主张登记册”的最小字段结构，用于把 Claims Policy 从口号落到可执行、可审计的载体（不包含任何具体主张内容）。

```tsv
clm_id\tclaim_text\tclaim_type\tevidence_level\tevidence_ids\tscope_boundary\tforbidden_extrapolation\towner\tstatus\tapproved_by_role\tapproved_at\treview_checklist_version\tlast_review_date\tlinked_gate_decisions\tnotes
```

字段说明（非保密）：
- `claim_type`：conclusion / hypothesis / goal（结论/假设/目标）
- `evidence_ids`：以 `EVD-###` 列表形式引用
- `scope_boundary`：适用边界（物种/场景/时间窗等类别描述）
- `forbidden_extrapolation`：禁止外推点（必须显式写出）
- `status`：draft / approved_for_external / retired
- `approved_by_role`、`approved_at`：对外审批角色与时间（非作者本人优先；要求可审计留痕）
- `review_checklist_version`：复核清单版本号（用于证明按冻结清单完成复核）

---

# 附录 I：DOI 元数据核验记录（字段级｜v0.9 已执行）

本附录用于记录“仅 DOI 元数据、公开可核查来源”的发布前核验。该记录不包含论文全文，仅包含可公开核查的元数据与核验留痕。

```tsv
evd_id\tdoi\ttitle\tvenue\tyear\tverified_by_role\tverified_at\tsource_url\tmatch_yes_no\tresolution\tnotes
```

字段说明（非保密）：
- `verified_by_role`：核验者角色（非作者本人）
- `verified_at`：核验时间（YYYY‑MM‑DD）
- `source_url`：Crossref 或出版社落地页链接
- `match_yes_no`：元数据是否一致
- `resolution`：若不一致的处置（修正/移除/待确认）

## I.1 v0.9 发布前核验记录（Crossref｜非保密）

本版本已对第 11 节全部 DOI 执行发布前核验，并将核验记录落盘为：
- `docs/nonconfidential/05-DOI-Verification.NC.tsv`
- `docs/nonconfidential/05-DOI-Verification.NC.csv`

对外目录同名文件亦已同步。

核验记录（TSV，节选为全量 13 条）：

```tsv
"evd_id"	"doi"	"title"	"venue"	"year"	"verified_by_role"	"verified_at"	"source_url"	"match_yes_no"	"resolution"	"notes"
"EVD-NC-001"	"10.1016/j.theriogenology.2024.06.005"	"Antibody fragments targeting the extracellular domain of follicular stimulating hormone receptor for contraception in male dogs and cats"	"Theriogenology"	"2024"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1016/j.theriogenology.2024.06.005"	"Y"	"none"	"doi_url=https://doi.org/10.1016/j.theriogenology.2024.06.005"
"EVD-NC-002"	"10.1021/jm049676l"	"Identification of Substituted 6-Amino-4-phenyltetrahydroquinoline Derivatives:  Potent Antagonists for the Follicle-Stimulating Hormone Receptor"	"Journal of Medicinal Chemistry"	"2005"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1021/jm049676l"	"Y"	"none"	"doi_url=https://doi.org/10.1021/jm049676l"
"EVD-NC-003"	"10.1210/en.2018-00317"	"Allosteric Regulation of the Follicle-Stimulating Hormone Receptor"	"Endocrinology"	"2018"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1210/en.2018-00317"	"Y"	"none"	"doi_url=https://doi.org/10.1210/en.2018-00317"
"EVD-NC-004"	"10.3389/fendo.2018.00757"	"Small Molecule Follicle-Stimulating Hormone Receptor Agonists and Antagonists"	"Frontiers in Endocrinology"	"2019"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.3389/fendo.2018.00757"	"Y"	"none"	"doi_url=https://doi.org/10.3389/fendo.2018.00757"
"EVD-NC-005"	"10.1016/j.mce.2016.07.013"	"Profiling of FSHR negative allosteric modulators on LH/CGR reveals biased antagonism with implications in steroidogenesis"	"Molecular and Cellular Endocrinology"	"2016"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1016/j.mce.2016.07.013"	"Y"	"none"	"doi_url=https://doi.org/10.1016/j.mce.2016.07.013"
"EVD-NC-006"	"10.1016/j.mce.2010.12.023"	"A negative allosteric modulator demonstrates biased antagonism of the follicle stimulating hormone receptor"	"Molecular and Cellular Endocrinology"	"2011"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1016/j.mce.2010.12.023"	"Y"	"none"	"doi_url=https://doi.org/10.1016/j.mce.2010.12.023"
"EVD-NC-007"	"10.1095/biolreprod.113.109397"	"Inhibition of Follicle-Stimulating Hormone-Induced Preovulatory Follicles in Rats Treated with a Nonsteroidal Negative Allosteric Modulator of Follicle-Stimulating Hormone Receptor1"	"Biology of Reproduction"	"2014"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1095/biolreprod.113.109397"	"Y"	"none"	"doi_url=https://doi.org/10.1095/biolreprod.113.109397"
"EVD-NC-008"	"10.1038/s41467-023-38721-0"	"Durable contraception in the female domestic cat using viral-vectored delivery of a feline anti-Müllerian hormone transgene"	"Nature Communications"	"2023"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1038/s41467-023-38721-0"	"Y"	"none"	"doi_url=https://doi.org/10.1038/s41467-023-38721-0"
"EVD-NC-009"	"10.1002/vms3.552"	"Vaginal stimulation enhances ovulation of queen ovaries treated using a combination of eCG and hCG"	"Veterinary Medicine and Science"	"2021"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1002/vms3.552"	"Y"	"none"	"doi_url=https://doi.org/10.1002/vms3.552"
"EVD-NC-010"	"10.1177/1098612X18791872"	"Hybrid model intermediate between a laboratory and field study: A humane paradigm shift in feline research"	"Journal of Feline Medicine and Surgery"	"2018"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1177/1098612X18791872"	"Y"	"none"	"doi_url=https://doi.org/10.1177/1098612x18791872"
"EVD-NC-011"	"10.1186/s13620-021-00189-z"	"Development of an ethogram/guide for identifying feline emotions: a new approach to feline interactions and welfare assessment in practice"	"Irish Veterinary Journal"	"2021"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1186/s13620-021-00189-z"	"Y"	"none"	"doi_url=https://doi.org/10.1186/s13620-021-00189-z"
"EVD-NC-012"	"10.3390/ani11010020"	"Comparison of the Morphology and Developmental Potential of Oocytes Obtained from Prepubertal and Adult Domestic and Wild Cats"	"Animals"	"2020"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.3390/ani11010020"	"Y"	"none"	"doi_url=https://doi.org/10.3390/ani11010020"
"EVD-NC-013"	"10.1016/j.theriogenology.2010.01.010"	"The GnRH antagonist acyline prevented ovulation, but did not affect ovarian follicular development or gestational corpora lutea in the domestic cat"	"Theriogenology"	"2010"	"自动核验（Crossref API）"	"2026-02-10"	"https://api.crossref.org/works/10.1016/j.theriogenology.2010.01.010"	"Y"	"none"	"doi_url=https://doi.org/10.1016/j.theriogenology.2010.01.010"
```
