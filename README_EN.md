# 🎓 Code to Learn (AI Engineering Tutor Protocol)

<div align="center">

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Platform](https://img.shields.io/badge/Platform-Claude_Code_|_Cursor_|_Gemini_|_Codex-purple.svg)
![Version](https://img.shields.io/badge/Version-1.0.0-emerald.svg)

**"AI can write code for you, but it cannot grow your engineering intuition for you."**

[English](README_EN.md) | [中文文档](README.md)

</div>

---

## 💡 Why Code to Learn?

When developers rely heavily on AI coding assistants (Cursor, Claude Code, Copilot), two critical pitfalls often arise:
1. **The Black Box Dependency**: The code works, but the developer has no clue why design decisions were made.
2. **System Fragility**: Single-line fixes cause chain-reaction bugs due to lack of upstream/downstream impact awareness.

**Code to Learn** shifts the paradigm: **Every real code change becomes an actionable, verifiable engineering lesson.**

---

## 🧭 The 7-Phase Learning Protocol

1. **Modify**: Implement clean, robust code with clear diffs.
2. **Explain**: Break down architectural roles and root causes using real project source code (no generic fluff).
3. **Impact**: Map direct callers, upstream/downstream data flows, and potential side-effects.
4. **Vocabulary**: Explain 1-2 core engineering concepts with simple real-world analogies and code references.
5. **Verify**: Check syntax, tests, and actionable local verification steps.
6. **Note**: Output copyable Obsidian/Notion Callout cards for personal knowledge bases.
7. **Quiz**: Provide 2 self-test scenario questions with folded answers.

---

## 🚀 Quick Setup

- **Cursor**: Copy [`.cursorrules`](.cursorrules) to project root or use `.cursor/rules/code-to-learn.mdc`.
- **Claude Code**: Add [`CLAUDE.md`](CLAUDE.md) to project root or place in `.claude/skills/`.
- **Gemini / Antigravity**: Save [`SKILL.md`](SKILL.md) to `~/.gemini/config/skills/code-to-learn/`.
- **Codex / WorkBuddy**: Import [`SKILL.md`](SKILL.md) directly as an agent skill.

---

## 📄 License

MIT License © 2026 Engineering Tutor Lab
