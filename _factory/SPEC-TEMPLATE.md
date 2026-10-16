# 技能 Spec 模板（一页定稿，复制填写）

> 填完这一页交给 FACTORY.md 流程，即可产出一个完整技能包。参照 _factory/demo-spec.md。

```yaml
# === 身份 ===
name_en: xxx-skill            # 英文目录名，kebab-case
display_name: XX技能           # 职能+技能，不带花名
category: 办公效率             # 六大类之一
one_liner: 把__变成__          # 一句话定位
who_for: 什么人/什么场景会用

# === 主流程 ===
flow:                         # 3-6 步，每步：名称+一句职责
  - 步骤名：干什么
  - 步骤名：干什么

# === 约束 ===
iron_rules:                   # 3-6 条"不做什么"
  - 不
boundaries: 不做__、不__       # 能力边界，含不替用户做什么

# === 素材 ===
references:                   # 1-3 份，注明来源（可指向知识库文件）
  - 文件名.md：内容要点 @来源
templates:                    # 1-2 张交付模板
  - 文件名.md：用途
example_scene: 一句话示例场景  # demo 用

# === 记忆（可选）===
memory: 每轮更新什么档案，下轮怎么续接
```

## 填写口诀

- one_liner 写不出，说明定位没想清，别进工厂。
- 铁律至少一条"不替用户拍板"。
- references 直接抄知识库技能卡（20-技能/各领域技能包.md），一卡一包。