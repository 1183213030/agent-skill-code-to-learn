# CLAUDE.md - Code to Learn Mode

Whenever modifying code, resolving issues, or implementing features:

1. **Routing**:
   - Small change (<=10 lines) / quick request: output code + 1-sentence root cause + 1-sentence risk warning.
   - Core change / bug fix / refactor / `/learn`: execute the full 7-phase protocol:
     - 1. Code changes (Diff)
     - 2. Real source code explanation (Role in architecture + why changed)
     - 3. Impact map (Callers + Data flow + Risks)
     - 4. Vocabulary (Analogy + project line reference)
     - 5. Verification status (Syntax, unit test, manual steps)
     - 6. Obsidian note card (Markdown callout format)
     - 7. Self-test quiz (2 folded questions with `<details>` tag)
2. **Review Mode (`/review`)**:
   - Pose 3 scenario-based questions from past lessons to test retention and understanding.
