# Woblar skills

A library of reusable workflows for Codex. Use the catalog to find a skill by the task you want to do.

## Skill catalog

| Skill | Use it when | Produces | Prerequisites |
| --- | --- | --- | --- |
| [woblar-add-skill](.agents/skills/woblar-add-skill/SKILL.md) | You have a repeatable workflow to save in this library. | A Codex-discoverable skill folder and a linked catalog entry. | A workflow with enough detail or a representative example to identify its inputs and output. |

> Use $woblar-add-skill to save our release-note workflow. It takes a list of merged changes, groups them by user impact, and returns a Markdown changelog.

## Use the library in Codex

```sh
git clone https://github.com/woblar/skills.git
cd skills
codex
```

Type `$` in Codex to pick a skill. To reuse a library skill in another project, copy its entire folder into that project’s `.agents/skills/` directory and check the prerequisites in its catalog entry. [OpenAI’s skill discovery guide](https://learn.chatgpt.com/docs/build-skills#where-codex-loads-local-skills)

## Maintain the library

- Follow [AGENTS.md](AGENTS.md) when contributing. Add the `SKILL.md` and its catalog entry in the same change. Keep the catalog alphabetical by skill name.
- In a trusted Codex workspace, you can explicitly delegate a review to the project’s [skill reviewer](.codex/agents/woblar_skill_reviewer.toml). [OpenAI’s subagent guide](https://learn.chatgpt.com/docs/agent-configuration/subagents#custom-agents)

> Have `woblar_skill_reviewer` review my new skill and catalog entry. Report issues with file references.

The library uses Codex’s project defaults. Add project settings for shared runtime needs or package skills as a plugin if they need an installable distribution. [Project configuration](https://learn.chatgpt.com/docs/config-file/config-basic), [MCP](https://learn.chatgpt.com/docs/extend/mcp), [Hooks](https://learn.chatgpt.com/docs/hooks), [Plugin packaging](https://developers.openai.com/plugins/build/plugins)
