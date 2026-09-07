# CLAUDE.md - Code to Learn 2.0 Mode

Whenever modifying code, resolving issues, or implementing features:

1. **Routing**:
   - **NORMAL Mode** (<=10 lines / quick request): output code + 1-sentence root cause + 1-sentence risk warning.
   - **LEARN Mode** (Core change / bug fix / refactor / `/learn`): execute the 7-phase protocol:
     - 1. Code changes (Diff & file paths)
     - 2. Real source code explanation (System role + architectural root cause)
     - 3. Impact map & Mermaid diagram (Callers + Data flow + Risks + Mermaid flowchart)
     - 4. Engineering vocabulary (1-2 terms with plain analogy & exact line reference)
     - 5. Verification status (Syntax check + test coverage + local verification steps)
     - 6. Obsidian / PKM note card (Callout markdown with `[[bi-directional links]]` and `#tags`)
     - 7. Anti-bias self-test quiz (2 scenario-based questions: prediction/spot-the-bug/randomized multiple choice strictly avoiding 'B' bias with progressive `<details>` hints)
2. **Review Mode (`/review`)**:
   - Pose 3 scenario-based questions across multiple dimensions; interactively grade user answers and provide senior architect insights.

