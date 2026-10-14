# 投资心理教练（invest-psych-coach）

只管心态、不管买卖的投资心理教练。基于行为金融学方法论，帮用户做情绪化操作复盘、三大心理偏差自查与投资纪律建设。

> 纯投资教育内容。不荐股、不预测行情、不建议仓位，每轮回复自带免责声明。

## 包结构

```
invest-psych-coach/
├── EXPERT.md                        # 专家主文件：人设 + 红线 + 五大工作场景 + 表达风格
├── references/
│   ├── biases.md                    # 三大偏差（损失厌恶/沉没成本/FOMO）判断标准与教练话术
│   └── concept-cards.md             # 8 张认知卡概念库（市场先生/安全边际/周期/复利…）
└── templates/
    ├── psych-review-card.md         # 心理复盘卡（五问归因 + 偏差勾选 + 下次预案）
    └── principles-card.md           # 投资原则卡（事前纪律 + 季度自检）
```

## 五大工作场景

| 场景 | 触发 | 动作 |
|---|---|---|
| A 情绪化操作复盘 | "我又追涨杀跌了" | 五问归因 → 生成心理复盘卡 |
| B 三大偏差自查 | 描述决策困惑 | 按 biases.md 判定 → 单点干预 |
| C 投资纪律建设 | 情绪平稳期 | 制定原则卡 + 季度自检机制 |
| D 认知卡教学 | 想系统学习 | 一次一张卡，讲完出题，答完解析 |
| E 被套心理疏导 | 情绪激动 | 共情接住 → 事实与情绪分离（不谈去留） |

## 合规设计

- EXPERT.md 第二节写死 6 条绝对红线：不荐股、不预测、不建议仓位，用户追问时温和拒绝并引导回心理层面
- 概念讲解中出现的标的名称一律替换为"某资产"
- 每轮回复末尾固定附加免责声明

## 打包提交

打包时**不要包含本 README**（可选，视平台要求），将 `EXPERT.md`、`references/`、`templates/` 打入 zip：

```powershell
Compress-Archive -Path EXPERT.md, references, templates -DestinationPath invest-psych-coach.zip -Force
```

提交至 WorkBuddy 开放平台「专家」类目，服务类目建议勾选：教育培训 / 投资教育（以平台当期类目为准）。

## License

CC BY 4.0
