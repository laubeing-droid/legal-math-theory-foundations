# LegalBench personal_jurisdiction：J01 补充筛查，旧账待对重
## 口径及来源
2026-11-16。独立补充记录，不修改理论或共享总账，不计全局净新增。已读回公开研究记事板，blob f468c5097e3e68020ae1c590ea5a9ad47db483ed，最新旧快照 LegalBench 14,591；19个早期已完子任务明细仍不明。当前公开仓树未发现 personal_jurisdiction 同名记录，但这不证明旧账未覆盖。
- [任务说明](https://github.com/HazyResearch/legalbench/blob/main/tasks/personal_jurisdiction/README.md)，读取blob d97cfe55b08c48977020bb5b1b8d414579b0a056，许可CC BY4.0；明确为人工构造的简化个人管辖假设题，不是真实案件。
- 固定数据版本 daec8237410aa23e3faf4bc41ad8b3a7e1696826：[train](https://huggingface.co/datasets/nguha/legalbench/blob/daec8237410aa23e3faf4bc41ad8b3a7e1696826/data/personal_jurisdiction/train.tsv)、[test](https://huggingface.co/datasets/nguha/legalbench/blob/daec8237410aa23e3faf4bc41ad8b3a7e1696826/data/personal_jurisdiction/test.tsv)。
实收train4、test50，共54条，README size写50，口径不同待解释。本批逐条筛查train0–3和test0–24，共29条。不是29案件或29新问题。未独立法源核验，不把简化规则移植为现行法律结论。
## 原创问题及题号
|问题|范围、归并与重要差异|
|---|---|
|J-P1 当事人角色与法院地必须明确|train0–3，test0–24均需先建原告/被告/诉地三元组；train1与test23–24互换起诉方，不能把原告或雇主的联系归给被告。test6–7原告住所与事故地拆开。|
|J-P2 时间及状态不可压扁|test3–5、12–14：已迁居、计划迁居、诉前尚未迁居不同；test4–5是相近描述不同法院地。现实中的住所认定需要事实与证据，不直接等同口语居住地。|
|J-P3 联系存在不等于请求关联|test0–2、11、19–21与train2：工作/度假/广告联系不自动关联本争议；原告后来迁居亦不能直接替代请求关联。test8–10比较经营地、被告所属州与受伤地。|
|J-P4 被告定向行为与原告单方移动分离|train3，test15–18、20、22：购买者自行带回、卖方知悉目的地、定向宣传、电话/邮件招徕是不同变量；17与18广告频度不同但同标Yes，不能由此推出实务阈值。|
|J-P5 标签理由与答案分别审计|test5 slice为Domicile而答案No，不宜把slice机械转为Yes；test10题设标示被告归属州，slice却为contacts+nexus，不应把分组字段当唯一法律理由。保留张力而非擅改金标。|
## 深度与待办
29条均首轮问题筛查；上述差异题作比较阅读，其余同机制归并。不另报统一精读数。需要独立法律复核的范围包括住所/个人管辖的真实认定标准、程序阶段及完整制度例外，当前为0。
下一断点test25。本批应在新文件保存并读回相等后才认定持久完成；是否与旧账重叠仍未知，全局净新增0。