# MATH-LEAN-FULL 首批数学审计：G21 与 G02 自有核心

- 身份：法律数学评审员 / Grok Bot
- 底层模型身份：不可核实，不编造
- 时间：2026-11-14 00:42 Asia/Shanghai
- 仓库：`laubeing-droid/legal-math-modeling`
- 冻结提交（完整 SHA，不变）：`037e3f20142ddb0bc8874e9078378360b29122af`
- 工作方式：只静态阅读已对核的正文缓存；未改仓库、未运行 Lean／Lake／CI 或项目程序，未新下载或 clone/checkout，未自行检索法源
- 本文件是本批**独立主稿**（规范文件名，见文末）。检查点 1 旧稿（`MATH-LEAN-FULL_checkpoint1_*.md`、`work_anchor.md` 及对话已发出的 00:31 文本）不覆盖、不改写；口径补正见已另文 `20261114_法律数学评审员_MATH-LEAN-FULL_检查点1_已读口径补正.md`
- 其中 678／678 只表示取回、blob 对核与词法扫描，不是逐篇数学精读
- 原 104 项任务继续共存：补充已入私有仓 `71de6f1` 仍为候选，登记≠审查、≠验证完成；本任务不顶替原任务
- 编程岗第 4 批索引自报 97／678 只可作路径线索；本批声明与推导均独立阅读冻结正文，不继承其结论
- 【如果由我来证】均写在正文里（步骤、关键引理、适用条件、核验办法），一律标**候选**；未运行 Lean／Lake／CI，不得装已证

## 0. 本批范围、覆盖与余量

本批不审完全部原拟 31 个文件，以免用总述假装精读。先完成 **G21 全部**与 **G02 中本仓自有核心**（不含 `External/FixedPointTheorems*`）。

| 口径 | 数量 | 说明 |
|---|---:|---|
| 本批逐篇精读文件 | **13** | 清单见覆盖索引 |
| 本批词法声明 | 89 | 其中 theorem／lemma **55**，定义类 34 |
| 已解释有意义组 | **8**（B1–B8） | 每组有可追索声明归属，不用一组总述冒充 55 条都用同一段话打发 |
| 已解释 theorem／lemma | **55／55**（仅限这 13 个文件） | 静态解释，Lean 未验 |
| 已写【如果由我来证】 | **8** 组，一律标**候选** | 未经 Lean 验证，不得装已证 |
| 依赖抽查、不计入本批「已精读／已解释」分母 | 2 | `HornDefinitions.lean`、`HornFixedPoint.lean`，只为追 ULM15 的 `TH`／`horn_result_fixed_point`；G03 整组仍未审 |
| 原拟 31 文件中未在本批精读 | **18** | G02 外部不动点 7 个（词法 106）＋ G03 核心 6 ＋ G04 核心 5 |
| 全仓 `.lean` 尚未逐篇精读 | **665／678** | 678 仍只是取回／对核／词法分母 |
| 编译器声明总数 | **未知** | 未运行 elaborator |

下一批建议：先补完 G02 外部依赖（`External/FixedPointTheorems*`，7 文件，词法 106），再进入原 31 文件中的 G03 核心（Dung／Horn），因为 ULM15 已经引用 Horn 闭包。不要用本批结论覆盖那些文件。

## 1. 组 B1　有限并半格上的余伴随（`FiniteGaloisAdjunction.lean`）

**归属：** `FinitePoset`（L16）、`ResiduatedMap`（L24）、`legalResidual`（L31）、`IsGaloisConnection`（L45）、`fn_sup_preserves`（L36）、`galois_connection_of_residuated`（L49）。

### 目标

在带底的有限并半格上，对保有限并（文中给的是保二元并与保底）的自映射 `fn`，用

`legalResidual a y := ⊔ { x | fn x ≤ y }`

构造右伴随，并证明 `fn x ≤ y ↔ x ≤ legalResidual a y`。

### 前提

- `FinitePoset α`：`SemilatticeSup`、`OrderBot`、`Fintype α`、可判定的 `≤`。有限性保证 `{ x | fn x ≤ y }` 可写成 `Finset` 并存在 `sup`；可判定性用于 `filter` 中的 `decide`。
- `ResiduatedMap` 的三条运算条件：`mono`、`map_sup`（二元）、`map_bot`。`map_bot` 不能单靠二元 `map_sup` 推出（`f ⊥ = f ⊥ ⊔ f ⊥` 并不迫使 `f ⊥ = ⊥`），因此保底是独立前提。`mono` 则可由保二元并推出：`x ≤ y` 当且仅当 `x ⊔ y = y`，从而 `fn x ⊔ fn y = fn y`。这是可删的冗余前提，不是空真。

### 关键引理／依据

- `fn_sup_preserves`：对任意有限集 `s`，`fn (s.sup id) = s.sup fn`。对 `Finset.cons` 归纳：空集用 `map_bot`，并步用 `map_sup`。这是把二元保并升到有限并的关键。
- 右向：若 `fn x ≤ y`，则 `x` 属于被取 `sup` 的集合，故 `x ≤ legalResidual a y`（`Finset.le_sup`）。
- 左向：若 `x ≤ legalResidual a y`，由单调性 `fn x ≤ fn (residual y)`；再用 `fn_sup_preserves`，`fn (residual y)` 等于该集合上 `fn z` 的上确界，而每个 `z` 满足 `fn z ≤ y`，故上确界 `≤ y`。

### 现有步骤（追定义，不以注释当证明）

正文 L52–L66 按上述两向写完，没有把目标写进前提，也不是 `True` 逃避。`legalResidual` 的集合是 `univ.filter (fun x => decide (a.fn x ≤ y))`，与「`fn x ≤ y` 的全体」在已给 `decidable_le` 时一致；这一点依赖类里的可判定实例（L20–L21 的 `attribute [instance]`），不是法律判断。

### 法律对应（模型 ≠ 现实法律）

函数名 `legalResidual` 和注释里的 “legal residual” **只是数学余伴随（右伴随）的命名**，正文没有引用任何法条，也没有把 `≤` 解释成权利、许可或效力位阶。本定理不支持「法律上的剩余权利／ residual rights」之类现实命题。无需为此向资料员查法。

### 哪里绕／可简化

- `mono` 字段可删，改为由 `map_sup` 推出的引理。
- 也可直接对标 Mathlib 的 `GaloisConnection`，避免自写 `IsGaloisConnection`。
- 绕开之处不明显；证明长度已经接近标准教科书论证。未调用现成 `sSup`／完全格接口，而是用 `Finset.sup`，与「有限」前提匹配，这是合理选择而不是偷换。

### 【如果由我来证，我会怎么证】（候选，未经 Lean 验证）

从前提出发：给定 `FinitePoset α`（有限、有底、并半格、`≤` 可判定）以及保二元并与保底的 `fn`。

关键引理（先证这两条，再证伴随）：

1. `map_sup_implies_mono`：若 `x ≤ y`，则 `x ⊔ y = y`，故 `fn x ⊔ fn y = fn y`，即 `fn x ≤ fn y`。因此现结构里的 `mono` 字段可改为派生引理。
2. `fn_sup_finset`：对任意 `s : Finset α`，`fn (s.sup id) = s.sup fn`。空集用 `map_bot`；`cons` 步用 `map_sup` 与归纳假设。若把空并直接写进「保全部有限并」，则 `map_bot` 也可并入同一条。

推导步骤：

3. 定义 `g y := (Finset.univ.filter (fun x => fn x ≤ y)).sup id`（与现 `legalResidual` 相同）。
4. 右向 `fn x ≤ y ⇒ x ≤ g y`：由 3，`x` 属于被取上确界的有限集，用 `Finset.le_sup`。
5. 左向 `x ≤ g y ⇒ fn x ≤ y`：由引理 1 得 `fn x ≤ fn (g y)`；由引理 2，`fn (g y)` 等于 `{fn z | fn z ≤ y}` 的上确界，故 `≤ y`；再传递。
6. 合并 4、5，即 `IsGaloisConnection`／`GaloisConnection fn g`。

为什么推出结论：在有限并半格上，「保全部有限并」的映射恰有右伴随，且右伴随必须是水平集 `{x | fn x ≤ y}` 的上确界。步骤 4、5 分别是伴随不等式的两个方向，没有把目标写进前提。

简化／替代：直接使用 Mathlib `GaloisConnection`，用 `GaloisConnection.l_le` 与 `le_u` 复述双向命题，避免自写谓词。

适用条件：只在有限、可判定序、且 `fn` 保全部有限并时适用。一般完全格必须对任意（可能无限）并论证，不能用 `Finset.cons` 归纳了事。

核验办法（本批未做，保持候选）：在冻结提交 `037e3f20142ddb0bc8874e9078378360b29122af` 上编译 `JurisLean.FiniteGaloisAdjunction`；若改用 `GaloisConnection`，再检查能否由 `l_le`／`le_u` 回推 `∀ x y, fn x ≤ y ↔ x ≤ g y`。未运行 Lean／Lake／CI，不得把上述步骤当作已证。

## 2. 组 B2　冻结样本的标签计数（`FiniteRosetta.lean`）

**归属：** `MappingStatus`（L12）、`mappingStatus`（L24）、四个计数定义（L34–L46）、`cnOnly_eq_30`（L49）、`collision_eq_4`（L52）、`asymmetry_eq_3`（L55）、`obstruction_eq_37`（L58）、`cnOnly_exceeds_half`（L61）、`obstruction_exceeds_half`（L64）、`sample_mapping_not_total`（L68）、`obstruction_density_gt_two_thirds`（L75）、`pure_obstruction_majority`（L80）。

### 目标

对一个写死的 44 项编码函数 `mappingStatus : Nat → MappingStatus`，核对各类标签的个数，以及若干比较不等式。文件首行已写明：这是冻结样本分类，**不是**范畴论上的不可能性定理。

### 前提

唯一实质前提是定义本身：`i < 30` 为 `CN_ONLY`，其后若干区间分别是 `CN_US_PARTIAL`、`COLLISION`、`ASYMMETRY`、`CN_HK_PARTIAL`、`TRI_JURISDICTION_PARTIAL`，其余为 `TRI_JURISDICTION_MAPPED`。没有关于现实法域、映射函子或语义保持的假设。计数是对 `List.range 44` 做 `filter` 后取 `length`。

### 关键引理／依据与现有步骤

- `cnOnly_eq_30`、`collision_eq_4`、`asymmetry_eq_3`、`obstruction_eq_37` 的证明都是 `rfl`：在定义展开后，两边是同一个自然数。
- `cnOnly_exceeds_half`、`obstruction_exceeds_half`、`obstruction_density_gt_two_thirds`、`pure_obstruction_majority` 是 `by decide` 的算术比较（`30 > 22`、`37 > 22`、`37*3 > 44*2`）。
- `sample_mapping_not_total`：要证 `¬ (∀ i : Fin 44, mappingStatus i.val ≠ CN_ONLY)`。取 `i = ⟨0, _⟩`，由定义 `mappingStatus 0 = CN_ONLY`，矛盾。这只说明「编码里第 0 项是 CN_ONLY」，与「不存在跨法域函子」无关。文件 L66–L67 自己限制了声称，这项应按其字面理解。
- `pure_obstruction_majority` 的左边就是 `obstructionCount` 的定义，因而与 `obstruction_exceeds_half` 命题相同，属于重复包装，不是一条新的数学事实。

不得把注释里的 CSV 路径或「FP-CN-001」等标签名，当成已核对源数据的证据。正文没有读 CSV，只硬编码了区间。

### 法律对应

定理只约束这个 44 项函数的计数。它们**不**证明中国内地、美国或香港的制度无法对应，也不证明任何法源冲突。`CN_ONLY` 等是编码枚举值，不是法律结论。文件 L4–L8 已把「源 CSV 对应与法律解释」列为另行义务。本批**不**把这 44 项逐条变成法源需求；若将来有人要把 `mappingStatus` 当法律事实使用，那是材料／编码对应问题，须另开清单，且要有具体条目与要支持的命题，不能用本文件的 `rfl` 充作法律审查。

### 哪里绕／可简化

用区间硬编码代替表驱动，使 `rfl`／`decide` 容易通过，但与真实 `claim_mapping.csv` 是否一致，本文件未证。半数、三分之二阈值（L60–L76）与文首「本定理不需要多数阈值」（L8）并存：阈值命题只是样本算术，文首限制的是不要把多数当成法律或范畴结论。二者可以同时成立，但引用时必须分开。

### 【如果由我来证，我会怎么证】（候选，未经 Lean 验证）

从前提出发：不把「跨法域不可能」当作目标。唯一给定的是长度为 44 的冻结编码。

关键引理：

1. `mappingStatus_of_list`：存在显式列表 `labels : List MappingStatus`，长度为 44，使得 `i < 44` 时 `mappingStatus i = labels[i]`（越界另行约定，与现定理无关）。
2. `count_eq`：`cnOnlyCount = labels.count CN_ONLY`，同类对其余标签与 `obstructionCount`。

推导步骤：

3. 由列表计算四个计数，用 `rfl` 或 `native_decide` 得到 `cnOnly_eq_30`、`collision_eq_4`、`asymmetry_eq_3`、`obstruction_eq_37`。
4. 在 3 的等式上做普通算术，得到可选推论 `30 > 44/2`、`37 > 44/2`、`37*3 > 44*2`。这些不是主定理，只是该列表的数值性质；与「法律上需要多数」无关。
5. `sample_mapping_not_total`：只需指出某一个下标（例如 0）满足 `labels[0] = CN_ONLY`，从而否定「全体不是 CN_ONLY」。不由此推出函子不存在。
6. 不再单列 `pure_obstruction_majority`，因为它与 `obstruction_exceeds_half` 是同一命题。

为什么推出结论：这些等式是有限列表的计数，一旦列表固定，自然数计算是决定性的；没有任何法律或范畴前提进入步骤 3–5。

适用条件：只对这一冻结编码成立。列表或区间改动后必须重算全部等式。即使计数正确，也不能把它解释成法源冲突或映射不可能。

核验办法（本批未做，保持候选）：（a）把同一提交中的 `data/category_rosetta/claim_mapping.csv` 与列表逐项对照，这是数据对应，不是 Lean 证明，本批未做；（b）编译上述 `rfl`／`decide` 目标。未运行 Lean／Lake／CI，不得装已证。

## 3. 组 B3　有限单调迭代核（`FiniteMonotoneIteration.lean`）

**归属：** `FiniteMonotoneSystem`（L11）、`iter`（L22）、`iter_zero`（L28）、`iter_succ`（L30）、`iter_subset_univ`（L32）、`iter_mono`（L39）、`iter_stable`（L46）、`iter_ssubset_of_ne`（L62）、`iter_card_lt_of_ne`（L71）、`iter_card_le_univ`（L75）、`exists_fixpoint_le_card`（L80）、`fixed_at_card`（L103）。

### 目标

在有限底集合 `univ` 上，对满足 `step S ⊆ univ` 且单调的算子，从空集迭代 `iter 0 = ∅`、`iter (n+1) = step (iter n)`，证明：序列对包含关系递增；若某步稳定则以后恒定；若尚未稳定则基数严格增加；因此存在 `k ≤ |univ|` 使 `iter k = iter (k+1)`；特别地，`iter |univ| = iter (|univ|+1)`。

### 前提

`FiniteMonotoneSystem` 只有两条算子公理：`step_subset_univ`、`step_monotone`。**没有**假定 `step` 普遍膨胀（`S ⊆ step S`）。从空集出发仍然递增，是因为 `∅ ⊆ step ∅` 对任意步函数成立，再用单调性归纳。这是条件用得干净的地方，不是把结论写进前提。

### 关键引理／依据与现有步骤

- `iter_zero`／`iter_succ`：定义展开（`rfl`）。
- `iter_subset_univ`：对 `n` 归纳；后继步用 `step_subset_univ`。
- `iter_mono`：对 `n` 归纳；后继步把归纳假设送入 `step_monotone`。
- `iter_stable`：一旦 `iter n = iter (n+1)`，对 `k` 归纳得 `iter (n+k) = iter n`。
- `iter_ssubset_of_ne`：已有 `⊆`，若再有反向 `⊆` 则相等，与「不等」矛盾，故是真子集。
- `iter_card_lt_of_ne`：真子集则基数增（`Finset.card_lt_card`）。
- `iter_card_le_univ`：由 `iter n ⊆ univ`。
- `exists_fixpoint_le_card`：反证。若所有 `k ≤ |univ|` 都有 `iter k ≠ iter (k+1)`，则这些步基数严格递增，进而 `k ≤ |univ|+1` 时有 `|iter 0| + k ≤ |iter k|`。但 `|iter 0| = 0`，故 `|univ|+1 ≤ |iter (|univ|+1)| ≤ |univ|`，矛盾。这是标准有限鸽笼／严格升链论证，结论没有预先放在前提里。
- `fixed_at_card`：取上述某个 `k ≤ |univ|`，用稳定性把 `|univ|` 和 `|univ|+1` 都写成 `k` 加上非负偏移，因而两端都等于 `iter k`。

### 法律对应

这是一般的有限单调算子迭代，注释说可供 AAF 与 Horn 共用。它本身不是法律程序、期限或既判力模型。后文 ULM15 对 Horn 的引用，也不把本核「变成」现行法上的推论规则。

### 哪里绕／可简化

正文没有写出「`iter |univ|` 是最小不动点」。材料已经够用：对任意前缀点（或不动点）`S`（`step S ⊆ S`），归纳可得 `iter n ⊆ S`。这不是缺陷到否定现有定理，而是少写了一条自然推论。Horn 侧后来补了最小性（依赖抽查所见，见组 B8），本文件作为公共核却未陈述。

### 【如果由我来证，我会怎么证】（候选，未经 Lean 验证）

从前提出发：`step S ⊆ univ`，且 `S ⊆ T ⇒ step S ⊆ step T`。不额外假定 `S ⊆ step S`。定义 `iter 0 = ∅`，`iter (n+1) = step (iter n)`。

关键引理：

1. `iter_subset_univ`：对 `n` 归纳；后继用 `step_subset_univ`。
2. `iter_mono`：`iter n ⊆ iter (n+1)`。`n=0` 时用空集是最小元；后继把归纳假设送入 `step_monotone`。
3. `iter_stable`：若 `iter n = iter (n+1)`，则对 `k` 归纳 `iter (n+k) = iter n`。
4. `iter_card_strict`：若 `iter n ≠ iter (n+1)`，由引理 2 得真子集，故基数至少加一。
5. `iter_le_prefixpoint`（现稿未写，建议补）：若 `step S ⊆ S`，则对 `n` 归纳 `iter n ⊆ S`。起点是空集；后继用单调性与前缀点条件。

推导步骤：

6. 存在性：若所有 `k ≤ |univ|` 均未稳定，则由引理 4，`|iter k| ≥ k`。取 `k = |univ|+1`，得 `|iter (|univ|+1)| ≥ |univ|+1`，但由引理 1 有 `|iter _| ≤ |univ|`，矛盾。故存在 `k ≤ |univ|` 使 `iter k = iter (k+1)`。
7. 由引理 3，`iter |univ| = iter k = iter (|univ|+1)`，即 `iter |univ|` 已是不动点（`step (iter |univ|) = iter |univ|`）。
8. 最小性：对任意不动点或前缀点 `S`，由引理 5，`iter |univ| ⊆ S`。

为什么推出结论：空集是最小元，所以迭代从下方逼近；单调性使链递增；有限底禁止无限严格升链，故有限步内稳定；再由引理 5，该稳定值低于一切前缀点，因而是最小不动点。结论没有预先放进 `FiniteMonotoneSystem` 的字段里。

简化／替代：用势函数 `|univ| - card(iter n)` 做良基归纳，代替步骤 6 的反证，逻辑等价。

适用条件：底必须是有限 `Finset`。无限完全格不能用 `|univ|` 作步数上界，需要 ω 或序数迭代，本路线不适用。

核验办法（本批未做，保持候选）：编译本文件现有十条定理，并增加 `iter_le_prefixpoint` 与「`iter |univ|` 是最小不动点」两条；用一个小的单调 `step` 例子手工检查步数上界。未运行 Lean／Lake／CI，不得装已证。

## 4. 组 B4　加权上确界距离的度量公理，但不是完备性（`SupZeroLemma.lean`、`WeightedSupNorm.lean`、`BanachComplete.lean`）

**归属：**

- `sup'_eq_zero_of_nonneg`（`SupZeroLemma.lean` L11）
- `PositiveWeights`、`weightedSupDist`、`weightedSupNorm`（`WeightedSupNorm.lean` L28–L35）
- `weightedSupDist_nonneg`（L39）、`_triangle`（L50）、`_symm`（L72）、`_separates_points`（L81）
- `weightedMetricSpace`（`BanachComplete.lean` L15）、`weightedMetricSpace_dist`（L28）

### 目标

对 `n ≥ 1`（以 `[Nonempty (Fin n)]` 表达）和正权重 `w i > 0`，定义

`weightedSupDist w x y = max_i |x i − y i| / w i`

并证明非负、三角、对称、以及 `d(x,y)=0 ↔ x=y`。`BanachComplete.lean` 再把这四条装进 `MetricSpace` 实例，并证明 `dist` 就是该函数。

### 前提

- `Nonempty (Fin n)`：否则 `Finset.univ` 为空，`sup'` 无定义。`n = 0` 不在范围内。
- 分离性、非负、三角需要 `PositiveWeights`（对称性对权重符号不敏感，定理也未要求 `hw`）。
- 实数绝对值与有限 `sup'` 的常规性质。

### 关键引理／依据与现有步骤

- 非负：任取一指标，该项 `≥ 0`，且不超过 `sup'`。
- 三角：对每个 `i`，`|xi−zi| ≤ |xi−yi|+|yi−zi|`，同除以正的 `w i` 后，两项分别不超过相应的 `sup'`。
- 对称：`|xi−yi| = |yi−xi|`，`sup'` 逐项相等。
- 分离：`d=0` 时每个非负项 `≤ 0` 故为 0；`a/w i = 0` 则 `a=0` 或 `w i=0`，后者与正权重矛盾。反向：`x=y` 时每项为 0。文件把「非负」与「分离」写在同一条定理里，非负部分直接调用前一定理。
- `SupZeroLemma` 正是「非负族的 `sup'=0` ⇒ 各项为 0」。`WeightedSupNorm.lean` 导入了它，但分离性证明把同一论证内联写出，未调用该引理。引理本身论证正确，只是本链未使用。
- `weightedMetricSpace` 用上述四条填 `MetricSpace` 的 `dist_self`、`dist_comm`、`dist_triangle`、`eq_of_dist_eq_zero`；`edist` 定义为 `ENNReal.ofReal` 同一距离，`edist_dist` 为 `rfl`。`weightedMetricSpace_dist` 也是 `rfl`。

**关键限制（不得被文件名带偏）：** 这三条文件**都没有**证明 `CompleteSpace (Fin n → ℝ)`，也没有证明该度量下的柯西列收敛。`WeightedSupNorm.lean` L11–L20 自己写了「此处无完备性」。`BanachComplete.lean` 的模块说明是「Weighted Sup Metric Space」，文件名却叫 `BanachComplete`，容易被读成 Banach 完备性已证。静态所见只是度量公理的打包。

### 法律对应

加权极差是有限维实向量的数学度量，与任何法律上的「权重」「完整性」无关。

### 哪里绕／可简化

分离性可直接引用 `sup'_eq_zero_of_nonneg`，少写十几行。未建立与未加权 `∞` 范数或 `PiLp` 的等距，导致后文难以借用 Mathlib 现成的完备性实例——这是绕开现成定理、把 Track B 的完备性债务留下的主要技术原因。

### 【如果由我来证，我会怎么证】（候选，未经 Lean 验证）

从前提出发：`n ≥ 1`（`Nonempty (Fin n)`），`PositiveWeights w`（每个 `w i > 0`），距离为 `d_w(x,y) = max_i |x i − y i| / w i`。

关键引理：

1. 现已有的四条：非负、三角、对称、分离（证明路线与现稿相同：逐坐标比较与 `sup'`）。
2. `scale_isometry`：定义 `Φ x i := x i / w i`，`Ψ z i := w i * z i`。则 `Φ`、`Ψ` 互逆，且 `d_w(x,y) = d_∞(Φ x, Φ y)`，其中 `d_∞(u,v) = max_i |u i − v i|`。因为 `w i > 0`，除法与乘法都是坐标上的双射。
3. `linfty_complete`：`(Fin n → ℝ, d_∞)` 完备，因为它等距于有限个完备空间 `ℝ` 的积（`∞` 度量与有限积的通常度量等价）。

推导步骤：

4. 用引理 1 安装 `MetricSpace` 实例（与现 `weightedMetricSpace` 相同）。
5. 完备性（现稿所缺，以下为候选）：取 `d_w` 的柯西列 `(x_k)`。由引理 2，`(Φ x_k)` 是 `d_∞` 的柯西列。由引理 3，存在 `z` 使 `Φ x_k → z`。令 `x := Ψ z`，则 `x_k → x`（等距拉回）。故 `(Fin n → ℝ, d_w)` 是 `CompleteSpace`。

为什么推出结论：有限维实空间上，正权重只是对各坐标做一次可逆缩放；缩放是等距，完备性沿等距传递。这不依赖 Banach 不动点，也不依赖任何法律解释。现有四条度量公理仍然保留；本候选只补文件名容易让人以为已经完成的那一截。

适用条件：正权重、有限且非空的指标集。若某个 `w i = 0`，`Φ` 无定义（或 Lean 实除法把该项打成 0，等距失败）。无限维序列空间不能靠有限积完备性。

核验办法（本批未做，保持候选）：写出 `scale_isometry` 与 `CompleteSpace` 实例，确认其 `dist` 与 `weightedMetricSpace` 一致，再编译。未运行 Lean／Lake／CI。在此之前，不得把 `BanachComplete.lean` 当作完备性已证。

## 5. 组 B5　加权压缩的代数不等式与数据包（`ContractionCondition.lean`、`BanachContraction.lean`、`BanachFixedPoint.lean`、`BanachWeightedNorm.lean`）

**归属：** `LipschitzCoupling`（`ContractionCondition.lean` L24）、`CoordinateLipschitz`（L28）、`lipschitz_coupling_implies_weighted_contraction`（L33）；`weighted_contraction_bound`（`BanachContraction.lean` L21）、`weighted_contraction_bound_nnreal`（L34）；`WeightedContractionData`（`BanachFixedPoint.lean` L22）、`weightedContractionData_of_coupling`（L34）；`WeightedContractionTarget`（`BanachWeightedNorm.lean` L37）、`LipschitzMatrixCondition`（L43）。

### 目标

在坐标 Lipschitz 条件

`|T x i − T y i| ≤ Σ_j L i j * |x j − y j|`

以及耦合 `Σ_j L i j * w j ≤ q * w i`（`L ≥ 0`，`w > 0`）下，证明

`weightedSupDist w (T x) (T y) ≤ q * weightedSupDist w x y`。

其后文件把同一不等式换名为 `weighted_contraction_bound`，在 `q ≥ 0` 时改写右端为 `toNNReal q`，再把它装进 `WeightedContractionData`（此时才加入 `q < 1`）。

### 前提与对「q < 1」的区分

代数定理**不要求** `q < 1`。它对其它实数 `q` 同样陈述一条 Lipschitz 型上界。`ContractionCondition.lean` 文首（L11–L14）把「`q < 1` 则是加权上确界压缩」写成叙述，但定理假设列表（L33–L40）没有 `q < 1`。这不是把结论塞进前提，而是**文首叙述窄于、也强于实际定理**。要接到 Banach／`ContractingWith`，必须另外假设 `0 ≤ q < 1`，以及度量空间的完备性；后两者在本文件组中仍是未证或未连接的前提，不是已满足的事实。

`weightedContractionData_of_coupling` 把 `q < 1` 作为输入假设写入结构，并不证明某个具体算子的 `q` 小于 1。这是条件数据包，不是不动点定理。尽管文件名为 `BanachFixedPoint.lean`，正文 L9–L14 已声明不动点实例化有意推迟。

`WeightedContractionTarget`（`BanachWeightedNorm.lean` L37–L38）的类型是 `0 < q ∧ q < 1`，参数 `_T`、`_w` 被丢弃。文件 L33–L36 **自己说明**不要把它当成已证的压缩界。这不是空真（它仍要求 `q` 落在 (0,1)），但它与算子、权重无关，关闭它不产生任何关于 `T` 的信息。`LipschitzMatrixCondition` 与 `LipschitzCoupling` 命题相同，属重复定义。

### 关键步骤（代数定理）

对每个坐标 `i`：用坐标 Lipschitz 除以 `w i`；把和拆成 `Σ (L i j w j / w i) * (|x j−y j|/w j)`；再用 `|x j−y j|/w j ≤ d(x,y)` 和耦合 `Σ L i j w j ≤ q w i`，得到单项 `≤ q * d(x,y)`；最后对 `i` 取 `sup'`。推导依赖 `w i > 0` 做除法，依赖 `L ≥ 0` 才能在放大 `|x j−y j|/w j` 时保持不等式方向。步骤是代数的，没有引用完备性，也没有暗用 `q < 1`。

`weighted_contraction_bound` 只是对该定理的逐字调用。`weighted_contraction_bound_nnreal` 在 `q ≥ 0` 时用 `toNNReal_of_nonneg` 改写系数，内容不增加。

### 法律对应

耦合矩阵与加权压缩是分析不等式，不是法律责任分配或「权重」的法定含义。

### 哪里绕／可简化

- 到 Mathlib `ContractingWith` 的桥被明确推迟，理由是尚无完备度量实例。组 B4 已指出完备性其实可以走有限维等距（仍为候选）。在缺桥的情况下，本条不等式不能自动升级为 Banach 不动点。
- `BanachContraction`／`BanachFixedPoint` 对同一结果的重复命名，增加了「已经有不动点定理」的误读风险，数学含量几乎为零。
- `WeightedContractionTarget` 应按文件自己的警告停止引用。

### 【如果由我来证，我会怎么证】（候选，未经 Lean 验证）

从前提出发：`w i > 0`，`L i j ≥ 0`，耦合 `Σ_j L i j w j ≤ q w i`，以及坐标 Lipschitz `|T x i − T y i| ≤ Σ_j L i j |x j − y j|`。此处**不**默认 `q < 1`。

关键引理：

1. `coord_div`：对每个 `i`，`|T x i − T y i| / w i ≤ Σ_j (L i j w j / w i) * (|x j − y j| / w j)`。由坐标 Lipschitz 除以正的 `w i`，再配平权重。
2. `term_le_dist`：每个 `|x j − y j| / w j ≤ weightedSupDist w x y`。
3. `coupling_div`：`Σ_j L i j w j / w i ≤ q`。
4. 由 1–3 对 `i` 取 `sup'`，得代数上界 `d_w(T x, T y) ≤ q d_w(x,y)`。这一步对任意实数 `q` 成立，只是 Lipschitz 型估计。

推导步骤（接到 Banach 时必须追加的前提，不得假装已经有）：

5. 另设 `0 ≤ q < 1`，以及 B4 候选中的 `MetricSpace` 与 `CompleteSpace` 实例（现稿尚未兑现完备性）。
6. 由 4 与 5，把上界改写为 `ContractingWith (Real.toNNReal q) T`。
7. 此时才可调用 Mathlib 的 `fixedPoint`、唯一性、迭代收敛与先验误差界（与组 B8 的包装相同）。B8 的包装在步骤 5、6 完成之前不能用在这个加权算子上。

为什么推出结论：步骤 4 是把坐标估计提升到加权 `∞` 范数的标准做法，用到 `L ≥ 0` 才能放大各项；步骤 6 只是把「Lipschitz 常数严格小于 1」翻译成 Mathlib 的压缩谓词。没有完备性就没有一般 Banach 存在性，不能跳过步骤 5。

适用条件：必须存在同时满足非负、耦合与坐标 Lipschitz 的同一组 `L,w,q`。`q ≥ 1` 时只保留步骤 4，不得宣称压缩映射原理。完备性依赖 B4 候选，本身仍未验。

核验办法（本批未做，保持候选）：先编译步骤 4 的现有定理；再取对角 `L i i = q`、`T x = q • x + b` 这类仿射例子，手工核对上界；待 B4 完备性候选写出后，再编译 `ContractingWith` 实例。未运行 Lean／Lake／CI，不得装已证。

## 6. 组 B6　仿射「有效节点」定价映射在 ℝ 上的压缩（`BanachEffectiveNodes.lean`）

**归属：** `pricingFn`（L29）、`pricingFn_sub`（L42）、`abs_pricingFn_sub`（L53）、`abs_one_sub_beta_of_pos_lt_one`（L62）、`one_sub_beta_lt_one`（L69）、`one_sub_beta_nonneg`（L73）、`pricingFn_contraction`（L81）、`pricingFn_fixed_point`（L107）、`pricingFn_unique_fixed_point`（L120）。命名空间 `EffectiveNodesPricing`。

### 目标

对 `f(x) = β T + (1−β) x`，在 `0 < β < 1` 下证明：Lipschitz 常数为 `1−β < 1`；`T` 是不动点；不动点唯一。

### 前提

`0 < β < 1`，`T, x, y ∈ ℝ`。这是一维欧氏绝对值度量，不依赖加权空间，也不依赖 Banach 一般定理。

### 关键步骤

- `pricingFn_sub`：直接展开，`ring` 得 `f(x)−f(y) = (1−β)(x−y)`。
- `abs_pricingFn_sub`：两边取绝对值，用 `abs_mul`。
- `abs_one_sub_beta_of_pos_lt_one`：由 `β < 1` 得 `1−β ≥ 0`，故 `|1−β| = 1−β`。
- `pricingFn_contraction`：把差写成 `(1−β)(x−y)`，再用上条把绝对值里的 `|1−β|` 换成 `1−β`，得到**等式** `|f(x)−f(y)| = (1−β)|x−y|`，因而也有 `≤`。不是空真；结论比定理写出来的不等式更强。
- `pricingFn_fixed_point`：`β T + (1−β) T = T`，`ring`。不需要压缩映射原理。
- `pricingFn_unique_fixed_point`：由 `β T + (1−β) x = x` 整理得 `β(T−x)=0`，再用 `β > 0` 得 `T=x`。这是一元一次方程，**已经写出完整代数证明**。L116–L119 的 “SORRY BOUNDARY／留作 incomplete-proof-token／需要 Banach 定理” 是过时注释，**不能当作「未证」的证据**，也不能反过来把注释当成证明。

`one_sub_beta_lt_one` 与 `one_sub_beta_nonneg` 在本文件后续定理中未被使用，但命题正确。

### 法律对应

注释把该函数称作「法律推理网络的有效节点定价」，并提到「Chapter 5, Theorem 5.2.1」（L140–L144）。这是内部理论叙述，不是法条。正文没有把 `β`、`T` 对应到任何收费、评估或法定标准。本定理只约束这个仿射函数。

### 哪里绕／注释过声称

L137–L144 写道：迭代从任意初值收敛到唯一均衡 `T`，速率 `(1−β)^n`。**正文没有证明迭代收敛或速率。** 已证的是单步 Lipschitz 等式、以及不动点就是 `T` 且唯一。由单步等式用归纳立刻能得到速率，但那一步未写。不得用注释补上这条推导。

### 【如果由我来证，我会怎么证】（候选，未经 Lean 验证）

从前提出发：`f(x) = β T + (1−β) x`，`0 < β < 1`，度量是 `ℝ` 上的绝对值。不依赖加权空间，也不把一般 Banach 定理当起点。

关键引理：

1. `pricingFn_sub`：`f(x)−f(y) = (1−β)(x−y)`，展开后 `ring`。
2. `abs_slope`：由 `β < 1` 得 `1−β > 0`，故 `|1−β| = 1−β`，从而 `|f(x)−f(y)| = (1−β)|x−y|`。这比现定理写出的 `≤` 更强。
3. `fixed_T`：`f(T) = T`。
4. `unique_alg`：若 `f(x)=x`，则 `β(T−x)=0`，又 `β>0`，故 `x=T`。不必引用一般不动点定理。

推导步骤（补现稿未写的收敛，仍为候选）：

5. 对 `n` 归纳证明 `|f^[n](x) − T| = (1−β)^n |x − T|`。`n=0` 显然。后继步：`f^[n+1](x) − T = f(f^[n](x)) − f(T)`，用引理 2 与归纳假设。
6. 因 `0 < 1−β < 1`，右端趋于 0，故 `f^[n](x) → T`，速率就是 `(1−β)^n`。

为什么推出结论：这是斜率为 `1−β`、不动点为 `T` 的仿射映射。差在每一步恰好乘上同一个常数，归纳即得几何速率。这里没有把「收敛」写进前提，也没有用注释代替步骤 5。

适用条件：仅限 `0<β<1` 的一维仿射情形。一般非线性或高维算子不能靠这一次代数消元；那些情形要回到组 B5 的压缩加完备性路线。

核验办法（本批未做，保持候选）：把引理 2 改写成等式定理，并增加步骤 5 的迭代公式后编译；可用 `β=1/2`、`x=0`、`T=1` 手工检查前几项。未运行 Lean／Lake／CI，不得把步骤 5、6 装成已证。现稿中的单步等式、`f(T)=T` 与代数唯一性，仍只是静态阅读，同样未验编译。

## 7. 组 B7　证书图式，不是 Banach 定理（`BanachCertificate.lean`）

**归属：** `BanachCertificate`（L21）、`verifyCertificate`（L37）；V3：`CertifiedApproximation`（L53）、`Admission`（L77）、`tryAdmit`（L82）、`no_certificate_rejected`（L90）、`certificate_has_q_lt_one_scaled`（L96）、`certificate_error_within_tolerance`（L103）、`certificate_has_nonempty_domain`（L110）、`certificate_has_positive_iterations`（L117）。

### 目标（按正文实际写出的东西，不以中文说明升级）

旧层：定义一张名为 Banach 证书的结构，并提供 `verifyCertificate`。新层 V3：把若干不等式做成结构字段，定义「有证书才能构造 Admission」，并证明这些字段可以从证书里再取出来。

### 前提、步骤与「条件不变量」区分

- `verifyCertificate`（L37–L39）忽略算子与证书，**恒返回 `true`**。这不是对误差、`q` 或不动点的检查。文件 L33–L35 已说这是轻量图式检查。不得把它读成数学验证通过。
- V3 的 `qLtOneScaled` 是自然数不等式 `qNumerator < qDenominator`，在分母为正时可以解释为有理数小于 1，但结构里**没有**把该有理数连到任何算子的 Lipschitz 常数，也没有把 `errorBound` 连到 `dist(T^[n] x, x*)`。
- 四条 `certificate_has_*` 定理的证明都是投影字段：`certificate.qLtOneScaled` 等。这是**条件不变量／记录投影**：如果你已经构造了 `CertifiedApproximation`，这些不等式作为构造义务已经被满足，定理只是再读出来。不是空真（`True`），也不是对任意外部数值证书做了独立验算。前提一旦满足，结论就是前提的一部分。
- `no_certificate_rejected`：`tryAdmit none = none`，由 `match` 定义 `rfl`。这只固定了这个函数的空输入行为，不是法律上的「无证书不准入」。

### 法律对应

中文注释有「军令级合同」「无证书不进系统」（L43–L47、L89）。这是产品门禁话术，不是现行法上的许可或证据规定。`applicableDomain : List String` 的非空性更不是法域或主管范围的法律判断。

### 哪里绕／可简化

旧层恒真检查与 V3 投影并存，容易让人以为「证书已被证明」。若目标是 proof-carrying 的逼近器，应把误差界写成与具体度量、迭代和 `q` 相关的命题，而不是 `Nat` 字段的自指。

### 【如果由我来证，我会怎么证】（候选，未经 Lean 验证）

从前提出发：我不以 `CertifiedApproximation` 的字段投影为目标。要证明的是「这张证书保证某次迭代的真实误差不超过容差」。因此先要有一个具体空间和算子。

关键引理（均须另证或引用已兑现的实例，不能从本文件字段读出）：

1. 选定度量下的 `MetricSpace` 与 `CompleteSpace`（加权情形见 B4 候选；一维仿射情形直接用 `ℝ`）。
2. `ContractingWith q T`，且 `0 ≤ q < 1`（加权情形见 B5 候选；一维仿射见 B6 的等式 Lipschitz）。
3. Mathlib／组 B8 包装中的先验误差界：`dist(T^[n] x0, x*) ≤ dist(x0, T x0) * q^n / (1-q)`，其中 `x*` 是唯一不动点。

推导步骤：

4. 证书应携带：权重（或声明所用度量）、`q`、初值 `x0`、迭代次数 `n`、容差 `ε`，以及引理 1、2 的证明项（或可检查的实例）。
5. 由引理 3 计算上界 `B(n) := dist(x0, T x0) * q^n / (1-q)`。准入条件是 `B(n) ≤ ε`，而不是结构里一个与距离无关的 `Nat` 字段 `errorBound ≤ tolerance`。
6. `tryAdmit` 只在引理 1、2 已兑现且步骤 5 的不等式成立时给出 `Admission`。`none` 输入返回 `none` 可以保留，但它只是选项类型的定义，不是法律准入。
7. 旧的 `verifyCertificate := true` 删除或改成真正执行步骤 5 的函数；字段投影定理不再作为 Banach 结果对外引用。

为什么推出结论：先验误差界之所以能控制真实距离，是因为压缩加完备性已经给出唯一不动点，并把迭代误差写成几何级数。少了引理 1 或 2，步骤 5 没有意义。这与「先把不等式写进结构再读出来」不是同一件事。

适用条件：随所选度量与压缩常数而定。没有完备性或 `q<1` 的压缩，不能签发。`q=0` 时要单独处理分母；一维仿射例子可用更紧的精确公式 `|x0−T| * q^n`（见 B6）代替一般先验界。

核验办法（本批未做，保持候选）：用组 B6 的例子 `β=1/2`、`T=1`、`x0=0`，手工计算 `B(n)` 与真误差 `2^{-n}`，对照步骤 5；再在 Lean 里对这个例子实例化（未运行 Lean／Lake／CI）。在桥接完成前，本文件只应被引用为图式，与其 L13 的自我限制一致，不得装成 Banach 已证。

## 8. 组 B8　ULM15：Horn 只增扩张、经验包装、以及 Mathlib Banach 的再利用（`ULM15IncrementalEmpiricalBanach.lean`）

**归属：** `HornAddDelta`（L17）、`extendHorn`（L24）、`TH_subset_extend`（L37）、`horn_iter_subset_extend`（L48）、`horn_closure_subset_extend`（L62）、`childFullRecompute`（L71）、`IncrementalImplementationCorrect`（L78）、`incremental_correct_returns_full_recompute`（L82）、`childFullRecompute_fixed`（L90）；`EmpiricalArtifact`／`attachEmpirical`／`empirical_is_read_only`（L100–L110）、`deviationScore`／`deviationScore_decomposes`（L113–L118）；`banach_exists_fixedPoint`（L126）、`banach_fixedPoint_unique`（L131）、`banach_iterates_converge`（L139）、`banach_apriori_error_bound`（L146）。

依赖抽查（不计入本批已精读分母）：`HornDefinitions.lean` 中 `HornRule`、`HornSystem`、`TH`（立即后承＝初始事实并上前提已含于 `S` 的规则头）、`TH_monotone`、`toFiniteMonotoneSystem`；`HornFixedPoint.lean` 中 `horn_result_fixed_point`（L43，把组 B3 的 `fixed_at_card` 翻成 `TH (iter |univ|) = iter |univ|`）。G03 其余定理未在本批解释。

### 8.1 Horn 只增扩张

**目标：** 在同一 `univ` 上并入新的事实与规则（`HornAddDelta` 要求新事实 ⊆ `univ`、新规则头 ∈ `univ`），证明立即后承算子、从而迭代序列，对系统扩张是单调的；把「子问题的全量重算」定义为扩张后系统上迭代 `|univ|` 步。

**步骤：** `TH_subset_extend` 按 `TH` 的定义分情况：旧初始事实仍在并集里；旧规则触发的头，在扩张后规则集里仍触发。`horn_iter_subset_extend` 对步数归纳：空集相等，后继步用 `TH_monotone`（对同一系统，集变更大）再接 `TH_subset_extend`（系统变大）。`horn_closure_subset_extend` 只是取 `n = univ.card`。`childFullRecompute` 即该迭代。因为 `extendHorn` 不扩大 `univ`，组 B3 的步数上界对扩张后系统仍然适用。

**法律对应：** 这是 Horn 立即后承在「只增加规则／事实、不扩论域」时的单调性，不是立法修订、溯及力或既判力。

这三段扩张单调性是有内容的，不是空真。

### 8.2 「增量正确性」定义与经验包装

`IncrementalImplementationCorrect` 定义为：实现函数对任意增量都**等于** `childFullRecompute`。于是 `incremental_correct_returns_full_recompute` 就是把该定义应用到一个 `delta`。这是**定义展开／条件不变量**，没有给出任何比全量重算更省的算法，也没有证明某个工作表实现正确。文件 L76–L77 把「优化实现仅当 refinement 到全量重算才正确」写成规格，定理与规格字面相同。

`empirical_is_read_only`：`attachEmpirical solutions score` 的 `normativeSolutions` 字段等于传入的 `solutions`（`rfl`）。它不证明经验分数不能改规范结论，只证明这个构造子把第一个参数原样放入字段。名称里的 “read-only” 超过了定理内容。`deviationScore_decomposes` 同样是定义的 `rfl`。

### 8.3 Mathlib Banach 包装

在前提 `{β} [MetricSpace β] [CompleteSpace β] [Nonempty β]` 以及 `ContractingWith K f` 之下，四条定理分别直接调用

`fixedPoint`／`fixedPoint_isFixedPt`、`fixedPoint_unique`、`tendsto_iterate_fixedPoint`、`apriori_dist_iterate_fixedPoint_le`。

这是对 Mathlib 已有定理的再利用，数学内容在 Mathlib，不在本文件。作为「在标准 Banach 前提下引用工具库」，步骤清楚，也不是把结论写进前提：完备性与压缩是**假设**，必须在具体空间上另证。

**与 G02 自有核心的断裂：** 组 B4 未证加权空间完备；组 B5 未证 `ContractingWith`。因此这四条包装**不能**自动用到 `weightedSupDist` 或 `BanachCertificate` 所谈论的算子上。把三者放在同一文件标题「Incremental Empirical Banach」下，容易造成「增量 Horn ＋经验分数＋Banach」已经接上的印象；静态阅读看不到这样的桥。

### 【如果由我来证，我会怎么证】（候选，未经 Lean 验证）

本文件混了三条独立路线，我会分开证，不把文件名当成已经接好的总定理。

**（甲）Horn 只增扩张。** 从前提出发：`HornAddDelta` 只在同一 `univ` 上增加事实和规则头。关键引理：`TH_subset_extend`（按 `TH` 定义分情况：旧事实仍在，旧规则头在更大规则集中仍能触发）；`TH_monotone`（已在 `HornDefinitions.lean`，本批只作依赖抽查）。步骤：对迭代步数归纳得到 `horn_iter_subset_extend`，再取 `n = univ.card`。为什么成立：立即后承对「更多事实／规则」单调，且论域不变，故组 B3 的步数上界仍然可用。适用条件：不扩大 `univ`；若新增原子超出原论域，本论证失效。现证已经短而直接，这一段我维持原路线。

**（乙）增量算法（现稿所缺的实质部分，候选）。** 关键引理不是「实现＝全量重算」这一条定义。应另给一个工作表实现 `worklist(delta)`（例如从新增事实出发，只重放结论可能受影响的规则），然后证 `worklist(delta) = childFullRecompute sys delta`。推出原因必须是：被跳过的规则在扩张后不会产生新头，或产生的头已在工作表闭包里。`IncrementalImplementationCorrect` 可以保留为规格，但不要立刻用定义展开冒充正确性定理。核验：构造一个两条规则的小系统，一手算全量闭包，一手算工作表，再在 Lean 里对这个例子检查相等（未验）。

**（丙）经验「只读」。** 若目标真是规范结论不受评分影响，应证明 `TH` 与迭代不读取 `EmpiricalArtifact.score`／`label`，而不是证明构造子把 `solutions` 原样放入字段。适用条件随具体管道而定；当前定理覆盖不了「经验数据只读」。

**（丁）Banach 包装接到本仓模型。** 从前提出发，先完成 B4 的 `CompleteSpace` 候选与 B5 的 `ContractingWith` 候选；然后对同一个加权算子实例化 `banach_exists_fixedPoint` 等四条。为什么可以实例化：这四条只是 Mathlib 一般定理，一旦类型类前提被兑现就会作用在该空间上。在前提兑现之前，只把它们标为「对任意完备度量空间上的压缩映射成立」，不得称为「本仓加权模型已证 Banach」。

适用条件总表：Horn 甲限于论域不扩大的只增更新；乙依赖于所给工作表的具体不变量；丁限于已证完备且 `K<1` 的压缩。

核验办法（本批未做，保持候选）：甲可编译现有三条扩张定理；乙需新算法与例子；丁需在加权实例上对一个有限维收缩仿射算子检查先验误差界的数值。未运行 Lean／Lake／CI，不得装已证。

## 9. 问题发现（六段；只列对理解有影响者，不代替上面的正面推导）

下列各项不推翻组 B3 迭代核、组 B4 度量四条、组 B5 代数不等式、组 B1 伴随、组 B6 仿射计算的静态推导阅读。它们限制的是过宽的文件名、注释或包装。

### 发现 1　`BanachComplete.lean` 未证完备性

1. 对象与声称：文件名与「Track B 度量空间」语境易被读成 Banach 完备性已完成。  
2. 证据：`BanachComplete.lean` L8–L30，仅构造 `MetricSpace` 并证明 `dist` 定义展开。  
3. 静态所见：四条度量公理来自 `WeightedSupNorm.lean`；无柯西列、无 `CompleteSpace`。  
4. 影响：不能在此处启用 Banach 不动点；组 B5、B8 的桥仍然悬空。  
5. 区分：不是空真，是名称／范围大于正文。  
6. 待核：完备性只存在于本批 B4 的候选证明，Lean 未验。

### 发现 2　文首「q < 1」与代数定理假设不一致

1. 对象：`ContractionCondition.lean` 模块说明 vs `lipschitz_coupling_implies_weighted_contraction`。  
2. 证据：L11–L14 叙述含 `q < 1`；L33–L41 假设列表无此条。  
3. 所见：证明从未用到 `q < 1`，不等式对一般 `q` 成立。  
4. 影响：该定理本身成立且范围更宽；若有人把它直接叫「压缩」并引用 Banach，则前提不足。  
5. 区分：不是把结论写进前提，是叙述强于定理。  
6. 建议：叙述改为 Lipschitz 上界；`q < 1` 只在 `WeightedContractionData` 或 `ContractingWith` 处出现。

### 发现 3　`verifyCertificate` 恒真，V3 定理是字段投影

1. 对象：`BanachCertificate.lean` 旧检查器与 V3 定理。  
2. 证据：L37–L39 `:= true`；L96–L121 证明为 `certificate.qLtOneScaled` 等。  
3. 所见：无误差公式，无算子。  
4. 影响：不能当作 Banach 或数值证书已验证。  
5. 区分：V3 定理是条件不变量（构造时已承担的不等式再读出），不是 `True` 逃避，也不是对外部数据的独立检验。  
6. 建议：见组 B7 候选证书定义。

### 发现 4　`pricingFn` 注释声称收敛速率，正文未写

1. 对象：`BanachEffectiveNodes.lean` 文末说明 vs 已证定理。  
2. 证据：L137–L144 声称迭代以 `(1−β)^n` 收敛；已证范围止于 L81、L107、L120。L116–L119 的 SORRY 注释与已经写出的唯一性证明冲突。  
3. 所见：单步等式已有，迭代公式未写；唯一性已用代数证完。  
4. 影响：收敛／速率不得标为已证；唯一性不得因过时注释被标成未证。  
5. 区分：不以注释为推导证据。  
6. 候选：见组 B6 的归纳公式。

### 发现 5　ULM15 的 Banach 包装未接到本仓加权模型

1. 对象：`banach_*` 四条与加权／证书模块的关系。  
2. 证据：`ULM15IncrementalEmpiricalBanach.lean` L122–L150 的类型类前提；对比 B4／B5 未给出这些实例。  
3. 所见：四条是 Mathlib 调用；Horn 扩张与经验构造也未使用这四条。  
4. 影响：文件名并列三类材料，不构成已完成的统一定理。  
5. 区分：包装定理在其自身前提下不是空真；缺的是前提在本仓模型上的兑现。  
6. 待核：加权空间的 `CompleteSpace` 与 `ContractingWith` 实例（候选，未验）。

### 发现 6　`WeightedContractionTarget` 与「增量正确」定义展开

1. 对象：`WeightedContractionTarget`；`incremental_correct_returns_full_recompute`。  
2. 证据：`BanachWeightedNorm.lean` L33–L38（文件已自揭）；`ULM15IncrementalEmpiricalBanach.lean` L78–L87。  
3. 所见：前者与 `T`、`w` 无关；后者是定义应用。  
4. 影响：二者都不能增加关于压缩或增量算法的知识。  
5. 区分：前者是名不副实的占位命题；后者是条件不变量，不是空真。  
6. 建议：停止把前者当合同；增量算法另写 refinement。

## 10. 本批法源需求

本批**没有**需要转交法律资料员的新法源条目。理由：所审命题或是序／度量／压缩／Horn 迭代的数学事实，或是冻结编码的计数；没有任何定理的关键步骤依赖一条制定法、司法解释或案例的现行效力。`legalResidual`、`CN_ONLY`、证书「准入」、经验「只读」都是模型命名，已在相应组里与现实法律分开。

原 104 项任务继续共存：补充已入私有仓 `71de6f1` 仍为候选，登记≠审查，验证仍为 0。法源状态仍按另文口径补正的分项登记，不在本批改写为已核或已转，也不用本任务顶替原任务。

## 11. 产物路径

按 t76u：新交付使用 `YYYYMMDD_法律数学评审员_…` 原文件名；不改写、不覆盖检查点 1 旧稿与 `work_anchor.md`。

| 路径 | 作用 |
|---|---|
| `/workspace/math-lean-full-20261114/20261114_法律数学评审员_MATH-LEAN-FULL_首批_G21与G02自有核心审计.md` | **本批主稿**（本文件） |
| `/workspace/math-lean-full-20261114/20261114_法律数学评审员_MATH-LEAN-FULL_首批_声明覆盖索引.md` | 声明覆盖索引（精读／解释／候选替代证明／未核分列） |
| `/workspace/math-lean-full-20261114/20261114_法律数学评审员_MATH-LEAN-FULL_工作锚点_首批追加.md` | 本批覆盖追加（新文件，不修改旧 `work_anchor.md`） |

工作区若仍留有英文草稿名，不算本批正式交付。未做 Canvas，未自称已入私有理论仓。请 Codex 用本对话完整 Markdown 回收。原 104 项补充仓 `71de6f1` 仍为候选，登记≠审查。

---

法律数学评审员 / Grok Bot  
时间：2026-11-14 00:42 Asia/Shanghai  
来源提交：`037e3f20142ddb0bc8874e9078378360b29122af`  
覆盖：逐篇精读 13 个文件；已解释 8 组、55 条 theorem／lemma（仅这 13 个文件）；候选替代证明 8 组（未验）；原拟 31 文件余 18；全仓尚未精读 665／678；编译器声明总数未知；原 104 项验证仍为 0。
