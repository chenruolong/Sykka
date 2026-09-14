# Sykka Competitor Activity Monitoring

本体系连续记录 RedotPay 与 KAST 在官方 X 和官网的公开动作，回答“竞品昨天对外做了什么、在说什么、用户对什么有反应”。它是行为时间序列，不代替事件级 [Intelligence Tracker](../intelligence-tracker.md)。

## 范围与覆盖

- 时区：Asia/Shanghai。
- 日窗口：前一自然日 00:00 至当日 00:00，不含结束时刻。
- 对象：RedotPay、KAST。
- 渠道：官方 X；官网 News / Blog、产品页、Help Center、Fees / Terms / FAQ。
- X：固定为 Partial / Best-effort Coverage。只能写“已发现 N 条”或“未可靠发现”，不能据此确认完整发帖总量或断言没有发帖。
- Website：按固定页面清单检查。首次读取建立基线；只有存在可复核的前后版本证据时才写 Page Update。页面未标修改时间时记录首次发现日期，不推断实际修改日期。
- 社区内容：可作为 Community Lead / 待官方验证保留在日报分析中，不进入官方 Activity Log。

## 每日输出

1. Executive Takeaways：2–4 条结论，说明证据及限制。
2. Messaging & Activity Analysis：按竞品聚合 Theme、渠道、互动和近期 Pattern。
3. Structured Activity Log：一条真实官方动作一行。
4. Monitoring Coverage：逐竞品、逐渠道说明检查状态、覆盖等级、发现数量和缺口。

没有发现动作时仍生成 Coverage。采集失败、没有可靠发现和确认没有活动是三种不同状态。

## Theme taxonomy

优先使用以下一级主题；必要时填写一个二级主题：

`Product`、`Card Spending`、`Distribution`、`Lifestyle`、`Security`、`Compliance`、`Partnership`、`Promotion`、`Referral`、`Membership`、`Education`、`Brand`。

新增主题前先检查现有数据，避免同义词分裂。主题描述内容在讲什么，不等同于事件优先级。

## Activity Signal

- High：对本周 Messaging / Campaign / 产品传播判断可能有明显影响，或值得进入 Intelligence 核查。
- Medium：有清晰信息增量或代表性，但尚不足以改变周度判断。
- Normal：常规官方活动，仍作为时间序列记录。

High / Medium / Normal 不等于 Intelligence 的 P0 / P1 / P2，也不自动触发 RD / KA / IND 入库。

## Content ID 与去重

格式：`<主体>-ACT-<YYYYMMDD>-<短标识>`，主体使用 `RD` 或 `KA`，例如 `RD-ACT-20260910-BLOCKSEC`。

- 同一 Campaign 或发布主题的官网文章与 X 帖可共享 Content ID，但保留为不同 Activity 行。
- 每一行以 `date + competitor + channel + action_type + url` 为稳定去重键；URL 缺失时使用 Content ID、发布时间和摘要联合判断。
- 重复抓取不新增行；互动变化更新同一行的指标和 captured_at，并在 notes 说明。
- 一个重要事实进入 Intelligence 后，在 intelligence_event_id 填写 RD / KA / IND ID；Activity ID 不改变。

## 字段定义

[activity-log.csv](activity-log.csv) 每条官方动作一行。互动指标只记录公开可见且能可靠读取的值；无法取得填 `N/A`，确认数值为零才填 `0`。date_confidence 使用 `Exact`、`Approximate` 或 `Unknown`。

[coverage-log.csv](coverage-log.csv) 每个日期、竞品一行。x_checked / website_checked 使用 `true` 或 `false`；x_coverage 第一阶段固定为 `Partial`，未检查则为 `Not checked`。发现数是“已发现动作数”，不代表平台完整总量。

## Messaging Shift 与升级

至少满足以下一种情况，才可在周报列为 Possible Intelligence escalation：

- 多个独立动作在连续日期形成稳定 Pattern；
- 品牌叙事相较可比历史窗口出现明显转向；
- 出现重要增长玩法、产品组合或 Campaign 机制；
- Fees / Terms / 产品规则等关键官网内容发生可核验变化；
- Activity 为已有 RD / KA / IND 事件提供新的事实、反证或落地进展。

单条普通帖子、单次高互动或社区转述不足以升级。没有可比历史样本时，不计算“显著高于基线”或声称 Messaging Shift。
