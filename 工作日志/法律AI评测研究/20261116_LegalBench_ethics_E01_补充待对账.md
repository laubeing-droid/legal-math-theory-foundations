# LegalBench nys_judicial_ethics E01：补充待对账
2026-11-16。公开树未见同名记录，旧账不全、重叠未知，净新增0。
[README](https://github.com/HazyResearch/legalbench/blob/main/tasks/nys_judicial_ethics/README.md)，blob ef06d04ef35e6f291d9fb367150e40b27b7d7d75，许可MIT。官方说明从2010/2021/2022/2023司法伦理意见摘要收集并由ChatGPT改写Yes/No，非原始意见全文。已打开[法院意见目录](https://www.nycourts.gov/legacyhtm/ip/judicialethics/opinions/)，只确认可得入口，未将具体题目回链到意见号、未核后续修改。
固定daec8237410aa23e3faf4bc41ad8b3a7e1696826：[train](https://huggingface.co/datasets/nguha/legalbench/blob/daec8237410aa23e3faf4bc41ad8b3a7e1696826/data/nys_judicial_ethics/train.tsv)、[test](https://huggingface.co/datasets/nguha/legalbench/blob/daec8237410aa23e3faf4bc41ad8b3a7e1696826/data/nys_judicial_ethics/test.tsv)。train8+test292=300。本批train0–7及test0–49共58条，均year2010。
|问题|ID/差异|
|---|---|
|E-P1 年份/法域/原意见追溯|全部；历史答复经改写，未核意见号与当前规则，不能作为现行纽约或其他法域司法伦理指导。train5–6涉及特定法条尤其不得忽略时效。|
|E-P2 许可/义务/禁止及否定方向|train3与test46，test9–14、20–29、32–45、47–48出现肯定/否定成对问题。Yes可能是“应回避”也可能“可以审理”，不能归为单一允许行为。成对题不计独立意见或案件。|
|E-P3 回避、披露、隔离及补救不同|train0–2、7，test0、2–3、13–17、19–21、36–37、42–43、47–49：法官、亲属、书记员/其亲属、过去雇员、候选筛选成员不同；关系类型/时间/经济联系与特定案件分开。test20含可解除回避而二分类丢弃条件。|
|E-P4 身份/场景限制|train3–4，test4–8、18、22–25、30–31、46：兼职/全职、本人/同事、行政办理/裁量行为、本院/他院、公益任职/倡议活动不同。不能凭职业头衔同一概括。|
|E-P5 中立信息/政治或募款活动|test1、8–12、26–35、38–39、44–45：客观信息/倡导、合理日程请求、非党派/党派标语、任职/募款、匿名/署名捐献不同。|
|E-P6 适当行动与必报/失当不同|train0、5–6，test15–16、40–41：概率与严重程度门槛、采取适当行动、报告与相关回避不等同。|
|E-P7 条件压缩风险|train4、test6等仅“遵守限制/指引”；test36–37宽泛改写未展开关系强度或强制回避情况，不得从金标推出相信公正即可处理所有冲突。test5意见委员会权限与法院法律问题分开。|
58条首轮问题筛查、差异比较，其余归并；非58独立真实案件。未核原意见全文、独立法核0，不复制题库。保存读回后下一test50，不改理论/共享账。