# LegalBench insurance_policy_interpretation I01：补充待对账
2026-11-16。公开目录未见同名任务记录，旧19任务明细仍缺；重叠未知、全局净新增0，不与旧14,591相加。不改理论/共享账。
## 来源和口径
[任务README](https://github.com/HazyResearch/legalbench/blob/main/tasks/insurance_policy_interpretation/README.md)，blob 9ee6eca86a8c246090814121cdd431191e818e52，CC BY4.0；来自Vague Contracts的保单—请求配对。标签由众包Yes/No/不能决定回答的95%多项比例置信区间下界是否达到0.5决定；无类别满足则标C。故C不能直接等于法院认定条款歧义，A/B也不是实际理赔裁判。
[train](https://huggingface.co/datasets/nguha/legalbench/blob/daec8237410aa23e3faf4bc41ad8b3a7e1696826/data/insurance_policy_interpretation/train.tsv)；[test](https://huggingface.co/datasets/nguha/legalbench/blob/daec8237410aa23e3faf4bc41ad8b3a7e1696826/data/insurance_policy_interpretation/test.tsv)。固定版本daec8237410aa23e3faf4bc41ad8b3a7e1696826，实际train5+test133=138。
本批train0–4及test0–29共35条，逐条首轮筛查、差异比较，其余归并。不是35真实案件，未独立法核或重算众包区间。
## 原创问题及ID
|问题|定位与差异|
|---|---|
|I-P1 标签来源与不确定性类型分离|train2，test2、5、8–10、12–13、16、20–21、23、27均C；可能涉及概念边界、因果不明、事实不足或评价分歧，不能机械统称法律歧义。test16明确后来恢复但仍C，尤其需要查众包分布而非硬改金标。|
|I-P2 定义的主体/对象/用途/地点逐项匹配|train0–1、4比较专业搬运人身份、退休亲属、自己搬运及存储；test3儿童与不利第三人，4/9液体类型，6/8/22/24配件与音响，28固定装置与便携物。近似词不等于满足定义。|
|I-P3 承保原因不是同时存在事件|test1、7、12–14、18–19、23、25：罢工后自己不买肥料、强风下电话惊扰、火与烟、树倒与地质原因、热作业与吸烟需分开因果链。不能用关键词共现代替原因。|
|I-P4 范围条件的时间/强度/状态|test0、10–11、15–18、23、26：临时离家、工作状态、永久全损、快速积水、破裂程度不同；必须保留原限定及事实时间。保单标题不能覆盖具体限制。|
|I-P5 基本承保与排除/注意义务分层|train2–3，test20–21：职业关联、定期维护逾期、明知持续警告未处理差异；不能将所有疏忽统一拒赔或统一承保。|
|I-P6 信念主体和认知时点|test27、29：实际紧急、被认为紧急、投保人知情/求助动机、应急人员感知应区分；条款有无“perceived”会改变待解释问题。|
## 状态
短条款不是完整保单；免赔额、限额、期间、批单、证据及实际法律均未核。保存读回后计35条持久记录；下一test30。独立法源核验0，不发布原题，待旧账对重。