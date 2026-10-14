# 投资心理教练（invest-psych-coach）

只管心态、不管买卖的投资心理教练。基于行为金融学方法论，帮用户做情绪化操作复盘、三大心理偏差自查与投资纪律建设。

> 纯投资教育内容。不荐股、不预测行情、不建议仓位，每轮回复自带免责声明。

## 包结构（官方专家包规范）

```
invest-psych-coach/
├── .codebuddy-plugin/
│   └── plugin.json                  # 核心配置：分类 08-FinanceInvestment、展示文案、快捷提示词
├── avatars/
│   └── expert.png                   # 512×512 头像
├── agents/
│   └── invest-psych-coach.md        # Agent 系统提示词：人设 + 红线 + 5 场景 + 3 附录
└── README.md
```

## 五大工作场景

| 场景 | 触发 | 动作 |
|---|---|---|
| A 情绪化操作复盘 | "我又追涨杀跌了" | 五问归因 → 生成心理复盘卡 |
| B 三大偏差自查 | 描述决策困惑 | 损失厌恶/沉没成本/FOMO 判定 → 单点干预 |
| C 投资纪律建设 | 情绪平稳期 | 制定投资原则卡 + 季度自检机制 |
| D 认知卡教学 | 想系统学习 | 8 张认知卡：一次一张，讲完出题，答完解析 |
| E 被套心理疏导 | 情绪激动 | 共情接住 → 事实与情绪分离（不谈去留） |

## 合规设计

- 系统提示词写死 6 条绝对红线：不荐股、不预测、不建议仓位，用户追问时温和拒绝并引导回心理层面
- 概念讲解中出现的标的名称一律替换为"某资产"
- 每轮回复末尾固定附加免责声明
- 市场分类：`08-FinanceInvestment`（金融投资）

## 打包提交

```powershell
Compress-Archive -Path .codebuddy-plugin, avatars, agents, README.md -DestinationPath ..\invest-psych-coach.zip -Force
```

提交至 WorkBuddy 开放平台「专家」类目，市场分类选择**金融投资**。

## License

CC BY 4.0
