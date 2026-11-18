# Woblar skills library

This repository holds reusable workflows for Codex. `README.md` is the human-facing catalog. Keep its entry for each skill current when the skill’s purpose, inputs, outputs, or prerequisites change.

## Add or update a skill

- Give each skill a self-contained folder under `.agents/skills/`. Use a lowercase, hyphenated name that matches the `name` in `SKILL.md`.
- Write a `description` that helps Codex recognize the task. Describe expected inputs, outputs, and an example in the body. Keep scripts, references, and assets inside the skill folder when they are needed.
- Inspect the change and check the affected behavior once. Prefer a small local or mocked check. Get approval before starting a broader suite or build when one is necessary.

## Public repository and authorization

- Use material suitable for public release, including synthetic inputs and examples. Keep credentials, private data, and machine-specific credential paths out of files, logs, and commits. When authorized work needs credentials, load them from the configured environment or a local env file through a parser. Keep their values out of output.
- For security work, state the defensive purpose, the owned or explicitly authorized target, and the permitted scope. Prefer source and configuration review and authorized mitigations. Confirm scope when ownership or authorization is unclear.
- Active security probes, red teaming, abuse simulation, load testing, and live provider or API evaluations each require an explicit request. Preserve existing security controls and use offline checks where practical.
