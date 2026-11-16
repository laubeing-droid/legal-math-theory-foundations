# LegalBench function_of_decision_section F01：补充待对账
2026-11-16。新增跨类型裁判文书修辞/段落功能筛查。公开目录未见同名记录，旧19子任务不详，旧账待对重、净新增0。仅新文件，不修改理论或总账。
## 来源
[任务README](https://github.com/HazyResearch/legalbench/blob/main/tasks/function_of_decision_section/README.md)，blob8717648a75c450bc06e7fdb12436de590feba94b，CC BY4.0。称从美国联邦上诉法院F.4th起始裁判顺序抽取段落、分七类；非全判决阅读。
固定commit daec8237410aa23e3faf4bc41ad8b3a7e1696826：[train](https://huggingface.co/datasets/nguha/legalbench/blob/daec8237410aa23e3faf4bc41ad8b3a7e1696826/data/function_of_decision_section/train.tsv)、[test](https://huggingface.co/datasets/nguha/legalbench/blob/daec8237410aa23e3faf4bc41ad8b3a7e1696826/data/function_of_decision_section/test.tsv)。实收train7+test367=374。
本批train0–6及test0–29共37条逐条首轮筛查；test全部引用1 F.4th 1，训练引用另含1 F.4th 100、25、87、513。37段不是37案；未回查全判决或现行法效力。
## 原创问题
|问题|ID/归并与差异|
|---|---|
|F-P1 数据标签需要语义质量审计|train0段末明显维持原判、标签却Facts，与train6 Decree存在显著张力，保留待回源，不默改；此示范可能干扰few-shot。|
|F-P2 一段多功能及分类粒度|train2兼问题/评价；train4兼规范/适用；test13兼争点/审查标准；test15含程序/规范却Facts；test29兼规范/当事人主张。单一标签压掉次功能，不能假设唯一自然类别。|
|F-P3 谁说/哪个法院/哪个程序|test0–11、15–18、20–23：家族历史、当事人信念、专家鉴定、刑事指控、引渡程序、后诉及当前上诉需分层。指控不等于事实已证，历史法院结论不等于本院结论。|
|F-P4 证据/程序标准影响事实地位|train3默认未受争议指称为真；test8引渡证据门槛；test10–11默认登记与默认判决不同；test20–21上诉补充材料与原审记录边界。分类任务没有验证证据真实性或实体权利。|
|F-P5 争点/规则/适用/结论/裁判主文分开|train3–6，test12–29：14/16/26–27归规则，17–18/21/23归适用，19/24为局部结论，25/28开启争点。局部胜负不等于最终主文；段落含判例引文不自动全属Rule。|
|F-P6 上下文依赖|test21开头与20末尾重复一句内容；指代、转折及下文引用需要邻段定位，不应将重复当新证据。test0–29为同案连续展开，随机段落拆分可能泄漏案情背景，未实测。|
37条仅筛查，不是37实际案件完整审读；未核引用判例全文，外部法核0，未模型评分。公开只保存原创问题和定位，不含原段落。
## 断点
保存读回后推进test30。全子任务尚未完成，待旧账对重及标签/上下文复核。另行探查corporate_lobbying仅下载/元数据查看，未形成完整批次，不计覆盖。