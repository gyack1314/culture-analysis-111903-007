# 合成分析资料契约

所有机构、企业、受访者、交易和事件均为本地合成，不来自新闻所涉真实主体，不声称新闻发生过这些分析问题。

seed.json与同名Parquet是相同原始值的两种载体；actions.json列尚未应用的后续输入动作。inventory.json只记录原件物理摘要和行数，不提供分析结论。时间均含时区或明确日期，金钱字段minor以CNY分计，空值保留未知含义。已有代码只做物理完整性检查，没有估计、预测、方案求解或产品发布功能。

forms/items定义题版、档数、方向、措辞版本及construct；相同item_id不覆盖旧wording。responses按person/form/item唯一，answer为有序等级，missing_reason为skipped/not_applicable/not_reached，均不等于1。bridge_assignments给同人两版施测顺序与间隔，split是预分配development/validation；未答另一版不自动成为完整桥接。正式观众和桥接样本分别有group与target_margins，名册只约束人群构成，不授权凭空外推无锚群体。candidate_anchors仅是待检验候选，不预先认定无差异；不指定IRT、等百分位或线性链接为答案。原始分布和链接估计分开发布。

items.text为真实合成题目措辞；wording保存其版本标识，不是无差异证明。responses.at只记录采集批次，施测先后由bridge_assignments固定；受访者split来自respondents。新增桥接受访者应实际提交两版原始回答后才形成可用桥接，actions中登记本身不算已答。
