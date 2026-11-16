# LegalBench successor_liability 补充批次 S01

日期：2026-11-16。直接筛查 train 0–2、test 0–23，共 27 条。与旧全局账重叠未知，**净新增仍为 0**；本次只记独立补充筛查。本轮其他已处理子任务为 hearsay 与 causality，本批不重叠这些范围。

## 来源、版本和状态

固定版本 `daec8237410aa23e3faf4bc41ad8b3a7e1696826`：
- [训练文件](https://huggingface.co/datasets/nguha/legalbench/blob/daec8237410aa23e3faf4bc41ad8b3a7e1696826/data/successor_liability/train.tsv)
- [测试文件](https://huggingface.co/datasets/nguha/legalbench/blob/daec8237410aa23e3faf4bc41ad8b3a7e1696826/data/successor_liability/test.tsv)
- [任务说明](https://github.com/HazyResearch/legalbench/blob/main/tasks/successor_liability/README.md)，读取 blob `4455d8054d025d6dcb2acabac6f73b3beb670344`，说明许可 CC BY 4.0。

实收 train 3、test 47，共 50 条，人工编写情境，不是真实案件数。说明标 four-way，但实际 answer 是标签列表，部分多标签；test12 出现 implied assumption of liability，不能按固定四选一盲目解析。issue 字段为已给定的问题类别，不等于模型从开放事实中识别问题的独立测试。

本批未核适用法域、完整交易文件或外部法源；源标签不是最终责任裁决。余 test24–46 共 23 条，下一候选 test24。原题不公开转载。

## 逐项索引

| split/index | 源标签 | 筛查关注与归并理由 |
|---|---|---|
| train/0 | de facto merger; mere continuation | 有限承接范围与交易结构分别保留 |
| train/1 | mere continuation; fraudulent conveyance | 知悉潜在缺陷、未起诉、经营持续三个时点/事实分开 |
| train/2 | express agreement | 明确承接与其余可能路径不同，未列标签不等于排除 |
| test/0 | de facto merger; mere continuation | 经营连续与股权/解散等要素分别保留 |
| test/1 | de facto merger; mere continuation | 关闭总部不自动否定其他连续性 |
| test/2 | de facto merger; mere continuation | 债务类型及旧产品线关联需要保留 |
| test/3 | de facto merger; mere continuation | 人员连续性不是全有全无；买方名称Large/Big不一致待核 |
| test/4 | de facto merger; mere continuation | 免责条款与法定/判例责任路径不能合并 |
| test/5 | de facto merger; mere continuation | 股权连续与人员/管理不连续分别记录 |
| test/6 | de facto merger; mere continuation | 未来责任措辞、伤害及解散时点不同 |
| test/7 | de facto merger; mere continuation | 承接范围限日常经营，不能自动覆盖所有旧损害 |
| test/8 | de facto merger; mere continuation | 与train1对照新增股权事实，不能推定未列欺诈路径已排除 |
| test/9 | express agreement | 持续支付义务与一次性债务不同 |
| test/10 | express agreement | 卖方仍存续不自动排除约定承接路径 |
| test/11 | express agreement | 协议未载但外部公告有承诺，需区分证据载体和效力 |
| test/12 | express agreement; implied assumption of liability | 实际履行行为与明文条款不同，出现说明四类外标签 |
| test/13 | express agreement | 合同服务债务承接范围记录 |
| test/14 | express agreement | 原义务人有偿付能力不等于承接义务消失 |
| test/15 | express agreement | 明确承接与连续性事实并存，单一标签非排他证明 |
| test/16 | express agreement | 与test7对照承接全部/必要经营债务差异 |
| test/17 | express agreement | 与train1/test8对照条款变化，不等于全部要件均已证明 |
| test/18 | fraudulent conveyance; mere continuation | 题设明示逃债目的，别当实际证明过程 |
| test/19 | fraudulent conveyance; mere continuation | 题设含评价词，区分事实输入与法律结论输入 |
| test/20 | fraudulent conveyance; mere continuation | 与test18福利类型不同，不默认跨制度完全等价 |
| test/21 | fraudulent conveyance; mere continuation | 待详读：题面写为支付清理费而转让，与逃避责任标签有张力 |
| test/22 | fraudulent conveyance; mere continuation | 行为许可变化、获知责任及交易时点分开 |
| test/23 | fraudulent conveyance; mere continuation | 特别法责任与一般继受责任路径需要另核 |

## 实务问题归纳

- S-P1：识别一种责任路径，不等于排除其他路径；多标签、单标签和最终承担责任需分开。明确承接常只标一种答案，并不证明其他路径不能同时主张。
- S-P2：资产转让、主体解散、持股和管理连续、产品线连续、债务产生及损害发现分别记事件。不要把交易完成当作全部责任结束。
- S-P3：债务承接应保留范围、时点、类型、条件与来源；合同、公告及履行行为不能被压成一个“已承接”字段。
- S-P4：题设给定知悉、逃债目的或法律评价，与实务中需要证明这些事实不同。来源字段应区分事实断言、推断与规范评价。
- S-P5：比较情境时不能丢失特别法、法域及债务类型。说明自身承认法域差异，具体多因素要求不能从本任务标签机械移植。
- S-P6：题目和标注也需要对照。test21 的支付/逃避目的用词，test3 的主体名称差异、test12 的标签域外值均列待核，不自行改原题或宣布金标错误。

## 下一步

保存读回后计已保存补充 27 条；继续 test24–46，并与既有问题合并或保留差异。旧账对重前不改全局总数，不修改理论、代码或共享总账。
