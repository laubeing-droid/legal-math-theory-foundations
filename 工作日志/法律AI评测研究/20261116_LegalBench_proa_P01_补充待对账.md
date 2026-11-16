# LegalBench proa P01：补充待对账
2026-11-16，公开仓树未见本任务同名记录，旧账明细不全；待对重、净新增0。新主题为明确私人诉权识别，不改理论/共享账。
[README](https://github.com/HazyResearch/legalbench/blob/main/tasks/proa/README.md)，blob a56565b54a70d70fa2997f96c0b10d8173bcac03，CC BY4.0，明确手工构造并借鉴州法，不能当现行真实法条。
固定版daec8237410aa23e3faf4bc41ad8b3a7e1696826，[train](https://huggingface.co/datasets/nguha/legalbench/blob/daec8237410aa23e3faf4bc41ad8b3a7e1696826/data/proa/train.tsv)、[test](https://huggingface.co/datasets/nguha/legalbench/blob/daec8237410aa23e3faf4bc41ad8b3a7e1696826/data/proa/test.tsv)。实收train5+test95=100。本批train0–4、test0–29共35条首轮筛查。
|问题|题号与差异|
|---|---|
|P-P1 私人/公共执法主体|train1由检察长追缴民事罚款标No；train2–4及test0–29私人权利人/责任对象不同；出现civil action或罚款不等于私人可诉。|
|P-P2 文字形式与诉权功能|train3–4，test3、5–7、9、12、17、24、27–28为责任或赔偿表述也标Yes，不仅寻找“可起诉”。但是责任存在、诉权、特定原告适格、实际胜诉不同，不能将标签扩张。|
|P-P3 主体和构成限制|test0–10、15–17、21–24、26–28：受损人、客户、善意取得者、直接违反者、受益/负责方、故意与损害因果条件各异；明确诉权不等于用户已满足条件。|
|P-P4 救济与程序路线|train2，test11、13–14、18–20、25：请求/抗辩、禁令、法定/实际损害、宣告、原案藐视程序、其他普通法救济分开。18私人原案动议与机关诉讼并列，不能合成任意新诉权。|
|P-P5 触发阈值与前置条件|test17、20、29含等待、次数/期间、通知且机关未行动；不能只抽“may”跳过条件。|
|P-P6 片段完整性/历史合法性|test0、1、4、7、8、15、17、26、29多处引用缺失或上下文依赖；尤其28劳动相关句只是人工测试文本，不认可其现实效力或适用。|
35条人工条款记录非真实案件/真实现行条文。独立法核0，不公开原文；保存读回后下一test30。