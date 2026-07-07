# Ian Xiaohei Illustrations

> 把神学概念、要理问答和教义论述里的定义、对比、进程、关系和张力，变成一张张白底、手绘、怪诞但清爽的解析配图。
>
> 16:9 横版 | Lizhi IP | 纯白手绘 | 少量红橙蓝中文批注 | Codex Skill

---

## 这个仓库是什么

这是一个 Codex Skill，用来指导 AI Agent 为中文概念文本生成解析配图，典型输入是神学概念、要理问答、教义论述、讲章和灵修笔记。

它不是通用插画 prompt，也不是 PPT 信息图模板。它的核心目标是：先理解文本里的语义锚点，再把其中一个定义、对比、进程、关系、张力或隐喻，变成一张有记忆点的 16:9 手绘解释图。

Skill 本身只提供语义类别和视觉语言，不预设任何教义内容；具体概念由每次输入的文本携带，所以它同样可以用于哲学、法学等其他抽象概念的解析配图。

默认视觉 IP 是 `Lizhi`：一只浅奶油色与浅棕色斑块分布稳定的小型垂耳兔，有深色圆点眼、清楚的小兔鼻和三瓣兔嘴。Lizhi 不是吉祥物，不是贴纸，也不是站在角落里的装饰物，而是正在认真参与概念运转的荒诞工作者。

一句话：**让 AI 不只是“配一张图”，而是把文本里的一个关键认知动作画出来。**

---

## 适合谁用

特别适合：

- 整理要理问答、教理学习笔记，需要解析配图的人
- 写神学概念讲解、讲章、灵修内容，需要文章插图的人
- 想把抽象概念画成具体隐喻的人
- 想要一种比 PPT 信息图更轻、更怪、更有个人识别度的配图风格的人
- 用 Codex 做内容生产，希望稳定复用一套视觉语言的人

不适合：

- 想要商业插画、品牌 KV 或精致扁平插画的人
- 想要传统 PPT 信息图、复杂架构图或流程图的人
- 想要儿童卡通、可爱 IP、表情包风格的人
- 想把大量正文、长段解释或完整课程页塞进一张图里的人
- 需要严格可编辑矢量源文件的人

---

## 它会产出什么

默认输出：

- 16:9 横版解析配图
- 单条问答或单个概念默认 1 张；一段论述默认 4-8 张 shot list
- 每张图的主题、核心意思、结构类型、Lizhi 动作和中文标注建议
- 最终 PNG 图片，保存到 workspace 的 `assets/<topic-slug>-illustrations/`

默认不输出：

- PPTX / PDF / Keynote
- SVG / HTML / Canvas 可编辑图
- 商业海报或封面 KV
- 大段文字型信息图

---

## 视觉风格

这个 skill 默认使用 “Lizhi 怪诞解析配图”风格：

- 纯白背景，不要纸纹、米色、阴影、渐变
- 黑色手绘线稿，细线，轻微抖动
- 大量留白，主体只占画面约 40%-60%
- 少量红色、橙色、蓝色中文手写批注
- 一张图只表达一个核心定义、对比、进程、关系、张力或隐喻
- Lizhi 必须参与核心动作，不能只是装饰
- 怪诞、有创意、清爽，但不幼稚、不卖萌

---

## 示例效果

### 两个断点

![两个断点](examples/images/01-two-breakpoints.png)

### 按目的分拣

![按目的分拣](examples/images/02-sort-by-purpose.png)

### 一鱼多吃

![一鱼多吃](examples/images/03-one-fish-many-uses.png)

### 承接路径

![承接路径](examples/images/04-handoff-path.png)

### 信息井

![信息井](examples/images/05-information-well.png)

### 想法压机

![想法压机](examples/images/06-idea-press.png)

### 内容发酵

![内容发酵](examples/images/07-content-fermentation.png)

### 信任桥

![信任桥](examples/images/08-trust-bridge.png)

这些图片是旧版风格校准样例，只用于校准线条密度、留白、颜色克制和构图反复刻提醒；不要把其中角色当作 Lizhi 形象参考。使用时应该从当前文本重新发明隐喻，不要照抄旧案例的物件和构图。

---

## 安装

克隆仓库：

```bash
git clone https://github.com/helloianneo/ian-xiaohei-illustrations.git
cd ian-xiaohei-illustrations
```

复制 skill 到 Codex skills 目录：

```bash
mkdir -p "${CODEX_HOME:-$HOME/.codex}/skills"
cp -R ./ian-xiaohei-illustrations "${CODEX_HOME:-$HOME/.codex}/skills/"
```

安装后，在 Codex 里使用：

```text
Use $ian-xiaohei-illustrations 为这条要理问答设计并生成一张 Lizhi 怪诞解析配图。
```

---

## 怎么用

### 单条要理问答生成一张图

```text
Use $ian-xiaohei-illustrations 为下面这条要理问答生成一张 16:9 解析配图。
画面要怪诞但清爽，Lizhi 必须承担核心动作。中文标注最多 5 个。

问：<粘贴问题>
答：<粘贴回答>
```

### 单个概念生成一张图

```text
Use $ian-xiaohei-illustrations 为“<概念或命题>”生成一张解析配图。
先想清楚这张图讲的是定义、对比、进程、关系还是张力，再发明一个低科技隐喻。
```

### 只做配图规划

```text
Use $ian-xiaohei-illustrations 先不要生图。
请分析下面这段文本哪里值得配图，输出 shot list。
每张图写清楚：对应哪条问答或哪个概念、主题、核心意思、结构类型、Lizhi 在做什么、建议中文标注词。

<粘贴文本>
```

### 去掉图里的标题或错误文字

```text
Use $ian-xiaohei-illustrations 帮我编辑这张图，去掉左上角的“定义图”标题，其他内容保持不变。
```

更多示例见 [examples/prompts.md](examples/prompts.md)。

---

## 工作流程

这个 skill 的流程是：

1. 读取问答、概念、论述、Markdown、Notion 内容、截图或用户给的主题
2. 提炼核心认知动作、理解转折和适合视觉化的内容
3. 先输出 shot list：每张图只选一个语义锚点（定义、对比、进程、关系、张力、问答递进、隐喻具象化）
4. 为每张图选择结构类型：定义图、对比图、进程图、关系图、张力图、问答链、层次图或隐喻图
5. 重新发明一个低科技、怪诞但成立的物理隐喻
6. 让 Lizhi 承担核心动作
7. 每张图单独调用图像模型生成
8. 按 QA checklist 检查：白底、留白、Lizhi 动作、中文标注、非 PPT 感、非旧案例复刻
9. 保存最终 PNG，并报告用途和路径

---

## 目录结构

```text
.
├── README.md
├── LICENSE
├── NOTICE.md
├── assets/
│   └── ian-wechat-qr.jpg
├── examples/
│   ├── images/
│   │   ├── 01-two-breakpoints.png
│   │   ├── 02-sort-by-purpose.png
│   │   └── ...
│   └── prompts.md
└── ian-xiaohei-illustrations/
    ├── SKILL.md
    ├── agents/
    │   └── openai.yaml
    ├── assets/
    │   └── examples/
    └── references/
        ├── style-dna.md
        ├── lizhi-ip.md
        ├── composition-patterns.md
        ├── prompt-template.md
        └── qa-checklist.md
```

真正需要安装到 Codex 的是子目录：

```text
ian-xiaohei-illustrations/
```

根目录的 README、LICENSE、NOTICE 和 examples 是 GitHub 分享文档。

---

## 注意事项

- 图片里的中文文字越短越稳定。
- 每张图只讲一个核心结构，不要把文本做成说明书。
- Lizhi 必须承担核心动作；如果去掉 Lizhi 画面仍然完全成立，说明 Lizhi 太装饰了。
- 示例图只用于校准线条密度、留白、颜色克制和角色参与方式，不要复刻构图，也不要把旧图角色当作 Lizhi 形象参考。
- AI 图像模型可能出现错字、幻觉标签、风格漂移或多余标题，生成后需要检查。
- 如果中文错字严重，优先减少标注词并重生成。

---

## 相关项目

- [Ian Handdrawn PPT](https://github.com/helloianneo/ian-handdrawn-ppt) — 中文手绘技术 PPT-style 页面图生成 Skill
- [Awesome Claude Code Skills](https://github.com/helloianneo/awesome-claude-code-skills) — Claude Code Skills / Agents / Plugins 精选合集
- [Obsidian + Claude AI Second Brain](https://github.com/helloianneo/obsidian-ai-second-brain) — Obsidian + Claude AI 个人知识库搭建指南

---

## 关于原作者

本仓库复刻自 **Ian (伊恩)** 的 [Ian Xiaohei Illustrations](https://github.com/helloianneo)，视觉风格与工作流框架来自原项目。

- GitHub: [helloianneo](https://github.com/helloianneo)
- X/Twitter: [@ianneo_ai](https://x.com/ianneo_ai)
- 网站: [www.ianneo.xyz](https://www.ianneo.xyz)

---

## License

MIT License. See [LICENSE](LICENSE).
