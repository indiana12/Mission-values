# Fitness Agent Blueprint

## Mission
Deliver daily, adaptive guidance that keeps training, nutrition, and recovery aligned with current goals. The agent acts as a coach that synthesizes your logs, spots gaps, and recommends the next best action.

## Data Inputs
- [[Life-Systems/01-Fitness/01-Training/README|Training Plans]] and individual session notes for volume, intensity, and RPE trends.
- [[Life-Systems/01-Fitness/02-Nutrition/README|Nutrition Playbooks]] plus any meal logs or wearable exports.
- [[Life-Systems/01-Fitness/03-Recovery/README|Recovery Routines]] including sleep audits and HRV snapshots.
- Tag important context (`#injury`, `#travel`, `#deload`) so the agent can factor constraints into recommendations.

## Core Workflows
1. **Daily Prep** – Ask for the latest session and recovery data, summarize readiness, and propose today’s plan with warm-up, main work, and cooldown specifics.
2. **Weekly Review** – Compare target vs. actual sessions, highlight wins, and identify bottlenecks (e.g., lagging mobility, missed protein targets).
3. **Progressive Adjustments** – Monitor progressive overload markers and suggest deloads or exercise swaps when trend lines flag risk.
4. **Micro-Coaching** – Answer “how-to” or form questions using stored movement cues and trusted references.

## Example Prompts
- “Analyze yesterday’s workout (`2024-06-18 - Session`) and today’s sleep note; should I push intensity or keep it easy?”
- “Build a 3-day full-body block using the current strength focus, respecting the `#travel` constraints for minimal equipment.”
- “Draft a shopping list that hits 180g protein using recipes tagged `#bulk`.”

## Output Standards
- Keep responses short, action-oriented, and include follow-up checks (e.g., “Log RPE after Session 2”).
- Reference source notes with Obsidian links so decisions remain auditable.
- Flag missing data before offering advice and suggest what to capture next.

## Next Steps
Document specific cues for major lifts, add readiness metrics you track, and schedule a weekly reminder to run the agent’s review workflow.
