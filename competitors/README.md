# Sykka 竞品情报

本目录维护一条从日常发现到周度沉淀、再到月度复盘的竞品情报链路。

核心问题是：是否出现足以改变 Sykka 产品、市场或竞争判断的新事实？主要产物为 [Event Tracker](intelligence-tracker.md) 和 [Monthly Review](monthly/README.md)。只有 P0 / P1 的 NEW 或实质 UPDATE 才进入 Tracker；普通社媒发帖、品牌内容、产品教育、Campaign 和常规互动不在本体系范围内。

## 调度关系

1. 每日 08:30 Intelligence Daily：检查前一自然日，发现并筛选 P0 / P1 候选；输出日报，不修改 GitHub。
2. 周五 17:00 Intelligence Weekly：整理过去 7 天日报，核验原始来源并去重，将合格的 NEW / UPDATE 增量写入 RD / KA / IND Tracker。
3. 每月月初 Monthly Review：回测上月 Watchlist，结合 Tracker、日报、周维护结果及其他已核验数据生成上月月报，并同步 Current Competitive View、Monthly Watchlist 和事件引用。

调度时间使用 Asia/Shanghai。周维护保留全部既有事件和历史，只更新事件证据与状态；Current Competitive View 原则上在月结更新，只有重大 P0 新证据足以改变整体判断时才允许周中调整。本文描述目标工作流，不单独证明每个自动任务已启用；任务状态以调度器中的当前配置和运行记录为准。
