# WorkBuddy Skills

个人自研的 WorkBuddy 技能包与专家包合集。每个作品都从真实使用场景中来，长期迭代。

## 命名规则

一经定稿不再改动。专家与技能走两套命名法，听名字即知身份：

1. **专家用花名**：青字辈，两字、常见字，取雅物系意象（花草果实、香草、颜料玉器等陪人养人的雅物）：青黛、青杏、青棠、青梧、青柠、青芷、青蘅、青竹。
2. **技能不用花名**：直接「职能+技能」，如 利弊决策技能——朴素直给，一眼可用。
3. **花名唯一**：专家花名永不复用，市场上每个都是独立商品，同名即内耗。
4. **标题格式**：专家=花名 · 职能+专家（如「青黛 · 投资心理专家」）；技能=职能+技能（如「利弊决策技能」）。
5. **英文目录名**：与花名或职能对应，如 decision-skill、invest-psych-coach。

## 作品列表
### 青黛 · 投资心理专家（invest-psych-coach）

只管心态不管买卖的投资心理教练：复盘情绪化操作，识别损失厌恶、沉没成本与追涨偏差，建立投资纪律。已上架 WorkBuddy 开放平台。

### 青杏 · 志愿填报策略专家（gaokao-strategy）

只管策略不管数据的高考志愿教练：等位分定位、冲稳保梯度排布、防滑档防退档终检、平行志愿规则科普，出分后 72 小时应急。纯方法论口径，数据一律引导官方渠道自查。

### 青棠 · 专业定位顾问专家（major-fit）

用证据选专业的定位顾问：兴趣-能力-出口三角定位、专业名称祛魅（十大名称陷阱排查表）、培养方案核查、就业出口前瞻、专业组调剂风险评估。不下「专业好坏」结论，只给核查方法。

### 青梧 · 家庭志愿调解专家（family-mediation）

志愿分歧的家庭调解师：把立场翻译成需求、先对齐十年目标再谈选项、城市学校专业三角交换谈判，主持家庭志愿会议产出家庭志愿公约。不站队不拍板，心理危机信号转介专业咨询。

### 利弊决策技能（decision-skill）

用「五步决策手术」（定诊、拆解、验尸、推演、开方）把纠结、冲动、事后后悔的决策拆开；内置道法术器四层透视、偏差解毒七查与决策备忘卡。

### 理性切换技能（system-switch）

在冲动与拖延之间装一个思维哨兵：识别判断由快直觉还是慢推理主导，用识别、延时、反证、推演四步强制切换系统2，交付切换检查单。

### 儿童情绪解读技能（emotion-decode）

把孩子的哭闹、顶嘴、拖延、粘人翻译成情绪信号：停判、解码、接绪、立规复盘四步解码，附行为对照密码本与情绪解码记录卡。

### 成长型思维养育技能（growth-mindset）

把「你真聪明」「你看看人家」改造成指向过程与成长的语言：捕捉、分类、改写、固化四步，附表扬话术改造表与考砸话术。

### 亲子沟通技能（parent-talk）

先接情绪、再处理事情的对话四步：闭嘴听、译感受、接情绪、议事情，替代说教与吼叫，附非暴力沟通亲子版与七大倾听陷阱清单。

### 学习习惯养成技能（study-habits）

诊断作业大战的真实卡点（启动难/分心/畏难/真不会），设计提示-程序-奖励的小习惯回路并外置清单计时器，家长五周逐步退出。

### 第二大脑建造师（second-brain-builder）

从零搭建 Obsidian 第二大脑知识库：3 套目录方案、Frontmatter 元数据规范、笔记三态生长模型、错题集方法论、领域包 D2 五步流程。

## 目录结构

```
workbuddy-skills/
|-- invest-psych-coach/      # 专家包（plugin.json + agents + avatars）
|-- gaokao-strategy/         # 专家包（高考志愿：青杏）
|-- major-fit/               # 专家包（专业定位：青棠）
|-- family-mediation/        # 专家包（家庭调解：青梧）
|-- decision-skill/         # 技能包（SKILL.md + references + templates + examples）
|-- system-switch/           # 技能包（技能工厂首件试产）
|-- second-brain-builder/    # 技能包
|-- emotion-decode/          # 技能包（育儿系列）
|-- growth-mindset/          # 技能包（育儿系列）
|-- parent-talk/             # 技能包（育儿系列）
|-- study-habits/            # 技能包（育儿系列）
|-- _factory/                # 技能工厂：SPEC 模板 + 生产指令 + 试产样例
`-- *.zip                    # 各自打包产物，上传 WorkBuddy 开放平台
```

## 打包上传

注意：技能包含中文文件名的模板，Compress-Archive 会损坏文件名编码，请用 .NET 打包：

```powershell
Add-Type -AssemblyName System.IO.Compression.FileSystem
[IO.Compression.ZipFile]::CreateFromDirectory("decision-skill","decision-skill.zip",[IO.Compression.CompressionLevel]::Optimal,$true)
```

然后到 WorkBuddy 开放平台上传 zip 提交审核。

## 技能工厂

批量生产走 `_factory/`：复制 `SPEC-TEMPLATE.md` 填一页 spec → 按 `FACTORY.md` 六道工序生成整包 → 过三条质量门出厂。知识库技能卡（一卡一包）可直接作 spec，试产样例见 `demo-spec.md`。

## License

技能与方法论采用 [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/deed.zh)——欢迎自由使用、修改、分发，注明出处即可。