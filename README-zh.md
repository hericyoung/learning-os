# Learning OS

> 一个用于终身学习的版本化操作系统，基于第一性原理思考、心智模型、知识策展以及 AI 协作构建。

[English](README.md) | [中文](README-zh.md)

Learning OS 不是简单的笔记或课程集合。

它是一个学习**如何思考**的系统，而不仅仅是学习**知道什么**。

其目标是构建可跨学科应用、能与现实世界观察相联系，并在数月或数年后可重构的、可复用的心智模型。

---

# 为什么选择 Learning OS？

传统的学习通常走向两个极端：

* **教科书驱动**：系统化，但脱离现实。
* **碎片化学习**：有趣，但缺乏结构。

Learning OS 将两者结合起来。

它遵循结构化的学习路径，同时不断将每个概念与现实世界的例子、产品、商业、技术和日常决策联系起来。

其目标不是记忆知识，而是逐步构建一个不断增长的认知网络。

---

# 它是如何工作的

Learning OS 旨在与 **AI 编程助手**作为协作思考伙伴协同工作。AI 会自动承担五个专门的角色：

| 角色 | 职责 |
|------|---------------|
| 🗺️ **地图守护者 (Map Keeper)** | 维护各学科的结构，防止碎片化学习 |
| 🏗️ **脚手架搭建者 (Scaffolding Builder)** | 在你已有的理解基础上构建新知识 |
| 🔗 **模型连接者 (Model Connector)** | 识别不同学科之间的共有模式 |
| 🏛️ **苏格拉底式向导 (Socratic Guide)** | 在得出结论之前通过提问鼓励推理 |
| 🧭 **知识策展人 (Knowledge Curator)** | 提炼课程、连接工件、综合里程碑，并支持长期复习 |

知识策展人不会存档对话内容。它会将机制、证据、联系、认知变化和未解决的问题保存为便于复习的工件 (artifacts)。

---

# 快速开始

## 前置条件

- Git
- 一个 AI 编程助手（请参阅下方针对特定平台的设置）

## 第一步：克隆仓库

```bash
git clone https://github.com/hericyoung/learning-os.git
cd learning-os
```

## 第二步：选择你的 AI 助手

### 选项 A: Gemini (VS Code / JetBrains IDE) — 原生支持 ✅

Learning OS 是作为 **Gemini Skill** 原生构建的。无需额外设置。

1. 在安装了 Gemini 插件的 IDE 中打开项目
2. `.agents/skills/learning-os/` 中的 skill 会被**自动发现**
3. 开始聊天 —— 当你讨论学习主题时，该 skill 就会激活

### 选项 B: Claude Code (Anthropic)

Claude Code 会读取项目根目录下的 `CLAUDE.md` 获取指令。

1. 确保已安装 [Claude Code](https://docs.anthropic.com/en/docs/claude-code)
2. 打开项目目录：
   ```bash
   cd learning-os
   claude
   ```
3. Claude 会自动读取 `CLAUDE.md` 文件并采用 Learning OS 的行为
4. 开始学习！

### 选项 C: OpenAI Codex CLI

Codex CLI 会读取项目根目录下的 `AGENTS.md` 获取指令。

1. 确保已安装 [Codex CLI](https://github.com/openai/codex)
2. 打开项目目录：
   ```bash
   cd learning-os
   codex
   ```
3. Codex 会自动读取 `AGENTS.md` 文件并采用 Learning OS 的行为
4. 开始学习！

### 选项 D: Cursor

Cursor 会读取 `.cursor/rules/` 目录以获取项目特定的规则。

1. 在 [Cursor](https://cursor.sh) 中打开项目
2. Cursor 会自动从 `.cursor/rules/learning-os.mdc` 加载规则
3. 在 Cursor 的 AI 面板中开始聊天

### 选项 E: GitHub Copilot

Copilot 会读取 `.github/copilot-instructions.md` 获取项目指令。

1. 在启用了 GitHub Copilot 的 VS Code 中打开项目
2. Copilot 会自动读取 `.github/copilot-instructions.md`
3. 使用 Copilot Chat 开始学习

### 选项 F: 手动使用 (无 AI 助手)

如果没有 AI 助手，你仍然可以将 Learning OS 作为一个知识框架使用：

1. 阅读 `SPECIFICATION/Learning-OS-Spec.md` 了解完整的方法论
2. 阅读 `SPECIFICATION/Roadmap.md` 了解学习进度
3. 使用 `.agents/skills/learning-os/resources/templates/` 中的模板手动创建模型、课程、观察结果、课程摘要、里程碑和反思
4. 将任何模板复制到相应的目录并填写：
   ```bash
   cp .agents/skills/learning-os/resources/templates/model-template.md MODELS/my-model.md
   ```

## 第三步：开始学习

一旦你的助手设置完毕，只需开始对话：

- *"我想了解为什么在短缺期间价格会上涨"*
- *"帮我构建一个用于决策的心智模型"*
- *"我注意到关于习惯养成的一些有趣的事情——让我们来探讨一下"*
- *"从我们上次停下的地方继续经济学课程"*

AI 将遵循 Learning OS 的方法论：从现实出发，用第一性原理进行分解，构建模型，跨领域应用，连接到你的知识图谱，并提炼已完成的学习内容以便将来重构。

## v1.1 生成的内容

在学习者展示了对课程的理解之后，Learning OS 会创建一个简洁的课程摘要，其中包含关键模型、推理过程、示例、先验联系、相关模型、局限性以及重构提示。

当声明的课程里程碑中的所有课程都完成后，它会创建一个综合的里程碑摘要。在此时，它还会向学习者提出反思性问题；反思文档仅根据学习者的回答生成。

所有工件都通过 `INDEX.md` 连接。`CHANGELOG.md` 记录重大更改，同时防止重复规则确保每个想法都有一个规范的归宿。

## 长期复习

复习不是钻研定义，也不是固定的间隔重复计划。学习者应该：

1. 借助知识图谱和里程碑确定方向。
2. 在重读之前尝试进行重构提示。
3. 从第一性原理重建模型。
4. 在新旧观察中测试它们。
5. 比较反思历史以查看认知变化。
6. 当理解加深时，完善规范模型和联系。

---

# 核心原则

* 第一性原理思考
* 心智模型
* 结构化进展（地图）
* 现实世界地标
* 苏格拉底式对话
* 跨学科联系
* AI 辅助脚手架
* 持续反思与迭代

---

# 仓库结构

```text
learning-os/
├── .agents/skills/learning-os/  # Gemini Skill (原生)
│   ├── SKILL.md                 # AI 行为定义
│   ├── references/              # 完整规范和路线图
│   ├── examples/                # 示例学习会话
│   └── resources/templates/     # 所有学习和知识工件的模板
├── .cursor/rules/               # Cursor 规则
├── .github/                     # GitHub Copilot 指令
├── CLAUDE.md                    # Claude Code 指令
├── AGENTS.md                    # OpenAI Codex / 通用代理指令
├── MODELS/                      # 可复用的心智模型 (输出)
├── COURSES/                     # 结构化学习路径 (输出)
├── OBSERVATIONS/                # 现实世界案例研究 (输出)
├── KNOWLEDGE/                   # 课程提炼、里程碑、反思
├── INDEX.md                     # 全局知识图谱和工件注册表
├── CHANGELOG.md                 # 版本化更改
├── SPECIFICATION/               # 原始规范 (参考)
└── README.md                    # 项目文档
```

---

# 学习哲学

学习始于现实。

现实揭示模式。

模式成为模型。

模型连接成系统。

系统化为直觉。

最终目标不是完成课程。

最终目标是培养一种看待和理解世界的方式。

---

# 当前状态

**版本:** v1.1

当前重点：

* 构建 Learning OS 框架 ✅
* Gemini Skill 集成 ✅
* 知识管理和复习系统 ✅
* 经济学 (进行中)

---

# 许可证

本项目旨在作为一个长期的个人知识系统。

随着新思想、新学科和新心智模型的发现，它开放于持续的演进。
