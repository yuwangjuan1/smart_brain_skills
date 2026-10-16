# WorkBuddy Skills

个人自研的 WorkBuddy 技能包与专家包合集。每个作品都从真实使用场景中来，长期迭代。

## 命名规则（青字辈家族）

所有技能与专家统一按以下规则命名，一经定稿不再改动；身份判定以标题后缀为准，花名意象池为辅助信号：

1. **统一前缀**：花名一律「青」字辈，两字、常见字——见「青X」即知是本系列出品。
2. **花名唯一**：每个技能 / 专家使用不同花名，永不复用——市场上每个都是独立商品，同名即内耗（搜索冲突、互相淹没）。
3. **意象池区分（雅物 / 利器）**：专家是陪你成长的人，名字要温；技能是替你干活的工具，名字要利。口诀：雅物为师，利器为用。
   - 专家池 · 雅物系（花草果实、香草、颜料玉器等陪人养人的雅物）：青黛、青杏、青棠、青梧、青柠、青芷、青蘅、青竹
   - 技能池 · 利器系（毒物、利器、猛禽、寒霜等干活锋利的利器）：青罂、青隼、青鸦、青砥、青锋
4. **标题格式**：花名 · 职能+身份，如「青黛 · 投资心理专家」「青罂 · 决策技能」。
5. **英文目录名**：花名拼音 + 职能英文，如 qingpeng-decision，与花名保持对应。

## 作品列表
### 青黛 · 投资心理专家（invest-psych-coach）

只管心态不管买卖的投资心理教练：复盘情绪化操作，识别损失厌恶、沉没成本与追涨偏差，建立投资纪律。已上架 WorkBuddy 开放平台。

### 青罂 · 决策技能（qingpeng-decision）

用「五步决策手术」（定诊、拆解、验尸、推演、开方）把纠结、冲动、事后后悔的决策拆开；内置道法术器四层透视、偏差解毒七查与决策备忘卡。

### 第二大脑建造师（second-brain-builder）

从零搭建 Obsidian 第二大脑知识库：3 套目录方案、Frontmatter 元数据规范、笔记三态生长模型、错题集方法论、领域包 D2 五步流程。

## 目录结构

```
workbuddy-skills/
|-- invest-psych-coach/      # 专家包（plugin.json + agents + avatars）
|-- qingpeng-decision/       # 技能包（SKILL.md + references + templates + examples）
|-- second-brain-builder/    # 技能包
`-- *.zip                    # 各自打包产物，上传 WorkBuddy 开放平台
```

## 打包上传

注意：技能包含中文文件名的模板，Compress-Archive 会损坏文件名编码，请用 .NET 打包：

```powershell
Add-Type -AssemblyName System.IO.Compression.FileSystem
[IO.Compression.ZipFile]::CreateFromDirectory("qingpeng-decision","qingpeng-decision.zip",[IO.Compression.CompressionLevel]::Optimal,$true)
```

然后到 WorkBuddy 开放平台上传 zip 提交审核。

## License

技能与方法论采用 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh)——欢迎自由使用、修改、分发，注明出处即可。