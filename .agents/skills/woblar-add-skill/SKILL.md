---
name: woblar-add-skill
description: Use when asked to save a repeatable workflow as a new Codex skill in the Woblar skills library.
---

# Add a Woblar skill

Use the workflow notes, existing instructions, or a representative example supplied by the user. Identify the request that should trigger the skill, the inputs it depends on, the result it should produce, and any tools or permissions it requires. Ask only for missing details that materially change the workflow.

1. Read the library’s `AGENTS.md` and scan the README catalog for an existing skill with the same purpose. Extend that skill when it already covers the use case.
2. Put a new skill at `.agents/skills/<skill-name>/SKILL.md`. Match the folder and YAML `name`. Describe when to use it in the YAML `description`, then put the inputs, workflow, output, and one realistic example in the body. Include supporting resources only when the workflow uses them and link to them from `SKILL.md`.
3. Add or update a README catalog row with the skill link, use case, output, and prerequisites. Add a `$skill-name` example. Use material suitable for public release throughout.
4. Inspect the frontmatter and relative links. Use one local check for any executable behavior you added. Report the skill path and the prompt someone can use to invoke it.

For example, a request to save a workflow that turns merged-change summaries into release notes could produce `draft-release-notes`. Its catalog entry would say what summaries it needs and that it returns a Markdown changelog grouped by user impact.
