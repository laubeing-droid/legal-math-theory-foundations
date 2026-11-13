# 20261113 形式化证明静态审核 · 可访问性核对

- 署名：法律编程审核员 / Grok
- 报告日期：2026-11-13（Asia/Shanghai）
- 写入时刻：2026-11-13 23:47:36 Asia/Shanghai
- 本轮范围：只交可访问性与精确来源 / 缺件。不做证明审核、不做小样、不给出全库通过或“3000+ 均已完成”之类结论。
- 授权依据：主人经 Codex 派遣的数学线独立静态审核（t387u / pt387u），后收窄为本轮只交可访问性。

## 1. 范围、只读边界与实际无运行声明

本轮只确认现有授权只读渠道实际能读到什么。已遵守并实际做到：

- 未修改任何仓库或代码，未 checkout / clone / fetch，未向仓库写入。
- 未运行 Lean、Lake、CI、测试，未安装组件。
- 不以历史 green、旧记忆中的定理计数、或本地陈旧副本当作当前验证。
- 未联系其他机器人，未改技能 / 例行 / 记忆，未实施迁移，未写 SOUL。
- 收窄后停止继续搜索与打开新源；未试用户电脑，未进入 LXPPS 工作区。
- 本文件是报告产物，仅写在 `/workspace/math-static-review/`。

旧记忆（例如 2026-10 前后 journal 中的 “5300 theorems”）只作线索，不是当前事实，不能用来认定当前声明均已完成。

## 2. 已核实的授权只读渠道

| 渠道 | 状态 | 本轮实际用法 |
| --- | --- | --- |
| GitHub 连接器 `cursor-github` | 已连接；对 `laubeing-droid/legal-math-modeling` 具备 pull（本轮只调用只读接口） | `search_repositories`、`list_commits`、`get_file_contents`（目录列举及下述已打开正文） |
| 盒内既有文件 | 可读 | 只读查看既有导出包元数据，以及本地陈旧副本的 git 元数据（不得当原文） |
| RecallMemory / 既有记录 | 可读，但非当前事实 | 仅用于寻找 owner/repo 与集中区线索；不作为当前证明状态 |

未另装连接器，未申请扩大权限，未猜令牌。获取拒绝不绕过。本轮未对用户电脑做任何探测。

## 3. 精确来源（当前固定 commit）

- 仓库：[`laubeing-droid/legal-math-modeling`](https://github.com/laubeing-droid/legal-math-modeling)（public，默认分支 `main`，语言标注 Lean）
- 当前 `main` 头（`list_commits` 以 `sha=main`、`per_page=15` 取第一条，已核实）：`037e3f20142ddb0bc8874e9078378360b29122af`
- 提交时间：`2026-11-09T06:05:40Z` = **2026-11-09 14:05:40 Asia/Shanghai**
- 提交说明：`fix(ci): fetch exact verified Lean release from official GitHub asset`
- 父提交：`8df4fbef91e2e31087fb4e516560b1027d7379f0`
- 提交页：https://github.com/laubeing-droid/legal-math-modeling/commit/037e3f20142ddb0bc8874e9078378360b29122af
- 树对象：`80c141c274938273f112843f53a902675b743d8c`（来自该 commit 对象，非另开树遍历）

此后凡称“当前固定原文”，均指上述 commit，而不是本地副本或记忆中的旧 tip。

ULM 不是另仓：在已连接账户下按名检索 `ULM user:laubeing-droid` 无独立仓库。ULM 以该仓内路径出现（目录列举可见 `docs/ulm-consolidated/`，以及 `proofs/lean/juris_lean/JurisLean/` 下 `ULM*.lean` 文件名）。这只说明路径存在，不表示已审读这些 Lean 原文。

## 4. 目录列举可读（仅名称 / 大小 / blob SHA，正文不作为本轮已打开审核原文）

下列均为对固定 commit `037e3f20142ddb0bc8874e9078378360b29122af` 的 `get_file_contents` 目录列举。目录项无字节大小（GitHub 列目录时 `size=0`）。

### 4.1 仓库根目录

| 类型 | 名称 | 大小（字节） | blob/tree SHA |
| --- | --- | --- | --- |
| file | `.gitattributes` | 1033 | `2d54101dddbd92036b8e39e563ff1b89160c5734` |
| dir | `.github` |  | `1ad4882e962e16c00f33e0ff8b91b067e2f6a88c` |
| file | `.gitignore` | 921 | `44d7d2f3bb20e69eee5e8bc23b8cdb82434ff324` |
| dir | `.planning` |  | `be1a8d2f4164da206ea197592fb4665f2b4a01af` |
| file | `AGENTS.md` | 10493 | `967354ce330686fc2d5f0c65d17aa001e9d3ea66` |
| file | `CITATION.cff` | 815 | `29b8595518f97055b5e70679aaf8016bfeaa8116` |
| file | `LICENSE` | 1299 | `3c8ca617c785d7a1e7722f0bef4eae3dd8699207` |
| file | `README.md` | 8112 | `1ced97f17883f0b79908334b7ec21d3b9ddba59a` |
| file | `README_CN.md` | 5408 | `5b153f6bf4004613227d6c9778064dbf0e754709` |
| file | `conftest.py` | 219 | `b3707e0a06f04ab652f52ae845ba44a7ebb00e09` |
| dir | `data` |  | `ba6346d9c06fe8f15540a51f9c71957ca5f4693e` |
| dir | `docs` |  | `7ff31d9c62ef0903423053637f73896903fc5b51` |
| dir | `paper` |  | `d0d93a4e57cbba2c5b18ac0f18010010d1920ad0` |
| dir | `program` |  | `fb566a11eeadf86c9c7f357d47a33b1afcafe5bc` |
| dir | `proofs` |  | `33dcdf135cd3b1be1162465483a8e5e508a88117` |
| dir | `reports` |  | `9058758c02c228ce7dcdc9696973ab236d400583` |
| file | `requirements.txt` | 316 | `7f987477c8c303292a97e3ad82e993f450719261` |
| dir | `runtime` |  | `f1da9df04197e9d22a5b604902d0d481a69e87f4` |
| dir | `scripts` |  | `ca1d3764b799b8111020b051e2ca62f9650bedde` |
| dir | `tests` |  | `d85cefc97dc4c6ee2fd90a8e0b468fc36a233360` |
| dir | `theory` |  | `d6eeb8cdd3ccce4ee176200a94ce979c0240bc6e` |
| dir | `tools` |  | `438450f22f8c79babbc2a89c00e5a8f7b7ca3602` |
| dir | `verification` |  | `a0537d39426722a7e3ae3d49805b7aee900a1f25` |
| dir | `work` |  | `f9746c145fc1c91d0b23924859ec0f7e6584a3d4` |

根目录列举中**没有**仓库根级 `lakefile` 或 `lean-toolchain`。Lean 工程文件出现在 `proofs/lean/juris_lean/` 的目录列举中（见 4.4）。

### 4.2 `docs/formal-release/`（证明清单与形式发布产物所在目录）

| 类型 | 名称 | 大小（字节） | blob/tree SHA |
| --- | --- | --- | --- |
| file | `ALLOWED_CLAIMS.md` | 1486 | `aaa2134f397d8666c40f96b94d18aa481e5957ca` |
| file | `CERTIFICATE_SCHEMA_V2.md` | 2813 | `0b04309ae27fa4534a789fcbf53d99b908fe08ed` |
| file | `FINAL_FORMAL_RELEASE_REPORT.md` | 3264 | `9cc56565f0dfbb12d96e98669d43aa50b9f095f0` |
| file | `FORBIDDEN_CLAIMS.md` | 1489 | `a0e373e1f98ed9b06cbabe89ced279a4668ddab2` |
| file | `FORMAL_RELEASE_REPORT.md` | 2251 | `4e3a9e81c5d6ee569d7dcfc92d2ba52957cfee66` |
| file | `SEVEN_AXIS_LANDING_REPORT_20260911.md` | 3340 | `c22f574c232cfb58c8af7602bbc7a83ffdfde9dc` |
| file | `axiom_audit.md` | 737 | `1546dfb7c9732e5f5d6ebff71ec323757d1dce30` |
| dir | `ci-evidence` |  | `99bfbaeab64ea1e291383f909ba009b00b3f5427` |
| file | `ci_run_index.json` | 1265934 | `6b1ba9c3fdc26229e4c03dab7b33647410a30267` |
| file | `ci_run_index.md` | 107183 | `8b8b239a7dc37def069075a858c9e4d2bdc0be42` |
| file | `claims_registry.json` | 3781 | `c310a2c8f14d370ad2ca3382b2ef65504079ea36` |
| file | `counterexample_registry.json` | 477 | `c60c44f681b943c20c19b34b337668fcc08dbe82` |
| file | `declaration_shape_report.json` | 1920 | `aeb27a0d603cdd2479ade77c3673ef53d571a816` |
| dir | `evidence` |  | `65c382d5cc4911f204e5170fb5c450ac7b584042` |
| file | `formal_release_certificate.schema.json` | 2066 | `6c9205ee636ff5fa387921ff02ac0487da0c4a51` |
| file | `gap_status.json` | 2300 | `21e8bce70008db6c6c1c5ba0bc61921f41002cb1` |
| file | `kernel_reuse_report.json` | 7451 | `e4cde6cbcb5161d008be72ac153f8cbedd719f16` |
| file | `proof_ledger.json` | 710 | `b0dc07ccfba84c117e61eafe6b62fe3b3dd851b6` |
| file | `real_cohort_probe.json` | 6455 | `cbeedffc720fb5c8de23e8a393539bf8f83af831` |
| file | `statement_duplication_census.json` | 33174 | `93c8da9c16cb5eb632412596f87278c5cdf548dc` |
| file | `statement_duplication_census.md` | 11976 | `a7911714e1d95e62dfac0170245edbd9c5885dcc` |
| file | `theorem_inventory_v3.json` | 2063111 | `5e8774d6b92ae6dd29bb63c24700456e232d6c28` |
| file | `theorem_manifest.json` | 833557 | `5cd79a90fa7ce544b8a10b2230383d6ebc4426cf` |
| file | `trivial_proof_census.json` | 666751 | `e4a47bf71f62337dd0eb1de09735dca7d4dc7735` |
| file | `trust_label_schema.json` | 794 | `08b9b8f90e6e491d574043544fe8bd3a2752863a` |
| file | `wave_cohort_probe.json` | 3680 | `06ec0d7a5ca581d5f4ac1e94254f9e02298d7a93` |

其中证明清单候选文件（本轮**只确认存在与体积，未把正文当作已打开审核原文**）包括：

- `theorem_inventory_v3.json`（2,063,111 字节）
- `theorem_manifest.json`（833,557 字节）
- `statement_duplication_census.json` / `.md`
- `declaration_shape_report.json`
- `trivial_proof_census.json`
- `kernel_reuse_report.json`
- `gap_status.json`
- `proof_ledger.json`
- `axiom_audit.md`
- `ci_run_index.json` / `.md`（历史构建索引，未在本轮打开，也不得当当前验证）

### 4.3 `proofs/lean/`

目录列举可见：

| 类型 | 名称 | 大小（字节） | blob/tree SHA |
| --- | --- | --- | --- |
| file | `BANACH_MATHLIB_API_LOCK.md` | 2980 | `04d584b95626d3ff95fc618588a75c40bed4ad82` |
| file | `BanachEffectiveNodes.lean` | 5039 | `f2fd97240a1a3043dedbaa51a034219e9148fc3a` |
| file | `README.md` | 2057 | `f89d87889b487bac610909cff49edfcc69b7e9fa` |
| dir | `juris_lean` |  | `203f9db8ecc253d7a5da70e774af8a0e0278d744` |

### 4.4 `proofs/lean/juris_lean/`

目录列举可见（完整页即该目录这一层）：

| 类型 | 名称 | 大小（字节） | blob/tree SHA |
| --- | --- | --- | --- |
| file | `JurisLean.lean` | 17057 | `09b779f877231334520646dc49cb22e61175cc4e` |
| dir | `JurisLean` |  | `fa90ada730fd1caf8d4b402aa58085d3bc89ba41` |
| file | `_axiom_audit.lean` | 450 | `81d27e82d11b2935acb97a6e163959b929035ae0` |
| file | `_check.lean` | 312 | `c35f3619b8e8691d7d90784acd19d5b2cc424946` |
| file | `_test.lean` | 112 | `39844f6c15854b26fbd42560a529fe9ffaa1b1ef` |
| file | `_test_omega.lean` | 82 | `dac59bfed3c9cb2dd5a33eecddc295671468a013` |
| dir | `cases` |  | `660a37765ebaf00d0fe530eab2dcf573c64ca4f1` |
| file | `lake-manifest.json` | 3129 | `5aa22a2c216598c1827e9e86b6242110152af9af` |
| file | `lakefile.lean` | 183 | `089154f1e07cc3ff964dff4dd3c87948717c0261` |
| file | `lean-toolchain` | 25 | `af9e5d339aeb37e4e6ba2603fb873e637678e304` |

`JurisLean/` 子目录本身只做了这一层列举（得到 tree SHA），**未**再展开其下各 `.lean` 文件正文，也未对 ULM 分文件做审核打开。

## 5. 本轮已打开正文（仅此一件作为已核实打开）

- 路径：`docs/ulm-consolidated/HANDOFF.md`
- 固定 commit：`037e3f20142ddb0bc8874e9078378360b29122af`
- blob SHA（目录/检索记录中的对象）：`f656d8fa3a8719c54e1ce86019ba70f099030da0`
- 链接：https://github.com/laubeing-droid/legal-math-modeling/blob/037e3f20142ddb0bc8874e9078378360b29122af/docs/ulm-consolidated/HANDOFF.md

该文件是 ULM 合并施工包的启动说明，不是证明清单，也不是核过的证明计数。按收窄要求，本轮不据此做审核结论，也不把文中任何条数写成当前库状态。

## 6. 不得当作当前固定原文的本地副本

`/workspace/legal-math-modeling-ro` 是盒内既有 git 工作副本，只读查看了其 git 元数据：

- `origin`：`https://github.com/laubeing-droid/legal-math-modeling.git`
- 本地 `HEAD`：`be64da98022c0ea2e57914362b44d6ac51fc73a8`
- 该提交日期：`2026-09-29T15:22:18+08:00`（2026-09-29 15:22:18 Asia/Shanghai）
- 说明：`chore(inventory): rebind after the nine-fix source commit`

该副本早于当前 `main` 头 `037e3f20`（2026-11-09）约六个星期，**不得当作当前固定原文**，也不得用它统计当前声明。本轮未对该副本做 fetch 或更新。

## 7. 既有导出包：可读，但无 T0

可打开的既有导出包（盒内文件）如下。JSON 顶层仅有 `format` / `version` / `bots`，**没有** `exported_at`、`cutoff`、`T0` 或同等截止字段。文件 mtime 只是盒内记录时间，不是来源事件时间，不能当成 T0。

| 路径 | 盒内 mtime（Asia/Shanghai，记录时间） | 格式观察 |
| --- | --- | --- |
| `/workspace/exports/grok-bot-export-法律数学评审员.json` | 2026-11-07 16:08:09 | `format=grok-bot-export`，`version=1`，1 个 bot（法律数学评审员）；无 T0 |
| `/workspace/exports/grok-bot-export-法律数学评审员-cursor-skills.json` | 2026-11-07 16:13（目录列举时间） | 同批导出产物；本轮未把其正文当增量全集打开 |
| `/workspace/grok-bot-export/grok-bot-export-法律编程审核员.json` | 2026-11-07 16:11:01 | `format=grok-bot-export`，`version=1`，1 个 bot（法律编程审核员）；无 T0 |
| `/workspace/grok-bot-export/bot-meta.json` | 2026-11-07 16:05:54 | 有 `memory_coverage_note`（说明记忆导出是检索子集、并非全量），无 T0 |

`/workspace/chatgpt-export-2026-11-06` 目录存在，但在 2026-11-13 查看时为空（仅 `.` / `..`），不能当作已交付的 ChatGPT 导出原文。

因此：既有导出包之后（任务所称 2026-11-07 之后）的数学经历增量，本轮**不能**在缺 T0、且未按来源事件时间核对原始对话的前提下宣称完整。切换前仍须补核。本轮按收窄要求不写增量正文清单。

## 8. 缺件

1. **数学理论集中区路径**：在已查的只读记录、导出包字段与已打开的 `HANDOFF.md` 中，**未能定位**名为或可确认等于“数学理论集中区”的既有目录。此为缺件。按主人收窄，不再扩大搜索（含用户电脑与 LXPPS）。未确认可写位置，不复制、不迁移。
2. **证明清单正文未作为本轮已打开审核原文**：`docs/formal-release/theorem_inventory_v3.json` 等仅完成目录列举（名称 / 大小 / blob SHA）。本轮不对清单正文做计数、绑定核对或小样。
3. **导出包无 T0**：见第 7 节。无法从包内元数据给出精确截止点。
4. **当前 commit 的构建 / 公理状态未核**：未跑 Lean / Lake / CI；也未把历史 Actions 结果当作当前验证。`ci_run_index.*` 仅在目录中见到文件名。
5. **`proofs/lean/juris_lean/JurisLean/` 下各证明源文件**：仅有目录 tree SHA，未展开、未打开正文。
6. **空的 `/workspace/chatgpt-export-2026-11-06`**：缺实际导出内容。
7. **本地陈旧副本与当前 main 不对齐**：见第 6 节，不能补作原文。

## 9. 验收与未核

**本轮可验收（可访问性）：**

- 已用现有 GitHub 只读连接器确认精确 owner/repo 与当前 `main` 固定 commit。
- 已列出该 commit 下根目录、`docs/formal-release`、`proofs/lean`、`proofs/lean/juris_lean` 的目录条目（含清单文件的名称 / 大小 / blob SHA）。
- 已打开并确认 `docs/ulm-consolidated/HANDOFF.md` 可读。
- 已记录导出包可读但无 T0，以及数学理论集中区路径缺件。
- 已声明未跑 Lean / Lake / CI，且本地 `legal-math-modeling-ro` 不得当当前原文。

**本轮明确未做、故未核：**

- 声明原始数量及计数定义的正文核对
- 重复 / 包装 / 别名与真正推导的区分
- 假设、公理、sorry / admit 及其他占位路径
- 依赖版本与传递边界的正文核对（`lean-toolchain` / `lakefile.lean` / `lake-manifest.json` 仅有目录条目；不在此给出版本结论）
- 固定版本上的历史构建证据覆盖范围
- 有原文位置的 2–3 个小样
- 2026-11-07 之后数学经历增量清单
- 数学理论集中区是否可写

后续若继续审核，须先打开固定 commit 上的清单与源文件正文，再做人话解释与真实性核对；本文件不构成任何通过结论。

## 10. 收窄前已发生、但不纳入本轮审核使用的说明

在主人收窄“只交可访问性、不要读清单正文或做小样”之前，工作过程中还取回过若干文件正文或副本。按收窄要求：**本文件不以它们为审核证据，不从中给出计数或通过/失败判定，也不做小样。** 仅记录以免把“未打开”写成与过程不符的假象：

- 曾用 GitHub 连接器取回 `docs/formal-release/declaration_shape_report.json`、`proofs/lean/juris_lean/lean-toolchain`、`proofs/lean/juris_lean/lakefile.lean` 的正文。
- 连接器把 `theorem_inventory_v3.json` 落到短截断副本后，曾用该仓已经公开可读的 raw URL，把与目录列举体积相符的文件放到 `/workspace/math-static-review/evidence/theorem_inventory_v3.json`。该副本存在这一事实予以记录，但**本轮不打开、不引用、不分析其正文**。

以上均发生在收窄指令之前；收窄之后未再搜索或打开新源。
