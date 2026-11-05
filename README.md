# 地方棋牌 · 数据治理审阅 V2

独立审阅站点：https://jiyunfei150-del.github.io/local-chess-governance-v2/

- 项目：地方棋牌（project_id=86），仅 friend_ads、friend_dwd、friend_dws、friend_ods。
- 元数据与活性拉取于 2026-11-04；方案更新于 2026-11-05。
- 第一批 36 张表：近 7 天调用 > 0 且近 30 天调用 > 4。
- 35 个候选指标，20 张 DWD/DWS 建模建议（复用现有 2 张，建议新增 18 张）。
- 不新增“房间创建与结束”业务过程；沿用“游戏域 / 游戏行为”。
- 本站是静态审阅方案；未写入治理平台、未创建业务表，SQL 仅经过 EXPLAIN 校验。
- 旧站点保持原样：https://jiyunfei150-del.github.io/project-table-activity/local-chess/
