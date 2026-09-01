# 🎓 Code to Learn (AI 工程导师技能)

<div align="center">

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Platform](https://img.shields.io/badge/Platform-Claude_Code_|_Cursor_|_Gemini_|_Codex-purple.svg)
![Version](https://img.shields.io/badge/Version-1.0.0-emerald.svg)
![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-brightgreen.svg)

**"AI 可以替你写代码，但不能替你长出工程能力。"**
**Turn every AI code change into an actionable engineering lesson.**

[中文文档](README.md) | [English](README_EN.md)

</div>

---

## 💡 为什么需要 Code to Learn？

很多开发者在使用 AI 编程（Cursor / Claude / Copilot）时，常常陷入两大困境：
1. **黑盒依赖**：代码跑通了，但底层原理和设计决策完全不清楚，脱离 AI 依然没有系统思维。
2. **系统失控**：单点修复引发多处连环 Bug，缺乏对架构上下游波及影响面的把控。

**Code to Learn** 重新定义了人机协作范式：**将每一次真实的代码变动，转化为深度可沉淀的工程实战课。**

---

## 📖 详细使用指南 (How to Use)

你可以根据当下的开发场景，通过以下 **三种模式** 随心使用：

### 1. 深度导师模式 (LEARN Mode - 核心玩法 ⭐)
当你遇到**复杂 Bug 排查、代码重构、新功能实现**，或想彻底搞懂底层架构原理时：

- **触发方式**：在提示词开头加上 `/learn`，或直接要求“深度讲解/用导师模式修改”。
- **使用示例**：
  > `/learn 帮我实现一个支持失败自动重试与拦截防重的请求封装`  
  > `/learn 帮我重构这个庞大的 Vue 表单组件，抽离业务逻辑和状态机`
- **交付闭环**：
  1. 🤖 **代码实现**：高质量代码变动与对比
  2. 📖 **真实原理解析**：基于项目真实源码，通俗讲透“为什么这样改”
  3. 🔗 **架构影响地图**：横向看同级调用，纵向看数据流向与连带风险
  4. 📚 **工程术语拆解**：提取核心概念（附生活通俗类比与具体代码行对应）
  5. 🛡️ **可信度与验证**：静态检查、测试用例与本地验证指引
  6. 📝 **Obsidian/Notion 沉淀卡片**：标准 Callout 格式，一键复制归档
  7. 🧠 **折叠自测题**：2 道场景思考题，先做题再点开查看解析

---

### 2. 极速日常模式 (NORMAL Mode - 效率优先)
当你只是修改小样式、调整配置、修一个拼写错误（改动 $\le 10$ 行）时：

- **触发方式**：正常提问，或附带 `quick/fast/快速改`。
- **使用示例**：
  > `把这个按钮颜色改成主题蓝并加个 loading 状态`  
  > `快速修复这个接口请求头缺少 Authorization 的问题`
- **交付内容**：快速给出代码变动 + 1 句话核心原因 + 1 句话避坑警示，**秒级交付，绝不打扰正常开发节奏**。

---

### 3. 复习教练模式 (REVIEW Mode - 间隔巩固)
当你想检验自己对此前学到的工程知识、架构设计是否真正掌握时：

- **触发方式**：直接输入 `/review`。
- **使用示例**：
  > `/review`  
  > `/review 考考我关于依赖注入、幂等性和防抖节流的实战场景题`
- **交付内容**：AI 扮演资深面试官/架构教练，出 3 道场景化思考题考你；待你作答后逐条批改、指出盲区并给出升阶点拨。

---

## 🧭 七阶段工程学习协议流程图

```text
                ┌──────────────┐
                │   用户需求    │
                └──────┬───────┘
                       ↓
                ┌──────────────┐
                │ 1. Modify    │  高质量完成代码修改，输出清晰 Diff
                └──────┬───────┘
                       ↓
                ┌──────────────┐
                │ 2. Explain   │  基于当前项目真实源码，白话讲透底层逻辑
                └──────┬───────┘
                       ↓
                ┌──────────────┐
                │ 3. Impact    │  横向看同级调用，纵向看数据流向与潜在风险
                └──────┬───────┘
                       ↓
                ┌──────────────┐
                │ 4. Vocabulary│  提取 1~2 个核心工程术语，结合代码行科普
                └──────┬───────┘
                       ↓
                ┌──────────────┐
                │ 5. Verify    │  静态检查 + 单元测试 + 本地可信度验证建议
                └──────┬───────┘
                       ↓
                ┌──────────────┐
                │ 6. Note      │  Obsidian / Notion 原生 Callout 卡片一键沉淀
                └──────┬───────┘
                       ↓
                ┌──────────────┐
                │ 7. Quiz      │  折叠答案的自测题，检验底层理解
                └──────────────┘
```

---

## 🚀 各平台一键接入指南

### 1. Cursor / Windsurf
- 将仓库中的 [`.cursorrules`](.cursorrules) 复制到你的项目根目录下，或在 `.cursor/rules/code-to-learn.mdc` 中配置。
- 在 Cursor 聊天窗口（`Ctrl+L` / `Cmd+L` 或 `Ctrl+K`）正常提问或输入 `/learn` 即可自动生效！

### 2. Claude Code
- 将 [`CLAUDE.md`](CLAUDE.md) 放入你的项目根目录，或将 [`SKILL.md`](SKILL.md) 放入 `.claude/skills/code-to-learn.md`。
- 在终端运行 `claude` 提问即可无缝唤醒。

### 3. Gemini / Antigravity
- 将 [`SKILL.md`](SKILL.md) 保存至 `~/.gemini/config/skills/code-to-learn/` 目录即可全局自动生效。

### 4. OpenAI Codex / Open Interpreter / WorkBuddy
- 将本仓库克隆或导入为 Skill 模块，配置前置触发词 `read_when: 当用户要求修改代码或学习工程原理时`。

---

## 📝 知识库卡片沉淀示例 (Obsidian / Notion 原生渲染)

```markdown
> [!NOTE] 工程心智模型 (Mental Model)
> - **任务定位**：修复 RouteScorer 高优先级异常入口持续占用的问题
> - **底层逻辑**：引入 HealthEngine 健康惩罚分，实现确定性评分衰减
> - **避坑警示**：Core 层不能直接依赖具体平台 Storage，需通过接口依赖注入
> - **涉及文件**：`core/RouteEngine.kt` → `core/RouteScorer.kt`

> [!QUESTION] 巩固思考 (Quiz)
> 1. 为什么不能直接在 RouteScorer 中实例化 SharedPreferences？
> <details>
> <summary>💡 查看解析</summary>
> **解析**：这会破坏核心逻辑与具体平台存储实现的解耦，导致无法在非 Android 环境进行单元测试。
> </details>
```

---

## 🤝 参与贡献

欢迎提交 Issue、PR，分享你在不同开发场景下的使用心得与优质模板！

- **开源协议**：[MIT License](LICENSE)
- **作者/维护者**：[Engineering Tutor Lab](https://github.com/1183213030/agent-skill-code-to-learn)
