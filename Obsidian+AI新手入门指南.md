# Obsidian + AI 新手入门：从零搭建你的第二大脑

> **适用人群**：没用过 Obsidian，或刚装好不知道怎么开始的同学
> **前置要求**：一台电脑（Windows/Mac/Linux 均可），能上网
> **预计耗时**：跟着做完核心部分约 2 小时，全部掌握约 1 周
> **最后更新**：2026-05-24

---

## 目录

1. [为什么选 Obsidian？](#一为什么选-obsidian)
2. [10 分钟装好 Obsidian](#二十分钟装好-obsidian)
3. [核心概念：5 分钟搞懂](#三核心概念-5-分钟搞懂)
4. [AI 插件选型：社区最新共识（2026）](#四ai-插件选型社区最新共识2026)
5. [实战：用 AI 搭建你的第一个知识库](#五实战用-ai-搭建你的第一个知识库)
6. [进阶：多源信息采集工作流](#六进阶多源信息采集工作流)
7. [范例：本指南是怎么写出来的](#七范例本指南是怎么写出来的)
8. [常见问题](#八常见问题)
9. [资源索引](#九资源索引)

---

## 一、为什么选 Obsidian？

**一句话**：你的笔记存在你自己的电脑上，格式是纯文本 Markdown，永远属于你。

| 对比维度 | Obsidian | Notion | 语雀/飞书文档 |
|---------|----------|--------|-------------|
| 数据存储 | **本地文件** | 云端服务器 | 云端服务器 |
| 格式 | Markdown（纯文本） | 私有格式 | 私有格式 |
| 离线使用 | ✅ 完全可用 | ❌ 需联网 | ❌ 需联网 |
| AI 集成 | 插件生态丰富 | 内置但封闭 | 有限 |
| 双向链接 | ✅ 核心功能 | 有但弱 | 无 |
| 数据迁移 | 随便拷走 | 导出麻烦 | 导出受限 |
| 价格 | **免费**（同步收费） | 免费版有限制 | 免费版有限制 |

**关键洞察**：Obsidian 的本质不是一个"笔记软件"，而是一个**本地知识图谱引擎**。你写的每一条笔记都是一个节点，双向链接就是节点之间的边。笔记越多，网络越密，AI 能挖掘的价值越大。

> 「一个好的工具应该让你专注于思考，而不是忙于操作。」——《精要主义》

---

## 二、10 分钟装好 Obsidian

### 2.1 下载安装

1. 打开 https://obsidian.md → 点击「Download」
2. 选择你的系统（Windows/Mac/Linux）
3. 安装完成后打开，会看到一个欢迎界面

### 2.2 创建第一个 Vault（知识库）

**Vault = 一个文件夹**，你所有的笔记都存在这个文件夹里。

1. 点击「Create new vault」
2. 名字建议用英文（避免路径中文乱码），比如 `my-knowledge-base`
3. 选择一个好找的位置，比如 `D:\Obsidian\my-knowledge-base`
4. 点击「Create」

> **重要**：Vault 就是普通文件夹。你可以用文件管理器直接查看、复制、备份。这是 Obsidian 的核心优势——你的数据你做主。

### 2.3 认识界面

打开 Vault 后，你会看到：

```
┌─────────────────────────────────────────────────┐
│  左侧栏            │  编辑区              │ 右侧栏  │
│  ┌──────────┐      │                      │        │
│  │ 文件浏览器 │      │  你在这里写笔记       │ 关系图谱 │
│  │ 搜索      │      │                      │ 标签    │
│  │ 标签      │      │                      │ 大纲    │
│  │ 日记      │      │                      │        │
│  └──────────┘      │                      │        │
└─────────────────────────────────────────────────┘
```

**先别管那么多**，只需要知道：
- **左侧栏**：找文件、搜内容
- **中间**：写笔记的地方
- **右侧栏**：看当前笔记的关联信息（装了插件后会更强大）

### 2.4 必做设置（5 个开关）

进入 `设置`（左下角齿轮）→ `编辑器`：

| 设置项 | 改成什么 | 为什么 |
|--------|---------|--------|
| 严格换行 | **开启** | Markdown 换行行为更符合直觉 |
| 显示行号 | **开启** | 方便定位长文档 |
| 智能缩进 | **开启** | 列表嵌套自动对齐 |

进入 `设置` → `核心插件`：

| 插件 | 开启/关闭 | 说明 |
|------|----------|------|
| 日记 | ✅ 开启 | 每天自动创建日记页 |
| 模板 | ✅ 开启 | 复用笔记格式 |
| 大纲 | ✅ 开启 | 右侧显示标题结构 |
| 关系图谱 | ✅ 开启 | 可视化笔记间的链接 |

---

## 三、核心概念：5 分钟搞懂

### 3.1 Markdown 基础语法

Obsidian 用 Markdown 写笔记。你只需要记住这几个：

```markdown
# 一级标题        → 最大的标题
## 二级标题       → 次级标题
**加粗文字**      → 加粗
*斜体文字*        → 斜体
- 列表项          → 无序列表
1. 有序列表       → 有序列表
> 引用内容        → 引用块
`代码`            → 行内代码
```代码块```      → 代码块

[链接文字](URL)   → 超链接
![[图片名.png]]  → 嵌入图片（Obsidian 特有语法）
```

**够用了**。90% 的笔记场景只需要上面这些。

### 3.2 双向链接（Obsidian 的灵魂）

这是 Obsidian 最核心的功能，也是它和普通 Markdown 编辑器的本质区别。

**普通笔记**：A 文件里提到了 B 文件，你得手动去找 B。
**双向链接**：A 链接到 B 的同时，B 自动知道"有人引用了我"。

语法：`[[笔记名]]`

```markdown
今天学了 [[Transformer架构]] 的注意力机制，
和之前看的 [[CNN基础]] 有本质区别。
```

写完之后：
- 在 `Transformer架构` 这个笔记的右侧栏，会自动显示"被 `今天的学习笔记` 引用"
- 在关系图谱里，这三个笔记会连线形成网络

**这就是"第二大脑"的核心**——不是你手动分类，而是笔记之间自动产生关联。

### 3.3 标签

在笔记任意位置加 `#标签名`：

```markdown
今天实习第一天，主要在看项目文档。
#实习 #Day1 #上电
```

之后在左侧栏的「标签」面板里，点击 `#实习` 就能看到所有带这个标签的笔记。

### 3.4 文件夹 vs 标签 vs 链接

| 维度 | 文件夹 | 标签 | 双向链接 |
|------|--------|------|---------|
| 适合 | 大类划分 | 主题标记 | 知识点关联 |
| 例子 | `/实习/`、`/课程/` | `#AI`、`#电气` | `[[注意力机制]]` |
| 限制 | 一个文件只能在一个文件夹 | 一个笔记可以有多个标签 | 无限制，随便链 |

**新手建议**：
- 文件夹别超过 3 层——太深你就不想整理了
- 标签别超过 50 个——太多了等于没有
- **多用双向链接**——这是 Obsidian 的真正威力

---

## 四、AI 插件选型：社区最新共识（2026）

> ⚠️ 以下结论来自 2025-2026 年 Reddit r/ObsidianMD 社区的实际使用反馈和对比评测，不是我编的。

### 4.1 三大主流 AI 插件对比

| 维度 | Smart Composer | Obsidian Copilot | Smart Connections |
|------|---------------|-----------------|-------------------|
| **核心能力** | 直接在笔记中写入/修改内容 | 全库聊天问答 | 发现笔记间的语义关联 |
| **AI 模型** | 多模型（Claude/GPT/Gemini/Ollama） | 多模型 | 多模型（含 Ollama 本地） |
| **直接修改笔记** | ✅ 有 diff 视图 | ❌ 只能聊天 | ❌ 只能聊天 |
| **全库检索** | ✅ 基于 Embeddings | ✅（需配置） | ✅（核心功能） |
| **MCP Server** | ✅ 支持 | ❌ | ❌ |
| **免费** | ✅ | ✅（基础功能） | ✅ |
| **社区评价** | 🥇 综合第一 | 🥉 第三 | 🥈 关联发现最佳 |
| **适合场景** | 在笔记里写东西、改东西 | 快速问答、总结 | 找关联、建上下文 |

### 4.2 新手推荐方案

**免费方案（推荐）**：
1. **Smart Composer**（主力）→ 在笔记中直接用 AI 写作/改写
2. **Smart Connections**（辅助）→ 自动发现笔记关联

**进阶方案**：
1. Smart Composer + **Claude API**（最强写入能力）
2. Smart Connections + **Ollama 本地模型**（隐私优先）
3. **Claude Cowork**（独立工具，指向 Vault 文件夹，适合批量操作）

**专业方案**：
1. Smart Composer + MCP Server（接入 Zotero 等外部工具）
2. **Agent Client 插件**（在 Obsidian 内调用 Claude Code）

### 4.3 安装 Smart Composer（手把手）

1. 打开 Obsidian → 设置 → 第三方插件 → 关闭安全模式
2. 点击「浏览」→ 搜索「Smart Composer」
3. 点击「安装」→「启用」
4. 设置 API Key：
   - 如果用 OpenAI：去 https://platform.openai.com/api-keys 生成
   - 如果用 Claude：去 https://console.anthropic.com/ 生成
   - 如果想免费：用 Ollama 本地模型（见下节）

### 4.4 免费本地 AI：Ollama 方案

不想花钱？用 Ollama 在本地跑 AI 模型：

1. 下载 Ollama：https://ollama.com/download
2. 安装后打开终端，运行：
   ```bash
   ollama pull qwen2.5:7b    # 中文能力好，7B 参数够用
   ```
3. 在 Smart Composer 设置里，模型选择 `Ollama`，地址填 `http://localhost:11434`
4. 完成——你现在有了一个完全本地、免费、隐私安全的 AI 笔记助手

> **硬件要求**：8GB 内存可跑 7B 模型，16GB 推荐。没有独显也能跑，就是慢一点。

### 4.5 Obsidian Copilot 安装

如果你更看重"全库聊天"（问 AI "我所有笔记里关于 XX 的内容总结一下"）：

1. 第三方插件 → 搜索「Copilot」→ 安装启用
2. 设置 API Key（同上）
3. 快捷键 `Ctrl+P` → 输入「Copilot: Open Chat」→ 打开聊天窗口
4. 输入问题，AI 会基于你整个 Vault 的内容回答

---

## 五、实战：用 AI 搭建你的第一个知识库

### 5.1 目录结构模板

在你的 Vault 文件夹里创建以下结构：

```
my-knowledge-base/
├── 00-Inbox/           # 收件箱：所有新想法先扔这里
├── 01-Daily/           # 日记：每天一篇
├── 02-Projects/        # 项目：实习/课题/竞赛，每个项目一个子文件夹
│   ├── 实习/
│   ├── 课程设计/
│   └── 竞赛/
├── 03-Areas/           # 领域：长期关注的知识领域
│   ├── 电气工程/
│   ├── AI技术/
│   └── 个人成长/
├── 04-Resources/       # 资源：收藏的文章、工具、教程
├── 05-Archive/         # 归档：已完成的项目、过期的笔记
└── Templates/          # 模板：复用的笔记格式
```

**核心逻辑**：新东西先进 Inbox → 定期整理到对应位置 → 项目结束移入 Archive。

> 「少即是多。不要试图一开始就设计完美的分类系统，先用起来，再迭代。」——《精要主义》

### 5.2 创建模板（自动化省时间）

在 `Templates/` 文件夹里创建 `日记模板.md`：

```markdown
# {{date:YYYY-MM-DD}} {{date:dddd}}

## 🎯 今日目标
- [ ] 

## 📝 今日记录


## 💡 今日洞察


## 🔗 相关笔记
- [[]]
```

设置 → 核心插件 → 模板 → 设置模板文件夹为 `Templates/`。

以后每天新建日记，按 `Ctrl+T` 就能自动插入这个模板。

### 5.3 用 AI 加速记笔记

装好 Smart Composer 后，在任何笔记中按 `Ctrl+J`（默认快捷键），输入：

**场景 1：会议/课堂记录整理**
```
帮我把上面的会议记录整理成结构化笔记，提取关键决策和待办事项
```

**场景 2：概念解释**
```
用通俗的语言解释什么是注意力机制（Attention Mechanism），给一个电气专业大一学生看
```

**场景 3：笔记关联**
```
分析这篇笔记和我库里哪些笔记有关联，建议我创建哪些双向链接
```

**场景 4：内容扩展**
```
基于上面的笔记大纲，展开写每一节的详细内容
```

### 5.4 双向链接实战

假设你在写实习日记：

```markdown
# 2026-05-24 实习第 3 天

今天主要在看公司的 [[电源管理系统]] 设计文档，
用到了 [[PID控制]] 的知识，和课上学的 [[自控原理]] 关联很大。

下午 leader 让我做一个 [[Buck电路仿真]]，
我用 [[MATLAB/Simulink]] 跑了一遍，发现 [[纹波电压]] 比预期大。

TODO：
- [ ] 查一下 [[纹波电压优化]] 的方法
- [ ] 把仿真结果整理成报告
```

写完之后，`电源管理系统`、`PID控制`、`Buck电路仿真` 这些笔记会自动出现在关系图谱里，点击就能跳转。等你实习结束，你的知识网络就已经自然长出来了。

---

## 六、进阶：多源信息采集工作流

> ⚠️ 这一章是本指南最有价值的部分。大多数人只会在百度搜东西，但真正的信息差来自**多平台交叉验证**。

### 6.1 核心理念：信息采集三原则

1. **不只搜一个平台**——Google/YouTube/Reddit/X 各有生态位
2. **优先看「人」说的话**——Reddit 评论区 > 博客软文 > 百度知道
3. **把采集过程本身记录下来**——下次不用重走弯路

### 6.2 工具准备

| 工具 | 用途 | 费用 |
|------|------|------|
| **Browser Use**（Claude 内置浏览器） | 抓取网页/YouTube/Reddit 内容 | 免费 |
| **yt-dlp** | 下载 YouTube 字幕/视频 | 免费开源 |
| **Web Search** | 多引擎搜索 | 免费 |
| **Obsidian Web Clipper**（可选） | 一键保存网页到 Vault | 免费插件 |

### 6.3 YouTube 字幕提取

**为什么要用 YouTube？** 英文技术教程的质量远超中文搬运内容，而 YouTube 是最大的技术教程平台。提取字幕 = 获得完整的文字版教程。

#### 方法一：yt-dlp 命令行（推荐）

```bash
# 安装 yt-dlp（需要 Python 环境）
pip install yt-dlp

# 下载某个视频的字幕（自动生成的也可以）
yt-dlp --write-sub --sub-lang en --skip-download --sub-format srt "https://www.youtube.com/watch?v=VIDEO_ID"

# 下载中文字幕（如果有）
yt-dlp --write-sub --sub-lang zh-Hans --skip-download --sub-format srt "https://www.youtube.com/watch?v=VIDEO_ID"
```

参数说明：
- `--write-sub`：下载字幕
- `--sub-lang en`：下载英文字幕（换成 `zh-Hans` 下载中文）
- `--skip-download`：只下字幕不下视频
- `--sub-format srt`：输出 SRT 格式

下载后的 `.srt` 文件可以直接复制粘贴到 Obsidian 笔记里，然后用 AI 总结：

```
帮我总结这个 YouTube 视频字幕的核心内容，提取 5 个关键要点
```

#### 方法二：Browser Use 直接抓取

如果不想装工具，用 Claude 内置的浏览器：

1. 告诉我："帮我打开这个 YouTube 视频并提取字幕"
2. 我会用浏览器打开视频页面，提取页面上的字幕文本
3. 保存到你的 Obsidian Vault 里

#### 字幕处理模板

把提取到的字幕粘贴到 Obsidian 笔记后，用 AI 做以下处理：

```markdown
# {{视频标题}}

## 原始信息
- 来源：{{YouTube URL}}
- 作者：{{频道名}}
- 时长：{{时长}}
- 提取日期：{{日期}}

## AI 总结（5 个要点）
（让 Smart Composer 生成）

## 关键术语
- [[术语1]]：解释
- [[术语2]]：解释

## 我的想法


## 原始字幕
<details>
<summary>点击展开完整字幕</summary>

（完整字幕内容）

</details>
```

### 6.4 Reddit 信息采集

**为什么用 Reddit？** Reddit 的 r/ObsidianMD、r/Productivity、r/studytips 等社区有大量真实用户的使用经验，比任何博客都靠谱。

#### 采集流程

1. **搜索**：在 Reddit 搜索关键词（如 `Obsidian AI plugin 2025`）
2. **筛选**：按「Top」排序，时间选「Past Year」
3. **提取**：阅读帖子正文 + 评论区（评论区往往比正文更有价值）
4. **记录**：用以下模板保存到 Obsidian

#### Reddit 笔记模板

```markdown
# Reddit 研究：{{主题}}

## 来源
- 帖子：[{{标题}}]({{URL}})
- 社区：r/{{子版块}}
- 发布时间：{{日期}}
- 点赞/评论：{{数据}}

## 原帖核心观点
- 

## 评论区精华（按点赞排序）
1. @{{用户名}}：……
2. @{{用户名}}：……
3. @{{用户名}}：……

## 我的收获
- 

## 相关链接
- [[]]
```

### 6.5 X（Twitter）信息采集

**为什么用 X？** AI 领域的最新动态、工具发布、技巧分享几乎都在 X 上第一时间出现。

#### 关键账号推荐

| 账号 | 领域 | 为什么关注 |
|------|------|-----------|
| @AnthropicAI | Claude 官方 | Claude 更新第一时间 |
| @OpenAI | GPT 官方 | GPT 更新第一时间 |
| @GoogleDeepMind | Gemini/Gemma | Google AI 动态 |
| @obsdmd | Obsidian 官方 | Obsidian 更新 |
| @elaboratecloud | Obsidian 社区 | Obsidian 技巧分享 |

#### 采集方法

1. **搜索技巧**：用 `Obsidian AI since:2025-01-01` 这样的搜索语法限定时间
2. **关注 Thread**：长推文 Thread 往往是深度教程
3. **浏览器抓取**：让我用 Browser Use 打开推文页面，提取文字内容

### 6.6 一站式工作流：一条信息的完整旅程

```
发现信息（Google/YouTube/Reddit/X）
        ↓
提取内容（yt-dlp/Browser Use/Web Search）
        ↓
保存到 Obsidian Inbox（原始内容）
        ↓
AI 总结（Smart Composer 提取要点）
        ↓
创建双向链接（关联已有笔记）
        ↓
标记标签（#来源 #主题 #质量评级）
        ↓
定期整理（Inbox → 对应 Area/Project）
```

---

## 七、范例：本指南是怎么写出来的

> **这一章本身就是「多源信息采集」的实战演示。** 你可以把这个过程当作模板，复用到任何主题的研究中。

### 7.1 采集过程记录

| 步骤 | 操作 | 用时 | 产出 |
|------|------|------|------|
| ① 需求分析 | 明确要写 Obsidian+AI 入门指南 | 1 min | 确定文章结构大纲 |
| ② Reddit 搜索 | 搜索 `Obsidian AI plugin 2025 2026` | 3 min | 找到 3 个高赞帖子 |
| ③ 帖子深度抓取 | 用 Browser Use 抓取帖子全文+评论区 | 5 min | 8000+ 字原始素材 |
| ④ Reddit 聚合搜索 | 搜索 `Smart Composer vs Copilot vs Smart Connections` | 3 min | 社区共识排名 |
| ⑤ GitHub 仓库验证 | 验证各插件的 Star 数、最近更新时间 | 2 min | 确认插件活跃度 |
| ⑥ 信息交叉验证 | Reddit 观点 vs GitHub 数据 vs 官方文档 | 3 min | 去伪存真 |
| ⑦ 结构化输出 | 整理成 Obsidian 笔记格式 | 10 min | 本指南 |
| ⑧ AI 辅助润色 | 用 AI 优化表达、补充缺失信息 | 5 min | 最终版本 |

**总耗时**：约 30 分钟完成从调研到成文的全过程。

### 7.2 你也可以这样做的通用流程

```
Step 1: 明确问题
   "我想了解 XX，XX 是什么？怎么用？哪个好？"

Step 2: 多平台搜索
   - Google: "XX tutorial 2025 2026"
   - YouTube: "XX beginner guide"
   - Reddit: "r/相关社区 XX"
   - X: "@相关账号 XX"

Step 3: 筛选高质量来源
   - Reddit：按点赞排序，看评论区
   - YouTube：看播放量+评论区
   - X：看转发数+回复质量

Step 4: 提取+整理
   - 用 Browser Use 抓取全文
   - 用 yt-dlp 提取 YouTube 字幕
   - 保存到 Obsidian Inbox

Step 5: AI 辅助分析
   - "帮我总结这篇文章的核心观点"
   - "对比这几个方案的优缺点"
   - "这些信息和我已有的哪些笔记有关联？"

Step 6: 形成自己的知识
   - 创建双向链接
   - 写自己的想法和评价
   - 标记质量等级
```

---

## 八、常见问题

### Q1：Obsidian 和 Typora/VS Code 有什么区别？

Typora 是纯 Markdown 编辑器，没有双向链接、没有插件生态、没有知识图谱。
VS Code 可以写 Markdown，但它是为程序员设计的，没有 Obsidian 的知识管理功能。
Obsidian = Markdown 编辑器 + 知识图谱 + 插件生态。

### Q2：免费版够用吗？

**完全够用**。Obsidian 本体免费，核心插件免费，Smart Composer 免费，Smart Connections 免费。
唯一收费的是 Obsidian Sync（跨设备同步），但你可以用 OneDrive/iCloud/坚果云免费替代。

### Q3：手机上能用吗？

可以。Obsidian 有 iOS 和 Android 版本。AI 插件在手机端也能用，但不支持本地模型（手机跑不动）和 MCP Server。

### Q4：笔记太多会不会卡？

不会。Obsidian 是本地应用，几十万字的 Vault 也能秒开。关系图谱如果节点太多会卡，可以设置只显示当前笔记的关联。

### Q5：AI 插件会不会泄露我的笔记内容？

看你用什么模型：
- **Ollama 本地模型**：数据完全不出你的电脑，零泄露风险
- **OpenAI/Claude API**：数据会发送到云端，但 API 模式下大模型厂商承诺不用于训练（详见各厂商政策）
- **Obsidian Sync**：笔记同步是加密的，和 AI 插件无关

### Q6：我想和团队共享笔记怎么办？

Obsidian 不是为团队协作设计的。如果需要多人协作，建议用 Notion/飞书。
Obsidian 更适合**个人知识管理**——你自己写、自己用、自己受益。

### Q7：我该从哪里开始？

**别想太多，直接开始写。**

1. 今天就创建一个 Vault
2. 写一篇日记（什么内容都行）
3. 安装 Smart Composer
4. 用 AI 帮你总结/扩展这篇日记
5. 体验双向链接的威力

然后**每天写一点**，一个月后你会惊讶于自己积累了多少知识。

---

## 九、资源索引

### 官方资源
- Obsidian 官网：https://obsidian.md
- Obsidian 帮助文档：https://help.obsidian.md
- Obsidian 论坛：https://forum.obsidian.md

### AI 插件
- Smart Composer：https://github.com/brianpetro/obsidian-smart-composer（GitHub）
- Obsidian Copilot：搜索 Obsidian 第三方插件「Copilot」
- Smart Connections：https://github.com/brianpetro/obsidian-smart-connections
- Agent Client：搜索 Obsidian 第三方插件「Agent Client」

### 外部工具
- Ollama（本地 AI）：https://ollama.com
- yt-dlp（YouTube 字幕提取）：https://github.com/yt-dlp/yt-dlp
- Obsidian Web Clipper：https://obsidian.md/clipper

### 学习社区
- Reddit r/ObsidianMD：https://www.reddit.com/r/ObsidianMD/
- Obsidian 中文社区：搜索「Obsidian 中文」微信群
- B 站 Obsidian 教程：搜索「Obsidian 入门」

### 作者相关
- Obsidian+AI 科研笔记系统搭建指南：（见「项目/00-研究生课题组」目录）
- career-breakthrough 求职工具包：https://github.com/Destined-at-Dawn/career_breakthrough

---

> **最后提醒**：工具只是手段，知识才是目的。
> 不要花太多时间折腾 Obsidian 的主题和插件配置，把时间花在**写有价值的内容**上。
>
> 「The best note-taking system is the one you actually use.」
> 最好的笔记系统是你真正在用的那个。

---

*本指南由项目作者整理，资料来源：Reddit r/ObsidianMD 社区、GitHub 开源社区、Obsidian 官方文档。*
*最后更新：2026-05-24*
