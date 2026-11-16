# LegalBench jcrew_blocker B01：补充待对账
2026-11-16，公开树未见同名记录，旧账19项未明；旧账待对重、净新增0。不改理论/总账。
[README](https://github.com/HazyResearch/legalbench/blob/main/tasks/jcrew_blocker/README.md)，blob017cdecea78b6d19dd3f727fdaffb8cfdd103e3f，CC BY4.0，称专家整理公开贷款条款；本轮未回查每份原贷款合同，不认定60条等于60案件。
固定版本daec8237410aa23e3faf4bc41ad8b3a7e1696826，[train](https://huggingface.co/datasets/nguha/legalbench/blob/daec8237410aa23e3faf4bc41ad8b3a7e1696826/data/jcrew_blocker/train.tsv)、[test](https://huggingface.co/datasets/nguha/legalbench/blob/daec8237410aa23e3faf4bc41ad8b3a7e1696826/data/jcrew_blocker/test.tsv)；实收train6+test54。本批train0–5及test0–26共33条逐条首轮筛查，差异对读。
|问题|题号/区别|
|---|---|
|B-P1 分类存在不等于保护强度或有效性|train0–2、test0–26均Yes；限制主体、接收方、资产、时间和例外不同，不能同标就认定同等阻止资产外流。|
|B-P2 路径与资产权利需展开|train0–2，test3–8、11–16、19–25：转让、投资、分配、独占许可、指定子公司身份及间接股权路径不同；法律所有权/实益所有权/使用权不是同义词。|
|B-P3 重大性及判断者|test0–1、4、7、9、18、22、26：借款人善意或合理判断、整个集团或国内子集团、单独或累计、无法经营阈值不同。条款带判断权不是客观已证明重大。|
|B-P4 例外及外部依赖|test2、5–6、10–12、17–20、23、26：日常经营、非独占许可、特定地域/业务线、证券化实体、共享服务及交叉引用依赖完整定义/附表，不得只摘禁止语句。test20片段中例外语句截断，不能补造全文。|
|B-P5 持续状态与行为限制|test4、8、13、15–16、19–22、24：指定时不得持有、任何时候不得持有、之后不得投资分开；仅一时点限制未必覆盖以后行为。|
|B-P6 关键词不等于功能|train3权属/许可陈述、train4资产出售定义例外、train5担保释放机制均No；出现IP、子公司或抵押不等于阻断条款。|
|B-P7 文本质量/重复|test5与6仅前导空白差异待程序确认；train2、test3、16有重复或近重复限制语句，不能当多份独立保护或独立案件。test10/20语法衔接应回源。|
33条非33独立案件；未核完整合同、现行法、保护效果、裁判或金标。下一test27；保存读回后计持久完成，独立法核0。