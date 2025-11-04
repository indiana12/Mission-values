# Git Handler Blueprint

## Mission
Provide reliable guidance and execution steps for version control tasks so commits stay clean, history is traceable, and collaboration remains smooth.

## Context & Inputs
- Repository root: `/Users/luckyprahaladreddy/Desktop/Obsidian Folder/Mission - Growth`.
- Track open work by reviewing `git status` and staged diffs; note untracked Markdown pages that Obsidian adds automatically.
- Reference project conventions in `AGENTS.md` for commit messaging and PR expectations.

## Core Workflows
1. **Status Sweep** – Check working tree, stash or branch off before shifting contexts, and summarize pending files.
2. **Commit Crafting** – Group related changes, run `npx markdownlint '**/*.md'`, then commit with imperative subject (`Update coding lab structure`).
3. **Branch Management** – Create feature branches (`git checkout -b feature/git-handler`) and keep them synced with `origin`.
4. **Pull/Sync** – Use `git pull --rebase origin main` to reduce merge commits; resolve conflicts with side-by-side diff review.
5. **Release Review** – Before merging, run final status, log history with `git log --oneline -5`, and ensure README links remain accurate.

## Command Palette
- `git status`, `git diff`, `git add -p` for staging discipline.
- `git stash push --include-untracked` when switching focus quickly.
- `git rebase -i origin/main` for commit cleanup.
- `git push -u origin <branch>` to publish work.

## Custom Commands
- **Pre Checks** – Ensure the active branch is `auto-push`; if not, switch with `git checkout auto-push`. Verify the branch is current by running `git pull --rebase origin auto-push` and confirming a clean status. After sync, run `git status -sb`, `npx markdownlint '**/*.md'`, and any relevant tests (e.g., `npm test`). Summarize outstanding issues and suggest fixes.
- **Backup** – Confirm you are on `auto-push`; if not, switch with `git checkout auto-push`. Run `git status` to surface pending files, stage everything with `git add .`, and commit using an imperative summary such as `Backup: sync fitness notes`. Push the snapshot via `git push origin auto-push` and report the new commit hash.

## Guardrails
- Never force push to shared branches without logging a reason.
- Protect `.obsidian/` customizations by committing intentional changes only.
- Capture conflict resolutions in the commit body (`Resolved mermaid diagram conflict in structure-map.md`).

## Example Prompts
- “Review current changes and suggest how to split them into commits.”
- “Generate the commands to rebase `feature/git-handler` onto `main` and list conflict hotspots.”
- “Draft a commit message summarizing updates to the Life-Systems fitness notes.”

## Next Steps
Create a reusable checklist note (`Git Release Checklist`) and add automation snippets for frequent operations (e.g., shell aliases, scriptable backups). Document where backup branches or stashes are stored so the agent can prune them on cadence.
