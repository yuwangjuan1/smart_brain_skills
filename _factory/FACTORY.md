# FACTORY：Spec → 技能包 生产指令

> 给 AI 的流水线操作手册。输入：一份填好的 SPEC；输出：可上传的技能包 + zip。

## 生产流程（六道工序）

1. **验料**：spec 是否填满？one_liner 与 iron_rules 缺一退回。
2. **起包**：建目录 `{name_en}/`，按 decision-skill 包结构生成骨架。
3. **写 SKILL.md**：六段固定结构，不许增删顶层段落—
   一你是谁（信念 2-3 条） / 二铁律 / 三开场分流 / 四主流程（每步引用 references）/ 五跨轮记忆 / 六输出与边界。
   frontmatter 字段照抄 decision-skill/SKILL.md。
4. **写 references**：按 spec 逐份生成；纯方法论，不放流程；文首标"用在哪"。
5. **写 templates + examples**：模板可直接空表使用；demo 必须虚构、完整走完全流程。
6. **打包质检**：
   - 全文搜 ·—→{TRI} 等占位符，必须为零；
   - 字符数：SKILL.md 3-6KB，references 单份不超 4KB；
   - 打包（中文文件名必须用 .NET，禁 Compress-Archive）：
     `Add-Type -AssemblyName System.IO.Compression.FileSystem; [IO.Compression.ZipFile]::CreateFromDirectory("src","dst.zip","Optimal",$true)`
   - git add + commit + push。

## 质量门（六条全过才出厂）

- [ ] 六段结构完整，铁律含"不替用户拍板"
- [ ] demo 从开场分流走到交付，含至少一次"回炉/拒绝"分支
- [ ] zip 解包检查文件名无乱码
- [ ] frontmatter 值含半角冒号（xx: yy）必须用双引号包裹整个值，否则 YAML 解析失败
- [ ] 更新已上架的包：版本号必须大于平台现存最新版本（如 1.0.0 递增到 1.1.0），否则解析被拒
- [ ] 专家包 plugin.json：defaultInitPrompt 的 en/zh 必须与 quickPrompts[0] 完全一致，否则解析被拒

## 产能节奏

- 每批 3-5 个，方向错开（认知/逻辑/系统各一）。
- 上架有章法：传平台 → 过审 → 更新展示站，一批一批来。