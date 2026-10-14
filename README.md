# WorkBuddy Skills

个人自研的 WorkBuddy / Claude 技能包合集。每个技能都从真实使用场景中来，长期迭代。

## 技能列表

### [第二大脑建造师](second-brain-builder/) `v1.0.0`

从零搭建 Obsidian 第二大脑知识库：

- 3 套目录方案（最小可用 / 标准版 / 创作驱动版）
- Frontmatter 元数据规范 + 笔记三态生长模型（🌱🌿🌲）
- 错题集方法论：五问结构、三类错因、复盘节奏
- 领域包建设 D2 五步流程 + 七件套结构

适用：想建知识库 / 笔记混乱需要重构 / Obsidian 入门 / 学了就忘。

## 目录结构

```
workbuddy-skills/
└── second-brain-builder/    # 技能包（zip 打包后可上传 WorkBuddy 开放平台）
    ├── SKILL.md             # 技能主指令
    ├── references/          # 方法论文档
    ├── templates/           # 可复制模板
    └── examples/            # 虚构示例
```

## 打包上传

```powershell
Compress-Archive -Path second-brain-builder -DestinationPath second-brain-builder.zip -Force
```

然后到 [WorkBuddy 开放平台](https://open.workbuddy.cn/) 上传 zip 提交审核。

## License

技能与方法论采用 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh)——欢迎自由使用、修改、分发，注明出处即可。
