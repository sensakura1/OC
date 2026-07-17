---
name: document-change-approval
description: Require explicit user approval before writing any proposed document creation, content edit, deletion, replacement, rename, or other document-file change. Use for every task that may add, modify, remove, move, or overwrite document content or document files, including Markdown, plain text, Word, PDF, spreadsheets, presentations, and similar documentation artifacts.
---

# Document Change Approval

Apply a preview-first approval gate to every document change.

## Required workflow

1. Inspect relevant files with read-only operations when needed.
2. Prepare the proposed result without writing, creating, deleting, renaming, moving, or overwriting any document file.
3. Show the proposed document content in the conversation before making the change:
   - For a new document, show its intended path and complete proposed content.
   - For an edited document, show the intended path and the exact replacement text, patch, or complete revised content needed for the user to judge the change.
   - For content deletion, show exactly what would be removed and enough surrounding context to identify it unambiguously.
   - For file deletion, rename, or move, list every affected path and state the resulting disposition.
   - For binary or layout-heavy documents, show all proposed textual content plus a concise description of formatting, layout, formulas, media, or structural changes that cannot be represented faithfully as plain text.
4. Explicitly ask the user to approve the displayed proposal.
5. Stop without using any file-writing or file-mutating tool until the user clearly approves that specific proposal.
6. After approval, apply only the approved changes. If the intended content or affected paths change materially, present the revised proposal and obtain approval again.
7. Verify the written result and report what changed.

## Approval rules

- Treat only an unambiguous authorization such as “同意写入”, “批准”, “按此修改”, or an equivalent statement as approval.
- Do not treat the original change request, silence, a request for revisions, or general positive feedback as approval to write.
- Scope approval only to the content and paths displayed in the proposal. Do not reuse it for later changes.
- Allow read-only inspection, analysis, drafting in the conversation, and validation that does not mutate files before approval.
- When another workflow or skill normally writes documents immediately, keep its formatting and validation guidance but enforce this approval gate before its first mutation.
- If the user explicitly asks only for a draft in the conversation, provide the draft and do not ask for write approval unless they also want it saved.
