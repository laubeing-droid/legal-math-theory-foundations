# MATH-LEAN-FULL 首批声明覆盖索引（G21 与 G02 自有核心）

- 身份：法律数学评审员／Grok Bot
- 底层模型身份：不可核实，不编造
- 时间：2026-11-14 00:42 Asia/Shanghai
- 冻结提交：`037e3f20142ddb0bc8874e9078378360b29122af`
- 对应主稿：`20261114_法律数学评审员_MATH-LEAN-FULL_首批_G21与G02自有核心审计.md`
- 本索引只登记覆盖口径，不另写推导。检查点 1 旧稿不覆盖。原 104 项补充仓 `71de6f1` 仍为候选，登记≠审查。
- 编程岗第 4 批索引自报 97／678 未纳入本表计数，亦未继承其结论。
- 未运行 Lean／Lake／CI；「已解释」是静态阅读，「替代证明」一律为候选。

## 1. 分项计数

| 口径 | 数量 | 说明 |
|---|---:|---|
| 取回／blob 对核／词法扫描（全仓分母） | 678／678 | 不是逐篇数学精读 |
| 本批逐篇精读文件 | **13** | 下节清单 |
| 本批词法声明 | 89 | theorem／lemma 55＋定义类 34 |
| 已解释 theorem／lemma | **55／55**（仅这 13 个文件） | 见第 3 节，每条有组号归属 |
| 已说明定义类声明 | 34／34（仅这 13 个文件） | 作为前提／定义在主稿中说明，不是单独证明 |
| 已解释有意义组 | **8**（B1–B8） | 每组有【如果由我来证】正文 |
| 候选替代／简化证明 | **8** 组 | 未验，不得装已证 |
| 依赖抽查文件 | 2 | `HornDefinitions.lean`、`HornFixedPoint.lean`；**不计入**本批已精读／已解释分母，G03 未审完 |
| 原拟 31 文件中尚未精读 | **18** | G02 外部不动点 7（词法 106）＋G03 核心 6＋G04 核心 5 |
| 全仓尚未逐篇精读 | **665／678** | |
| 编译器声明总数 | 未知 | |
| 原 104 项验证 | 0 | 补充 `71de6f1` 仍候选 |

## 2. 已精读文件（13）

| 组 | 路径 | 词法声明（定理／引理＋定义类） |
|---|---|---|
| B1 | `proofs/lean/juris_lean/JurisLean/FiniteGaloisAdjunction.lean` | 6（命题 2，定义类 4） |
| B2 | `proofs/lean/juris_lean/JurisLean/FiniteRosetta.lean` | 15（命题 9，定义类 6） |
| B3 | `proofs/lean/juris_lean/JurisLean/FiniteMonotoneIteration.lean` | 12（命题 10，定义类 2） |
| B4 | `proofs/lean/juris_lean/JurisLean/SupZeroLemma.lean` | 1（命题 1，定义类 0） |
| B4 | `proofs/lean/juris_lean/JurisLean/WeightedSupNorm.lean` | 7（命题 4，定义类 3） |
| B4 | `proofs/lean/juris_lean/JurisLean/BanachComplete.lean` | 2（命题 1，定义类 1） |
| B5 | `proofs/lean/juris_lean/JurisLean/ContractionCondition.lean` | 3（命题 1，定义类 2） |
| B5 | `proofs/lean/juris_lean/JurisLean/BanachContraction.lean` | 2（命题 2，定义类 0） |
| B5 | `proofs/lean/juris_lean/JurisLean/BanachFixedPoint.lean` | 2（命题 1，定义类 1） |
| B5 | `proofs/lean/juris_lean/JurisLean/BanachWeightedNorm.lean` | 2（命题 0，定义类 2） |
| B6 | `proofs/lean/juris_lean/JurisLean/BanachEffectiveNodes.lean` | 9（命题 8，定义类 1） |
| B7 | `proofs/lean/juris_lean/JurisLean/BanachCertificate.lean` | 10（命题 5，定义类 5） |
| B8 | `proofs/lean/juris_lean/JurisLean/ULM15IncrementalEmpiricalBanach.lean` | 18（命题 11，定义类 7） |

依赖抽查（未计入上表）：

- `proofs/lean/juris_lean/JurisLean/HornDefinitions.lean`（追 `TH`、`TH_monotone`、`toFiniteMonotoneSystem`）
- `proofs/lean/juris_lean/JurisLean/HornFixedPoint.lean`（追 `horn_result_fixed_point`）

## 3. 已解释定理／引理归属（55）

「解释状态」指主稿已按目标／前提／步骤／法律对应作静态说明，不是 Lean 核验通过。

| 组 | 种类 | 路径:行号 | 词法全名 | 解释 | 替代证明（候选） |
|---|---|---|---|---|---|
| B7 | theorem | `BanachCertificate.lean:90` | `JurisLean.BanachCertificateV3.no_certificate_rejected` | 已解释 | 主稿 §7 候选：用先验误差界做可检查准入，不用字段投影或恒真检查器 |
| B7 | theorem | `BanachCertificate.lean:96` | `JurisLean.BanachCertificateV3.certificate_has_q_lt_one_scaled` | 已解释 | 主稿 §7 候选：用先验误差界做可检查准入，不用字段投影或恒真检查器 |
| B7 | theorem | `BanachCertificate.lean:103` | `JurisLean.BanachCertificateV3.certificate_error_within_tolerance` | 已解释 | 主稿 §7 候选：用先验误差界做可检查准入，不用字段投影或恒真检查器 |
| B7 | theorem | `BanachCertificate.lean:110` | `JurisLean.BanachCertificateV3.certificate_has_nonempty_domain` | 已解释 | 主稿 §7 候选：用先验误差界做可检查准入，不用字段投影或恒真检查器 |
| B7 | theorem | `BanachCertificate.lean:117` | `JurisLean.BanachCertificateV3.certificate_has_positive_iterations` | 已解释 | 主稿 §7 候选：用先验误差界做可检查准入，不用字段投影或恒真检查器 |
| B4 | theorem | `BanachComplete.lean:28` | `weightedMetricSpace_dist` | 已解释 | 主稿 §4 候选：保留四条度量公理，另补等距传递的完备性（现稿未证） |
| B5 | theorem | `BanachContraction.lean:21` | `weighted_contraction_bound` | 已解释 | 主稿 §5 候选：先证任意 q 的 Lipschitz 上界，再在 q<1 与完备性之下接 ContractingWith |
| B5 | theorem | `BanachContraction.lean:34` | `weighted_contraction_bound_nnreal` | 已解释 | 主稿 §5 候选：先证任意 q 的 Lipschitz 上界，再在 q<1 与完备性之下接 ContractingWith |
| B6 | lemma | `BanachEffectiveNodes.lean:42` | `EffectiveNodesPricing.pricingFn_sub` | 已解释 | 主稿 §6 候选：单步等式＋代数唯一性（现稿已有，仍未编译核验）；补迭代速率公式（现稿未写） |
| B6 | lemma | `BanachEffectiveNodes.lean:53` | `EffectiveNodesPricing.abs_pricingFn_sub` | 已解释 | 主稿 §6 候选：单步等式＋代数唯一性（现稿已有，仍未编译核验）；补迭代速率公式（现稿未写） |
| B6 | lemma | `BanachEffectiveNodes.lean:62` | `EffectiveNodesPricing.abs_one_sub_beta_of_pos_lt_one` | 已解释 | 主稿 §6 候选：单步等式＋代数唯一性（现稿已有，仍未编译核验）；补迭代速率公式（现稿未写） |
| B6 | lemma | `BanachEffectiveNodes.lean:69` | `EffectiveNodesPricing.one_sub_beta_lt_one` | 已解释 | 主稿 §6 候选：单步等式＋代数唯一性（现稿已有，仍未编译核验）；补迭代速率公式（现稿未写） |
| B6 | lemma | `BanachEffectiveNodes.lean:73` | `EffectiveNodesPricing.one_sub_beta_nonneg` | 已解释 | 主稿 §6 候选：单步等式＋代数唯一性（现稿已有，仍未编译核验）；补迭代速率公式（现稿未写） |
| B6 | theorem | `BanachEffectiveNodes.lean:81` | `EffectiveNodesPricing.pricingFn_contraction` | 已解释 | 主稿 §6 候选：单步等式＋代数唯一性（现稿已有，仍未编译核验）；补迭代速率公式（现稿未写） |
| B6 | theorem | `BanachEffectiveNodes.lean:107` | `EffectiveNodesPricing.pricingFn_fixed_point` | 已解释 | 主稿 §6 候选：单步等式＋代数唯一性（现稿已有，仍未编译核验）；补迭代速率公式（现稿未写） |
| B6 | theorem | `BanachEffectiveNodes.lean:120` | `EffectiveNodesPricing.pricingFn_unique_fixed_point` | 已解释 | 主稿 §6 候选：单步等式＋代数唯一性（现稿已有，仍未编译核验）；补迭代速率公式（现稿未写） |
| B5 | theorem | `BanachFixedPoint.lean:34` | `weightedContractionData_of_coupling` | 已解释 | 主稿 §5 候选：先证任意 q 的 Lipschitz 上界，再在 q<1 与完备性之下接 ContractingWith |
| B5 | theorem | `ContractionCondition.lean:33` | `lipschitz_coupling_implies_weighted_contraction` | 已解释 | 主稿 §5 候选：先证任意 q 的 Lipschitz 上界，再在 q<1 与完备性之下接 ContractingWith |
| B1 | lemma | `FiniteGaloisAdjunction.lean:36` | `fn_sup_preserves` | 已解释 | 主稿 §1 候选：派生单调性、有限并归纳、余伴随两端 |
| B1 | theorem | `FiniteGaloisAdjunction.lean:49` | `galois_connection_of_residuated` | 已解释 | 主稿 §1 候选：派生单调性、有限并归纳、余伴随两端 |
| B3 | theorem | `FiniteMonotoneIteration.lean:28` | `FiniteMonotoneSystem.iter_zero` | 已解释 | 主稿 §3 候选：鸽笼稳定＋补最小不动点 `iter_le_prefixpoint` |
| B3 | theorem | `FiniteMonotoneIteration.lean:30` | `FiniteMonotoneSystem.iter_succ` | 已解释 | 主稿 §3 候选：鸽笼稳定＋补最小不动点 `iter_le_prefixpoint` |
| B3 | theorem | `FiniteMonotoneIteration.lean:32` | `FiniteMonotoneSystem.iter_subset_univ` | 已解释 | 主稿 §3 候选：鸽笼稳定＋补最小不动点 `iter_le_prefixpoint` |
| B3 | theorem | `FiniteMonotoneIteration.lean:39` | `FiniteMonotoneSystem.iter_mono` | 已解释 | 主稿 §3 候选：鸽笼稳定＋补最小不动点 `iter_le_prefixpoint` |
| B3 | theorem | `FiniteMonotoneIteration.lean:46` | `FiniteMonotoneSystem.iter_stable` | 已解释 | 主稿 §3 候选：鸽笼稳定＋补最小不动点 `iter_le_prefixpoint` |
| B3 | theorem | `FiniteMonotoneIteration.lean:62` | `FiniteMonotoneSystem.iter_ssubset_of_ne` | 已解释 | 主稿 §3 候选：鸽笼稳定＋补最小不动点 `iter_le_prefixpoint` |
| B3 | theorem | `FiniteMonotoneIteration.lean:71` | `FiniteMonotoneSystem.iter_card_lt_of_ne` | 已解释 | 主稿 §3 候选：鸽笼稳定＋补最小不动点 `iter_le_prefixpoint` |
| B3 | theorem | `FiniteMonotoneIteration.lean:75` | `FiniteMonotoneSystem.iter_card_le_univ` | 已解释 | 主稿 §3 候选：鸽笼稳定＋补最小不动点 `iter_le_prefixpoint` |
| B3 | theorem | `FiniteMonotoneIteration.lean:80` | `FiniteMonotoneSystem.exists_fixpoint_le_card` | 已解释 | 主稿 §3 候选：鸽笼稳定＋补最小不动点 `iter_le_prefixpoint` |
| B3 | theorem | `FiniteMonotoneIteration.lean:103` | `FiniteMonotoneSystem.fixed_at_card` | 已解释 | 主稿 §3 候选：鸽笼稳定＋补最小不动点 `iter_le_prefixpoint` |
| B2 | theorem | `FiniteRosetta.lean:49` | `cnOnly_eq_30` | 已解释 | 主稿 §2 候选：表驱动计数；多数不等式降为可选推论 |
| B2 | theorem | `FiniteRosetta.lean:52` | `collision_eq_4` | 已解释 | 主稿 §2 候选：表驱动计数；多数不等式降为可选推论 |
| B2 | theorem | `FiniteRosetta.lean:55` | `asymmetry_eq_3` | 已解释 | 主稿 §2 候选：表驱动计数；多数不等式降为可选推论 |
| B2 | theorem | `FiniteRosetta.lean:58` | `obstruction_eq_37` | 已解释 | 主稿 §2 候选：表驱动计数；多数不等式降为可选推论 |
| B2 | theorem | `FiniteRosetta.lean:61` | `cnOnly_exceeds_half` | 已解释 | 主稿 §2 候选：表驱动计数；多数不等式降为可选推论 |
| B2 | theorem | `FiniteRosetta.lean:64` | `obstruction_exceeds_half` | 已解释 | 主稿 §2 候选：表驱动计数；多数不等式降为可选推论 |
| B2 | theorem | `FiniteRosetta.lean:68` | `sample_mapping_not_total` | 已解释 | 主稿 §2 候选：表驱动计数；多数不等式降为可选推论 |
| B2 | theorem | `FiniteRosetta.lean:75` | `obstruction_density_gt_two_thirds` | 已解释 | 主稿 §2 候选：表驱动计数；多数不等式降为可选推论 |
| B2 | theorem | `FiniteRosetta.lean:80` | `pure_obstruction_majority` | 已解释 | 主稿 §2 候选：表驱动计数；多数不等式降为可选推论 |
| B4 | lemma | `SupZeroLemma.lean:11` | `sup'_eq_zero_of_nonneg` | 已解释 | 主稿 §4 候选：保留四条度量公理，另补等距传递的完备性（现稿未证） |
| B8 | theorem | `ULM15IncrementalEmpiricalBanach.lean:37` | `JurisLean.ULM.TH_subset_extend` | 已解释 | 主稿 §8 候选：维持扩张单调；增量算法另证；Banach 包装须先兑现 B4／B5 实例 |
| B8 | theorem | `ULM15IncrementalEmpiricalBanach.lean:48` | `JurisLean.ULM.horn_iter_subset_extend` | 已解释 | 主稿 §8 候选：维持扩张单调；增量算法另证；Banach 包装须先兑现 B4／B5 实例 |
| B8 | theorem | `ULM15IncrementalEmpiricalBanach.lean:62` | `JurisLean.ULM.horn_closure_subset_extend` | 已解释 | 主稿 §8 候选：维持扩张单调；增量算法另证；Banach 包装须先兑现 B4／B5 实例 |
| B8 | theorem | `ULM15IncrementalEmpiricalBanach.lean:82` | `JurisLean.ULM.incremental_correct_returns_full_recompute` | 已解释 | 主稿 §8 候选：维持扩张单调；增量算法另证；Banach 包装须先兑现 B4／B5 实例 |
| B8 | theorem | `ULM15IncrementalEmpiricalBanach.lean:90` | `JurisLean.ULM.childFullRecompute_fixed` | 已解释 | 主稿 §8 候选：维持扩张单调；增量算法另证；Banach 包装须先兑现 B4／B5 实例 |
| B8 | theorem | `ULM15IncrementalEmpiricalBanach.lean:109` | `JurisLean.ULM.empirical_is_read_only` | 已解释 | 主稿 §8 候选：维持扩张单调；增量算法另证；Banach 包装须先兑现 B4／B5 实例 |
| B8 | theorem | `ULM15IncrementalEmpiricalBanach.lean:116` | `JurisLean.ULM.deviationScore_decomposes` | 已解释 | 主稿 §8 候选：维持扩张单调；增量算法另证；Banach 包装须先兑现 B4／B5 实例 |
| B8 | theorem | `ULM15IncrementalEmpiricalBanach.lean:126` | `JurisLean.ULM.banach_exists_fixedPoint` | 已解释 | 主稿 §8 候选：维持扩张单调；增量算法另证；Banach 包装须先兑现 B4／B5 实例 |
| B8 | theorem | `ULM15IncrementalEmpiricalBanach.lean:131` | `JurisLean.ULM.banach_fixedPoint_unique` | 已解释 | 主稿 §8 候选：维持扩张单调；增量算法另证；Banach 包装须先兑现 B4／B5 实例 |
| B8 | theorem | `ULM15IncrementalEmpiricalBanach.lean:139` | `JurisLean.ULM.banach_iterates_converge` | 已解释 | 主稿 §8 候选：维持扩张单调；增量算法另证；Banach 包装须先兑现 B4／B5 实例 |
| B8 | theorem | `ULM15IncrementalEmpiricalBanach.lean:146` | `JurisLean.ULM.banach_apriori_error_bound` | 已解释 | 主稿 §8 候选：维持扩张单调；增量算法另证；Banach 包装须先兑现 B4／B5 实例 |
| B4 | theorem | `WeightedSupNorm.lean:39` | `weightedSupDist_nonneg` | 已解释 | 主稿 §4 候选：保留四条度量公理，另补等距传递的完备性（现稿未证） |
| B4 | theorem | `WeightedSupNorm.lean:50` | `weightedSupDist_triangle` | 已解释 | 主稿 §4 候选：保留四条度量公理，另补等距传递的完备性（现稿未证） |
| B4 | theorem | `WeightedSupNorm.lean:72` | `weightedSupDist_symm` | 已解释 | 主稿 §4 候选：保留四条度量公理，另补等距传递的完备性（现稿未证） |
| B4 | theorem | `WeightedSupNorm.lean:81` | `weightedSupDist_separates_points` | 已解释 | 主稿 §4 候选：保留四条度量公理，另补等距传递的完备性（现稿未证） |

## 4. 定义类声明（34，已在主稿说明，非单独证明对象）

| 组 | 种类 | 路径:行号 | 词法全名 |
|---|---|---|---|
| B7 | structure | `BanachCertificate.lean:21` | `BanachCertificate` |
| B7 | def | `BanachCertificate.lean:37` | `verifyCertificate` |
| B7 | structure | `BanachCertificate.lean:53` | `JurisLean.BanachCertificateV3.CertifiedApproximation` |
| B7 | inductive | `BanachCertificate.lean:77` | `JurisLean.BanachCertificateV3.Admission` |
| B7 | def | `BanachCertificate.lean:82` | `JurisLean.BanachCertificateV3.tryAdmit` |
| B4 | def | `BanachComplete.lean:15` | `weightedMetricSpace` |
| B6 | def | `BanachEffectiveNodes.lean:29` | `EffectiveNodesPricing.pricingFn` |
| B5 | structure | `BanachFixedPoint.lean:22` | `WeightedContractionData` |
| B5 | def | `BanachWeightedNorm.lean:37` | `WeightedContractionTarget` |
| B5 | def | `BanachWeightedNorm.lean:43` | `LipschitzMatrixCondition` |
| B5 | def | `ContractionCondition.lean:24` | `LipschitzCoupling` |
| B5 | def | `ContractionCondition.lean:28` | `CoordinateLipschitz` |
| B1 | class | `FiniteGaloisAdjunction.lean:16` | `FinitePoset` |
| B1 | structure | `FiniteGaloisAdjunction.lean:24` | `ResiduatedMap` |
| B1 | def | `FiniteGaloisAdjunction.lean:31` | `legalResidual` |
| B1 | def | `FiniteGaloisAdjunction.lean:45` | `IsGaloisConnection` |
| B3 | structure | `FiniteMonotoneIteration.lean:11` | `FiniteMonotoneSystem` |
| B3 | def | `FiniteMonotoneIteration.lean:22` | `FiniteMonotoneSystem.iter` |
| B2 | inductive | `FiniteRosetta.lean:12` | `MappingStatus` |
| B2 | def | `FiniteRosetta.lean:24` | `mappingStatus` |
| B2 | def | `FiniteRosetta.lean:34` | `cnOnlyCount` |
| B2 | def | `FiniteRosetta.lean:38` | `collisionCount` |
| B2 | def | `FiniteRosetta.lean:42` | `asymmetryCount` |
| B2 | def | `FiniteRosetta.lean:46` | `obstructionCount` |
| B8 | structure | `ULM15IncrementalEmpiricalBanach.lean:17` | `JurisLean.ULM.HornAddDelta` |
| B8 | def | `ULM15IncrementalEmpiricalBanach.lean:24` | `JurisLean.ULM.extendHorn` |
| B8 | def | `ULM15IncrementalEmpiricalBanach.lean:71` | `JurisLean.ULM.childFullRecompute` |
| B8 | def | `ULM15IncrementalEmpiricalBanach.lean:78` | `JurisLean.ULM.IncrementalImplementationCorrect` |
| B8 | structure | `ULM15IncrementalEmpiricalBanach.lean:100` | `JurisLean.ULM.EmpiricalArtifact` |
| B8 | def | `ULM15IncrementalEmpiricalBanach.lean:106` | `JurisLean.ULM.attachEmpirical` |
| B8 | def | `ULM15IncrementalEmpiricalBanach.lean:113` | `JurisLean.ULM.deviationScore` |
| B4 | def | `WeightedSupNorm.lean:28` | `PositiveWeights` |
| B4 | def | `WeightedSupNorm.lean:31` | `weightedSupDist` |
| B4 | def | `WeightedSupNorm.lean:35` | `weightedSupNorm` |

## 5. 未核／下一批余量

原拟 31 文件中尚未精读的 18 个：

- G02 外部：`External/FixedPointTheorems.lean` 及其下 `apply_cubical_sperner`、`brouwer`、`convex_homeos`、`cubical_sperner`、`cubical_sperner_prep`、`kakutani`（7 文件，词法 106）。建议作为下一批，以补完 G02。
- G03 核心：`DungAAF.lean`、`DungDefinitions.lean`、`DungFixedPoint.lean`、`HornAAFContract.lean`、`HornDefinitions.lean`、`HornFixedPoint.lean`（后两份本批仅依赖抽查，不得标为已精读／已解释整组）。
- G04 核心：`AuthorityLattice.lean`、`DDLDefinitions.lean`、`DefeasiblePriority.lean`、`Hohfeld.lean`、`PermissionConflict.lean`。

全仓其余文件（665 个尚未精读，含上述 18 个）均保持未核。不得用本批 13 个文件的解释冒充 31 或 678 已完成。

---

法律数学评审员／Grok Bot  
时间：2026-11-14 00:42 Asia/Shanghai  
来源提交：`037e3f20142ddb0bc8874e9078378360b29122af`  
覆盖：精读 13；解释 8 组／55 条 theorem／lemma；候选替代证明 8 组；原拟 31 余 18；全仓未精读 665／678；原 104 项验证 0。
