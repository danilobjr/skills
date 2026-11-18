---
name: save-plan
description: Save the current execution plan verbatim to a timestamped Markdown file.
disable-model-invocation: true
---

# Save Plan

1. **Select the plan.** Use the latest complete execution plan presented in the conversation unless the user identifies another one. If the target is ambiguous or its full text is unavailable, ask the user to identify or provide it before continuing. Proceed only with one complete, identified plan.

2. **Resolve the destination.** Save under `docs/plans/` at the current project root, creating the directory if needed. Respect active write restrictions: if they block this destination, explain the restriction and request the necessary mode or permission change instead of saving elsewhere. Proceed only when the intended destination is writable.

3. **Name the file.** Obtain the current local date and time when saving. Use:

   ```text
   YYYY-MM-DD_HH-MM-SS_<plan-name>.md
   ```

   Derive `plan-name` from the plan's title or, if absent, its main subject:
   - Transliterate accented characters to their unaccented equivalents and lowercase the text.
   - Separate words with hyphens, remove other punctuation, collapse repeated hyphens, and trim leading/trailing hyphens.
   - Ensure the result is nonempty and contains only `a-z`, `0-9`, and single hyphen separators.

   If normalization produces an empty name, ask the user for a name that satisfies these rules before saving.

   Example: `Refatoração da autenticação` becomes `2026-11-18_14-32-07_refatoracao-da-autenticacao.md`.

   If the path already exists, obtain a fresh timestamp and retry until the path is unused.

4. **Save verbatim.** Write only the selected plan's original Markdown, preserving its wording, language, headings, lists, code blocks, and ordering. Exclude surrounding conversational commentary; add no summary, metadata, or new sections. Create a new file without overwriting any existing file.

5. **Verify and report.** Read the saved file and compare its entire content with the selected plan. Finish only when the content matches and the filename follows the required format. Reply with only the saved file's project-relative path.
