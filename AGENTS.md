# AI Agent Collaboration Rules

## Onboarding — every session starts here

1. Read `AI_SHARED_KNOWLEDGE/RECENT_CONTEXT.md` for the latest state.
2. Read `AI_SHARED_KNOWLEDGE/PROJECT_INDEX.md` to find active projects.
3. Check `AI_SHARED_KNOWLEDGE/handoff/` for pending handoffs addressed to you.
4. Only then begin your task.

## What to record

Use this repository as shared working memory, not a chat archive.

- Confirmed decisions and the reasoning behind them
- Verified facts with sources
- Project status changes
- Deliverables and their locations
- Handoffs to other agents with clear next actions
- Unfinished work and blockers

## What NOT to record

- Raw chat transcripts
- Secrets, passwords, API keys, OAuth tokens, or personal data
- Duplicate information already in another file
- Assumptions presented as facts — label uncertainty clearly

## File and branch rules

- Never commit directly to `main`. Always use a feature branch and PR.
- One PR per logical change. Keep PRs small and reviewable.
- Branch naming: `<agent>/<short-description>` (e.g. `claude/fix-readme`, `gpt/add-research`)
- Do not overwrite another agent's files. Create a new version or a separate file.
- Write commit messages in English. PR descriptions may use Korean or English.

## Handoff protocol

When handing work to another agent:

1. Write a summary in `AI_SHARED_KNOWLEDGE/handoff/<FROM>_TO_<TO>.md`
2. Include: what was done, what remains, key files, and the recommended next action.
3. Update `RECENT_CONTEXT.md` with a dated entry.
4. Update `CHANGELOG.md`.

## Conflict resolution

- If two agents edit the same file, the later agent must read the current version first and merge.
- When in doubt, ask the user rather than overwriting.

## Agent registry

| Agent | Strengths | Handoff file |
|---|---|---|
| Claude | Code, review, PR automation, structured analysis | `CLAUDE_TO_*.md` / `*_TO_CLAUDE.md` |
| GPT/Codex | Code generation, broad knowledge, conversational | `GPT_TO_*.md` / `*_TO_GPT.md` |
| Genspark | Web research, real-time search, data gathering | `GENSPARK_TO_*.md` / `*_TO_GENSPARK.md` |

New agents: add a row here and follow the same rules.
