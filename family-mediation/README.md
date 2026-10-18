# 家庭志愿调解师（family-mediation）

志愿分歧的家庭调解师。立场翻译成需求、目标对齐先行、城市学校专业三角交换谈判、家庭志愿会议主持，产出家庭志愿公约。

> 纯沟通流程辅导。不站队、不替家庭拍板、不做心理治疗（危机信号转介专业咨询），每轮回复自带免责声明。

## 包结构（官方专家包规范）

```
family-mediation/
├── codebuddy-plugin/
├──   ├── plugin.json           # 核心配置：分类 09-EducationLearning、展示文案、快捷提示词
├── avatars/
├──   ├── expert.png            # 512x512 头像
├── agents/
├──   ├── family-mediation.md   # Agent 系统提示词：人设 + 红线 + 5 场景 + 3 附录
├── README.md
```

## 五大工作场景

| 场景 | 触发 | 动作 |
|---|---|---|
| A 立场翻译 | 家庭为志愿争执 | 收集立场 → 翻译需求 → 回放确认 → 需求翻译表 |
| B 目标对齐 | 翻译完成后 | 十年后生活想象 → 找交集定总纲 → 标差异后议 |
| C 交换谈判 | 需求摆清后 | 三角交换配对 → 组合 2 套方案 → 每套附对冲预案 |
| D 家庭志愿会议 | 分歧进入深水区 | 议程 + 发言规则 + 决策权阶梯 → 家庭志愿公约 |
| E 僵局疏导 | 谈崩/冷战/翻旧账 | 休会 48 小时 + 降温作业 → 最小共识复谈 → 必要时转介 |

## 合规设计

- 系统提示词写死 5 条绝对红线：不站队、不替家庭拍板、不做心理治疗、不评价对错
- 三类典型冲突（安全型/补偿型/放养遇反弹）只翻译恐惧不贴标签
- 每轮回复末尾固定附加免责声明，危机信号优先转介
- 市场分类：`09-EducationLearning`（教育学习）

## 打包提交

```powershell
Compress-Archive -Path .codebuddy-plugin, avatars, agents, README.md -DestinationPath ..\family-mediation.zip -Force
```

提交至 WorkBuddy 开放平台「专家」类目，市场分类选择**教育学习**相关类目。

## License

CC BY 4.0