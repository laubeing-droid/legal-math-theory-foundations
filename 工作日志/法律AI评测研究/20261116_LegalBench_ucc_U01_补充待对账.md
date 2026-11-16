# LegalBench ucc_v_common_law U01：补充筛查，旧账待对重
2026-11-16。授权研究日志独立文件，不改理论、共享总账或题目。公开目录未发现本子任务同名记录，但早期19项完成清单仍缺，故旧账重叠未知、全局净新增0。此前公开记事板blob f468c5097e3e68020ae1c590ea5a9ad47db483ed的14,591不得直接相加。
## 来源与范围
[任务说明](https://github.com/HazyResearch/legalbench/blob/main/tasks/ucc_v_common_law/README.md)，blob 4cfdd89407e5150e2348429af5ead069841dc804，CC BY4.0，人工构造简单合同，明确忽略混合目的合同。
固定数据commit daec8237410aa23e3faf4bc41ad8b3a7e1696826：[train](https://huggingface.co/datasets/nguha/legalbench/blob/daec8237410aa23e3faf4bc41ad8b3a7e1696826/data/ucc_v_common_law/train.tsv)、[test](https://huggingface.co/datasets/nguha/legalbench/blob/daec8237410aa23e3faf4bc41ad8b3a7e1696826/data/ucc_v_common_law/test.tsv)。
实收train6、test94；本批train0–5及test0–29，共36条逐条问题筛查。不是案件数。未核现行法，不将金标视为法律意见。
## 原创问题与ID
|问题|记录及区别|
|---|---|
|U-P1 交易对象与行为分开|train0–3及test0–6、11、14–19、21–29：同样出现自行车、房屋、电视或工具，买卖、修理、拍摄、寻找、安装分别提取。test18服务于制造商仍是服务题，不能把客户行业当合同标的。|
|U-P2 不动产、服务、物品不是关键词互斥桶|train4，test2–3、7–10、12–13：土地买卖、房屋租用、装修、专业服务与雇佣分开；不能将普通法标签解读为没有其他特别法。test4系统采购是否带安装、test8装修是否带材料未明确；任务人为排除混合目的，不是现实已排除。|
|U-P3 适用UCC不等于适用Article 2|train5、test20租用动产也标UCC；README主要用Article 2买卖说明。须将交易类型、具体篇章及当地法分开核查，不由二分类替代。此处记录描述/标签粒度张力，不宣布金标错。|
|U-P4 适用规则不等于合同已成立或有效|train3及test1、15–16、23、25、27：口头接受、订单、重复供货、付款与笼统合同表述不同；题设预设合同，不足以验证实务中的签署权限、要件、证据和可执行性。金额/持续期限不能由这一标签完成审查。|
## 深度/断点
36条首轮筛查，重要差异对比阅读，其他按上述机制归并；不另报统一精读数。无原题公开、独立法核0。保存读回相等后才计持久完成；下一test30。