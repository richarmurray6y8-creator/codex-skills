---
name: handoff
description: Create a self-contained, actionable handoff document so another agent can continue the current work.
---

# Handoff

Write a handoff that lets a new agent understand the main objective, the current problem, and exactly how to continue without needing the preceding conversation. Use the user's language. If arguments are supplied, focus on the requested continuation without omitting the main task and essential history.

## Gather and reconcile context

- Review the available conversation and earlier handoffs first. Identify the enduring objective, accepted decisions, latest user instructions, existing authorization, constraints, and whether the work is paused.
- When useful and safe, inspect current files, repository state, or task status read-only. Do not start a build, download, change state, or resume paused work merely to fill a handoff gap.
- Distinguish observations verified now from earlier reports, hypotheses, and unknowns. Record dates or versions where state may have changed. If context and current evidence disagree, explain the discrepancy; do not invent missing facts.

## Put the essentials in one document

Adapt detail to the task. Include concrete, useful information under the following topics when applicable:

1. **Main objective and current problem:** what the user is trying to achieve, why the current issue matters, symptoms, evidence, likely causes, and what is still unknown.
2. **Work plan and progress:** the intended sequence, what was actually done, current stage, results and their scope, pending work, and rejected or superseded approaches. Identify relevant versions or commits when different results belong to different versions.
3. **Next actions:** the first safe, specific steps in priority order, commands or exact UI entry points when appropriate, how to tell they succeeded, remaining blockers, and final acceptance criteria. Do not present unexecuted steps as completed.
4. **Files, URLs, and environment:** exact absolute paths or usable URLs for every source, test, output, log, plan, repository, issue, and official page needed to continue; explain what each is for. Include relevant branch names, commit IDs, uncommitted changes, running-state caveats, and dependencies where applicable. Mark unavailable or unverified entries clearly.
5. **Boundaries and preferences:** preserve the user's latest instructions, decisions, pause state, do-not-touch items, login and download restrictions, authorization boundaries, and communication preferences.
6. **Suggested skills:** name only skills that would materially help the next agent and why.

Include essential facts directly, even if also present in another document. Link to supporting artifacts for long source code, full logs, detailed specifications, and complete diffs instead of copying them wholesale. Do not make the recipient open a second document merely to learn the task, current status, or next step.

Remove passwords, tokens, API keys, session cookies, and other secrets; never use URLs containing credentials. Preserve necessary non-secret paths, repository addresses, and identifiers so the handoff remains usable. Do not guess a missing path or URL.

## Tell the receiving agent how to start

Include directions in the handoff: first review the task context already available in its conversation, including prior handoffs and the user's latest instructions, to reconstruct the long-running main objective and current stage. Reconcile that context with this document and fresh evidence; the user's latest instruction governs. If the agent has no prior context, it must read the entire handoff before acting. Do not assume it can access a conversation it has not been given.

## Review, save, and deliver

Before delivery, reread the complete document as if you were a new agent with no prior context. Check that it can identify the problem, objective, verified progress, pending plan, immediate next action, necessary paths and URLs, constraints, and success condition. Fix gaps or ambiguous references; explicitly mark genuinely unavailable details. Check that links and paths are usable when possible and that no secrets are included.

Save the handoff as UTF-8 in the operating system's temporary directory, not the current workspace: use %TEMP% on Windows; otherwise use TMPDIR if set, or /tmp. Preserve an existing handoff path when the user asks to update that specific document. In the final response, provide its absolute path as a clickable link and state any important pause or unresolved blocker.