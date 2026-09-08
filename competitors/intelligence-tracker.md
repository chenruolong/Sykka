# Sykka Competitive Intelligence Tracker

Daily Brief → Event Tracker → Monthly Review → Current Competitive View / Monthly Watchlist。维护对象是事件及证据，不是新闻篇数。

V2：Tracker 是证据 / 长期记忆层；[月报](monthly/README.md)是阶段性判断层。Tracker 只保留当前判断、观察重点和事件证据，不追加日报全文或周维护日志。已有首轮扫描记录作为初始化证据保留。

- 创建：2026-09-07；最近维护：2026-09-08（V2 结构升级，未重新核验事件；首轮扫描覆盖限制见扫描记录）。
- 时间口径：Asia/Shanghai；日期 YYYY-MM-DD，来源时间保留原时区。
- 节奏：每日发现与去重，每周五沉淀过去 7 天日报及全部 Active Signals。
- 入库：P0 和值得持续跟踪的 P1；P2 默认过滤。
- 本文是维护规范，不代表自动扫描、提醒或 GitHub 定时写入已经接通。

## Current Competitive View

Last Reviewed: 2026-09-07

原则上在月结时复核和更新；只有重大 P0 的新增证据足以改变整体判断时，才允许周中调整。引用事件 ID、证据和判断日期，区分事实、推测、待验证假设。完成判断复核才更新 Last Reviewed，结构编辑或例行周维护不刷新该日期。月度变化及原因写入对应月报；周中 P0 调整在关联事件 Timeline 留下日期、原判断、新判断及依据，月结时回溯。

| 对象 | 当前判断 | 持续关注 | 支撑事件 / 判断日期 |
| --- | --- | --- | --- |
| RedotPay | 事实：披露香港两家子公司 AML/CFT 审查；推测：加强可对外展示的信任证据，尚不能推导全球合规或经营效果 | 审查范围、报告与整改披露 | RD-001 / 2026-09-07 |
| KAST | 事实：Reserve 连接余额与会员奖励，每日游戏连接回访与消费；推测：同时争取余额留存和消费频次，实际增量未证实 | 奖励资格、成本、活动后持续消费 | KA-001、KA-002 / 2026-09-07 |
| Industry | 事实：Ethena Pay 已公开推出；推测：发行生态开始自建消费者分发入口。单个案例不足以认定全行业趋势 | 底层资产、真实可用范围与实际使用规模 | IND-001 / 2026-09-07 |

趋势判断须说明证据支持什么、仍不确定什么、什么证据会改变判断。官宣不等于全面可用，相关性不等于因果，历史 Sykka 规划不等于当前已上线能力。

## Monthly Watchlist｜2026-09

初始化状态：待首次月结制定；暂无可核验的上月月报 Watchlist，不将已有 Open Questions 冒充上月决定。当前事件仍按各自 Open Questions 跟踪。

每月月结后，以月报 Next Month Watchlist 更新本节标题为目标月份 `YYYY-MM`。仅保留当月清单，历史清单保留在对应月报；日报优先检查这些线索。每项写明事件 ID（可引用多个 RD/KA/IND ID）、待验证问题、检查来源和复查日期或触发条件。尚未入库的线索标“待分配 ID”，核验并去重后再分配。

| 事件 ID | 待验证问题 / 观察重点 | 检查来源 | 复查日期 / 触发条件 | 来源月报 |
| --- | --- | --- | --- | --- |
| 待制定 | 首次月结后填写 | — | 首次月结 | 无 |

## 收集范围与来源

RedotPay、KAST 为核心，覆盖产品、市场、增长、商业化、体验及公司动态。品牌词与 card、account、transfer、fee、KYC、license、partnership、funding、users、payment volume 等组合搜索。

行业围绕 stablecoin payment / card / account / off-ramp / remittance / cross-border payment / spending / settlement。ether.fi Cash、Karta、Tria、Kolo、Plasma One、Gnosis Pay、Wirex 为雷达层，仅在变化对 Sykka 有明确意义时纳入。普通币价、上币及无关公链新闻不纳入。

| 来源层 | 使用方式 |
| --- | --- |
| 官方与监管 | 官网 News / Blog、官方 X / LinkedIn、商店版本说明、监管文件；核实原始公告及适用范围 |
| 新闻媒体 | Reuters、Bloomberg、The Block、CoinDesk 等扩大覆盖，再追溯原始来源 |
| 行业数据 | PaymentScan、Artemis、DefiLlama、Dune、研究报告；记录统计期、地区、平台、单位、方法及限制 |
| 用户声音 | Reddit、X、App Store / Google Play 评论；发现 VOC 与异常，不单凭投诉确认故障原因或规模 |
| 深挖来源 | Help Center、Fee Schedule、Terms、API / Changelog、合作方及发卡机构公告 |

官方来源只确认其明确声明的内容。转载同一公告不算独立验证。Sensor Tower 使用实际取得的导出或截图，不假设自动读取付费账号；App 留存不等于卡消费留存。

## 事件编号规则

- RedotPay：`RD-001`；KAST：`KA-001`；行业及其他竞品：`IND-001`。
- 三类独立递增，至少三位，不按年重置；创建前检查 Active 与 Closed 的最大编号。
- 一个事件一个永久 ID，后续报道及阶段进展沿用原 ID；关闭后不复用。
- 跨主体事件选一个主要归属，注明关联对象；独立事项才另建 ID 并交叉引用。
- 合并重复事件保留最早 ID，另一 ID 留合并说明及指向，不删除历史。
- 未入库的日报候选用标题和来源识别，每周入库时分配正式 ID，不声称已写入 Tracker。

## 状态规则

| Status | 含义与条件 |
| --- | --- |
| Watching | 已发现值得跟踪的信号，关键事实或影响待验证 |
| Developing | 出现实质新增证据或阶段进展，关键判断仍未确定 |
| Confirmed | 核心事实已有原始文件、官方明确确认或可复核证据；注明确认范围和未确认部分，仍可跟踪 |
| Closed | 事件结束、被证伪、合并或失去跟踪价值；保留关闭理由、最终判断和重开条件 |

常见路径 Watching → Developing → Confirmed → Closed，但不强制逐级流转。有充分证据可直接 Confirmed，被证伪可直接 Closed；反证可使状态下调并记录理由。Closed 不等于已证实。关闭后有实质进展沿用原 ID 重开；无新消息不等于问题已解决。

## Active Signals

### RD-001｜RedotPay 披露香港子公司 AML/CFT 独立审查

- Priority: P1
- Status: Confirmed
- First Seen: 2026-09-07
- Last Updated: 2026-09-07
- Monthly Review: 无（尚无已核验的月报引用）
- 本轮判定：NEW（首次入库；事件本身是 8 月预告的后续披露）

#### What Happened
RedotPay 于 9 月 7 日公告称，某四大会计师事务所已审查其香港持牌子公司 Red Dot Trust Limited、Red F. Technology Limited 的 AML/CFT 流程与控制，涵盖治理、客户尽调、交易监测、质量保证及人员培训。公告未具名事务所，也未附完整审查报告。[S1]

#### Timeline
- 2026-08-29｜官方文章预告独立审查及 9 月进一步披露；仅作历史背景。[S2]
- 2026-09-07｜公告明确两家香港主体及审查范围。[S1]

#### Current Assessment
- 事实：已确认上述官方披露存在；Confirmed 仅适用于披露及其明确范围。
- 推测：独立审查可能被用于增强合作方信任，但不能据此认定转化、留存或风控效果改善。
- 待验证假设：具体审查意见、例外及整改要求是否支持更广泛的合规能力判断。不能外推为全球业务认证、新牌照或资金安全担保。

#### Why It Matters to Sykka
竞品信任建设开始使用具体控制范围和受审主体作为证据。可据此整理对外信任说明需要哪些可披露材料；不凭公告数量比较安全水平。

#### Open Questions
- [ ] 是否公开事务所名称、报告期间、审查意见或整改事项？｜查官方补充和审查方披露｜2026-09-11 复查。

#### Sources
- S1｜[AML/CFT 独立审查公告](https://www.redotpay.com/news/weve-received-an-independent-review-of-our-aml-cft-controls-from-a-big-four-firm)｜RedotPay 官方｜发布 2026-09-07，查阅 2026-09-07｜浏览器核验正文；属于公司声明，未取得审查报告。
- S2｜[Building Trust](https://www.redotpay.com/ro/news/building-trust-how-were-protecting-users-at-redotpay)｜RedotPay 官方｜发布 2026-08-29，查阅 2026-09-07｜支持此前已预告；站点该语言路径返回英文正文。

### KA-001｜KAST Reserve 将余额奖励与会员权益、消费资金连接

- Priority: P0
- Status: Confirmed
- First Seen: 2026-09-07
- Last Updated: 2026-09-07
- Monthly Review: 无（尚无已核验的月报引用）
- 本轮判定：NEW（官方页面本周更新；确切首次上线日期待确认）

#### What Happened
9 月 3 日更新的官方说明将 Reserve 定义为独立 USD 余额：符合条件的奖励每日累计，通常记入 Spending Balance；余额可用于符合条件的卡消费，转账前需移回 Spending。奖励由 KAST 自行资助，可变更、暂停或终止；官方明确它不是利息、APY、收益或投资回报，也不是受保银行存款，且不同于 KAST Earn 中的 Gauntlet / USD Prime。[S1]

页面列示的引导期奖励率：Standard 6%；Premium 前 $50,000 最高 9%；Private 前 $200,000 最高 12%，后两者超额部分 6%。引导期至 2026-12-31 或全体 Reserve 存入达到 $100M，以先发生者为准，之后使用较低奖励表。这些是页面的促销口径，不改写为保证年化收益。[S1]

#### Timeline
- 2026-09-03｜官方文章标注 Last updated，披露余额使用方式、会员档位及引导期条件；不能据此确定首发日期。[S1]
- 2026-09-07｜核验页面，将促销奖励和 Earn 产品分开记录。

#### Current Assessment
- 事实：上述产品规则已由官方公开；未实测 App、兑付或所有地区资格。
- 推测：机制将留存余额、付费会员与消费资金结合，可能提高用户预留余额的意愿。
- 待验证假设：是否增加持续自有资金消费，而不是短期逐利余额；补贴到期后的余额和会员留存未知。

#### Why It Matters to Sykka
需要比较“余额为什么留下、何时转成真实消费、奖励成本由谁承担”。可关注净入金、可用余额、持续消费和奖励成本的关联，不能只比较最高宣传比例。

#### Open Questions
- [ ] 适用国家、余额法律属性、奖励计算周期及完整资格是什么？｜核验 Reserve 条款和 App 说明｜2026-09-11。
- [ ] 引导期是否提前结束、奖励是否调整？｜官方页面及活动规则｜2026-09-11 后持续观察；2026-12-31 前复查。

#### Sources
- S1｜[Introducing USD Reserve Account](https://www.kast.xyz/blog/usd-reserve-account)｜KAST 官方｜页面更新 2026-09-03，查阅 2026-09-07｜浏览器核验；首次发布日期未知，完整法律条款及账户内资格尚未核验。

### KA-002｜KAST 用每日猜拳解锁限时消费返现加倍

- Priority: P1
- Status: Confirmed
- First Seen: 2026-09-07
- Last Updated: 2026-09-07
- Monthly Review: 无（尚无已核验的月报引用）
- 本轮判定：NEW（本周官方更新，首次上线日期待确认）

#### What Happened
官方 9 月 1 日更新的说明称，用户每日在 23:30 UTC 前选一次石头、剪刀或布，00:00 UTC 公布结果；获胜后自动启用 24 小时返现提升，普通轮次为 2 倍，特定轮次以 App 为准。适用于支持市场、完成验证且有有效卡的合格会员；参与选择免费，原有返现上限与合格消费规则继续适用。[S1]

#### Timeline
- 2026-09-01｜官方页面更新，并明确日循环、奖励窗口及基本资格。[S1]
- 2026-09-07｜首轮核验后入库；没有效果数据，不认定活动已提高消费留存。

#### Current Assessment
- 事实：公开机制为“每日选择 → 回访看结果 → 限时消费奖励”，不是无条件额外返现。
- 推测：将 App 回访动机连接至短期消费窗口。
- 待验证假设：App 活跃增长是否转化成增量消费，还是仅将原有消费挪到奖励期。

#### Why It Matters to Sykka
可作为增长实验设计参照：分开衡量游戏参与、奖励激活、真实消费增量和奖励成本。观察方法值得借鉴，尚无证据支持直接复制活动。

#### Open Questions
- [ ] 完整上限、排除交易、平局规则和结束时间是什么？｜活动条款与 App｜2026-09-11。
- [ ] 是否出现规则调整或可靠效果数据？｜官方后续及公开研究｜2026-09-11 复查。

#### Sources
- S1｜[Daily Rewards Are Back with Rock Paper Scissors](https://www.kast.xyz/blog/daily-rewards-rock-paper-scissors)｜KAST 官方｜页面更新 2026-09-01，查阅 2026-09-07｜浏览器核验；未核验完整活动条款或运营成效。

### IND-001｜Ethena Pay 将 USDe 延伸到面向消费者的支付应用

- Priority: P1
- Status: Confirmed
- First Seen: 2026-09-07
- Last Updated: 2026-09-07
- Monthly Review: 无（尚无已核验的月报引用）
- 本轮判定：NEW

#### What Happened
Ava Labs 于 9 月 1 日宣布 Ethena Pay 已推出，围绕 USDe 余额提供持有、转账和消费界面，底层采用 Avalanche，连接 Visa 消费场景。该文称 iOS 已可用，Android、美国及欧盟开放仍属后续计划。[S1]

当前地区页列出 48 个国家/地区；与发布稿“50 多个”及 9 月 2 日媒体“49 个”的说法不一致。本记录使用 9 月 7 日产品地区清单作为当前范围，不将国家数差异直接解释为退出市场。[S2][S3]

#### Timeline
- 2026-09-01｜Ava Labs 发布上线公告。[S1]
- 2026-09-02｜媒体补充介绍，但其覆盖数不等于当前官方清单。[S3]
- 2026-09-07｜核验产品地区页：48 个国家/地区，美国、欧盟等仍列为后续开放。[S2]

#### Current Assessment
- 事实：发布公告与产品地区清单存在；Confirmed 不代表全部用户可无条件开通，亦未实测资金链路。
- 推测：USDe 的发行生态在向直接消费者分发延伸，新增“持有 → 转账 → 消费”的竞争入口。
- 待验证假设：实际开放规模、使用留存、地区限制及经济可持续性；不采信未经原始证据验证的用户数量。

#### Why It Matters to Sykka
雷达范围应包括稳定币或合成美元发行生态自建应用。比较产品时同时看底层资产、退出路径和真实可用地区，不能只比较卡权益。

#### Open Questions
- [ ] 48 / 49 / 50+ 差异源自统计方法、更新还是资格调整？｜对照地区清单和发布方修订｜2026-09-11。
- [ ] Android、美国及欧盟何时实际开放？｜官方公告与商店｜2026-09-11 复查。

#### Sources
- S1｜[Ethena Pay on Avalanche](https://www.avax.network/about/blog/ethena-pay-shows-how-avalanche-is-powering-the-next-generation-of-neobanks)｜Ava Labs 合作方公告｜发布 2026-09-01，查阅 2026-09-07｜支持上线及方向，非独立运营审计。
- S2｜[Available Jurisdictions](https://pay.ethena.fi/jurisdictions)｜Ethena Pay 官方｜发布日期未标，查阅 2026-09-07｜当前列表 48；功能另有资格限制。
- S3｜[Ethena Launches Ethena Pay](https://stablecoininsider.org/ethena-launches-ethena-pay-on-avalanche/)｜Stablecoin Insider｜发布 2026-09-02，查阅 2026-09-07｜仅用于记录来源口径差异。

### Active Signal 复制模板

以下模板不占用 ID。

```markdown
### <RD/KA/IND-NNN>｜<事件名称>

- Priority: <P0 / P1>
- Status: <Watching / Developing / Confirmed>
- First Seen: <本系统首次发现日期>
- Last Updated: <最近实质更新日期>
- Monthly Review: <无；纳入后追加月报链接，月份为 YYYY-MM，可多个>

#### What Happened
<事实摘要；实际发生日期、对象、地区、平台、产品及适用限制。未知写待确认。>

#### Timeline
- <YYYY-MM-DD>｜<新增事实、证据或状态变化>｜<来源 S1>
- <YYYY-MM-DD>｜<后续进展；与此前相比新增什么>｜<来源 S2>

#### Current Assessment
- 事实：<已确认什么，引用来源>
- 推测：<当前解释及依据；无则写无>
- 待验证假设：<尚不能确认什么，如何验证>

#### Why It Matters to Sykka
<影响哪项产品、增长、市场或商业化判断；建议验证什么。涉及 Sykka 现状注明依据及日期，未知写待确认。>

#### Open Questions
- [ ] <问题>｜验证方式：<查什么>｜下次复查：<日期或触发条件>

#### Sources
- S1｜[原始标题](URL)｜发布者 / 来源类型｜发布日期：<日期>｜查阅日期：<日期>｜支持：<具体事实>｜限制：<声明、样本、口径或访问限制>
- S2｜[原始标题](URL)｜发布者 / 来源类型｜发布日期：<日期>｜查阅日期：<日期>｜支持：<具体事实>｜限制：<限制>
```

Timeline 按时间顺序追加，更正保留原判断及理由。First Seen 不随报道变化；证据、判断、状态或问题实质变化才更新 Last Updated。例行复查无变化只更新文档最近维护日期。来源编号在事件内唯一。

Monthly Review 记录实际纳入过的月报月份，使用链接列表，如 `[2026-09](monthly/2026-09.md), [2026-10](monthly/2026-10.md)`；不提前登记尚未生成的月报，不覆盖旧月份，同月不重复。仅回填月报引用不改变事件 Last Updated；关闭或重开事件时保留该字段。

## Closed Signals

当前无已关闭事件。关闭时将完整条目从 Active 移到本节，保留 ID、Timeline、Sources、Monthly Review，Status 改为 Closed，补充：

- Closed On: <关闭日期>
- Closure Reason: <结束 / 被证伪 / 暂无跟踪价值 / 合并至某 ID>
- Final Assessment: <最终结论及尚未解决的限制>
- Reopen If: <重新跟踪的证据或条件>

## 每日 NEW / UPDATE / DUPLICATE / COMMENTARY 判定

先读取近期日报及 Tracker（含 Closed），按“主体 + 事项 + 地区 / 产品 + 发生时间”做事件级比较，不按标题或媒体去重。覆盖前一自然日新出现、新确认或明显变化的信息，同时检查 Active Signals。

| 判定 | 条件 | 处理 |
| --- | --- | --- |
| NEW | 未跟踪过的独立事件，有价值的新事实或信号 | 按优先级进入日报，符合条件的列为每周入库候选 |
| UPDATE | 已有事件新增事实、证据、范围、数据、落地进度或反证 | 引用原 ID，写此前 / 本次新增 / 当前判断，每周补入原 Timeline |
| DUPLICATE | 同一事实换媒体、标题或措辞传播，无实质增量 | 不重复推送或新增事件，必要时补更可靠来源 |
| COMMENTARY | 评论、采访、预测或观点，没有新事实 | 默认过滤；有战略价值时注明作者及观点属性，不作为事实确认依据 |

采访披露可核验新事实时，事实部分按 NEW / UPDATE 处理。新文章不等于新事件；迟发现的旧事标明实际发生日期及迟发现原因。无法读取历史或 Tracker 时注明“去重覆盖不足”，不声称完成全量去重。

日报默认 3–5 条，以 P0/P1 为主，不凑数。每条含“优先级 / 判定 / 已有事件 ID → 发生了什么 → 对 Sykka 的意义 → 来源”。无重要增量则说明无值得关注的 P0/P1 动态。日报提及不代表已写入 GitHub。

## P0 / P1 / P2 优先级

| Priority | 标准 | 典型情况与处理 |
| --- | --- | --- |
| P0 | 需及时知晓，可能直接改变产品、市场或竞争判断 | 核心能力、重要市场或费率变化、牌照、大型合作、重大融资与规模披露、大规模事故；优先推送并入库 |
| P1 | 有明确相关性和信息增量，值得观察但尚不改变整体判断 | 重要版本、其他竞品新能力、集中 VOC、支付基础设施或监管变化、市场异常增长；推送，需持续跟踪时入库 |
| P2 | 对判断影响小或增量有限 | 普通 PR、小活动、单个投诉、无新增事实的采访；默认过滤 |

综合 Sykka 相关性、影响程度、信息可信度、新颖性排序，不做机械分数乘法，不按热度排序。主体关注顺序不等于事件优先级，不是每条 RedotPay/KAST 消息都为 P0。重复信息先过滤，即使原事件为 P0 也不重复推送；重大监管及基础设施变化可升 P0。

Priority 表示关注程度，Status 表示证据和跟踪阶段，两者独立。高影响但未核实的信号可优先核查，必须标待确认，不因 P0 就认定属实。

## 首轮扫描记录｜2026-09-07

- 窗口：2026-09-01 00:00 至 2026-09-07 18:47，Asia/Shanghai；含今日未完整自然日。8 月材料只作背景或排除项，不冒充本周新闻。
- 结果：新增 RD-001、KA-001、KA-002、IND-001；无已有事件更新或关闭。P0 1 条、P1 3 条。所有 First Seen 为本系统首次发现日，不是事件发生日。
- 去重范围：当前 Tracker 为空、没有可读取的历史日报集合；仅完成本轮候选之间去重，未声称覆盖全部历史推送。
- 已覆盖：品牌与业务词的限定日期网页检索；RedotPay News、KAST Blog 实时页面及选中文章；KAST Business、Ethena Pay 产品页与合作方公告；用户反馈搜索结果。搜索缓存落后于实时页面，已改用浏览器核验核心竞品正文。
- 缺口：未系统遍历全部官方 X / LinkedIn 帖文，未拉取 App Store / Google Play 全量版本或评论，未读取付费行业数据；不能将未发现解释为没有变化。后续优先补社媒及商店版本覆盖。

| 候选 / 来源 | 本轮处理及理由 |
| --- | --- |
| [KAST Business 9 月报道](https://www.cryptocards.guru/blog/kast-business-account-team-cards/) 与[产品页](https://www.kast.xyz/business) | 待补证：当前产品页可核实账户、团队卡及申请入口，但早期官方博客已有 Business 预告；“9 月 1 日首发”只有二手说法，尚不能区分首次发布与新阶段。2026-09-11 查原始日期及发布变化，不计本轮 NEW。 |
| [MAS 稳定币咨询报道](https://www.crowdfundinsider.com/2026/09/305006-monetary-authority-of-singapore-mas-considers-ban-on-interest-for-regulated-stablecoins/) | 待补证：报道指向[MAS 原文](https://www.mas.gov.sg/news/media-releases/2026/mas-consults-on-legislative-amendments-to-implement-stablecoin-regulatory-framework)，当前返回维护页。2026-09-11 优先复查原文，尚不把禁止付息或实施日期作为法律事实入库。 |
| [KAST SEPA 活动](https://www.kast.xyz/blog/sepa-deposit-spend-cashback) | 旧活动仍在进行：页面更新 8 月 30 日，活动从 8 月 21 日开始。本周无已核实规则变化，保留作下轮增长研究候选，不算本周新增。 |
| [September Supercharge](https://www.kast.xyz/blog/september-supercharge-earn-up-to-3x-points) | 排除旧闻：正文明确是 2025 年 9 月，不能因标题含 September 当作本周活动。 |
| [RedotPay 单条投诉](https://www.reddit.com/r/CryptoCurrency/comments/1w5450b/warning_redotpay_traps_users_with_microfees_bad/)及[近似重复帖](https://www.reddit.com/r/CryptoCurrency/comments/1w546ns/title_warning_redotpay_traps_users_with_microfees/) | P2 / 重复候选：不足以证实集中异常或故障原因，未作为两个独立用户信号入库。 |
| [Visa 结算融资文章](https://www.visa.com/en-us/thought-leadership/innovation/financing-stablecoin-linked-card-programs) | 排除：页面标注 2026-09-08，晚于扫描截止日期，不引用其数字形成当日判断。 |

下次维护：2026-09-11。优先补 KA-001 的完整条款、MAS 原文及 KAST Business 日期，再检查四个 Active Signals。未创建或修改任何自动任务。

## 每周维护 Checklist

每周五回顾过去 7 天日报及全部 Active Signals；上次维护更早则补查遗漏区间。主要维护 Active Signals 的 Timeline、Last Updated、Status、Current Assessment，并关闭已结束事件；不例行改写整体竞争判断，不追加周维护日志。

- [ ] 读取 GitHub 最新文件，确认最近维护日期、编号、日报覆盖范围，记录来源或历史缺口。
- [ ] 筛选新增：仅将 P0 和需持续跟踪的 P1 入库；先查 Active / Closed 去重，再分配 ID。
- [ ] 更新进展：核验原始来源，追加 Timeline，注明新增事实、反证及地区 / 平台 / 时间范围；有实质变化才刷新 Last Updated。
- [ ] 校准判断：分别更新 Priority、Status、Current Assessment，不把社区信号或营销声明扩大为已确认结论。
- [ ] 复查问题：处理 Open Questions，为未解决问题填写验证方式及下次复查日期 / 触发条件。
- [ ] 关闭或重开：结束、证伪、合并或无持续价值的事件移至 Closed，保留全文、理由及重开条件。
- [ ] 检查重大 P0：只有新增证据足以改变整体判断才周中调整 Current Competitive View，记录依据及 Last Reviewed；其余留待月结复核。
- [ ] 检查质量：ID 唯一，来源可追溯，日期与数据口径齐全；失效来源标记并补证据，不删除历史。
- [ ] 提交前重读远端，避免覆盖他人变更；只提交本次维护文件，更新最近维护日期。
- [ ] 提交后读取文件核对，报告新增 / 更新 / 关闭的 ID、判断变化、未解决事项及提交链接。

建议提交说明：`维护竞品情报：YYYY-MM-DD，新增 N / 更新 N / 关闭 N`。无实质变化仅更新文档最近维护日期；覆盖范围和缺口写在提交说明或当次交付，不向 Tracker 追加周日志，不制造事件更新。先运行 1–2 周，再根据漏报、重复、优先级及 Sykka 相关性调整规则。
