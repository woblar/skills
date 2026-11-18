---
name: woblar-add-skill
description: Add or update a reusable skill in the Woblar skills library. Use when asked to save a repeatable workflow or adapt an existing skill for Codex and Claude Code in this library.
---

# Add a Woblar skill

Use the workflow notes, existing instructions, or a representative example supplied by the user. Identify the request that should trigger the skill, the inputs it depends on, the result it should produce, and any tools or permissions it requires. Ask only for missing details that materially change the workflow.

1. Locate the `woblar/skills` checkout and read its `AGENTS.md` and README catalog. If you cannot identify the library, ask where it is before editing. Extend an existing library skill when it already covers the use case.
2. Put the canonical skill at `skills/<skill-name>/SKILL.md`. Match the folder and YAML `name`. Describe when to use it in `description`, then put the inputs, workflow, output, and a realistic example in the body. Keep the workflow portable. Link any needed supporting files using relative paths.
3. Add a relative directory symlink named `<skill-name>` under both `.agents/skills/` and `.claude/skills/`, each pointing to `../../skills/<skill-name>`. For adapted skills, check redistribution terms and retain applicable license and attribution. Record any new license or exclusions only for this skill and with the rights holder’s authorization.
4. Update the catalog’s skill link, use case, output, prerequisites, and license. Check the frontmatter, resource links, and both discovery links. Use one local check for any executable behavior you added. Report the skill path and an invocation for each host.

For example, a request to save a workflow that turns merged-change summaries into release notes could produce `draft-release-notes`. Its catalog entry would say what summaries it needs and that it returns a Markdown changelog grouped by user impact.
