# 🎓 Code to Learn (AI 工程导师技能)

<div align="center">

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Platform](https://img.shields.io/badge/Platform-Claude_Code_|_Cursor_|_Gemini_|_Codex-purple.svg)
![Version](https://img.shields.io/badge/Version-1.0.0-emerald.svg)
![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-brightgreen.svg)

**"AI 可以替你写代码，但不能替你长出工程能力。"**

[中文文档](README.md) | [English](README_EN.md)

</div>

---

## 💡 为什么需要 Code to Learn？

很多开发者在使用 AI 编程（Cursor / Claude / Copilot）时，常常陷入两大困境：
1. **黑盒依赖**：代码跑通了，但底层原理和设计决策完全不清楚，脱离 AI 依然没有系统思维。
2. **系统失控**：单点修复引发多处连环 Bug，缺乏对架构上下游波及影响面的把控。

**Code to Learn** 重新定义了人机协作范式：**将每一次真实的代码变动，转化为深度可沉淀的工程实战课。**

---

## 🧭 核心工作流：七阶段工程学习协议 (7-Phase Protocol)

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

## 🎯 智能三模式路由 (Mode Routing)

| 模式 | 触发场景 | 输出交付 |
| :--- | :--- | :--- |
| **`NORMAL` (极速模式)** | 改动 $\le 10$ 行、样式微调、或用户要求 `quick/fast` | 代码改动 + 1 句话原理 + 1 句话避坑，**绝不阻碍正常开发效率** |
| **`LEARN` (深度导师)** | 默认开启 / 涉及架构重构、复杂 Bug、新功能、或输入 `/learn` | 完整执行七阶段工程学习协议 |
| **`REVIEW` (复习教练)** | 用户输入 `/review` 或要求 `复习以前知识/出题考我` | 读取历史知识点，生成 3 道场景化自测题并启发式批改 |

---

## 🚀 多平台一键安装指南

### 1. Cursor / Windsurf
- 在项目根目录创建 `.cursorrules`，或在 `.cursor/rules/code-to-learn.mdc` 中粘贴本仓库的 [`.cursorrules`](.cursorrules) 内容。
- 设置为 `Always Active`（全局生效）。

### 2. Claude Code
- 将 [`CLAUDE.md`](CLAUDE.md) 放入项目根目录，或将 [`SKILL.md`](SKILL.md) 放入 `.claude/skills/code-to-learn.md`。

### 3. Gemini / Antigravity
- 将 [`SKILL.md`](SKILL.md) 放入 `~/.gemini/config/skills/code-to-learn/` 目录即可自动加载。

### 4. OpenAI Codex / Open Interpreter / WorkBuddy
- 将本目录作为 Skill 模块导入，配置触发词 `read_when: 当用户要求修改代码或学习工程原理时`。

---

## 📝 知识库沉淀卡片示例 (Obsidian 渲染)

```markdown
> [!NOTE] 工程心智模型 (Mental Model)
> - **任务定位**：修复 RouteScorer 高优先级异常入口持续占用的问题
> - **底层逻辑**：引入 HealthEngine 健康惩罚分，实现确定性评分衰减
> - **避坑警示**：Core 层不能直接依赖具体平台 Storage，需通过接口依赖注入
> - **涉及文件**：`core/RouteEngine.kt` → `core/RouteScorer.kt`
```

---

## 🤝 贡献与交流

欢迎提交 Issue 和 Pull Request，分享你调教出的更优质的导师 Prompt 与行业实战模板！

- **开源协议**：[MIT License](LICENSE)
- **作者**：Engineering Tutor Lab
