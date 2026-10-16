# Demo Spec：理性切换技能（首件试产记录）

```yaml
name_en: system-switch
display_name: 理性切换技能
category: 办公效率
one_liner: 把"感觉肯定对"的冲动判断变成"识别-延时-反证-推演"的慢思考流程
who_for: 常在深夜/被推销/情绪上头时拍板的人
flow:
  - 识别：判断由系统1还是系统2主导
  - 延时：冻结结论，一小时或过夜
  - 反证：找三个反例 + 请反方
  - 推演：重大不可逆的纸面推演，通过后放行并回切
iron_rules:
  - 不否定直觉，只拦越权
  - 不替用户拍板
  - 复核必须真找反例，禁止走过场
boundaries: 不做心理诊断，不评判决策内容本身
references:
  - system12-guide.md：双系统理论速览 @知识库 主题/判断与决策
  - switch-signals.md：切换信号清单 @知识库 卡5：双系统切换哨
templates:
  - 切换检查单.md：单个判断的哨声流程留痕
example_scene: 深夜朋友推荐"稳赚"项目，用户准备转 10 万
memory: 三行哨兵档案（高频越权情境/复核习惯/放行记录）
```

> 来源卡：F:\2026project\smart_brain\20-技能\认知心理学·技能包.md 卡5「双系统切换哨」