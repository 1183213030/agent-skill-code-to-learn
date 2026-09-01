# 🎓 Code to Learn (AI Engineering Tutor Protocol)

<div align="center">

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Platform](https://img.shields.io/badge/Platform-Claude_Code_|_Cursor_|_Gemini_|_Codex-purple.svg)
![Version](https://img.shields.io/badge/Version-1.0.0-emerald.svg)
![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-brightgreen.svg)

**"AI can write code for you, but it cannot grow your engineering intuition for you."**
**Turn every AI code change into an actionable engineering lesson.**

[English](README_EN.md) | [中文文档](README.md)

</div>

---

## 💡 Why Code to Learn?

When developers rely heavily on AI coding assistants (Cursor, Claude Code, Copilot), two critical pitfalls often arise:
1. **The Black Box Dependency**: The code works, but the developer has no clue why design decisions were made.
2. **System Fragility**: Single-line fixes cause chain-reaction bugs due to lack of upstream/downstream impact awareness.

**Code to Learn** shifts the paradigm: **Every real code change becomes an actionable, verifiable engineering lesson.**

---

## 📖 How to Use

Choose from **three distinct modes** based on your current coding workflow:

### 1. Deep Tutor Mode (LEARN Mode - Recommended ⭐)
When refactoring, debugging complex issues, implementing new architecture, or seeking deep engineering insights:

- **Trigger**: Prefix your prompt with `/learn` or ask for a detailed architectural breakdown.
- **Example Prompts**:
  > `/learn Implement an Axios interceptor that handles automatic JWT token refresh on 401 errors.`  
  > `/learn Refactor this monolithic form component into a finite state machine.`
- **Deliverables**:
  1. 🤖 **Code Changes**: Clean diffs and implementation details.
  2. 📖 **Root-Cause & Architectural Role**: Explain why the change was made based on actual source code.
  3. 🔗 **Impact Map**: Direct callers, data flow direction, and potential side-effects.
  4. 📚 **Engineering Vocabulary**: Core concepts with real-world analogies and exact code line references.
  5. 🛡️ **Verification Status**: Syntax, test coverage, and local testing instructions.
  6. 📝 **Obsidian / Notion Note Card**: Standard Callout format for 1-click archiving.
  7. 🧠 **Self-Test Quiz**: 2 folded scenario questions with `<details>` tags.

---

### 2. Fast / Daily Mode (NORMAL Mode - Zero Friction)
For trivial edits, minor CSS tweaks, or small fixes (<= 10 lines of code):

- **Trigger**: Ask normally or add `quick/fast`.
- **Example Prompts**:
  > `Change button background to primary blue and add a loading spinner.`  
  > `Quick fix: fix the missing query parameter in the API call.`
- **Deliverables**: Clean code + 1-sentence root cause + 1-sentence risk warning. **Instant delivery without long essays.**

---

### 3. Review Coach Mode (REVIEW Mode - Active Recall)
To test and consolidate what you have learned from past coding sessions:

- **Trigger**: Type `/review`.
- **Example Prompts**:
  > `/review`  
  > `/review Quiz me on Dependency Injection, Idempotency, and Race Conditions.`
- **Deliverables**: AI acts as a senior interviewer/architect, asking 3 probing scenario-based questions and providing in-depth feedback after you answer.

---

## 🧭 The 7-Phase Protocol Workflow

```text
                ┌──────────────┐
                │ User Request │
                └──────┬───────┘
                       ↓
                ┌──────────────┐
                │ 1. Modify    │  Implement clean code with clear diffs
                └──────┬───────┘
                       ↓
                ┌──────────────┐
                │ 2. Explain   │  Explain root causes based on real source code
                └──────┬───────┘
                       ↓
                ┌──────────────┐
                │ 3. Impact    │  Trace callers, data flow, and side-effects
                └──────┬───────┘
                       ↓
                ┌──────────────┐
                │ 4. Vocabulary│  Extract terms with analogies & code locations
                └──────┬───────┘
                       ↓
                ┌──────────────┐
                │ 5. Verify    │  Syntax + Unit Tests + Local verification steps
                └──────┬───────┘
                       ↓
                ┌──────────────┐
                │ 6. Note      │  Obsidian / Notion Callout card for archiving
                └──────┬───────┘
                       ↓
                ┌──────────────┐
                │ 7. Quiz      │  Folded scenario questions for active recall
                └──────────────┘
```

---

## 🚀 Quick Setup across Platforms

### 1. Cursor / Windsurf
- Copy [`.cursorrules`](.cursorrules) to your project root or configure `.cursor/rules/code-to-learn.mdc`.
- Type `/learn` in the chat window (`Ctrl+L` / `Cmd+L` or `Ctrl+K`) to activate!

### 2. Claude Code
- Add [`CLAUDE.md`](CLAUDE.md) to your project root or place [`SKILL.md`](SKILL.md) in `.claude/skills/code-to-learn.md`.
- Run `claude` in your terminal.

### 3. Gemini / Antigravity
- Save [`SKILL.md`](SKILL.md) to `~/.gemini/config/skills/code-to-learn/`.

### 4. OpenAI Codex / Open Interpreter / WorkBuddy
- Import this repository as a skill module with trigger `read_when: when user asks to modify code or learn engineering principles`.

---

## 📝 Obsidian / Notion Card Preview

```markdown
> [!NOTE] Mental Model
> - **Task**: Fix RouteScorer health penalty starvation issue
> - **Underlying Logic**: Introduced HealthEngine penalty deduction for deterministic degradation
> - **Key Rule**: Core logic must not depend directly on platform-specific storage
> - **Affected Files**: `core/RouteEngine.kt` → `core/RouteScorer.kt`

> [!QUESTION] Retention Quiz
> 1. Why should we inject LocalRepository instead of instantiating SharedPreferences directly?
> <details>
> <summary>💡 Reveal Answer</summary>
> **Explanation**: Direct instantiation couples core business logic to the Android platform, breaking unit testability.
> </details>
```

---

## 🤝 Contributing

Issues and PRs are welcome! Feel free to share your customized prompt templates and real-world case studies.

- **License**: [MIT License](LICENSE)
- **Author / Maintainer**: [Engineering Tutor Lab](https://github.com/1183213030/agent-skill-code-to-learn)
