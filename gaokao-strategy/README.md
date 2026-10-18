# 志愿填报策略教练（gaokao-strategy）

只管策略、不管拍板的高考志愿教练。帮家庭做位次定位、冲稳保梯度设计、平行志愿规则科普与防滑档防退档终检。

> 纯方法论与策略教育。不提供分数线数据、不承诺录取结果，每轮回复自带免责声明。

## 包结构（官方专家包规范）

```
gaokao-strategy/
├── codebuddy-plugin/
├──   ├── plugin.json              # 核心配置：分类 09-EducationLearning、展示文案、快捷提示词
├── avatars/
├──   ├── expert.png               # 512x512 头像
├── agents/
├──   ├── gaokao-strategy.md       # Agent 系统提示词：人设 + 红线 + 5 场景 + 3 附录
├── README.md
```

## 五大工作场景

| 场景 | 触发 | 动作 |
|---|---|---|
| A 等位分定位 | 给出分数或位次 | 位次为锚定选池 → 生成等位分定位卡 |
| B 冲稳保梯度排布 | 有了选池要排志愿 | 分池 → 定比例 → 排顺序 → 生成梯度排布表 |
| C 防滑档退档终检 | 梯度排完 | 退档三雷 + 滑档压力测试 → 生成终检清单 |
| D 平行志愿规则科普 | 问规则 | 排队进场比喻讲三大原则 + 认知卡出题 |
| E 出分后 72 小时应急 | 马上要交表 | 最短路径模式，保住保底段与退档清零 |

## 合规设计

- 系统提示词写死 5 条绝对红线：不替用户拍板、不提供分数线数据、不承诺录取、不暗示内部渠道
- 所有数据一律引导用户查省考试院官网、一分一段表、高校招生章程
- 每轮回复末尾固定附加免责声明
- 市场分类：`09-EducationLearning`（教育学习）

## 打包提交

```powershell
Compress-Archive -Path .codebuddy-plugin, avatars, agents, README.md -DestinationPath ..\gaokao-strategy.zip -Force
```

提交至 WorkBuddy 开放平台「专家」类目，市场分类选择**教育学习**相关类目。

## License

CC BY 4.0