# Woblar skills library

This repository holds reusable workflows for Codex and Claude Code. `README.md` is the catalog. Keep each entry current when the skill’s purpose, inputs, outputs, prerequisites, or license changes.

## Add or update a skill

- Give each skill a self-contained folder at `skills/<name>/`. Use a lowercase, hyphenated name that matches the `name` in `SKILL.md`. Add matching relative directory symlinks in `.agents/skills/` and `.claude/skills/` pointing to `../../skills/<name>`.
- Write a `description` that helps both tools recognize the task. Describe expected inputs, outputs, and an example in the body. Keep scripts, references, and assets inside the skill folder when they are needed.
- Keep the main workflow usable from either host. Describe capabilities the skill needs and what it can deliver when a tool is unavailable. Place host-specific metadata or guidance inside the skill when it helps.
- Set licensing per skill. When adapting an existing skill, verify permission to redistribute the adaptation and carry over the applicable license and attribution. Confirm the rights holder and scope before adding a new license. Keep asset exclusions explicit.
- Inspect the change and check the affected behavior once. Prefer a small local or mocked check. Get approval before starting a broader suite or build when one is necessary.

## Public repository and authorization

- Use material suitable for public release, including synthetic inputs and examples. Keep credentials, private data, and machine-specific credential paths out of files, logs, and commits. When authorized work needs credentials, load them from the configured environment or a local env file through a parser. Keep their values out of output.
- For security work, state the defensive purpose, the owned or explicitly authorized target, and the permitted scope. Prefer source and configuration review and authorized mitigations. Confirm scope when ownership or authorization is unclear.
- Active security probes, red teaming, abuse simulation, load testing, and live provider or API evaluations each require an explicit request. Preserve existing security controls and use offline checks where practical.
