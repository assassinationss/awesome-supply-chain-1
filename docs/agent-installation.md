# Install the supply-chain skills

The repository follows the open [Agent Skills specification](https://agentskills.io/specification). Each skill is a directory containing `SKILL.md`, with optional references, scripts, assets, agent metadata, and output templates.

## Install one skill across coding agents

The cross-agent `skills` CLI supports Codex, Claude Code, Cursor, GitHub Copilot, and many other compatible agents.

List the available skills:

```bash
npx skills add kishorkukreja/awesome-supply-chain --list
```

Install the decision-framing skill interactively:

```bash
npx skills add kishorkukreja/awesome-supply-chain --skill supply-chain-decision-to-delegation
```

Install it globally for Codex and Claude Code:

```bash
npx skills add kishorkukreja/awesome-supply-chain \
  --skill supply-chain-decision-to-delegation \
  --global \
  --agent codex \
  --agent claude-code
```

Use `--copy` when the environment cannot create or follow symbolic links.

## Claude Code plugin

The repository is a Claude Code marketplace and plugin. Add the marketplace, then install the plugin:

```text
/plugin marketplace add kishorkukreja/awesome-supply-chain
/plugin install supply-chain-skills@awesome-supply-chain
```

For local validation or development:

```bash
claude plugin validate .
claude --plugin-dir .
```

Plugin skills are namespaced by Claude Code. Invoke the new skill with:

```text
/supply-chain-skills:supply-chain-decision-to-delegation
```

## Codex

Install the selected skill through the cross-agent CLI shown above, or copy the skill directory into the Codex skills directory.

Project-scoped installation:

```bash
mkdir -p .agents/skills
cp -R skills/supply-chain-decision-to-delegation .agents/skills/
```

User-scoped installation:

```bash
mkdir -p ~/.codex/skills
cp -R skills/supply-chain-decision-to-delegation ~/.codex/skills/
```

Start a new Codex thread after installing so the skill can be discovered. The skill contains `agents/openai.yaml` for Codex-facing metadata and uses normal implicit invocation.

## Claude Code standalone skill

Project-scoped:

```bash
mkdir -p .claude/skills
cp -R skills/supply-chain-decision-to-delegation .claude/skills/
```

User-scoped:

```bash
mkdir -p ~/.claude/skills
cp -R skills/supply-chain-decision-to-delegation ~/.claude/skills/
```

## Other compatible agents

Use the `skills` CLI and select the target agents interactively, or pass one or more `--agent` values. The skill itself remains portable because the core workflow is in `SKILL.md` and supporting Markdown files.

Agent-specific metadata is optional:

- Claude Code uses the repository's `.claude-plugin/plugin.json` and marketplace.
- Codex can use `.codex-plugin/plugin.json` and each skill's `agents/openai.yaml`.
- Other Agent Skills-compatible tools use the standard `SKILL.md` structure.

## Verify an installation

Ask the agent:

> Help me turn a recurring supplier-delay problem into a scoped decision and identify whether an AI use case is justified.

The agent should invoke `supply-chain-decision-to-delegation`, begin with a concrete operating moment, and avoid recommending an agent before clarifying the decision owner, evidence, stakes, reversibility, and consequences.

## Source specifications

- [Agent Skills specification](https://agentskills.io/specification)
- [Claude Code plugins](https://code.claude.com/docs/en/plugins)
- [Claude Code plugin marketplaces](https://code.claude.com/docs/en/plugin-marketplaces)
- [Cross-agent skills CLI](https://github.com/vercel-labs/skills)
