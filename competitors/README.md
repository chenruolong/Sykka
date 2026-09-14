# Sykka 竞品情报

本目录包含两条相互连接、职责独立的监控链路。

| 链路 | 核心问题 | 主要产物 | 升级条件 |
| --- | --- | --- | --- |
| Competitive Intelligence | 是否出现足以改变竞争判断的新事实？ | [Event Tracker](intelligence-tracker.md)、[Monthly Review](monthly/README.md) | P0 / P1 NEW 或实质 UPDATE |
| Competitor Activity | 竞品每天对外做什么、说什么、用户对什么有反应？ | [Activity Log](activity/activity-log.csv)、[Coverage Log](activity/coverage-log.csv)、[Weekly Pattern](activity/weekly/README.md) | 连续 Pattern、重大 Messaging Shift、重要增长玩法、关键官网变化或与已有事件形成实质关联 |

允许同一事实出现在两条链路中，但分析对象不同。例如合作公告可作为 Activity 记录其传播动作，同时作为 Intelligence 事件记录合作事实。通过 Content ID 与 RD / KA / IND ID 建立关联，不为避免重复而删除任一层必要证据。

## 调度关系

1. 08:30 Intelligence Daily：发现并筛选 P0 / P1 事件。
2. 09:00 Activity Daily：扫描 RedotPay / KAST 的 X 与官网，更新 Activity 与 Coverage。
3. 周五 16:30 Activity Weekly：从过去 7 天记录中识别 Pattern。
4. 周五 17:00 Intelligence Weekly：消费周度 Pattern，判断是否建立或更新 RD / KA / IND。
5. 月结：结合事件 Tracker、Watchlist、Activity 周度总结及其他已核验数据形成 Monthly Review。

调度时间使用 Asia/Shanghai。本文描述目标工作流，不单独证明每个自动任务已启用；任务状态以调度器中的当前配置和运行记录为准。
