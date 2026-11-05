# 地方棋牌 · 数据治理审阅 V2

独立审阅站点：https://jiyunfei150-del.github.io/local-chess-governance-v2/

项目为地方棋牌（project_id=86），仅 friend_ads、friend_dwd、friend_dws、friend_ods。元数据与活性拉取于 2026-11-04，方案更新于 2026-11-05。

第一批补录 36 张表：近 7 天调用 > 0 且近 30 天调用 > 4。35 个候选指标完整保留。

本期建设建议收敛为 5 张 DWD + 2 张 DWS：

- DWD：标准登录事件、支付成功订单、账号属性日快照、玩家对局时长、房卡标准流水。
- DWS：账号日登录付费汇总（保留支付全集、空账号对账）、登录分群留存汇总（D+1/3/7）。
- 另复用 2 张现有 DWS，不计入新增。其他主题先使用现有 ODS/ADS，不为每个指标单独建表。

本期 7 张建议表均直接展示 SELECT 逻辑，可下载SQL。新建模SQL仅做静态字段检查与模拟数据检查，未做引擎EXPLAIN，未执行建表或业务取数。时长单位、事件键与房卡映射需先验收，未确认处保留未知状态。35 条原候选指标SQL的EXPLAIN记录与本期建模SQL区分展示。

沿用已有业务域、业务过程。没有写入治理平台或创建业务表。

旧站点保持原样：https://jiyunfei150-del.github.io/project-table-activity/local-chess/
