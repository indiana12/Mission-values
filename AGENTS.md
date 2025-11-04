# Repository Guidelines

## Project Structure & Module Organization
- Root-level Markdown files such as `README.md` and `Welcome.md` hold the primary narratives; keep themes cohesive within each file.
- `.obsidian/` stores workspace preferences—do not edit its contents manually, but commit relevant configuration changes when they improve shared workflows.
- Add new topical documents at the root or in clearly named folders (for example, `growth-experiments/`), and include a short lead section that explains how the page should be used.

## Build, Test, and Development Commands
- No build step is required; these notes render directly in Obsidian or any Markdown viewer.
- Validate formatting before committing with `npx markdownlint '**/*.md'` (install locally if needed). Configure overrides in `.markdownlint.json` if the default ruleset conflicts with our conventions.
- Use `rg "<keyword>"` to locate existing coverage of a topic before adding new content.

## Coding Style & Naming Conventions
- Write in concise, action-oriented prose; prefer short paragraphs and bullet lists for decision records.
- Use Title Case for H1 headings, Sentence case for H2+, and keep section IDs stable to preserve Obsidian backlinks.
- Name files with lowercase-hyphenated slugs (e.g., `weekly-retrospective.md`) and timestamp working drafts with `YYYY-MM-DD` when chronology matters.
- Embed cross-references with relative links (`[[Welcome]]`) and tag strategic themes with `#growth`, `#experiments`, etc., to aid discovery.

## Testing Guidelines
- Run `npx markdownlint '**/*.md'` after substantial edits to catch structural issues (headings, spacing, link syntax).
- Manually open new or updated pages in Obsidian and confirm backlinks, callouts, and embedded media render correctly.
- When introducing new folders, verify mobile sync on a secondary device before closing the task.

## Commit & Pull Request Guidelines
- Write imperative, present-tense commit subjects under 60 characters (e.g., `Document Q3 growth ritual`); include a blank line before extended descriptions.
- Squash trivial fixups locally so each commit delivers a logical documentation slice.
- Pull request descriptions should summarize the intent, list affected files or sections, and note any follow-up tasks (e.g., templates to update). Attach screenshots if layout changes are involved.

