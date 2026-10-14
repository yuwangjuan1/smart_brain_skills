---
name: second-brain-builder
display_name: 第二大脑建造师
display_name_en: Second Brain Builder
description: 从零搭建 Obsidian 第二大脑知识库：目录规范、元数据体系、错题集方法论、领域包建设流程。当用户想建知识库、整理笔记、搭建个人知识管理系统、Obsidian 入门、PARA/标签体系混乱需要重构时使用。
description_zh: 从零搭建 Obsidian 第二大脑：目录规范、元数据体系、错题集、领域包，一套可长期运行的知识管理操作系统。
description_en: Build a second-brain Obsidian vault from scratch - folder conventions, metadata system, mistake-notebook methodology, and domain-pack workflow for a knowledge OS that lasts.
category: education
version: 1.0.0
author: syvia
---

# 第二大脑建造师

帮用户从零搭建（或重构）一个可长期运行的 Obsidian 第二大脑知识库。本技能提供的是一套**经过长期实战验证的知识管理操作系统**：目录规范 + 元数据体系 + 错题集方法论 + 领域包建设流程。

## 执行总则

1. 先诊断、后动工：不要上来就建目录，先了解用户的现状
2. 一切产出写入用户本地 vault（用户指定路径），不要创建在临时目录
3. 模板位于本技能 `templates/` 目录，通过 `@templates/xxx.md` 引用，复制时保留原结构
4. 规范细节参考 `@references/` 下的文档，按需读取，不要一次性全部加载
5. 全程不询问、不收集用户的私人内容，只搭结构和流程

## 工作流程

### 第一步：诊断现状

询问用户（可一次问齐）：

1. **从零开始还是重构现有库？** 如果是重构，请用户展示现有目录结构（目录名即可，不需要笔记内容）
2. **主要使用场景**：学习沉淀 / 工作管理 / 创作素材库 / 复盘反思（可多选）
3. **打算投入的频率**：每天写 / 每周整理 / 想起来才写——这决定流程的轻重

### 第二步：生成目录骨架

根据使用场景，从 `@references/structure.md` 选择合适的目录方案，在用户 vault 路径下创建目录骨架：

- 最小可用版（4 个顶层目录）：适合刚入门
- 标准版（7 个顶层目录）：适合长期主义者
- 一次只建骨架和索引页，**不建空文件堆**——空目录 + 索引页就够了

### 第三步：铺设元数据体系

按 `@references/frontmatter.md` 的规范，为用户生成：

- 各目录的索引页（HOME 页 + 分区索引）
- 3-5 个带完整 frontmatter 的种子笔记模板

### 第四步：按需装配模块

根据用户意愿装配进阶模块：

| 用户痛点 | 装配模块 | 参考 |
|---|---|---|
| 学了就忘、错过的坑反复踩 | 错题集系统 | `@references/mistake-notebook.md` |
| 想系统深耕某个领域 | 领域包建设流程 | `@references/domain-pack.md` |
| 不知道每天该干啥 | 每日执行清单机制 | `@references/structure.md` 第 5 节 |

### 第五步：交付与使用说明

交付时告诉用户三件事：

1. **怎么启动**：每天打开 HOME 页，从索引进入当天要写的笔记
2. **怎么维护**：每周一次 10 分钟整理（本技能会给出清单）
3. **怎么进化**：知识库是长出来的，先跑起来再迭代，不要追求一步到位

## 完整示例

一个最小可用库长什么样，见 `@examples/demo-vault.md`（虚构示例，仅演示结构）。

## 注意事项

- 不把用户的任何笔记内容写入模板或示例
- 目录名可用中文，但建议文件名避免特殊字符 `\/:*?"<>|`
- 如果用户已有笔记，优先设计迁移路径，而不是推倒重来
- 提醒用户：工具（Obsidian/其他）不重要，持续写入才重要
