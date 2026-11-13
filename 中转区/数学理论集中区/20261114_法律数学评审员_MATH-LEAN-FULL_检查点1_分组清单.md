# MATH-LEAN-FULL 检查点 1 附件：分组文件清单

来源提交：`037e3f20142ddb0bc8874e9078378360b29122af`
本附件只列文件分母、词法声明次数与分组；不是数学内容审查完成，也不是编译器声明总数。

措辞更正（2026-11-14 00:34 Asia/Shanghai）：此处 678 个文件只表示已取回、blob 对核并完成词法扫描，以便分组与索引。**不是** 678 个文件正文的逐篇数学精读，也不能把本清单称作「已读 678」。逐篇精读／解释从零累计。

## G00_tooling　工具与入口

- 分组依据：Lake config and ad-hoc check scripts; not library proofs.
- 文件数：9
- 词法声明次数：3（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean.lean` | `09b779f877231334520646dc49cb22e61175cc4e` | 17057 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/BanachScratch.lean` | `b6e47f87804315353bf9c4bfa016ba31bf47f45c` | 644 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Basic.lean` | `cf876673178a2a80fe85b21d9e6f658e4dbdee12` | 89 | 1 | 0 | 1 | 0 | 0 | 0 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/ScratchApi.lean` | `fc43c147030f57c4959d88eecdcae1f3fc4a9524` | 1580 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/_axiom_audit.lean` | `81d27e82d11b2935acb97a6e163959b929035ae0` | 450 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/_check.lean` | `c35f3619b8e8691d7d90784acd19d5b2cc424946` | 312 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/_test.lean` | `39844f6c15854b26fbd42560a529fe9ffaa1b1ef` | 112 | 1 | 1 | 0 | 0 | 0 | 0 | 0 | 1 |  |
| `proofs/lean/juris_lean/_test_omega.lean` | `dac59bfed3c9cb2dd5a33eecddc295671468a013` | 82 | 1 | 0 | 1 | 0 | 0 | 0 | 0 | 1 |  |
| `proofs/lean/juris_lean/lakefile.lean` | `089154f1e07cc3ff964dff4dd3c87948717c0261` | 183 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |

## G01_baseline_copies　基线/包外副本

- 分组依据：Version-controlled copies or baselines outside or beside the main package; audit after originals, do not treat as independent proofs.
- 文件数：9
- 词法声明次数：48（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/engineering_proof_artifacts/banach/BanachEffectiveNodes.lean` | `fe5cd2b160f178b70b47a840896783d47ebde9a6` | 6307 | 10 | 10 | 0 | 8 | 0 | 2 | 0 | 0 |  |
| `proofs/engineering_proof_artifacts/galois/FiniteGaloisAdjunction.lean` | `8b5f1be4b50bad1457eecd84d2b0e952da4a90a0` | 5978 | 5 | 5 | 0 | 2 | 0 | 3 | 0 | 0 |  |
| `proofs/lean/BanachEffectiveNodes.lean` | `f2fd97240a1a3043dedbaa51a034219e9148fc3a` | 5039 | 9 | 9 | 0 | 3 | 5 | 1 | 0 | 0 |  |
| `proofs/strict_proof_baseline/lean/BanachEffectiveNodes.lean` | `ebc908239df6722303d49387e70253bb30e2a8f4` | 3955 | 5 | 4 | 1 | 1 | 1 | 1 | 1 | 1 |  |
| `proofs/strict_proof_baseline/lean/FiniteGaloisAdjunction.lean` | `c129c03bd3e29cd8cc75b4f3a91ed854a8ef834a` | 5837 | 8 | 6 | 2 | 0 | 0 | 4 | 1 | 3 |  |
| `proofs/strict_proof_baseline/lean/FiniteRosetta.lean` | `9f355becbf463f43bd97b169c3f959736b196159` | 6039 | 11 | 11 | 0 | 0 | 1 | 1 | 0 | 9 |  |
| `proofs/strict_proof_baseline/p0a_category/FiniteRosetta.lean` | `fbbd684802ddc8e2377f840f7d3ead4628737329` | 1116 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/strict_proof_baseline/p0c_banach/BanachEffectiveNodes.lean` | `369c1e6c2a9549e5109944aab47cdb8360f3b33a` | 1084 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/strict_proof_baseline/p0d_privilege_epsilon/FiniteGaloisAdjunction.lean` | `eaf84c7cf0345dc11c67e7b95f1856f61bba848f` | 936 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |

## G02_fixed_point_metric　不动点与度量

- 分组依据：Monotone iteration, weighted norms, Banach / contraction / fixed-point cores.
- 文件数：18
- 词法声明次数：174（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/BanachCertificate.lean` | `bda6dbc4a49d481f574b1d70819a939987601d81` | 3939 | 10 | 10 | 0 | 5 | 0 | 2 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/BanachComplete.lean` | `622b6b515a7633680c170d752a34aa1d4b952857` | 1156 | 2 | 2 | 0 | 1 | 0 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/BanachContraction.lean` | `35e600d43189f76cd0da37c2830879a21fbdaa5c` | 1828 | 2 | 2 | 0 | 2 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/BanachEffectiveNodes.lean` | `f2fd97240a1a3043dedbaa51a034219e9148fc3a` | 5039 | 9 | 9 | 0 | 3 | 5 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/BanachFixedPoint.lean` | `a3a98eb70aa554641004e7ebd794e53ad921e71c` | 1699 | 2 | 2 | 0 | 1 | 0 | 0 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/BanachWeightedNorm.lean` | `c48a8ff290079cb2c9f9b2696b556491d27a5ccb` | 1899 | 2 | 2 | 0 | 0 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/ContractionCondition.lean` | `636152a4604a8c5976ae9e40176a48008fbb54f2` | 3508 | 3 | 3 | 0 | 1 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/FixedPointTheorems.lean` | `fc3c74d065011421ab9274144e8ae368a317ba80` | 1048 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/External/FixedPointTheorems/apply_cubical_sperner.lean` | `73c048fb13d1fc9e4349845bf6ce7cb10f4d4432` | 9412 | 11 | 11 | 0 | 2 | 5 | 4 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/FixedPointTheorems/brouwer.lean` | `520834668e85d055a6438eb5e72cd286cb5744ef` | 2691 | 3 | 3 | 0 | 3 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/FixedPointTheorems/convex_homeos.lean` | `7f5819a6489eb7e401793db7efff22faf077bb02` | 5741 | 4 | 4 | 0 | 1 | 3 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/FixedPointTheorems/cubical_sperner.lean` | `d6968e4f8f3c8379077c55589393f3aa5dfb0f01` | 21734 | 19 | 19 | 0 | 2 | 15 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/FixedPointTheorems/cubical_sperner_prep.lean` | `9f1d8b527fcfb18fe711fd818cdb606381d353bc` | 48475 | 62 | 62 | 0 | 0 | 46 | 14 | 1 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/External/FixedPointTheorems/kakutani.lean` | `239b609d2b9d7ec19e6ea66daaf2993a977b1208` | 10829 | 7 | 7 | 0 | 1 | 4 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FiniteMonotoneIteration.lean` | `e5ac4891202803e9c775d6760caca2852166e443` | 4470 | 12 | 12 | 0 | 10 | 0 | 1 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/SupZeroLemma.lean` | `173f48658de72f49ba904f353716094f3795fd48` | 633 | 1 | 1 | 0 | 0 | 1 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/ULM15IncrementalEmpiricalBanach.lean` | `b0cd45c040cbce95808868fc469a0534d284d4fd` | 5671 | 18 | 18 | 0 | 11 | 0 | 5 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/WeightedSupNorm.lean` | `ff2bdd6cc36f38221b5c3bb170cd13bab06edf0f` | 4616 | 7 | 7 | 0 | 4 | 0 | 3 | 0 | 0 |  |

## G21_order_galois_rosetta　有限序/Galois/Rosetta

- 分组依据：Finite poset / Galois adjunction / Rosetta cores.
- 文件数：2
- 词法声明次数：21（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/FiniteGaloisAdjunction.lean` | `c292a56f7f36e168e9e8d47a100dfddfe587e41c` | 2584 | 6 | 6 | 0 | 1 | 1 | 2 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/FiniteRosetta.lean` | `f27d2f74366ff93c28968b3010347fcc2ffa2b59` | 3292 | 15 | 15 | 0 | 9 | 0 | 5 | 0 | 1 |  |

## G03_argumentation　论证与 Horn/AAF

- 分组依据：Dung AAF, Horn, attack, argument compiler and related ULM slices.
- 文件数：16
- 词法声明次数：181（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/ASPWitness.lean` | `efb9d723f7da631a6188110d1472b145a2b173ef` | 1958 | 8 | 8 | 0 | 5 | 0 | 2 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/ArgumentCompilerSpec.lean` | `347d128855fdd9140fcec9a5fe6cf62d725dc1ca` | 3688 | 11 | 11 | 0 | 5 | 0 | 5 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/ArgumentSemanticsRegistry.lean` | `a692464336cfc733c4c70dd95cbac56f5a71adaa` | 2428 | 11 | 11 | 0 | 6 | 0 | 3 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/AttackDecision.lean` | `72e35a496a24f543235a42f8542acbad0b29a22c` | 2559 | 9 | 9 | 0 | 5 | 0 | 4 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/DungAAF.lean` | `be3a3d91490b3dbde0218e37aa659eba0c730281` | 307 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/DungDefinitions.lean` | `972f3e8952a19d874eebfe0edbc0bfad552de1c7` | 2022 | 5 | 5 | 0 | 0 | 0 | 3 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/DungFixedPoint.lean` | `5258b02c8c17decf7d5b5eea953408a1c1713c97` | 10161 | 21 | 21 | 0 | 16 | 1 | 4 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/HornAAFContract.lean` | `0606892d07b7b11962673e5c44417e4db1fa1de5` | 3069 | 10 | 10 | 0 | 5 | 0 | 4 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/HornDefinitions.lean` | `df24f834ef57da8fd64c529dd69a6b92ef8902f0` | 2588 | 6 | 6 | 0 | 2 | 0 | 2 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/HornFixedPoint.lean` | `d30c6e23040f7daa6d960989f1bbe62d84c0f9dd` | 5029 | 10 | 10 | 0 | 10 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/HornOperationalRefinement.lean` | `9e9ef698ee37e60f85bc1b35f5285a2324d15570` | 792 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/TypedAttack.lean` | `d4a9b0f54edcd10a0dbd5cab5be9eca05e5dd88c` | 2720 | 9 | 9 | 0 | 5 | 0 | 2 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/ULM07HornSupport.lean` | `1e6c76260917e63f3f1796d7fb4a623ef10b13e1` | 2521 | 10 | 10 | 0 | 5 | 0 | 3 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/ULM08ArgumentConstruction.lean` | `1fcf0d51ddbcfc7e90218920fa5bacd086fc4fb7` | 5771 | 19 | 19 | 0 | 7 | 0 | 7 | 0 | 5 |  |
| `proofs/lean/juris_lean/JurisLean/ULM09AttackDefeat.lean` | `36906403d4f487823dec9fe2b165cd7f73a97b40` | 4465 | 16 | 16 | 0 | 6 | 0 | 5 | 0 | 5 |  |
| `proofs/lean/juris_lean/JurisLean/ULM10DungProfiles.lean` | `e36cb9ee799f7e1c9535d86a3047b501b3084289` | 9474 | 36 | 36 | 0 | 15 | 0 | 17 | 0 | 4 |  |

## G04_deontic_legal_syntax　道义与法律句法

- 分组依据：Deontic / Hohfeld / authority / legal syntax and IVL translations.
- 文件数：23
- 词法声明次数：314（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/AuthorityLattice.lean` | `5107d6cb8de1ce2d08dd05572c943529e5519557` | 1492 | 5 | 5 | 0 | 3 | 0 | 1 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/DDLDefinitions.lean` | `666a90d2004ad292ecd0457fca61438b1b02ac87` | 5112 | 20 | 20 | 0 | 9 | 0 | 11 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/DefeasiblePriority.lean` | `59dfba1e415f6009cb55eba055c81b1fa2d92616` | 3102 | 10 | 10 | 0 | 4 | 0 | 4 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Hohfeld.lean` | `fb5392deff8d5cb35621537798b4d176efdf1427` | 1927 | 7 | 7 | 0 | 4 | 0 | 2 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/IVLToAAF.lean` | `3729ae079c7fecacb9fd38034eac402db6b3e455` | 2044 | 6 | 6 | 0 | 3 | 0 | 2 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/IVLToASP.lean` | `babe9a49cdfc813c8c8f54de53841ffc6ce7f8a0` | 1950 | 6 | 6 | 0 | 3 | 0 | 1 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/IVLToHorn.lean` | `c68850d5feeab2ef8c9135e0c17002de6158d2d7` | 1745 | 6 | 6 | 0 | 3 | 0 | 1 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/IVLToSMT.lean` | `e4749f352a19cdeeeb389fc4c2770b77a26af4b9` | 2076 | 8 | 8 | 0 | 3 | 0 | 2 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/JC_Formalization.lean` | `4748f10efd3196791d4e4d8a9a80f3f997cf49a6` | 8307 | 18 | 18 | 0 | 6 | 0 | 7 | 0 | 5 |  |
| `proofs/lean/juris_lean/JurisLean/LegalIVL.lean` | `f67e3a5c0af297f75636d3727d6a04e5209f8793` | 3169 | 14 | 14 | 0 | 3 | 0 | 1 | 0 | 10 |  |
| `proofs/lean/juris_lean/JurisLean/LegalIVLWellFormed.lean` | `c06724b2bbca52bdbfc048423854b0f46322613d` | 1719 | 6 | 6 | 0 | 4 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/LegalIds.lean` | `a1337a545dceb8d4b6c20868198296dd7e6ab5e2` | 5140 | 26 | 26 | 0 | 6 | 0 | 4 | 0 | 16 |  |
| `proofs/lean/juris_lean/JurisLean/LegalModelV2.lean` | `525a96473b1e1d2c291a5e3f1fefc4854298f251` | 9940 | 35 | 35 | 0 | 13 | 0 | 6 | 0 | 16 |  |
| `proofs/lean/juris_lean/JurisLean/LegalSpec.lean` | `d9b13881a452f8a25e7b2869e1435a9392fecaa6` | 2119 | 8 | 8 | 0 | 2 | 0 | 1 | 0 | 5 |  |
| `proofs/lean/juris_lean/JurisLean/LegalSpecNormalize.lean` | `e1bb8c62de380e6ee8561989010cb31247ad4749` | 2423 | 7 | 7 | 0 | 5 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/LegalSpecToIVL.lean` | `0f5c6030ab0c5af3258f33ef9baeeaad67fd60ad` | 3509 | 10 | 10 | 0 | 7 | 0 | 3 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/LegalSpecWellFormed.lean` | `a660b7c2ced7b2680a6ef31bf3bc4146f2e4e8e5` | 2078 | 7 | 7 | 0 | 5 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/LegalSyntax.lean` | `52f519b1d9014500ce377e898b7037a291958f1c` | 7400 | 41 | 41 | 0 | 5 | 0 | 5 | 0 | 31 |  |
| `proofs/lean/juris_lean/JurisLean/LegalWellFormed.lean` | `4670cf78a307bf899606a6c95672100a7a96887f` | 4869 | 18 | 18 | 0 | 9 | 0 | 9 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/PermissionConflict.lean` | `fb79d22a899b052917534d78f5a55ff12ebf0829` | 3115 | 14 | 14 | 0 | 6 | 0 | 2 | 0 | 6 |  |
| `proofs/lean/juris_lean/JurisLean/ReceiptAuthority.lean` | `510dfabe9d44a30f01c3e94d638e05a3c1fffd53` | 4125 | 15 | 15 | 0 | 7 | 0 | 5 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/ULM01NormalForm.lean` | `1a5e62ed0d771b1904e9bf530d57a832012fcc48` | 3796 | 15 | 15 | 0 | 3 | 0 | 3 | 0 | 9 |  |
| `proofs/lean/juris_lean/JurisLean/ULM04Obligations.lean` | `48e13460960071c16df6b1bd224d79c5ced028a1` | 3652 | 12 | 12 | 0 | 3 | 0 | 5 | 0 | 4 |  |

## G23_noninterference　非干涉

- 分组依据：Proposal and taint noninterference lemmas.
- 文件数：2
- 词法声明次数：18（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/ProposalNoninterference.lean` | `290b6e301d97ac518ca485f4d46007e3e61cf935` | 1921 | 5 | 5 | 0 | 4 | 0 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/TaintNoninterference.lean` | `b3fc1890f202abe33097f2f57babaafd41d4aa15` | 3894 | 13 | 13 | 0 | 8 | 0 | 3 | 0 | 2 |  |

## G17_certificates_contracts　证书与合同

- 分组依据：Certificates, checkers, witnesses, backend and safety contracts.
- 文件数：18
- 词法声明次数：212（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/BackendContract.lean` | `5f59c049a9715fa1e9f9b0bb64323a36e17a2eaf` | 3686 | 15 | 15 | 0 | 9 | 0 | 3 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/CanonicalSerialization.lean` | `b4d15111b763ff97852f0038610ef10f20425951` | 4004 | 14 | 14 | 0 | 7 | 0 | 5 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/CertificateChecker.lean` | `d1855bfcdd6e4826de00bd7b1cd1c05790921249` | 6357 | 11 | 11 | 0 | 8 | 0 | 2 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/CertificateCheckerV2.lean` | `3e55f066e8b74730e455bb025e300f872ecbdf45` | 2974 | 9 | 9 | 0 | 5 | 0 | 2 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/CertificateV2.lean` | `f1372e33227dda32ccbcf5d88a1a0d6d425880d6` | 3671 | 12 | 12 | 0 | 5 | 0 | 5 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/EndToEnd.lean` | `6fcb473d06c07b7dfa1a0c372fd36d5d2a7f68a0` | 6448 | 18 | 18 | 0 | 10 | 0 | 8 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/ExactNumericContract.lean` | `2568d5b31f9a938931d2d7736f0b938eb9a7ac0c` | 2929 | 14 | 14 | 0 | 7 | 0 | 5 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/FactAdmissionSpec.lean` | `fbb828e31949812aa5b44d86095008fba0d2924d` | 6216 | 20 | 20 | 0 | 12 | 0 | 3 | 0 | 5 |  |
| `proofs/lean/juris_lean/JurisLean/FailureStatus.lean` | `b914ce92197081da63fa14ecaca7c99655550442` | 2271 | 10 | 10 | 0 | 6 | 0 | 3 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/HumanResearchReceiptSpec.lean` | `1a0b6897075befac65297fcbd39e8d9c4eae2857` | 2832 | 9 | 9 | 0 | 5 | 0 | 2 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/ProposalEnvelopeSpec.lean` | `fb10247683df0a51ba6d06c8ea78956beb9b510b` | 2357 | 8 | 8 | 0 | 4 | 0 | 2 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/SMTWitness.lean` | `c7e8104f25fc392cfd78f07072dcc5be188698a3` | 2146 | 8 | 8 | 0 | 5 | 0 | 1 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/SafetyTheorems.lean` | `44c8bcb49e1c32d67f872aff1d3726278d505427` | 3229 | 7 | 7 | 0 | 7 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/SolverRouting.lean` | `8184505c3698ee4fdbe746a0109e66e6099fbdb4` | 2138 | 7 | 7 | 0 | 5 | 0 | 1 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/SourceBundleSpec.lean` | `dc2a3f077a07007e59372d6ae326f21fcf826969` | 4168 | 16 | 16 | 0 | 6 | 0 | 7 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/SourcePathSpec.lean` | `e796d8c0e6af5785fcd683af92e661d78db54ab9` | 3930 | 15 | 15 | 0 | 6 | 0 | 6 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/TranslationRefinement.lean` | `fd48702307d03d42c79ef51f35fb2ab9e2588dd1` | 3225 | 12 | 12 | 0 | 4 | 0 | 7 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/TranslationWitness.lean` | `a1be59e9695f364f91e0572302fd713f07dde628` | 2220 | 7 | 7 | 0 | 4 | 0 | 1 | 0 | 2 |  |

## G22_realization_bridges　实现桥

- 分组依据：Posterior-law and trained-decision realization bridges.
- 文件数：2
- 词法声明次数：47（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/PosteriorLawRealization.lean` | `13afa8acb269b27f231705373648e3d93b96622f` | 6719 | 21 | 21 | 0 | 12 | 0 | 9 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/TrainedDecisionRealization.lean` | `0de074ceeaa86bb194d07393650ab3a4e9c94a8a` | 14031 | 26 | 26 | 0 | 17 | 0 | 9 | 0 | 0 |  |

## G05_temporal_feedback　时间与反馈（非 Seams）

- 分组依据：Temporal applicability and feedback / recall bridges not in Seams.
- 文件数：6
- 词法声明次数：118（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/BoundedRecall.lean` | `e96df6e7b661c47b71297bdb4c6732881e292b81` | 6891 | 26 | 22 | 4 | 14 | 0 | 7 | 4 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FeedbackHistoryBridge.lean` | `b5a855e6c9d2af1284e9090c36113da69f8f0266` | 11012 | 29 | 29 | 0 | 17 | 2 | 4 | 6 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/SequentialFeedback.lean` | `0aaa49f1005ba3144c32d3eb1a3975f4af17756e` | 9402 | 21 | 21 | 0 | 13 | 0 | 8 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/TemporalApplicability.lean` | `13edb3efec81903fcb3c30147044281c4aaaa97a` | 4146 | 15 | 15 | 0 | 7 | 0 | 5 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/TemporalArithmetic.lean` | `c836ae520a916e1aff2eb5a4148fc808b3f0c295` | 4075 | 14 | 14 | 0 | 8 | 0 | 5 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/TemporalKripke.lean` | `792898fbe0e194a78effe1e35b9821b9a4b5161f` | 3926 | 13 | 13 | 0 | 2 | 4 | 5 | 0 | 2 |  |

## G18_ulm_remainder　其余 ULM 切片

- 分组依据：Remaining ULM slices not placed in more specific groups.
- 文件数：9
- 词法声明次数：233（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/ULM02Outcome.lean` | `955e8e74c317da4c982ca04554fc95c25f243fb4` | 2054 | 12 | 12 | 0 | 6 | 0 | 1 | 0 | 5 |  |
| `proofs/lean/juris_lean/JurisLean/ULM03TypedGraph.lean` | `8f75e3f3098a0599a25a2cb263c6e9df0ab336dd` | 2533 | 13 | 13 | 0 | 4 | 0 | 4 | 0 | 5 |  |
| `proofs/lean/juris_lean/JurisLean/ULM05Machine.lean` | `5aecb865fb2d90e7540c8810310f9caddf1d799a` | 2938 | 16 | 16 | 0 | 7 | 0 | 4 | 0 | 5 |  |
| `proofs/lean/juris_lean/JurisLean/ULM06FactEvidence.lean` | `6258fa1cb1f77c813b9b580739c565dc028c0f38` | 3574 | 17 | 17 | 0 | 5 | 0 | 3 | 0 | 9 |  |
| `proofs/lean/juris_lean/JurisLean/ULM11BranchQuery.lean` | `48929d86f945d176590c40756e827a91fffd4d5a` | 8393 | 39 | 39 | 0 | 10 | 0 | 19 | 0 | 10 |  |
| `proofs/lean/juris_lean/JurisLean/ULM12Procedure.lean` | `9a2b09426f05ab91f9e677bc50cbcbe0aacf70d0` | 9314 | 33 | 33 | 0 | 11 | 0 | 7 | 0 | 15 |  |
| `proofs/lean/juris_lean/JurisLean/ULM13DomainCompositionExact.lean` | `89d024cd0e86ad67f3bdc82b340ed902df626a0b` | 5321 | 24 | 23 | 1 | 7 | 0 | 7 | 0 | 10 |  |
| `proofs/lean/juris_lean/JurisLean/ULM14CoverageTrust.lean` | `9d88927e4549b1649e4c6db1ac1c34ea67174e84` | 9762 | 48 | 48 | 0 | 18 | 0 | 17 | 0 | 13 |  |
| `proofs/lean/juris_lean/JurisLean/ULM16TheoryComposition.lean` | `c4d0a8c1a7defcf831793948637e942db6877581` | 11327 | 31 | 31 | 0 | 27 | 0 | 2 | 0 | 2 |  |

## G19_axiom_audit_wrappers　公理审计包装

- 分组依据：Axiom-audit wrapper modules (often enumerative #print / import surfaces, not theorem bodies).
- 文件数：4
- 词法声明次数：0（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/AxiomAudit.lean` | `6961cc7efda640ddf93c57081ef8c998f7632c5f` | 367811 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/ULMAllTheoremsAxiomAudit.lean` | `789ff0ec03ff025b0cea47f7bdecb5e7a08f28c0` | 8359 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/ULMAxiomAudit.lean` | `451c06ff8738b32537835fc4bccf130a3afb968d` | 1705 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/ULMCoreCompAxiomAudit.lean` | `451c06ff8738b32537835fc4bccf130a3afb968d` | 1705 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |

## G06_game_theory　博弈与 Mandate

- 分组依据：Game trees, Kuhn, Nash, deviation, mandate and finite-horizon game bridges.
- 文件数：62
- 词法声明次数：1417（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Concepts/ConstantSum.lean` | `32f473ac96c07003702a45043629b0f8be54a43a` | 6269 | 7 | 7 | 0 | 7 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Concepts/Deviation.lean` | `889dae53b2258171b4144baf9a5b211da97b4af2` | 3380 | 9 | 9 | 0 | 2 | 0 | 6 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Concepts/Minimax.lean` | `526d9c8f36cf994b75bc0fa07300d396532b6b7a` | 4191 | 6 | 6 | 0 | 4 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Concepts/MixedExtension.lean` | `8ae79337575d30cac274b2a50a6c3774ce01005d` | 12414 | 10 | 10 | 0 | 9 | 0 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Concepts/ProductSimplexBrouwer.lean` | `2e53c75e453d46d481ea48182ea37264deb3b938` | 9056 | 16 | 16 | 0 | 10 | 0 | 4 | 1 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Concepts/SecurityStrategy.lean` | `90ddf56db5c83ff3daa90e995fbc6488b1733483` | 9355 | 15 | 15 | 0 | 11 | 0 | 4 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Concepts/SolutionConcepts.lean` | `c15702b1cbd0876798d2306f7ae4fbbb4c3cffc4` | 15666 | 35 | 35 | 0 | 13 | 0 | 22 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Concepts/ZeroSum.lean` | `5cd01e41936df9e56079bee21062888e8134180d` | 2960 | 4 | 4 | 0 | 4 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Concepts/ZeroSumNash.lean` | `ba1a38ca239a2c5c0ff2206333912b6b9faccc4c` | 5900 | 8 | 8 | 0 | 8 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Core/GameForm.lean` | `a7158beb993bfaff9c5cfada855507c6e87e8481` | 33016 | 86 | 86 | 0 | 50 | 0 | 31 | 0 | 5 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Core/GameProperties.lean` | `43ed4dfc33a1e3a87beddb90a55a9fd09747fdc9` | 4379 | 12 | 12 | 0 | 1 | 0 | 11 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Core/KernelGame.lean` | `8588bb1e0b40f6b78ed290305719b7c853ea1399` | 6103 | 14 | 14 | 0 | 5 | 0 | 6 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Languages/EFG/Refinements.lean` | `e63ab57ccc6aebd4923d26f810c0a8b7a2446f87` | 19686 | 30 | 30 | 0 | 22 | 0 | 5 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Languages/EFG/Syntax.lean` | `8565fa5b01e3a456fdc2351fb9316316111faab0` | 24069 | 56 | 55 | 1 | 26 | 0 | 16 | 1 | 13 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Math/Coupling.lean` | `036a0bb544eeebb8030482d3e49f03ff514d01a7` | 8613 | 10 | 10 | 0 | 3 | 0 | 6 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Math/OptimizationLocalGlobal.lean` | `f50a12e481a6613e24cd15f347601cc57dab3cf9` | 6074 | 15 | 15 | 0 | 11 | 0 | 4 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Math/PMFProduct.lean` | `9074b953a05ae4e945e0628d2c34d3a247940413` | 79065 | 88 | 88 | 0 | 34 | 45 | 8 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Math/ParameterizedChain.lean` | `034f45459b8f712f62ac6f07c7d9598bd4d574b3` | 22348 | 24 | 24 | 0 | 20 | 0 | 4 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Math/Probability.lean` | `5f9a6e717ff0d872dea4edd9b88a3edea355ce58` | 17721 | 26 | 26 | 0 | 20 | 0 | 5 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Math/ProbabilityMassFunction.lean` | `1d4807d8e7bea067b67cd4af3156664b05fae874` | 27061 | 53 | 53 | 0 | 45 | 0 | 8 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Math/TraceRun.lean` | `18d3a3a411dcf4c39c066e4c0aa9acc0984731b1` | 10017 | 13 | 13 | 0 | 8 | 0 | 4 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Semantics/DSMachine.lean` | `5d4931f00a70ebc24d78d142ccd39fb501da8fbb` | 1663 | 1 | 1 | 0 | 0 | 0 | 0 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Semantics/TransitionTrace.lean` | `3314705941ee29b13edf9e298b7695df3a194d18` | 6582 | 15 | 15 | 0 | 13 | 0 | 1 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Theorems/Kuhn.lean` | `979c22cdbf77e0c9f2a1e21fd432ec474949bbbb` | 3624 | 3 | 3 | 0 | 0 | 0 | 3 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Theorems/Kuhn/BehavioralToMixed.lean` | `c7d850b76ed6e38923228f8c848905c15b032480` | 5203 | 6 | 6 | 0 | 3 | 0 | 0 | 1 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Theorems/Kuhn/BehavioralToMixedCore.lean` | `f14f8737d4ec367297bda099bc9dc8631e8ffc89` | 28456 | 21 | 21 | 0 | 16 | 0 | 5 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Theorems/Kuhn/CorrelatedRealization.lean` | `154b268bb91a95b0d59fec6eeb646a909adeb6f0` | 99348 | 75 | 75 | 0 | 67 | 0 | 0 | 4 | 4 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Theorems/Kuhn/KuhnModel.lean` | `4afad1c11631c2496500824862a440f07ed8867c` | 17885 | 43 | 43 | 0 | 10 | 0 | 20 | 1 | 12 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Theorems/Kuhn/MixedToBehavioralCore.lean` | `479c37a9a9ed9c2ffe715edf2ddf63d519ea8cd7` | 58334 | 53 | 53 | 0 | 41 | 0 | 10 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Theorems/Kuhn/ObsModel.lean` | `cd683d02e31cbdf9161ebdac1024e7e9e4c9755c` | 26912 | 63 | 63 | 0 | 21 | 0 | 17 | 1 | 24 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Theorems/Minimax.lean` | `fd6fac294a4f260bed35cd56e44298932d8a6ef6` | 10187 | 10 | 10 | 0 | 10 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Theorems/NashExistenceMixed.lean` | `9a46ffe143c30b70c414c7e6204ad472d979fec5` | 30896 | 44 | 44 | 0 | 35 | 0 | 9 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/GameTheory/Theorems/OneShotDeviation.lean` | `fdeb83db7d4dba0303a778b6d1928e83160a2e2b` | 17785 | 8 | 8 | 0 | 7 | 0 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FiniteGameFeedbackBridge.lean` | `6254de5b0f60358926ca18c496a1dcb06305e8a6` | 22565 | 43 | 43 | 0 | 29 | 0 | 8 | 2 | 4 |  |
| `proofs/lean/juris_lean/JurisLean/FiniteHorizonAdequacy.lean` | `17662ff6c9c6e265c2401d37bff9489a0ff2c30e` | 9828 | 24 | 24 | 0 | 13 | 0 | 10 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FiniteHorizonGame.lean` | `41c95caea04cd80599b04434fd11a1ad2a8a77cb` | 10523 | 32 | 32 | 0 | 21 | 0 | 8 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/FiniteHorizonKuhn.lean` | `955fc506b995301b015037956cc8371308ff7950` | 7496 | 11 | 11 | 0 | 9 | 0 | 1 | 1 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FiniteHorizonRecords.lean` | `1e12d6b4a5c124327d8a376809ca3bd947aa74f3` | 7754 | 32 | 32 | 0 | 17 | 0 | 8 | 4 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/CaseIsomorphism.lean` | `66348a0f56a0a30e3d17b1e9185157cc5e092387` | 14347 | 37 | 37 | 0 | 21 | 0 | 15 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/CohortInterval.lean` | `ef6d0c3a91e4bacb4aacaddbbf25c6613f499989` | 5196 | 16 | 16 | 0 | 10 | 0 | 5 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/CohortRate.lean` | `13307fbadc5aba1c9be6322d772b1007dcc3d711` | 3506 | 6 | 6 | 0 | 5 | 0 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/DerivedCertificate.lean` | `14a049164c64c786153814e6a69347ee462ab0bf` | 6040 | 15 | 15 | 0 | 9 | 0 | 5 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/Disclosure.lean` | `c93e491cbee3005deee3ae308bfb6692ee3b2d79` | 3432 | 11 | 11 | 0 | 7 | 0 | 4 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/GameTree.lean` | `24bef05d069f5ecbb4e5523e06b00ef4e62a2235` | 7568 | 19 | 19 | 0 | 15 | 0 | 3 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/GateTable.lean` | `c1f24e19be5cfbeee5e0d1af36e5995fd315a89f` | 2749 | 6 | 6 | 0 | 6 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/Kernel.lean` | `434b8962dc62809b73ba1a59e70c06d9fe8de284` | 4806 | 19 | 19 | 0 | 13 | 0 | 4 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/LinearScorer.lean` | `dfc9e8780aa128681e53d6b4bf209f55884f6801` | 4273 | 12 | 12 | 0 | 9 | 0 | 3 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/MatrixGame.lean` | `0bcd8bb70b4c51289b7da9dee8fee5e07dc0d03d` | 4166 | 11 | 11 | 0 | 8 | 0 | 3 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/MixedPennies.lean` | `3d45351236eb42ad328db80294c64a60effff3c2` | 7084 | 13 | 13 | 0 | 11 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/OneShotDeviation.lean` | `b5d1571ceccc9d0a123b771d9eb2c781461185d9` | 25334 | 40 | 40 | 0 | 25 | 0 | 13 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/PureNash.lean` | `367d2ef267b49aa86d78972c1a6d9d9d1eea95d3` | 28046 | 46 | 42 | 4 | 27 | 0 | 15 | 4 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/ReLUApprox.lean` | `cef9cbdc943032c73f5be09842a05a1d97f7c503` | 7807 | 14 | 14 | 0 | 9 | 0 | 5 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/ReLUFamily.lean` | `1518aec28da7edd812b0b7e022691ff60de5d20a` | 9596 | 14 | 14 | 0 | 13 | 0 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/RouteDecision.lean` | `fe62f3e1f225fdb1a258b23803b0ea7e1d012d22` | 5833 | 19 | 19 | 0 | 10 | 0 | 8 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/SequentialGames.lean` | `9ba1634ac920d12d4941e5411c236724a72c6ea8` | 10016 | 15 | 15 | 0 | 9 | 0 | 3 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/SourceRank.lean` | `40942393cb230240025793866b36700a465ffaf2` | 2967 | 7 | 7 | 0 | 7 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/StructureInvariants.lean` | `5b536289036ae484fd8abfca4d73d9271b12e92a` | 4383 | 9 | 9 | 0 | 7 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/SubstrAdmission.lean` | `67c39a28fcfafbe1955813136213e80dd4ae5783` | 3705 | 9 | 9 | 0 | 7 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/TaxSlices.lean` | `4a35dafd6f7614e719e06e66a5e9e99460abbec9` | 4541 | 12 | 12 | 0 | 9 | 0 | 2 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/Waterfall.lean` | `289c9ae0a85df228d42809ba237230b69a60f8e3` | 4020 | 12 | 12 | 0 | 10 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/ZeroSumSion.lean` | `d4f975fdebb0ff39aaba4e4817a5f921b139a469` | 14469 | 19 | 19 | 0 | 18 | 0 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Mandate/ZeroSumValue.lean` | `1081b0dbfe26b67eebf67e1b1da6e6efd54454da` | 18103 | 15 | 15 | 0 | 15 | 0 | 0 | 0 | 0 |  |

## G14_neural_analysis　分析/逼近与 ForMathlib 候选

- 分组依据：External analytic / approximation lemmas, including ForMathlib candidates.
- 文件数：17
- 词法声明次数：174（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/External/NeuralNetworkProofs/ForMathlib/ConvolutionDegreeBound.lean` | `26a03b47653489dfa829f63d1583c84f5f9d6fe4` | 13482 | 11 | 11 | 0 | 2 | 8 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/NeuralNetworkProofs/ForMathlib/ConvolutionIteratedDeriv.lean` | `0cbed03af072bf2342c434092bfea8472f94c576` | 3188 | 1 | 1 | 0 | 1 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/NeuralNetworkProofs/ForMathlib/ConvolutionPolynomial.lean` | `3490b9e4cc39c97bec7fa9de748c76efd3f13891` | 12311 | 16 | 16 | 0 | 6 | 9 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/NeuralNetworkProofs/ForMathlib/IteratedDerivPolynomial.lean` | `c11e8fb98a5d49d586cdc703ae62b5cea143a3ce` | 10774 | 15 | 15 | 0 | 4 | 11 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/NeuralNetworkProofs/ForMathlib/PolynomialDistribution.lean` | `cf7250e55cc41d44874bbfcb4a83004c1118f7b7` | 10388 | 6 | 6 | 0 | 1 | 4 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/NeuralNetworkProofs/ForMathlib/RidgePowersSpan.lean` | `bc6055e781e44e2e82abb2c94af418ffa344d410` | 13353 | 16 | 16 | 0 | 13 | 0 | 3 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/NeuralNetworkProofs/ForMathlib/SmoothCompactAntideriv.lean` | `abce47de8c8812fbba29149d5e8fa3ca6e3b01b0` | 9712 | 9 | 9 | 0 | 1 | 7 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/NeuralNetworkProofs/ForMathlib/UniformRiemannConvolution.lean` | `fcc74b51f2663fa92c36371b0930f4203858044a` | 41098 | 21 | 21 | 0 | 19 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/NeuralNetworkProofs/UniversalApproximation/Leshno.lean` | `713b5db3fb69f71558bffbd8ad679c9fde7da4d5` | 6124 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/External/NeuralNetworkProofs/UniversalApproximation/Leshno/ClassM.lean` | `3df57546232a632a669304e8317b6317a3aba9fb` | 3926 | 5 | 5 | 0 | 2 | 0 | 2 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/External/NeuralNetworkProofs/UniversalApproximation/Leshno/Converse.lean` | `c00ca22e672d88a22d59a451f8e312b54805c522` | 14913 | 26 | 25 | 1 | 19 | 0 | 5 | 1 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/External/NeuralNetworkProofs/UniversalApproximation/Leshno/Family.lean` | `f6a12bfe58ff732079450fc9192e688685eb00d6` | 8352 | 11 | 11 | 0 | 6 | 0 | 5 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/NeuralNetworkProofs/UniversalApproximation/Leshno/Mollify.lean` | `a5d77b06d17d91dc75abf31d4b79d1e3013e8e83` | 16907 | 8 | 8 | 0 | 8 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/NeuralNetworkProofs/UniversalApproximation/Leshno/MollifyDef.lean` | `30b1928671fe18777db2e4a379276d0189ecf749` | 2336 | 2 | 2 | 0 | 1 | 0 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/NeuralNetworkProofs/UniversalApproximation/Leshno/Ridge.lean` | `cd0904fc538321525a288bb8d9a76fabe3f079bf` | 12956 | 14 | 14 | 0 | 9 | 0 | 5 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/NeuralNetworkProofs/UniversalApproximation/Leshno/SmoothEngine.lean` | `2e39d1a66624b443359ad64960b9f290a6963152` | 21480 | 8 | 8 | 0 | 3 | 4 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/External/NeuralNetworkProofs/UniversalApproximation/Leshno/Theorem.lean` | `c9fe81c158aca45bda5e649807118af6529b022d` | 6386 | 5 | 5 | 0 | 3 | 1 | 1 | 0 | 0 |  |

## G07_seams_process　Seams 过程与针桥

- 分组依据：Seams: process, statute chain, temporal/calendar, unified needles and bridges.
- 文件数：71
- 词法声明次数：4008（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/Seams/AdjudicationBridge.lean` | `c10782dddbec6c06231956f2a97da38afec2c463` | 57823 | 91 | 91 | 0 | 62 | 0 | 26 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/BoundaryBridge5.lean` | `f68a52a9ce9f39553d4a6faf7ee4468e4c4e2d6d` | 18278 | 23 | 23 | 0 | 15 | 0 | 6 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/BoundaryClosure.lean` | `af08e307e1f07aa70be872598dff9cb22f724170` | 61870 | 86 | 86 | 0 | 57 | 0 | 21 | 0 | 8 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/BurdenStatutes.lean` | `4608ee573dbb7c05ec3db46a8dd69bb556246390` | 73049 | 129 | 129 | 0 | 78 | 0 | 37 | 0 | 14 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/CaseInput.lean` | `4c848700a7e2963dc6a5cc17dc74d38dcbbc458c` | 6090 | 6 | 6 | 0 | 3 | 0 | 2 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/ClaimBasis.lean` | `b01e5fd16451034141bb1752e515589e38908915` | 22384 | 49 | 49 | 0 | 32 | 0 | 9 | 0 | 8 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/FullProcess.lean` | `ca4e981cb1b9aefdb98221e1f34a3e49f2ac23c0` | 70129 | 144 | 144 | 0 | 96 | 0 | 41 | 0 | 7 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/InstitutionalEffects.lean` | `8189f3690eeeabb202329e38d40b7508cc5eb64c` | 43312 | 112 | 112 | 0 | 73 | 0 | 26 | 0 | 13 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/LegacyConeBridge.lean` | `d0f9c21b6ddffc5b3fe0725affa51f6ff66dda0c` | 33925 | 59 | 59 | 0 | 26 | 0 | 33 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/Limitation.lean` | `bac13d7e07590c7de3d1c2ec33d0eb7376c73d3a` | 14476 | 24 | 24 | 0 | 12 | 0 | 9 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/PayoffEquilibrium.lean` | `3000779f0abbf9bc19bab14243c702a71bdd886d` | 42494 | 85 | 85 | 0 | 46 | 0 | 32 | 0 | 7 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/PrecedentFlow.lean` | `a57d9f70cc1825a8dcd5cc5eb7ac34e8aea68d53` | 53494 | 101 | 101 | 0 | 55 | 0 | 33 | 0 | 13 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/Probability.lean` | `229f057e73cc1d3186b91003a8da184dd6d55916` | 65896 | 106 | 106 | 0 | 66 | 0 | 32 | 0 | 8 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/ReductionConditions2.lean` | `4400df63e955588c4abf0e4bba6e8ea38e872367` | 41726 | 56 | 56 | 0 | 35 | 0 | 20 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/Representation.lean` | `725d8fd030ac5621fd087c3eca44272ccbf3e2fe` | 25697 | 45 | 45 | 0 | 30 | 0 | 13 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/SanctionInterest.lean` | `dcf5536fa7ed1943bb57ad70dd1979604c7d8558` | 36315 | 46 | 46 | 0 | 40 | 0 | 6 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/SourceNorms.lean` | `4318b7301781ea65897b47d8310a79e26728aa11` | 31311 | 44 | 44 | 0 | 29 | 0 | 13 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/StatuteChain.lean` | `4d21df8a5bd973913f3b08df491c351f782a1ede` | 66295 | 68 | 68 | 0 | 56 | 0 | 12 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/Temporal.lean` | `184abad3118981b4bd5d44c8cd989e06ad7fd159` | 35677 | 57 | 57 | 0 | 40 | 0 | 16 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/Transitions.lean` | `ff7544e492530f8668c47c277c8d305b758b4659` | 39737 | 63 | 62 | 1 | 43 | 0 | 17 | 2 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/Uncertainty.lean` | `be7428505eb44d91e145e710ff77713c71d969b8` | 43486 | 70 | 70 | 0 | 44 | 0 | 24 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/Unified.lean` | `0bec1a947d69431252e7fd8f2def5768d1bcf945` | 23063 | 16 | 16 | 0 | 8 | 0 | 7 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedAdmission.lean` | `da816ad4d5f14f28c3e28701f66c81747d9b55c4` | 11302 | 18 | 18 | 0 | 9 | 0 | 5 | 0 | 4 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedAnalysis.lean` | `39d2e3cf3efe8d8e1237a980dd0fed24c8eeecec` | 6987 | 18 | 18 | 0 | 8 | 0 | 6 | 0 | 4 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedArgumentation.lean` | `786dc7ea8e1d909e50ea832911998ba753ada260` | 16136 | 20 | 20 | 0 | 14 | 0 | 4 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedBeta.lean` | `d664b2787418cadc083a3eb2da9408d13314001c` | 9102 | 15 | 15 | 0 | 8 | 0 | 4 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedBetaDomain.lean` | `9a39eb8dab05afc4428878434638886379b9e4e7` | 92698 | 84 | 84 | 0 | 69 | 0 | 15 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedCAD.lean` | `1fd4d08d102f66688e2498c32399fcc051126802` | 9132 | 16 | 16 | 0 | 11 | 0 | 3 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedCAD2.lean` | `538f0ebb7f3368ad63de86937d745bc35f0825b0` | 8873 | 15 | 15 | 0 | 8 | 0 | 7 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedCADCore.lean` | `ff598f6895405b6837a092554c9daa6cc7709fb1` | 52597 | 95 | 93 | 2 | 47 | 0 | 38 | 0 | 10 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedCalendar.lean` | `f67fb65392d584c33b749d2dae54662b7714a4ae` | 62949 | 95 | 95 | 0 | 73 | 0 | 19 | 1 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedComposition.lean` | `fc30fa6babaf56488cf3df39a97dc4099e669f09` | 5468 | 7 | 7 | 0 | 4 | 0 | 2 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedEquilExist.lean` | `7971c99b8f631f654fbccd07077284cbc90e1850` | 42830 | 75 | 75 | 0 | 47 | 0 | 25 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedEvalLayer.lean` | `b5c804b191d8c19866200bfff7b0f7f2c8dadca9` | 54267 | 125 | 125 | 0 | 67 | 0 | 46 | 0 | 12 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedEvents.lean` | `4dfba9382e1fbc84d2079958a06997147abf7866` | 12277 | 18 | 18 | 0 | 8 | 0 | 5 | 0 | 5 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedFinalization.lean` | `b468c08815e77bb7f5ecfb540a4fe3661ee08ad5` | 18042 | 24 | 24 | 0 | 18 | 0 | 2 | 0 | 4 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedFourteenFamilies.lean` | `52cd07b46561a2c90fb509e81615f14beaebea86` | 82865 | 164 | 164 | 0 | 81 | 0 | 52 | 0 | 31 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedGuards.lean` | `d26fe486c3043f82f334fb355c7cd33f15373986` | 11504 | 28 | 28 | 0 | 17 | 0 | 6 | 0 | 5 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedHornIT.lean` | `9c60001bf7a42b9c981e63510ffa41eb75b53059` | 9803 | 15 | 15 | 0 | 10 | 0 | 4 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedInstance.lean` | `b0e399d729e6de81d14b5caa04637751f4913788` | 50206 | 81 | 81 | 0 | 58 | 0 | 22 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedLegacy.lean` | `e6c94695aaa3531872623b2cb440f38fe5bdd2bc` | 4213 | 10 | 10 | 0 | 2 | 0 | 4 | 0 | 4 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedMasterNeedle.lean` | `bacf1e1301f9af9703fbd392fc188668b966fd0f` | 62555 | 74 | 74 | 0 | 44 | 0 | 29 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedNeedlesGap05.lean` | `1d8959315159d76100a6412f227f480099339404` | 72715 | 91 | 91 | 0 | 71 | 0 | 19 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedNeedlesGapLate.lean` | `217373aef8e6d18f3bd132709db290b9589cb0fe` | 44489 | 57 | 57 | 0 | 32 | 0 | 18 | 0 | 7 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedNeedlesGapMid.lean` | `b92134662e8f028a4430c00c652b3b9e118a00b1` | 41021 | 80 | 80 | 0 | 46 | 0 | 26 | 0 | 8 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedNeedlesS0S1.lean` | `6803236455db1d80eacacd9275797ba204d97480` | 32424 | 53 | 53 | 0 | 21 | 0 | 19 | 0 | 13 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedNeedlesS2.lean` | `4f09d0910f5353212f8303c3eb1b400fac6e9831` | 8753 | 11 | 11 | 0 | 7 | 0 | 3 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedNeedlesS3a.lean` | `95a8d9230eaadedd768f4b124eb179fb1b62ca62` | 36144 | 35 | 35 | 0 | 26 | 0 | 9 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedNeedlesS3b.lean` | `80b8891b2e98b148c9569d1d5e5c06f64d029861` | 53762 | 74 | 74 | 0 | 40 | 0 | 27 | 0 | 7 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedNeedlesS4.lean` | `194b2e5a6a6646d90710b8f752861c8eacb4c2b3` | 26855 | 53 | 53 | 0 | 28 | 0 | 18 | 0 | 7 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedNeedlesS5.lean` | `5d654d752a676550419148bc7a71b77fc6e94d0a` | 8496 | 10 | 10 | 0 | 10 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedNeedlesS6S7.lean` | `e8d3dd473ffb5455392c46f37b8307b5c1bbb9aa` | 22339 | 25 | 25 | 0 | 16 | 0 | 6 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedNeedlesTotal.lean` | `a5794312871efdd01cd565cad38abe071b3738b7` | 4805 | 3 | 3 | 0 | 3 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedNeedlesXT.lean` | `911f6643664c8a132043720abe5171202059a654` | 17134 | 23 | 23 | 0 | 13 | 0 | 5 | 0 | 5 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedNeedlesXU.lean` | `de48b71649681b4a9e430c7ebb4d7a09e3d4eaf0` | 37800 | 36 | 36 | 0 | 22 | 0 | 13 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedNetTrajectory.lean` | `130dff5c16b9f696090c1f9b4030e2d19635ce9a` | 61962 | 107 | 107 | 0 | 62 | 0 | 39 | 0 | 6 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedNormFlow.lean` | `fa25555765165879b37efe6f6837e18f10f3c3d9` | 5231 | 13 | 13 | 0 | 4 | 0 | 5 | 0 | 4 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedPayoffChain.lean` | `39a17bba3e803ed9c0e347e159c59e699f76589c` | 55933 | 84 | 84 | 0 | 61 | 0 | 20 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedPerformance.lean` | `e006f52323f94b16094cb548dfeb99f944ae2cae` | 7728 | 22 | 22 | 0 | 9 | 0 | 8 | 0 | 5 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedQuantLedger.lean` | `a2c095c717114e7d7d710307063e3af80b923bd0` | 55542 | 173 | 173 | 0 | 79 | 0 | 71 | 0 | 23 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedQuantileNarrow.lean` | `f6a03fa62a763749190fbfd0fbb9b9696bfc79c3` | 44375 | 60 | 60 | 0 | 44 | 0 | 13 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedQuantities.lean` | `0243b713c91f980229c1e73d5bcab602a8152fb6` | 9376 | 16 | 16 | 0 | 14 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedSemantics.lean` | `6eedc7ed436774c8d3835bdb24ff96e2cacb5f1c` | 8121 | 12 | 12 | 0 | 6 | 0 | 4 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedSummary.lean` | `ec7feb42e2a2fe000b990bce7f25b8472e94c93b` | 13562 | 36 | 36 | 0 | 20 | 0 | 9 | 0 | 7 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedTrajectory.lean` | `2fa65f2d3dd6120be0f565919e8ceb394318b0bf` | 24804 | 66 | 60 | 6 | 28 | 0 | 16 | 15 | 7 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedUtility.lean` | `4f6aad07a5bd750b4d29a189b8b983690fa2a14c` | 8577 | 17 | 17 | 0 | 8 | 0 | 7 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedW4Behavior.lean` | `b15ff29918b42267ab6afaf92f4b79fd37f6749e` | 39357 | 89 | 89 | 0 | 41 | 0 | 37 | 0 | 11 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedW4Deviation.lean` | `622877601db76b19198fc16e2ae7b530728f5ea0` | 45858 | 101 | 101 | 0 | 55 | 0 | 30 | 0 | 16 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedW4Games.lean` | `fc002d0476308ceb4da9f1298840bfdc6e2e4200` | 59083 | 87 | 87 | 0 | 49 | 0 | 24 | 0 | 14 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UnifiedW4Interp.lean` | `6125367d853dfa7b8f5272d51f68771fad7b410b` | 32267 | 71 | 71 | 0 | 37 | 0 | 26 | 0 | 8 |  |
| `proofs/lean/juris_lean/JurisLean/Seams/UniformContinuous.lean` | `997859f97496d90ea06ca055a4328e49133d90cb` | 17664 | 26 | 26 | 0 | 24 | 0 | 2 | 0 | 0 |  |

## G09_fullmath　FullMath

- 分组依据：FullMath contracts, acceptance and related closure modules.
- 文件数：65
- 词法声明次数：1506（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/FullMath/Acceptance.lean` | `b8d78d2f53aaf170040722183d166e6a70c4e6b2` | 94771 | 219 | 219 | 0 | 219 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Action/IncentiveEnumeration.lean` | `17d213ccf4aadf6e876c7a8707e52151d557a965` | 2591 | 8 | 8 | 0 | 3 | 0 | 5 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Action/Mechanisms.lean` | `e989a9d07e8e41dcd0c991b37582f688ebeb5e59` | 2082 | 5 | 5 | 0 | 1 | 0 | 3 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Action/RobustDecisions.lean` | `11e917670ba94ec84b160a93ea6a6d4aede828d6` | 2133 | 6 | 6 | 0 | 4 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Action/Settlement.lean` | `f43bbe648d99e80a47284a56185b6c6d0155d2c9` | 3079 | 10 | 10 | 0 | 5 | 0 | 4 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/All.lean` | `3acbf32f253a281ffde9c76f477640783a090422` | 3311 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/FullMath/Burden/DomainAgnostic.lean` | `e48da453257491b0e3aed2159b5b229919845124` | 3029 | 11 | 11 | 0 | 6 | 0 | 2 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Burden/Families.lean` | `6dc059a3bdc05209502cc0a7bed3dfc0a2332440` | 4271 | 14 | 14 | 0 | 5 | 0 | 9 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Burden/Readiness.lean` | `55255dd9ec19d90120c4d89423905fcb772e16de` | 2513 | 11 | 11 | 0 | 5 | 0 | 3 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Burden/SourceTime.lean` | `dbd6876cb49ac93a371e3d6c15bbef6394d90e83` | 3818 | 14 | 14 | 0 | 7 | 0 | 5 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Burden/Standards.lean` | `97f46864c6f9d3950426972a11a809854a4d3527` | 3583 | 8 | 8 | 0 | 4 | 0 | 1 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Causal/PartialIdentification.lean` | `7a7f7b72653220ddcae9c8cf5093f83717dd2429` | 3812 | 9 | 9 | 0 | 6 | 0 | 2 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/CompletionAudit.lean` | `a516d67442acc5943ec2b737841a13b694c5dfaa` | 47378 | 217 | 217 | 0 | 217 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Composition/CheckerCorrespondence.lean` | `f1024b547e6a4aa0a16f10f1739584c97fa4f496` | 2231 | 7 | 7 | 0 | 4 | 0 | 3 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Composition/DomainChains.lean` | `791a8365c94ea13883c41001166026bfad26b4e4` | 1961 | 5 | 5 | 0 | 3 | 0 | 1 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Composition/EnvelopePipeline.lean` | `015b97d86011fe613698b9eadd0ded504af10935` | 2191 | 7 | 7 | 0 | 5 | 0 | 1 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Composition/RelationalComposition.lean` | `765eada61f0097060ba41a9d8299b3dcf09f3a30` | 1308 | 3 | 3 | 0 | 2 | 0 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Composition/ScenarioBridge.lean` | `5a6bf5af74df52589edb762e43df0f7f8477d09d` | 2705 | 4 | 4 | 0 | 2 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Composition/UnifiedCorrectness.lean` | `c7f739eade9fcaab0af491ffe25c62f12c530329` | 2147 | 8 | 8 | 0 | 5 | 0 | 2 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Contracts.lean` | `7e7eab7158226a16a0ce1d73c8cd17f7b678c7e5` | 256048 | 503 | 503 | 0 | 0 | 0 | 459 | 0 | 44 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Core/BusinessSemantics.lean` | `b27e4fe17ddb64a44707537696db85de9c68d36f` | 5637 | 18 | 18 | 0 | 4 | 0 | 11 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Core/Foundations.lean` | `71dea00eb60063288ce58dd6127ecbc650688675` | 2093 | 9 | 9 | 0 | 3 | 0 | 2 | 0 | 4 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Core/IdentityCodec.lean` | `0d2f7c378dcb07e7bf9fa4352461db6821611d15` | 4606 | 17 | 17 | 0 | 9 | 0 | 6 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Document/ByteSyntax.lean` | `78e141af0d6c177807a03bd75febc14548cbc475` | 5576 | 26 | 26 | 0 | 14 | 0 | 11 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Evidence/Admission.lean` | `4db366e795a3054cb6bc7c481feb65b31b40b058` | 3080 | 8 | 8 | 0 | 5 | 0 | 2 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Evidence/Provenance.lean` | `33b0919d13034a3c29947b17356e92689cde83f8` | 3974 | 10 | 10 | 0 | 5 | 0 | 3 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Evidence/Withdrawal.lean` | `36f6a3b540dfcc8e332f228a52f331be4250ac35` | 8035 | 13 | 13 | 0 | 10 | 0 | 2 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Gaps/Gaps.lean` | `7976c1fea9ca80dbb37acf61696e1fc8bd18e60a` | 6097 | 13 | 13 | 0 | 11 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/GenericKernels.lean` | `ce5a8bbeb93259b42631b912d8331bbbe2194a47` | 5793 | 22 | 22 | 0 | 15 | 0 | 7 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Logic/ArgumentConstruction.lean` | `6878b98d6aa9cd1250c6b7a3a5d6bff0a1098b50` | 9961 | 15 | 15 | 0 | 7 | 0 | 6 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Logic/ArgumentIdentity.lean` | `e0a032cb518db326f7dce2c4b5dca16e906dc8c6` | 5294 | 5 | 5 | 0 | 4 | 0 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Logic/AttackCompilation.lean` | `a47c6e5b71204d455ea45dce1d678d972575f760` | 5952 | 11 | 11 | 0 | 4 | 0 | 3 | 0 | 4 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Logic/ExtensionProfiles.lean` | `2f0d9542ab15f921e1c2dab75a2cae29e7916cba` | 11768 | 28 | 28 | 0 | 17 | 0 | 10 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Logic/HornFixpoint.lean` | `6e97e57d2a33db22cc18b749998828c128e0f6a9` | 7076 | 20 | 20 | 0 | 16 | 0 | 4 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Logic/QueryAggregation.lean` | `f01fda22dfedbe59c8fdb0293f04546647b3a29f` | 6175 | 11 | 11 | 0 | 6 | 0 | 3 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Numeric/Banach.lean` | `a81f8f8076cce1156cf2e3b95a99a261c66be6a2` | 7122 | 10 | 10 | 0 | 8 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Numeric/Bellman.lean` | `35d4df191f2899cec64028d00509a682709e392f` | 5585 | 7 | 7 | 0 | 4 | 0 | 3 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Numeric/Convexity.lean` | `a19c2c4f31b3e652d6b6724c50d141ce4fada777` | 3574 | 8 | 8 | 0 | 5 | 0 | 2 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Numeric/IntegerBranch.lean` | `aebd8c7ea18c418fdbd13c88a8c7ba783964ae87` | 3792 | 5 | 5 | 0 | 5 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Numeric/Intervals.lean` | `165dfc45fb10880e3e6aa59de36d0c6c1f0b8cd2` | 6554 | 13 | 13 | 0 | 8 | 0 | 4 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Numeric/LinearPrograms.lean` | `c2ea5965a011735173ff3a3437c524f04e72651c` | 3031 | 6 | 6 | 0 | 2 | 0 | 4 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Numeric/Quantities.lean` | `a2d3fe7a19564005cf0fe4e718d6321fdbc2929d` | 5527 | 21 | 21 | 0 | 10 | 0 | 10 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Probability/BetaInterval.lean` | `86cc1dd1f9e290ce98ad001e51e17bd68b039341` | 3359 | 6 | 6 | 0 | 4 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Probability/Brier.lean` | `d8fd5493db522c091d060ac042dabc016fdcdfde` | 1332 | 3 | 3 | 0 | 2 | 0 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Probability/Conditioning.lean` | `53fffc9f5e2eca61ea7e56b288a7a2e7cfedae09` | 2899 | 7 | 7 | 0 | 3 | 0 | 3 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Probability/DirichletPosterior.lean` | `6535cfe3498c5b2beecfc55d754612ece3e765c5` | 5943 | 11 | 11 | 0 | 8 | 0 | 3 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Probability/E01Contract.lean` | `add5d59147e72075e50aae30b2aff8373e2d534f` | 4355 | 8 | 8 | 0 | 5 | 0 | 2 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Probability/EvidenceIdentity.lean` | `df20caff7d94d708e42066d0388d5446fd02ae51` | 6621 | 14 | 14 | 0 | 8 | 0 | 5 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Probability/FiniteBN.lean` | `65eb84406639995cbc860e50ca7eaec868e7f5ef` | 3589 | 8 | 8 | 0 | 2 | 0 | 2 | 2 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Probability/Misspecification.lean` | `9d540d6cd24496fd45501b9bfe9cbf160f4e43bd` | 2617 | 4 | 4 | 0 | 3 | 0 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Probability/ModelAveraging.lean` | `e00791089b96251b417e67a02b04eec13ca688fb` | 3771 | 5 | 5 | 0 | 3 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Probability/PAV.lean` | `54b4a5071ab4e95a25b60dffc3b0459ce17a1944` | 4072 | 6 | 6 | 0 | 3 | 0 | 2 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Probability/SplitNoLeak.lean` | `a9ddf51bae458377797de969838e84a06d9a4f2d` | 2690 | 10 | 10 | 0 | 5 | 0 | 4 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Probability/UnprocessedMass.lean` | `23c1367c81b178121c517f308d2f770e8924d97a` | 1843 | 2 | 2 | 0 | 2 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Probability/VariableElimination.lean` | `0c01aa47c36b0704c9f00b646690ee463971a007` | 4025 | 9 | 9 | 0 | 5 | 0 | 4 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Representation/FiniteCertificates.lean` | `3451c095b19db94a9e462225156d7b38b26dfb3c` | 3701 | 12 | 12 | 0 | 6 | 0 | 5 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Representation/SymbolicRepresentation.lean` | `ce02f82de12d65b197f3d21be76100330fd003a0` | 6220 | 17 | 17 | 0 | 4 | 0 | 7 | 0 | 6 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Roots/SevenRoots.lean` | `06f2aea34c0d094eb38c97bad79c3bb198edec21` | 11709 | 19 | 19 | 0 | 14 | 0 | 2 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/FullMath/Tranche1.lean` | `3987e8cc179fad8eac77d0054c88eac8642e71bf` | 587 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/FullMath/Tranche2.lean` | `a05e6aa2795612d656c901b4d64d5b0c4aac393d` | 801 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/FullMath/Tranche3.lean` | `78a31229115bc263a4a10ed4f6766f3b0de19659` | 258 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/FullMath/Tranche4.lean` | `87289b422f6af3c05e42c1ecd2edbdd7f29f0dae` | 309 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/FullMath/Tranche5.lean` | `96f41f2a78f94443583b194b526c824b15029363` | 177 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/FullMath/Tranche6.lean` | `b4beaa4c78c79641b7cf5fea1d40af162e6f548a` | 390 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/FullMath/Tranche7.lean` | `2e938a99bdde7294d9dd0356dd1af94238acb092` | 36 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |

## G10_remaining_closure　RemainingClosure

- 分组依据：RemainingClosure family.
- 文件数：19
- 词法声明次数：688（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/RemainingClosure/Audit.lean` | `01afc58f85fc6f288310f1848b456bb13bc0069c` | 663 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/RemainingClosure/CNSemanticConnection.lean` | `ca6298fe2dbc43edc05cd51c9c34a07584e9ad90` | 140107 | 284 | 279 | 5 | 113 | 60 | 88 | 12 | 11 |  |
| `proofs/lean/juris_lean/JurisLean/RemainingClosure/CouplingLift.lean` | `c025a00050df860b9ff7405e425a8bc9c5d1b221` | 5909 | 6 | 6 | 0 | 2 | 2 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/RemainingClosure/EntitySemantics.lean` | `5d9936e2712dfc078dedeb5b975cae25de2ec014` | 20117 | 33 | 30 | 3 | 20 | 0 | 9 | 3 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/RemainingClosure/EvidenceConditioning.lean` | `15b3baa981df4164ad7a531009563e5323ed5f68` | 8498 | 18 | 16 | 2 | 12 | 0 | 3 | 2 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/RemainingClosure/FullEventLog.lean` | `76ad2a3e473f09f5f6589a3807c2bb45c66f91a6` | 16412 | 53 | 53 | 0 | 36 | 0 | 14 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/RemainingClosure/InterpretationChoice.lean` | `3c719ced36445eaee954a7e226587c9f87c43480` | 22491 | 49 | 45 | 4 | 23 | 7 | 12 | 6 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/RemainingClosure/MultiAgentFeedback.lean` | `09a25617b0eb6e44031af9188a298d3c7332482f` | 32003 | 47 | 47 | 0 | 17 | 8 | 21 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/RemainingClosure/PolicyIndependentFeedback.lean` | `5ffb0465b93fde347a1680ed0d90bea82e31bb7e` | 2885 | 7 | 5 | 2 | 4 | 0 | 1 | 2 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/RemainingClosure/ProcessTransport.lean` | `e2077188f74d95034593df647ba6ac3c1f7fdbf4` | 13316 | 26 | 25 | 1 | 9 | 9 | 5 | 2 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/RemainingClosure/RuleEvolution.lean` | `6eba0097402f7e0892614fb7745c1e12e757f0b5` | 13703 | 25 | 22 | 3 | 11 | 5 | 6 | 3 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/RemainingClosure/TemporalFeedback.lean` | `6009733ce6a720e10a0a90832871c58309509c36` | 35530 | 79 | 63 | 16 | 27 | 6 | 21 | 16 | 9 |  |
| `proofs/lean/juris_lean/JurisLean/RemainingClosure/UnifiedClosure.lean` | `1d87d7aef5405403930f4c7f3ba63d62c0469286` | 2878 | 3 | 2 | 1 | 2 | 0 | 0 | 1 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/RemainingClosure/W1Atoms.lean` | `076b7d030d6a09f00fd81c322ee45e15b2c7e5f4` | 8052 | 8 | 8 | 0 | 2 | 5 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/RemainingClosure/W1Audit.lean` | `4a1837bc3a33ae1535c490f1297c4992f9e90877` | 129 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/RemainingClosure/W1Invariant.lean` | `a30d65b54c1bf505f6bd43f3c7bb5efed7589ede` | 5092 | 7 | 7 | 0 | 4 | 2 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/RemainingClosure/W1Laws.lean` | `a38530df92a714edaf9686b444de35cbdadb55a9` | 10177 | 19 | 19 | 0 | 7 | 7 | 5 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/RemainingClosure/W1Sharp.lean` | `ad88db8fc3526838504dbc21086be290731b47d1` | 2526 | 8 | 8 | 0 | 3 | 3 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/RemainingClosure/W1Transport.lean` | `bc0b8b3ccebef64bcf26a3a44baff07d0bd30dc4` | 10606 | 16 | 16 | 0 | 1 | 12 | 2 | 1 | 0 |  |

## G08_cn_jurisdiction　CN 模块

- 分组依据：CN (mainland-related formalization) modules; legal correspondence remains un-checked until 法律资料员 returns sources.
- 文件数：34
- 词法声明次数：1152（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105.lean` | `b094cef8c0427c06b0f5bf9008dbdb7d7100d40d` | 8716 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/Acceptance.lean` | `d3264d042a09e8b14164017314a95db54df29c4b` | 9620 | 43 | 43 | 0 | 14 | 0 | 28 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/Algebra.lean` | `5b6a82cc2246cd0e8969c2647b4cbc51ffcbc150` | 7360 | 29 | 29 | 0 | 21 | 0 | 5 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/Checkpoint1.lean` | `9e4533a9db3c434b06c9569ce802fa13948a9c65` | 154 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/Checkpoint2.lean` | `7895d22c261c5a98e43f7cce5cb7805be65e4c36` | 282 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/Edges.lean` | `6e72b2fa42670de060f63f192300ae7df3050781` | 12296 | 17 | 17 | 0 | 5 | 0 | 12 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/EffectIR.lean` | `46107932c5ce34cea9e23f556f6bf33d96ab8754` | 4389 | 13 | 13 | 0 | 6 | 0 | 6 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/EngineConsumers.lean` | `2dd73dcb9fe474dd4193c5afda9fbb9f7ecc0eb9` | 16075 | 34 | 32 | 2 | 10 | 0 | 20 | 2 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/EngineExamples.lean` | `67b2ba5e87c2e12b2ca5c4a484a3798473ad5e57` | 11308 | 32 | 32 | 0 | 3 | 0 | 29 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/EngineTypes.lean` | `1651da7580eb7dc167bf9771e0449553f3956901` | 4032 | 5 | 5 | 0 | 0 | 0 | 1 | 0 | 4 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/EvidenceInstitutions.lean` | `3d4b8bd3666c22c7245f472209f16ff787fb06aa` | 6809 | 11 | 11 | 0 | 3 | 0 | 8 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/Examples.lean` | `8fc98ea77f01f1363a41ec9e1933eecc29c67164` | 19224 | 83 | 83 | 0 | 24 | 0 | 59 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/Exchange.lean` | `82d08e6362b59a79162d94787180dd3562c85622` | 5552 | 18 | 17 | 1 | 7 | 0 | 8 | 1 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/Execution.lean` | `fa9a4309f0ecd3b43054d914048b48a7ed91bac6` | 18032 | 27 | 27 | 0 | 7 | 0 | 16 | 0 | 4 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/FinancialMerge.lean` | `bdf90828ed906e38d5cf90a02329d4a2752224a2` | 6946 | 13 | 11 | 2 | 3 | 0 | 8 | 2 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/Foundation.lean` | `41ad0a4a7c91a66b072b8f5b340d2e24835914d2` | 11522 | 33 | 33 | 0 | 18 | 0 | 14 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/InstitutionRules.lean` | `6a154a50171444e4fd7d196e5fb07e5c1d2deacf` | 24989 | 136 | 136 | 0 | 77 | 0 | 43 | 0 | 16 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/Institutions.lean` | `fa52cded53e32c9ebf96298e1e39eadb5ab4dcfd` | 21552 | 58 | 58 | 0 | 26 | 0 | 30 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/OperationalReady.lean` | `70c5de5e45cbf23d1c29000aa67261d49ec0e051` | 3915 | 6 | 6 | 0 | 4 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/Operators.lean` | `88f03833c9cdc629c297807921c435d685cadbf0` | 17275 | 37 | 37 | 0 | 10 | 0 | 20 | 0 | 7 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/Payloads.lean` | `1eca1abe22a903634807e165dcfa89c75214e381` | 15897 | 57 | 57 | 0 | 36 | 0 | 19 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/PolicyIR.lean` | `b069f527e72601c2a1cb2ebe43e8c05345389469` | 6066 | 22 | 22 | 0 | 7 | 0 | 11 | 0 | 4 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/Program.lean` | `f36da88b11705d38f94c72c64b26d74f14824220` | 6076 | 17 | 17 | 0 | 9 | 0 | 6 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/QuietHistory.lean` | `2d915c9ce2fee973fb2e40094d6e94a94f4584bc` | 3918 | 10 | 10 | 0 | 4 | 0 | 4 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/Ready.lean` | `da813dca3a91952ac141fe8665a3432d8a3c7b13` | 18781 | 34 | 34 | 0 | 14 | 0 | 20 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/Runtime.lean` | `ad7ff12f44772275b3efac6d91ab0bae369a7db4` | 10963 | 30 | 30 | 0 | 5 | 0 | 16 | 0 | 9 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/State.lean` | `ef40e22c07f0679a3c49364e4454e4b34022acae` | 10601 | 34 | 34 | 0 | 8 | 0 | 15 | 0 | 11 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Completion20261105/WorldSemantics.lean` | `cb8fe73848adcb2af31e8dfe1598c156e9083a6d` | 7987 | 20 | 20 | 0 | 12 | 0 | 7 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Ops.lean` | `5bbac252840287d3acc827c8a876dab0d8e1dad9` | 3585 | 29 | 29 | 0 | 11 | 0 | 8 | 0 | 10 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Revision20261101/Ops.lean` | `6140f8e5ac6a069637048cd19a2cd4d18c9fdd5b` | 9541 | 60 | 60 | 0 | 8 | 0 | 17 | 0 | 35 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Revision20261101/Rights.lean` | `0685fbd71eac71f06f4490f6e6f57b3d497de94a` | 5805 | 35 | 35 | 0 | 15 | 0 | 10 | 0 | 10 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Revision20261101/World.lean` | `cd85897f4bd2f00855217472583bb632f511b3df` | 19423 | 92 | 92 | 0 | 19 | 0 | 49 | 0 | 24 |  |
| `proofs/lean/juris_lean/JurisLean/CN/Walls.lean` | `10e9753ba22feae8223689019bea354ffe8d884c` | 18163 | 87 | 87 | 0 | 43 | 0 | 16 | 0 | 28 |  |
| `proofs/lean/juris_lean/JurisLean/CN/World.lean` | `561da330968039678876f3c7a1e536933bc97ed6` | 4625 | 30 | 30 | 0 | 17 | 0 | 8 | 0 | 5 |  |

## G11_business_genealogy　业务根与谱系

- 分组依据：Business relation / process modules at package root.
- 文件数：31
- 词法声明次数：1102（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/BusinessProcessRealization.lean` | `28e015ecd934505560599be64ea7cb9c44375d5c` | 14863 | 27 | 23 | 4 | 13 | 1 | 7 | 6 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/BusinessRelations.lean` | `4d3f117fd4ce0bbb61b21faaaf3777889ca02716` | 9355 | 34 | 33 | 1 | 16 | 0 | 15 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/BusinessRelationsAudit.lean` | `a33a1e7691f4af4b48f0e8331f77d4a98d1a44e7` | 1699 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/BusinessRelationsDelta.lean` | `16000416bb065f291dc9b6a7caf8e668326af47d` | 4737 | 14 | 14 | 0 | 8 | 0 | 6 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/BusinessRoot/All.lean` | `9be9c31bd299db7633d4c5f7e59a918d5b5e035c` | 430 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/BusinessRoot/Analytics.lean` | `983d3bc97e61840dda168ce6a71c39eb984d7718` | 8008 | 22 | 22 | 0 | 17 | 0 | 5 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/BusinessRoot/ArtifactParser.lean` | `5f12a8c5676d96b58591bde49b689ab464d30d26` | 9636 | 17 | 17 | 0 | 4 | 0 | 9 | 0 | 4 |  |
| `proofs/lean/juris_lean/JurisLean/BusinessRoot/GuardMachine.lean` | `c8cacc77dd3237e54b68a4acd5341a5f3170c7cc` | 3863 | 7 | 7 | 0 | 3 | 0 | 3 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/BusinessRoot/InputCodec.lean` | `4fc8146515e52c46a9b647b0abe34dacb7b4e460` | 3088 | 9 | 9 | 0 | 5 | 0 | 3 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/BusinessRoot/PrincipalChecker.lean` | `c84ed7b9a5da1948ce31a978587eca4df1e204f4` | 4589 | 8 | 8 | 0 | 8 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/BusinessRoot/Root.lean` | `28f52020a4f9d8bbd4cb02b57f60b19c8412f861` | 16720 | 47 | 47 | 0 | 25 | 0 | 19 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/BusinessRoot/RootAudit.lean` | `773f8b0aeeeaa2924f3b271a54b59ea7268d9ece` | 1030 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/BusinessRoot/Semantics.lean` | `8d2699a3b91ecbceffed9b76f3e9df380209e3b4` | 9204 | 25 | 25 | 0 | 0 | 0 | 17 | 0 | 8 |  |
| `proofs/lean/juris_lean/JurisLean/BusinessRoot/SevenAxis.lean` | `0efeae9c5c525ed4abeb42f2c5320f74098d2566` | 16360 | 53 | 53 | 0 | 19 | 0 | 21 | 0 | 13 |  |
| `proofs/lean/juris_lean/JurisLean/BusinessRoot/SevenAxisAudit.lean` | `b250549808593a7ea3c9d23395825bbee22efb82` | 1457 | 1 | 0 | 1 | 0 | 0 | 0 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/BusinessRoot/SevenAxisCases.lean` | `3c1269d9b22f09f515b894e2a780077e9bf81f3a` | 18249 | 34 | 34 | 0 | 32 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Genealogy/All.lean` | `e0048bbb108bbd6f139172c24e3f9e7518638f02` | 478 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Genealogy/Boundary.lean` | `d10d99e56e2344aac85bec3ff6ea356b7ed46182` | 7555 | 24 | 24 | 0 | 5 | 0 | 5 | 0 | 14 |  |
| `proofs/lean/juris_lean/JurisLean/Genealogy/General.lean` | `038632bd716f4c989a58ab77c74c65a39e6816e5` | 16054 | 44 | 44 | 0 | 22 | 0 | 16 | 0 | 6 |  |
| `proofs/lean/juris_lean/JurisLean/Genealogy/Part0.lean` | `efc7bb01da90cb3f234c38fc75fcc871d8ee4a39` | 6882 | 37 | 37 | 0 | 12 | 0 | 14 | 0 | 11 |  |
| `proofs/lean/juris_lean/JurisLean/Genealogy/Part1.lean` | `0f36d2720fcc1af038a883af1dd775756d9afc60` | 9413 | 38 | 38 | 0 | 17 | 0 | 10 | 0 | 11 |  |
| `proofs/lean/juris_lean/JurisLean/Genealogy/Part2.lean` | `3cb7de5e4bec4373a1f1b6575ac912d8e977a63d` | 4179 | 21 | 21 | 0 | 9 | 0 | 6 | 0 | 6 |  |
| `proofs/lean/juris_lean/JurisLean/Genealogy/Part3.lean` | `0901a3981611094e89bd919dc6de2c6e6b5dfdab` | 8005 | 42 | 42 | 0 | 18 | 0 | 13 | 0 | 11 |  |
| `proofs/lean/juris_lean/JurisLean/Genealogy/Part4.lean` | `10661c5bb3af1f6b59dae1d6388ca1aeb830b90b` | 20258 | 96 | 96 | 0 | 40 | 0 | 26 | 0 | 30 |  |
| `proofs/lean/juris_lean/JurisLean/Genealogy/Part5.lean` | `62d4e1f42826c970ced278d80739b9ad4006ee7c` | 10138 | 47 | 47 | 0 | 23 | 0 | 16 | 0 | 8 |  |
| `proofs/lean/juris_lean/JurisLean/Genealogy/Part6.lean` | `5bee2ba9332740c13ba1c092aeb6a9d088e3ee04` | 12031 | 59 | 59 | 0 | 23 | 0 | 21 | 0 | 15 |  |
| `proofs/lean/juris_lean/JurisLean/Genealogy/TSpectrum/Batch1.lean` | `b8df48fbcd56b3bfbee708e4b93446188d451bf1` | 37162 | 94 | 93 | 1 | 21 | 0 | 35 | 0 | 38 |  |
| `proofs/lean/juris_lean/JurisLean/Genealogy/TSpectrum/Batch2.lean` | `7a9df7cbec9c4eb1d34db31d1ebf67131c1d2008` | 37996 | 83 | 83 | 0 | 23 | 0 | 31 | 0 | 29 |  |
| `proofs/lean/juris_lean/JurisLean/Genealogy/TSpectrum/Batch3.lean` | `f3ea591c9f1f54196236593df39ae83d67eccccc` | 10057 | 59 | 59 | 0 | 20 | 0 | 21 | 0 | 18 |  |
| `proofs/lean/juris_lean/JurisLean/Genealogy/TSpectrum/Batch4.lean` | `3c3d8244d886210039a0b3ffe9635757de8a84cd` | 19550 | 137 | 137 | 0 | 67 | 0 | 3 | 0 | 67 |  |
| `proofs/lean/juris_lean/JurisLean/Review20261110/BusinessTransport.lean` | `10d56d1376a128f5b788253f22b7016d6e43d661` | 10553 | 23 | 19 | 4 | 13 | 0 | 5 | 4 | 1 |  |

## G12_unified_v2　统一模型与内核

- 分组依据：Unified model v2 / v21 modules.
- 文件数：19
- 词法声明次数：287（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/ClosedLoopKernel.lean` | `3e7cf4b87a79e5574df21f6aeb27ff9817a9382c` | 14500 | 55 | 55 | 0 | 23 | 6 | 15 | 9 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/KernelV3.lean` | `e893962ffff24dc645a63ff0b247c72058cb9030` | 9209 | 37 | 37 | 0 | 14 | 0 | 8 | 0 | 15 |  |
| `proofs/lean/juris_lean/JurisLean/OriginalModelClosure.lean` | `324578c3212b1a043f662585e5932d51aa966f64` | 7712 | 13 | 9 | 4 | 4 | 0 | 5 | 4 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/UnifiedChainAudit.lean` | `15f13a2a2c36bde2508144fd9e1a0ba96d61ff41` | 6081 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/UnifiedFeedbackBridge.lean` | `c2a845d53e06221f5e0093358f3fe5db7fa00f5f` | 13175 | 37 | 37 | 0 | 11 | 12 | 8 | 5 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/UnifiedModel.lean` | `e916b5f9366a7cd17c2ccfb8fb1105b25b643335` | 14859 | 38 | 35 | 3 | 11 | 5 | 13 | 3 | 6 |  |
| `proofs/lean/juris_lean/JurisLean/UnifiedV2/All.lean` | `d22aca510a211628d87c3282cf0c3886605ebec9` | 119 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/UnifiedV2/Audit.lean` | `62c5216f1d2db340d9ad1f68174a9d8c836f2aae` | 2427 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/UnifiedV2/Composition.lean` | `69eabe8db6c101f82a9bf1f22f8311e2b61a758d` | 2688 | 5 | 5 | 0 | 3 | 0 | 1 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/UnifiedV2/ConcreteBridge.lean` | `6120f69f7b17b6879bf1cbe41bfd048986b938fa` | 3243 | 12 | 12 | 0 | 6 | 0 | 6 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/UnifiedV2/FiniteContract.lean` | `6e5bbc3a7618be721f9f789637b49eb4b16e1717` | 4645 | 18 | 18 | 0 | 11 | 0 | 6 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/UnifiedV2/LegalInterfaces.lean` | `708fe960a11234b7c00a6217bc0f23474f332bad` | 2232 | 13 | 13 | 0 | 6 | 0 | 3 | 0 | 4 |  |
| `proofs/lean/juris_lean/JurisLean/UnifiedV2/Quantified.lean` | `16492169fc182f9743bab062f0804f5d451121ba` | 3543 | 18 | 18 | 0 | 14 | 0 | 4 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/UnifiedV21/All.lean` | `3478e49206a94975e8989c26130f29c365bd2933` | 189 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/UnifiedV21/Audit.lean` | `c433de24fd9eaf1d7dbe7ed509a68801420d6dc3` | 1002 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/UnifiedV21/Authority.lean` | `762971717ef13f3f89e58a7f830da530dfcbf0a4` | 1485 | 6 | 6 | 0 | 3 | 0 | 1 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/UnifiedV21/ConcreteRoot.lean` | `576a0779cfee03746e31a50fbdb48380c7b83c3d` | 4665 | 19 | 19 | 0 | 8 | 0 | 10 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/UnifiedV21/Context.lean` | `a03b322740f6ecc046b97332f01cf97d033b1ffb` | 1598 | 6 | 6 | 0 | 4 | 0 | 1 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/UnifiedV21/Representation.lean` | `db5da77603c6777201f87b3fdb816e61220ae0fd` | 2455 | 10 | 10 | 0 | 5 | 0 | 3 | 0 | 2 |  |

## G13_candidates　Candidates 候选波次

- 分组依据：Dated candidate modules; treat as candidate formalizations, not automatically as mainline.
- 文件数：234
- 词法声明次数：3485（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/Candidates/AdaptiveRoundLedger20261027.lean` | `2c166e51169957e1ec65f16c39ca4bec7ed8ae30` | 18250 | 37 | 37 | 0 | 15 | 0 | 12 | 0 | 10 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/AdaptiveRoundLedgerAudit20261027.lean` | `813bae8f408bfaba8ddaaac135deac128c531b03` | 13165 | 8 | 8 | 0 | 0 | 0 | 8 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/AdaptiveValidation20261027.lean` | `d9a4211c36d139f6a2dd3765cc462120682b4915` | 13862 | 18 | 18 | 0 | 12 | 0 | 6 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/AdaptiveValidationAudit20261027.lean` | `987d7ff96f229a2feef877bd34e6039095ccdfd2` | 3208 | 1 | 1 | 0 | 0 | 0 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/AuthorizationClosureAudit20261104.lean` | `83e3689d8dc80aef2c6ed2ec72f08d8783bd1741` | 30990 | 84 | 83 | 1 | 27 | 0 | 49 | 0 | 8 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/BernoulliMeanInstance20261031.lean` | `f15cbdb6328d63b3ae68fcbe58a493cabaa51ef7` | 3380 | 8 | 7 | 1 | 5 | 0 | 2 | 1 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/BetaEnclosureInstance20261031.lean` | `541c080e83c6fcc578ca5d0211c68cb540e3fcc1` | 3674 | 3 | 3 | 0 | 2 | 0 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/BetaFutureSampling20261031.lean` | `913213e54776d0c8a75d8b75343fa00362b77d53` | 23013 | 37 | 36 | 1 | 22 | 0 | 9 | 6 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/BusinessFeedbackLoop20261027.lean` | `540661500942f0530f32cbbabcecfadba6f3f67e` | 26313 | 48 | 48 | 0 | 23 | 0 | 16 | 0 | 9 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/BusinessFeedbackLoopAudit20261027.lean` | `18da62e4d25e699cd166704d50a639f06b2426d5` | 24898 | 16 | 16 | 0 | 0 | 0 | 16 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/BusinessMeasurement20261027.lean` | `c01ef9cc49e9792386f629453f14562f90f8dd0c` | 17122 | 33 | 33 | 0 | 14 | 0 | 9 | 0 | 10 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/BusinessMeasurementAudit20261027.lean` | `2c887adfc5938fb22ce98b7e4d75bdf9e853212f` | 8763 | 11 | 11 | 0 | 0 | 0 | 11 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/CalibrationSemantics20261027.lean` | `45d0e08c6f153a302e9c9a023224a97c94640dda` | 7669 | 14 | 14 | 0 | 8 | 0 | 6 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/CalibrationSemanticsAudit20261027.lean` | `e3f764d97dc9cb2019a1fb68b20256ca76ab826b` | 2290 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/CausalSelection20261027.lean` | `b6bbfdaf70c1b945d5d0731308655adac3c91535` | 14939 | 40 | 40 | 0 | 13 | 0 | 24 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/CausalSelectionAudit20261027.lean` | `01d39d30c4d7cfcf6b5568f0d2acddcd478f5c14` | 4838 | 5 | 5 | 0 | 0 | 0 | 5 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/CommitReadback20261027.lean` | `a850d7f0b1011572a62279868992bde69e06b9c5` | 6450 | 8 | 8 | 0 | 4 | 0 | 2 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/CommitRecovery20261027.lean` | `3dfc870cba101ab0adc80b00de6ec641cb7432b0` | 14802 | 17 | 17 | 0 | 10 | 0 | 5 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/CommitRecoveryAudit20261027.lean` | `86129576e067ebaade3a2b6229643285b96941f4` | 15877 | 9 | 8 | 1 | 0 | 0 | 9 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/CompilerClosure20261026.lean` | `5c08ccb106cec36e9dbdd3bd56d42b6b5866bfd7` | 11140 | 19 | 19 | 0 | 17 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/CompilerOriginalBoundaries20261031.lean` | `d103813adb826581ead659dedfcc4fce00c69003` | 4358 | 10 | 10 | 0 | 3 | 0 | 7 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/CompilerOriginalBoundariesAudit20261031.lean` | `f5317adb77b862d430b583150cac19d5330e8a98` | 786 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/CompilerProvenance20261027.lean` | `297d4fc111a9fd0720bdd28b57b95e002a32af7a` | 19515 | 29 | 29 | 0 | 16 | 0 | 9 | 0 | 4 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/CurrentContextRollback20261027.lean` | `f777fafeec161379d880de8d5569351581738d5b` | 11051 | 14 | 14 | 0 | 9 | 0 | 4 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/CurrentContextRollbackAudit20261027.lean` | `c43e88fd257a6fefb894c68126af3f2a700e427f` | 7699 | 7 | 7 | 0 | 0 | 0 | 7 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/DecisionTrajectoryConsumer20261027.lean` | `9c4bc3505754034cf05c4ed9d37555bd35005075` | 19755 | 20 | 20 | 0 | 12 | 0 | 6 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/DecisionTrajectoryConsumerAudit20261027.lean` | `6cc68dd26bc50a670c105797a607d4db1be504c2` | 12401 | 16 | 16 | 0 | 0 | 0 | 16 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/EquicorrelatedMean20261030.lean` | `72ed0d3a41106e8fe77f91f996aaa2bf5f361da5` | 7534 | 3 | 3 | 0 | 3 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/EventFeedbackConsumer20261027.lean` | `0a63d7ee7c5140fcc2a27af85355051febe93af2` | 17877 | 52 | 52 | 0 | 15 | 0 | 22 | 0 | 15 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/EventFeedbackConsumerAudit20261027.lean` | `8dc73c76412695875b78182813a6807a7027810b` | 10538 | 13 | 13 | 0 | 0 | 0 | 13 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/EvidenceWorlds20261027.lean` | `d86610db853c322a48ca66529e96146becdf8ae7` | 9807 | 23 | 23 | 0 | 14 | 0 | 8 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/EvidenceWorldsAudit20261027.lean` | `635aff005fdb53fd7088b54e0e69abb8a907df2f` | 9636 | 12 | 12 | 0 | 6 | 0 | 6 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/ExactProbability20261027.lean` | `838fb9669826396357d90ca42cd54a66abd263b2` | 9114 | 14 | 14 | 0 | 11 | 0 | 3 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/ExactProbabilityAudit20261027.lean` | `1e1305eca0c3fb95ab57f2db3ba133d29de05e7a` | 2162 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/ExchangeableRank20261031.lean` | `af967506262f770bbc16053aa8d5ce83dd81e655` | 41352 | 69 | 69 | 0 | 5 | 40 | 20 | 4 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/FeedbackLabelSemantics20261027.lean` | `aeda89c70181043fbe3a90f4b567014917a39d5b` | 13081 | 22 | 22 | 0 | 13 | 0 | 8 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/FeedbackLabelSemanticsAudit20261027.lean` | `e1e0384ec64e40aad74d21d3a2dd0c3ea033ca53` | 3308 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/Acceptance.lean` | `52c751a746e8a08c67f22f035abe28366f2a40a8` | 20327 | 94 | 94 | 0 | 62 | 0 | 32 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/Authorization.lean` | `0f218e3292f53c2cd2a23e4ed19195272d32ea6c` | 2774 | 9 | 9 | 0 | 1 | 0 | 6 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/AxiomAudit.lean` | `6c8afdec64c2e1a37baba22b18b2c757cfa17198` | 43514 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/Behavior.lean` | `f3f72145e8acdbf73e0302a9ce0fdbf425b312cd` | 2469 | 12 | 12 | 0 | 3 | 0 | 7 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/CIAll.lean` | `0cad535fe39d2ea2921d613c097f1adada9d2874` | 1197 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/Calibration.lean` | `9ee36840a26c87dd4ace011051fd11a735011b1b` | 4087 | 12 | 12 | 0 | 9 | 0 | 2 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/Compiler.lean` | `5068dc7b66c8eefbdba821830e873ff9ebc2774a` | 6847 | 19 | 19 | 0 | 10 | 0 | 6 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/Decision.lean` | `698e40b8cb26c4880f81c0d4018e5d539d3efb82` | 11062 | 35 | 35 | 0 | 17 | 0 | 12 | 0 | 6 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/EvidenceProcedure.lean` | `694be6d8c778c7ebf6e049823fcf249695532f42` | 3719 | 17 | 17 | 0 | 4 | 0 | 10 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/Feedback.lean` | `e527bb5c8b43016ca81ed7de9b7a1b9ba4c9bb0d` | 7276 | 16 | 16 | 0 | 6 | 0 | 3 | 0 | 7 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/Harness.lean` | `1ac61ceb4af81d3fede975e098a00f802e8aa040` | 5168 | 14 | 14 | 0 | 9 | 0 | 5 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/Interfaces.lean` | `8e7c3b357a4aacbe0d3ba2d1af6fcac717857839` | 5158 | 28 | 28 | 0 | 0 | 0 | 0 | 0 | 28 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/Iteration.lean` | `7668283ed14b3f8db7929f300c2eb287f5b80ca1` | 2066 | 7 | 7 | 0 | 4 | 0 | 2 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/Learning.lean` | `de5e437895b18977a066d70a0cbdc7a6b5e02cfd` | 9314 | 19 | 19 | 0 | 15 | 0 | 3 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/Ledger.lean` | `1a2632047bf0ee7f8f6fc8c32a85e601514f2d64` | 30850 | 71 | 71 | 0 | 36 | 0 | 28 | 0 | 7 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/Pipeline.lean` | `33816dfd39dae9e22ff2981113e7c4ef04caa75f` | 14906 | 19 | 19 | 0 | 5 | 0 | 9 | 0 | 5 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/Policy.lean` | `d54891a5c722214be2c4b30033ea69e3aa121dd6` | 3091 | 7 | 7 | 0 | 5 | 0 | 1 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/Probability.lean` | `4bf501776139af88b82f424526a8984a756bd092` | 10534 | 30 | 30 | 0 | 22 | 0 | 5 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/Progress.lean` | `d8e039d26c163691dd13385d58f93d2d875351e5` | 1214 | 5 | 5 | 0 | 4 | 0 | 0 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/RSI.lean` | `b0239a3cb86b91153dc1ec45f228e648f52e6aab` | 4175 | 17 | 17 | 0 | 6 | 0 | 7 | 0 | 4 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/Representation.lean` | `57e3770af97ac8361c36c35e08959c55fbe1299c` | 4327 | 17 | 17 | 0 | 8 | 0 | 6 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/Temporal.lean` | `dfca2f35a7cee919ff7d5813f9dc19f0bde2b935` | 3205 | 10 | 10 | 0 | 3 | 0 | 6 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/Trace.lean` | `4fe47a0b6e0364dc1753da5aed252718580d817e` | 8889 | 14 | 14 | 0 | 9 | 0 | 3 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Final20261021/Transactions.lean` | `3347aaae3e87c1238af682c10f285490fe994ea1` | 11334 | 29 | 29 | 0 | 19 | 0 | 5 | 0 | 5 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/FinalizeReadClosureAudit20261105.lean` | `9dc9eea511681e7ef80c4b045266f366bc70cb75` | 18953 | 40 | 40 | 0 | 12 | 0 | 28 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/FiniteLegalValidation20261027.lean` | `a3876253a1da37cb4a1f7b7b5d657ed025adf767` | 34408 | 66 | 66 | 0 | 30 | 0 | 28 | 0 | 8 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/FiniteLegalValidationAudit20261027.lean` | `cf5c4901f2e51f7ebae9c2692e06f6f85c1623d0` | 21206 | 19 | 19 | 0 | 3 | 0 | 16 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/FiniteTraceInvariantAudit20261105.lean` | `ef95e20f35bd46417678ae05dced5cfd48bba174` | 9777 | 15 | 15 | 0 | 9 | 0 | 6 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/FixedDriverSeparationAudit20261105.lean` | `f731e5f25a935ba3f1550e97b086a60bd0b2013c` | 3799 | 7 | 7 | 0 | 2 | 0 | 2 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/FormalTail20261024.lean` | `2948013348c3cb909b3c18dcc914f0b3cb9846b0` | 61155 | 137 | 137 | 0 | 69 | 5 | 58 | 0 | 5 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/FormalTailCAND8AxiomAudit20261027.lean` | `084b6596bfd8d1cb7962cc53b96ba170d10225f2` | 14131 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/GroupedConformalInstance20261031.lean` | `38470671dd4363bc767782d55d4c7414c75ab05a` | 2230 | 1 | 1 | 0 | 1 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/HarnessOriginalInstances20261031.lean` | `983366d90f375bdb536e9d9e6e94a19c6734aa77` | 7642 | 16 | 16 | 0 | 5 | 0 | 11 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/HarnessOriginalInstancesAudit20261031.lean` | `6109ec6e19a598358b4b8503e339ea31a8c92c29` | 1545 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/HarnessRisk20261027.lean` | `1d7ca00ccd03fe8d0d23c9b790b734d89d063643` | 11939 | 23 | 22 | 1 | 15 | 0 | 6 | 2 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/HarnessRiskAudit20261027.lean` | `a48c98905705df07a1ce7a50fd034a173e8b0c76` | 4648 | 2 | 2 | 0 | 2 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/HistoricalRevocationClosureAudit20261105.lean` | `6632e9ab0b1ce9145f567f9b153c32d686148946` | 13347 | 39 | 39 | 0 | 10 | 0 | 28 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/IntervalDecisionConsumer20261027.lean` | `41c2317d2e56ad0fbbbe500c183c70eb182fa04f` | 18872 | 20 | 20 | 0 | 10 | 0 | 7 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/IntervalDecisionConsumerAudit20261027.lean` | `c1731dccbfb5cfbac028ad248981a9645d502bee` | 6519 | 6 | 6 | 0 | 0 | 0 | 6 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/LearningBoundary20261027.lean` | `0bb0b16fe8bb19a25c524f2a238425d7dc8e78c5` | 3998 | 12 | 12 | 0 | 7 | 0 | 5 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/LearningBoundaryAudit20261027.lean` | `4182b0e1c2bcb97fc48c43d3d9842dc800a5c284` | 1047 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/LearningBridge20261027.lean` | `228e5a363d74c1156ede8e7d62ebc26658497dba` | 9679 | 9 | 9 | 0 | 8 | 0 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/LearningConsumer20261027.lean` | `f40fd915f991ebcecce5176589f6ba5e47c17c96` | 10049 | 16 | 16 | 0 | 8 | 0 | 4 | 0 | 4 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/LearningConsumerAudit20261027.lean` | `14de6490b4f4530d53d339825f33a64170f2ef67` | 2679 | 3 | 3 | 0 | 0 | 0 | 3 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/LearningDependence20261027.lean` | `23c8b659f6737aaaf3be1a000b98bb476ede7ae7` | 6325 | 10 | 9 | 1 | 7 | 0 | 2 | 1 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/LearningERM20261027.lean` | `796111a2a7f5b78ae20e8cb62938681f847f72de` | 9978 | 12 | 12 | 0 | 8 | 0 | 4 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/LearningERMAudit20261027.lean` | `e1564ea676076c4e2de4d7adf289ef7c54e67f8f` | 1402 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/LearningEventSplit20261027.lean` | `a6a7604fd453ac1f54a0687473586f2d421667c0` | 4192 | 11 | 11 | 0 | 6 | 0 | 4 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/LearningEventSplitAudit20261027.lean` | `7df80cdc114e05c16bb7b14d864b2790a14cdd5e` | 1740 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/LearningFiniteClass20261027.lean` | `61fd14d9a69cadb2dac803f056b97a7fc0dd2fbc` | 11418 | 7 | 7 | 0 | 5 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/LearningProvenanceAudit20261027.lean` | `817729121a40d7b8aba5d5eacf4a1f57ded1cdd8` | 2969 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/LearningRisk20261027.lean` | `f9985642bbce53054f4ebafb83f4a2b0327019c1` | 8540 | 15 | 15 | 0 | 10 | 0 | 5 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/LearningSplit20261027.lean` | `48dcb27e302b5dd6da57e54a7d6be2683a9b90f9` | 10658 | 31 | 31 | 0 | 18 | 0 | 11 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/LearningSplitAudit20261027.lean` | `d82ed519742d812e1501db9c43b39e7eeefc7ff4` | 3635 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/LearningTheoryAudit20261027.lean` | `0b5d44a217d3b26e67c26b63419828a8dce64f0b` | 2707 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/LegalActionDomain20261027.lean` | `4fec4510a20e185dd1ac205f509255e4fd94b5c2` | 23815 | 39 | 39 | 0 | 17 | 0 | 15 | 0 | 7 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/LegalActionDomainAudit20261027.lean` | `c1ebc34fa0951d69bfe36064a045e18223b6bf12` | 17162 | 17 | 17 | 0 | 5 | 0 | 12 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/LoadedLegalConsumer20261027.lean` | `f36cc9b5efad66fb472e3c1fd98b258bd363d45d` | 22148 | 21 | 21 | 0 | 12 | 0 | 7 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/LoadedLegalConsumerAudit20261027.lean` | `ef291424d6a784b54e44407208b407e6a906a262` | 16878 | 12 | 12 | 0 | 0 | 0 | 12 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/MeasuredPolicy20261027.lean` | `b5dd2e5ea9073ef01ed36e2eef3805a3cbc8e169` | 23580 | 35 | 35 | 0 | 11 | 0 | 14 | 0 | 10 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/MeasuredPolicyAudit20261027.lean` | `9bbadcd86ece738ab02e1a49c4973c63a850e01a` | 8919 | 11 | 11 | 0 | 0 | 0 | 11 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/MeasurementLikelihood20261027.lean` | `e5d37c165ac8ed6725c2ebc1427f5960f483b67e` | 4497 | 8 | 8 | 0 | 7 | 0 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/MeasurementLikelihoodAudit20261027.lean` | `9856f80483d784652f2058fa32ff9d38e392a81a` | 1920 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/Original07_3RowInterpretation20261102.lean` | `2b5d659d1d26a54e4bf6a6705c6dc486ca6e273a` | 4679 | 7 | 7 | 0 | 2 | 0 | 3 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Original07_3RowInterpretationAudit20261102.lean` | `9f4e774927ac86a9776263f2d74549c734cf41d7` | 289 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/Original07_4ObservationInstance20261102.lean` | `780400e74d5d2c270fb1ac08f0e4f6003289ad7c` | 3271 | 10 | 10 | 0 | 1 | 0 | 4 | 0 | 5 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/Original07_4ObservationInstanceAudit20261102.lean` | `638c3819200711964c6ae98ccc3dc755653fe997` | 2782 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/ParametricAllocationAudit20261104.lean` | `3a59d16acd3e8c79cb4a3f5efeb1a54d309fe725` | 13539 | 24 | 24 | 0 | 5 | 0 | 7 | 0 | 12 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/PartialStepGateAudit20261105.lean` | `22f4570d1d384dd144521e8237a9be83c86054c8` | 13825 | 27 | 27 | 0 | 7 | 0 | 19 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/PendingCommit20261027.lean` | `a3f1511f12e94d5c925b1719a8436e3e9e2b9a1e` | 9648 | 7 | 7 | 0 | 4 | 0 | 2 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/PolicyEvaluation20261027.lean` | `0cde74741de7d516fee6264f680dc80749f5dc1d` | 16674 | 35 | 35 | 0 | 16 | 0 | 19 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/PolicyEvaluationAudit20261027.lean` | `9d4c4bac7d32530af070c71457f092700e0c2830` | 4603 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/PolicyPredictionBoundary20261106.lean` | `bc78e3320b2f2a697f9050beed03e041909c80c7` | 1482 | 1 | 1 | 0 | 1 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/PolicyResponse20261027.lean` | `d96e63a9ba60fc8a089c815417c36c3b2cc2cf78` | 10696 | 27 | 27 | 0 | 17 | 0 | 10 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/PolicyResponseAudit20261027.lean` | `bf575e6bcb99b004bf7ff76c900c1f4265bcc691` | 3965 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/ProbabilityIntervalConsumer20261027.lean` | `58b9d0dc1c1694b11f2b8014e019be7b88b53e60` | 17981 | 18 | 18 | 0 | 9 | 0 | 8 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/ProbabilityIntervalConsumerAudit20261027.lean` | `8b213cd9a3b005fcc2d84c3f4c7b0479bd233159` | 5370 | 5 | 5 | 0 | 0 | 0 | 5 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/ProcedureClosure20261027.lean` | `df075e11163f7ae8b09fc09ea464832a2f14e078` | 8470 | 21 | 21 | 0 | 14 | 0 | 7 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/ProcedureClosureAudit20261027.lean` | `033d14ad6edf9e8057c5217db633e6131cf6e47d` | 9970 | 14 | 14 | 0 | 6 | 0 | 8 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/ProtectedFeedback20261027.lean` | `f1792782e9617947ab714eb9baf0b4a621d5b560` | 23383 | 29 | 29 | 0 | 12 | 0 | 13 | 0 | 4 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/ProtectedFeedbackAudit20261027.lean` | `05f5535843be026f4e9ab48f7b65484bbab0bd46` | 9913 | 14 | 14 | 0 | 0 | 0 | 14 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/ProtocolDependencyAudit20261105.lean` | `68d124df431e5391f3f601a97e345e703e3e1849` | 6565 | 2 | 2 | 0 | 2 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/RSIAdmittedStatistics20261106.lean` | `e0268ccf9b1ef7c139d3905e89e9fb81d810811e` | 2506 | 7 | 7 | 0 | 1 | 0 | 6 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/RSIScopedCondition20261106.lean` | `59762d5a5e2110a02a7ec8dcf660457c49090547` | 2314 | 6 | 6 | 0 | 1 | 0 | 3 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/RepresentationRefinementAudit20261105.lean` | `9f1a62e7db5a7cc6640bbc789fbe1cf0c69c1b5b` | 18986 | 25 | 25 | 0 | 13 | 0 | 9 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/RestitutionFiniteClosureAudit20261104.lean` | `8b6826241eba8bf385e1e96b7cccb25556f3b5c0` | 27323 | 58 | 58 | 0 | 21 | 0 | 32 | 0 | 5 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SampleCalibrationConsumer20261027.lean` | `8cdf3df1894294db5fdab81ac5ccb9f26cfbfc28` | 29915 | 22 | 22 | 0 | 10 | 0 | 10 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SampleCalibrationConsumerAudit20261027.lean` | `c131b3eb96690ed979910a05a641a095147a9b00` | 5340 | 5 | 5 | 0 | 0 | 0 | 5 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SelectiveCalibration20261027.lean` | `100a13a2ac6ae1e9b373e56e91a8451059a7c785` | 14876 | 15 | 15 | 0 | 8 | 0 | 7 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SelectiveCalibrationAudit20261027.lean` | `7704f0b4a3432bccf0051eddbe69d1845318481f` | 2349 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/SemanticIndependenceAudit20261104.lean` | `5c315c548e43164b7d3a016130a41a25ff036f2f` | 9141 | 24 | 24 | 0 | 7 | 0 | 13 | 0 | 4 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SingleDebtStreamAudit20261103.lean` | `f54859db839ef138a2a14aa84a7b024c17e28fe5` | 20310 | 21 | 21 | 0 | 11 | 0 | 10 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SourceAction20261027.lean` | `b0e5366206edaf3475b0b51ad81d9c61aeacdf00` | 13069 | 24 | 24 | 0 | 9 | 0 | 9 | 0 | 6 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SourceActionAudit20261027.lean` | `bdf6b07a1dacc4b91ec5c4910e20a32de637eb24` | 15065 | 13 | 13 | 0 | 0 | 0 | 13 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SourceCompilation20261027.lean` | `4d12fbf0a0c9682383a1a20d2bc98641df76416c` | 15083 | 35 | 35 | 0 | 9 | 0 | 14 | 0 | 12 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SourceCompilationAudit20261027.lean` | `818f7fa0b342ffa98fccc36de57b6d57e8506c74` | 8241 | 12 | 12 | 0 | 0 | 0 | 12 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SourceDependencySnapshotAudit20261103.lean` | `c67eb086492afd6769201e6c43b126f04563f878` | 7543 | 9 | 9 | 0 | 4 | 0 | 3 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SourceFinalBridgeAudit20261102.lean` | `b0072ee5f97ed616bc050687036b392b7c7ad747` | 6444 | 2 | 2 | 0 | 2 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SourceFiniteStageAudit20261102.lean` | `66e9e54b41e23ee0cc9b674277ba72381db00f8c` | 2462 | 1 | 1 | 0 | 1 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SourceHornBoundaryAudit20261103.lean` | `4646028d2d4bc6c27569a85061132d507ec624d4` | 12332 | 13 | 13 | 0 | 2 | 0 | 11 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SourceOpening20261027.lean` | `da449db47193f2425b533491fc38eded123f120e` | 15200 | 22 | 22 | 0 | 11 | 0 | 9 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SourceOpeningAudit20261027.lean` | `73c7b96b59a7780cec9df41a8c938979afa14dda` | 8441 | 6 | 6 | 0 | 0 | 0 | 6 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SourcePaymentIdentityAudit20261103.lean` | `f9fad633ecb4be0fe0123eaad5a4ebdb3faf137d` | 9843 | 3 | 3 | 0 | 2 | 0 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SourcePolicyExhaustionAudit20261103.lean` | `6bdd95aad9b500260f42de0f0c45cd57f3da99c7` | 8142 | 8 | 8 | 0 | 3 | 0 | 4 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SourceRepresentation20261027.lean` | `8663aeeabd8d97542af8a36da92058b369e59418` | 8582 | 28 | 28 | 0 | 17 | 0 | 9 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SourceRepresentationAudit20261027.lean` | `d0adba4ec93f4b8388772adc196deaee3d26f4c4` | 5345 | 2 | 2 | 0 | 0 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SourceStages20261027.lean` | `dbfde3641b97f64dbc119292abbac99b30596207` | 29160 | 51 | 50 | 1 | 26 | 0 | 19 | 1 | 5 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SourceStagesAudit20261027.lean` | `31832cc272b5d80657113d2fc759bf543f4c4836` | 12941 | 11 | 11 | 0 | 2 | 0 | 9 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SourceTemporalBoundaryAudit20261103.lean` | `d43d9b231c33debbd5fca4c07e80386fc83c0c52` | 9158 | 3 | 3 | 0 | 3 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/SourceTemporalIdentityAudit20261103.lean` | `79c14ad2cd719c7df73d5793037c88d0b1dab005` | 6994 | 1 | 1 | 0 | 1 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/TemporalInterpretation20261027.lean` | `2d2104073a7c6c85cf6408080bdf3a866167c45a` | 19018 | 39 | 38 | 1 | 18 | 0 | 17 | 1 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/TemporalInterpretationAudit20261027.lean` | `b68b39006af4701a371f80c0641dcee68b2e4059` | 14711 | 34 | 33 | 1 | 6 | 0 | 26 | 1 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U00ActualAssessmentChoice20261031.lean` | `c526d6f8b90b62a441e51b3e3bcc9b2c8ceb8546` | 13118 | 2 | 2 | 0 | 2 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U00ActualAssessmentChoiceAudit20261031.lean` | `3544bc4487d9cc713161dba6557ebd2f1bca24f9` | 295 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U00ActualSourceProtocol20261031.lean` | `cfa58104baf68c79ab21147efeb003a411f9d793` | 7821 | 4 | 4 | 0 | 2 | 1 | 1 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U00ActualSourceProtocolAudit20261031.lean` | `558d869909e1af0589828b65706fff97df6b2d78` | 1154 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U00ActualStatisticalJoin20261031.lean` | `1f76509e04ba52c5d11e6d2de654b8a1313f13d8` | 14795 | 8 | 8 | 0 | 5 | 0 | 3 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U00ActualStatisticalJoinAudit20261031.lean` | `4322c2e4c6d95eeef501baa8f46eabfe2d9f562d` | 899 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U00MeasuredRSIEntry20261031.lean` | `168bf2944d744f36682af6b4afcc3c4783959a90` | 21622 | 15 | 15 | 0 | 6 | 0 | 7 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U00MeasuredRSIEntryAudit20261031.lean` | `c89227b047e0232e8187ed39e796f4602de49323` | 715 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U00RSICandidateBridge20261031.lean` | `d7ecf6403fa736c3b1a279d42cf0c9f4bcb4e13a` | 24324 | 26 | 26 | 0 | 8 | 0 | 14 | 0 | 4 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U00RSICandidateBridgeAudit20261031.lean` | `1d0537ed648d78a58adef19672b86f1608b5e25b` | 682 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U00RoundPostBridge20261031.lean` | `ba03d32b3b3c05b36f3978d445952fade142b259` | 9806 | 4 | 4 | 0 | 4 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U00RoundPostBridgeAudit20261031.lean` | `c1aa76a669e26d666ada3d29f319f6d65d306937` | 494 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U00SourcePersonalEpisode20261031.lean` | `0cfa43b218f8766bc1bd91bbefab593cc0902990` | 20117 | 14 | 14 | 0 | 5 | 0 | 6 | 0 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U00SourcePersonalEpisodeAudit20261031.lean` | `13a6ba663622252f6c173138993b449e76e90620` | 4501 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U01_4OriginalClosureAudit20261030.lean` | `029fb587146a1b808f8e52e74568136fe4a47128` | 2380 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U02_1ActualPipeline20261029.lean` | `cb85a6b6f8b04607bb78e3f308a3710f134773dd` | 16389 | 9 | 9 | 0 | 4 | 0 | 5 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U02_4ExternalConditionRisk20261030.lean` | `ef1e4edb0eaef17bd8fbf746d8a69e4086eaf5f7` | 9682 | 4 | 4 | 0 | 4 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U02_4OriginalClosureAudit20261030.lean` | `588d46e1a57b1227c538763548a2d049b387ba17` | 1046 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U03DebtClosureAudit20261027.lean` | `07ebfc7c0933b077a272406e9f6e6f65f36c0c83` | 2915 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U04LogisticContract20261101.lean` | `0ab38716d0ae3daebb5a9e1abb2966f602480871` | 11314 | 28 | 28 | 0 | 20 | 0 | 7 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U04LogisticContractAudit20261101.lean` | `f29300d13f0dde6c1c2ad32df9f1f7137ccc0f6e` | 1485 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U04OriginalObservationIdentificationAudit20261101.lean` | `8c29ffd7b688a4cd0cb0186ea296df7cab3fb414` | 3436 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U04_1OriginalClosureAudit20261031.lean` | `990581eecd2cc8dc04f6562dbab60edd9a01e390` | 2891 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U04_1OriginalProbabilityInstances20261101.lean` | `1db74fb5112fef02bfac5303483958976a3eaeb7` | 7390 | 16 | 14 | 2 | 12 | 0 | 2 | 2 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U04_1OriginalProbabilityInstancesAudit20261101.lean` | `719f2c0b41d79b2b2820ff98f5598bdee29afce5` | 909 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U04_2OriginalObservationInstances20261101.lean` | `108256d48109283a0f20797cd24608724262f69e` | 8275 | 12 | 11 | 1 | 9 | 0 | 2 | 1 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U04_2SharpConditioning20261029.lean` | `568170d63e2d93a3739d2c1f1dd277c02580d27a` | 23917 | 30 | 27 | 3 | 17 | 0 | 9 | 4 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U04_4OriginalClosureAudit20261031.lean` | `a7e2c649711fbdc9c39aed48977f0de9d4dabc2d` | 1078 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U04_6OriginalIdentificationInstances20261101.lean` | `26c8a05ed86dd1080402c711531a9a2c675fdb27` | 3493 | 10 | 9 | 1 | 7 | 0 | 2 | 1 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U05_1OriginalCalibrationAudit20261101.lean` | `cf7803c804c26ee350dc961ec1e3a04edcab61d6` | 1199 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U05_1OriginalCalibrationInstances20261101.lean` | `30110df0f587093f92066f4e5929f98ee1d696bd` | 6783 | 8 | 8 | 0 | 6 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U05_1OriginalClosureAudit20261031.lean` | `36f252f36da01ce55460d6ddebab0a3f626e214c` | 1451 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U05_2OriginalGroupCalibrationAudit20261101.lean` | `5f6d10982c5ce29ee7f0acb894f9e8760db6cbd8` | 1039 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U05_2OriginalGroupCalibrationInstances20261101.lean` | `4e0af0ec75eafd4bb9d937faf9331c7f1ca27a85` | 9892 | 7 | 7 | 0 | 5 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U05_3OriginalSelectiveRiskAudit20261101.lean` | `1c4143bb113c1dbb4749622534ce73aaf1862492` | 1170 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U05_3OriginalSelectiveRiskInstances20261101.lean` | `366c30071e2d466a3717a833a07787b1f24f6621` | 19317 | 13 | 13 | 0 | 9 | 0 | 4 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U05_5OriginalShiftAudit20261101.lean` | `20c1c5cdf885156a4b48c55353813895534ff329` | 914 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U05_5OriginalShiftInstances20261101.lean` | `cb5031dd5d9038de4b85ca1da1dfdeb2eb240506` | 9583 | 7 | 6 | 1 | 4 | 0 | 2 | 1 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U05_6OriginalMonitoringAudit20261101.lean` | `9db0b6cbc20c35130d795697f0762384001b6d32` | 1584 | 1 | 0 | 1 | 0 | 0 | 0 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U06_1FiniteBellman20261030.lean` | `56d9895cd8bb9aacb9868185fb86561939f2ee45` | 17710 | 27 | 27 | 0 | 13 | 0 | 10 | 1 | 3 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U06_1OriginalCashIdentityAudit20261101.lean` | `7a14983a4e33a4408ba1e86255141d1ed627a024` | 1805 | 1 | 0 | 1 | 0 | 0 | 0 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U06_1OriginalCashIdentityInstances20261101.lean` | `e51614b5095d8ba4acc764bbf1829e41620ad3a7` | 21255 | 36 | 35 | 1 | 15 | 0 | 19 | 1 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U06_2EquilibriumTransfer20261030.lean` | `6dfdc56ff31d25bc3e16749ba31bfa9224916381` | 35711 | 66 | 66 | 0 | 30 | 0 | 27 | 2 | 7 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U06_2OriginalExpectedUtilityAudit20261101.lean` | `e56228790b639baf135bf0332a1235b3d881e028` | 1486 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U06_2OriginalExpectedUtilityInstances20261101.lean` | `f28391db575a975440b545911d49c6334242e78c` | 12118 | 13 | 11 | 2 | 10 | 0 | 1 | 2 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U06_3OriginalCommonRobustStrategy20261102.lean` | `bc33026b38402ebcf134f1c22ddab8e944879ab0` | 25910 | 58 | 55 | 3 | 24 | 0 | 25 | 3 | 6 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U06_3OriginalStrategyAudit20261102.lean` | `5f79297dafbbc328a0a649bdcbfd885997e3b96b` | 6647 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U06_4ConditionalInformation20261031.lean` | `9876be79ca5c2c907d34d8417fd31bdc38e1ecba` | 11622 | 21 | 21 | 0 | 14 | 0 | 7 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U06_4ConditionalInformationAudit20261031.lean` | `c952144a84cc8df1805425384d1b91a7bd45c941` | 485 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U06_5FiniteObservationInstance20261031.lean` | `bc4efe80213dcb8eb53bfdc3c10600c7ab2a3d0b` | 13257 | 28 | 28 | 0 | 3 | 13 | 10 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U06_5FiniteObservationInstanceAudit20261031.lean` | `0afc525904493ca7229636f2247c5e290c8323a9` | 736 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U06_5OriginalClosureAudit20261031.lean` | `8c4334e39fe1373d36747896342856f3412e51ca` | 764 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U06_5OriginalModels20261031.lean` | `8c0463111dda39a51f6a1416bdacf584fc900aab` | 12472 | 29 | 28 | 1 | 3 | 15 | 10 | 1 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U06_6OriginalRiskEvaluation20261102.lean` | `93749f53a981d096670eeee2532cb53684c7f00d` | 20065 | 38 | 35 | 3 | 21 | 0 | 12 | 3 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U06_6OriginalRiskEvaluationAudit20261102.lean` | `6557a43c618800f96464b2b55a042c2197007ca9` | 3013 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U06_7OriginalCashBargainBridge20261102.lean` | `e1cc96143425dca7b71e1595e3a491c48e799e3f` | 6506 | 15 | 14 | 1 | 3 | 0 | 11 | 1 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U06_7OriginalChapterAudit20261102.lean` | `cb3336c14a58d15893579733aacee461139149bc` | 4029 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U06_OriginalFiniteExamples20261031.lean` | `942f6ce76899b3bd0ad830f205ad5c27437669a3` | 8423 | 14 | 13 | 1 | 11 | 0 | 2 | 1 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U06_OriginalFiniteExamplesAudit20261031.lean` | `e2c62f9435dff7dd20a8003824fd7ea319dc41a5` | 3034 | 1 | 0 | 1 | 0 | 0 | 0 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U07_2JointObject20261029.lean` | `2d595c0978adb0c1f8c9ae64e093081e213e4b5d` | 6542 | 5 | 5 | 0 | 1 | 0 | 3 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U07_3FixedBindingAudit20261029.lean` | `a879591dc7c67d8bd22caeae9c62dc08a5dedf4a` | 20285 | 8 | 8 | 0 | 6 | 0 | 2 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U09_2OriginalClosureAudit20261030.lean` | `2f92f90bd411b31d2a1bf4ad5e04e3cde8969d13` | 413 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U10_1DebtClosureAudit20261030.lean` | `9b5fc10ca457e0a27f5ff59e7a842c99443f11a7` | 2105 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U10_1RefreshRuleProtocol20261030.lean` | `084765f0ccd07686925599f350c7980807f5da4d` | 32271 | 21 | 21 | 0 | 12 | 0 | 7 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U11_1DebtClosureAudit20261030.lean` | `aae5c1d7776060b8ff04435242a1c2c77e42d66c` | 8128 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U11_1NamedCausalBridge20261030.lean` | `e5e49cb60e7cb9a7bdb75584b4528f91bbc8dd10` | 16645 | 16 | 16 | 0 | 8 | 0 | 8 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U11_1OriginalInstances20261030.lean` | `76502e19c94977cc042b2417d7fef30d91859cf1` | 6644 | 8 | 8 | 0 | 5 | 0 | 3 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U12_1CausalPolicyBridge20261030.lean` | `95e95e5a6ef63aeabd6e67e61e852207ac919609` | 32672 | 24 | 24 | 0 | 14 | 0 | 8 | 1 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U12_1DebtClosureAudit20261030.lean` | `fd9f8ba98b6f6f4be305bda1b986d7a3f80cf321` | 4771 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U12_1OriginalInstances20261030.lean` | `ba4a3fc1826c66947204011721bea84e5c91269b` | 2363 | 3 | 3 | 0 | 3 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U12_3MARSequential20261030.lean` | `ed53a76de1d0b5e9c1c7bdb76a2c22d94d09be2a` | 12222 | 19 | 19 | 0 | 9 | 0 | 8 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U12_3MeasuredPolicyBridge20261030.lean` | `7d263d210ea0ad1fefc6e74c5257bd2258b66c75` | 23606 | 13 | 13 | 0 | 10 | 0 | 3 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U12_3PolicyLearningAudit20261030.lean` | `6321266a223513a5511e07d26ca25f7dd42d1bac` | 7740 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U12_3SequentialFinite20261030.lean` | `672a71bd2394d4547679d3aa70d3278d62d4cdf6` | 9339 | 13 | 13 | 0 | 5 | 0 | 7 | 1 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U12_4FrozenAuditModel20261029.lean` | `b9a76d478e83e29c3cdc2dcb06232a3a3b53e3c0` | 4942 | 7 | 5 | 2 | 1 | 0 | 4 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U13_3DebtClosureAudit20261028.lean` | `e5aa6fa365420a79b4c617015b1a1c3744f05e1d` | 2988 | 3 | 1 | 2 | 1 | 0 | 0 | 0 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U13_4ColdStartFallback20261030.lean` | `615dd0d966be5801fb490d243307f5b1e24bdbfc` | 26124 | 41 | 41 | 0 | 16 | 0 | 17 | 0 | 8 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U13_4ColdStartFallbackAudit20261030.lean` | `13e87d19d95252952db5c347cda28eada51629ed` | 5503 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U14_1DebtClosureAudit20261028.lean` | `6319d9360bd71c610bf8973c2e7b0477d7281e3a` | 3481 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Candidates/U14_4LearnerProxyWitness20261106.lean` | `ef34da416eeaa4ca49bbb68f611c47768fa0b6f9` | 1903 | 1 | 1 | 0 | 1 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/U15_1IterationBoundaries20261106.lean` | `fa19cfd35d2f71c2cbce91071ec91cfd88db2485` | 3463 | 2 | 2 | 0 | 2 | 0 | 0 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/ValidatedFeedbackLoad20261027.lean` | `748ceaebfb5b119bf8b9c70056df9cdad7dcbb5d` | 13591 | 24 | 24 | 0 | 9 | 0 | 8 | 0 | 7 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/ValidatedFeedbackLoadAudit20261027.lean` | `5f868763b4ffa06f83e832d9661d5cefa28a8f6d` | 10976 | 17 | 16 | 1 | 0 | 0 | 17 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/W6JudgmentCashAudit20261104.lean` | `1da4927e4d5ec77738388ebe600167181bd161c3` | 20586 | 58 | 58 | 0 | 17 | 0 | 32 | 0 | 9 |  |
| `proofs/lean/juris_lean/JurisLean/Candidates/WitnessedCashAllocationAudit20261104.lean` | `25241033f8e5a02af5551cf973fa3931556c57d1` | 14084 | 15 | 15 | 0 | 6 | 0 | 9 | 0 | 0 |  |

## G15_review_20261110　Review20261110

- 分组依据：Review20261110 modules.
- 文件数：6
- 词法声明次数：73（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/Review20261110/Audit.lean` | `09a73c3df0fcc6eda3af7c961295f91b1918a211` | 327 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Review20261110/DelayAugmentation.lean` | `6921d6a40bb534d2f02c41fd8ea159eaccb24e20` | 5114 | 21 | 16 | 5 | 6 | 1 | 7 | 5 | 2 |  |
| `proofs/lean/juris_lean/JurisLean/Review20261110/FeedbackW1.lean` | `a344e1c0a648ac64ae0711461caa64d87d1e3aab` | 7481 | 21 | 21 | 0 | 3 | 9 | 9 | 0 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Review20261110/InvariantClosure.lean` | `4a04188034657fcdf8166576f33fb9e85435f0ec` | 3628 | 8 | 6 | 2 | 4 | 1 | 1 | 2 | 0 |  |
| `proofs/lean/juris_lean/JurisLean/Review20261110/ObservationBridge.lean` | `18f24aee9515c3d7f0294a0072ad6362367f831f` | 3206 | 9 | 9 | 0 | 6 | 0 | 2 | 0 | 1 |  |
| `proofs/lean/juris_lean/JurisLean/Review20261110/OccurrenceHistory.lean` | `2831dddf9c10c26478e00db2a76fa9c95df40da8` | 2824 | 14 | 14 | 0 | 7 | 0 | 5 | 0 | 2 |  |

## G16_consolidated　Consolidated 聚合

- 分组依据：Consolidated aggregation modules.
- 文件数：2
- 词法声明次数：0（非编译器总数）

| 路径 | blob SHA | 字节 | 词法声明 | 具名 | 匿名 | theorem | lemma | def | instance | 其他 | 零声明 |
|---|---|---:|---:|---:|---:|---:|---:|---:|---:|---:|---|
| `proofs/lean/juris_lean/JurisLean/Consolidated/All.lean` | `ca2e5d90e81545cd1037121f66f5762865136513` | 137 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |
| `proofs/lean/juris_lean/JurisLean/Consolidated/Audit.lean` | `e70c08ad718759cb685b3b5b629ea48c829e1374` | 1012 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 0 | 是 |

