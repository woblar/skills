# Woblar skills

A library of reusable workflows for Codex and Claude Code. Each skill lives in one folder under `skills/` and is discoverable by both tools.

## Skill catalog

| Skill | Use it when | Produces | Prerequisites | License |
| --- | --- | --- | --- | --- |
| [illustrate-a-topic](skills/illustrate-a-topic/SKILL.md) | You want to explain a concept, mechanism, or comparison in a pastel whiteboard style using one or more of ten layouts. | A researched illustration per layout and source links, or a storyboard and prompt. | A topic and access to authoritative sources. Finished images require an image-generation tool. | [MIT for instructions and configuration](skills/illustrate-a-topic/LICENSE). See the [scope notice](skills/illustrate-a-topic/NOTICE.md). |
| [woblar-add-skill](skills/woblar-add-skill/SKILL.md) | You have a repeatable workflow to save in this library. | A skill discoverable by both tools and a linked catalog entry. | A checkout of `woblar/skills` and a workflow or example that identifies the inputs and output. | No license declared. |

## Use the library

```sh
git clone https://github.com/woblar/skills.git
cd skills
```

| Tool | Start | Illustrate a Topic | Add a skill |
| --- | --- | --- | --- |
| Codex | `codex` | `Use $illustrate-a-topic to explain how a heat pump works using theme 4.` | `Use $woblar-add-skill to save our release-note workflow.` |
| Claude Code | `claude` | `/illustrate-a-topic Explain how a heat pump works using theme 4.` | `/woblar-add-skill Save our release-note workflow.` |

Codex discovers the links in `.agents/skills/`. Claude Code discovers the links in `.claude/skills/` and gets shared project instructions through `CLAUDE.md`. On systems where Git checks out symlinks as plain text, replace the link stubs locally with copies of the corresponding folders in `skills/`. [Codex skill discovery](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills) · [Claude Code skill discovery](https://code.claude.com/docs/en/skills#choose-where-skills-load)

To reuse a skill in another project, copy the files its terms permit into a same-named folder in your tool’s discovery directory. Keep the license and notices with those files, and check the skill’s prerequisites.

## Maintain the library

- Follow [AGENTS.md](AGENTS.md) when contributing. Add the folder in `skills/`, both discovery links, and its catalog entry in the same change. Keep the catalog alphabetical by skill name.
- In a trusted Codex workspace, you can explicitly delegate a review to the project’s [skill reviewer](.codex/agents/woblar_skill_reviewer.toml). [OpenAI’s subagent guide](https://learn.chatgpt.com/docs/agent-configuration/subagents#custom-agents)

> Have `woblar_skill_reviewer` review my new skill and catalog entry. Report issues with file references.

## Licensing

Licenses are set per skill. Check the catalog and the skill’s own license and notices before reuse. When adapting a third-party skill, verify that its terms permit public redistribution and preserve the required license notices and attribution.
