# Harada Goal Decomposition

An agent skill for turning an ambitious goal into a practical plan using the Harada Method and its Open Window 64 matrix. The instructions are written in the open [Agent Skills format](https://agentskills.io/specification) and are designed for compatible agents, including Claude Code, Codex, Hermes Agent, and OpenCode.

The skill helps you clarify a goal, map the areas that support it, identify actionable steps, and choose a realistic set of priorities for the next one or two weeks. You can also use it to review an existing plan and adjust it based on actual progress.

## What it does

- Defines an outcome, a target date, and observable success criteria.
- Explores why the goal matters and distinguishes actions within your control from external outcomes.
- Organizes the goal into eight supporting areas and up to eight actions for each area.
- Turns the map into stages, checkpoints, near-term actions, and manageable routines.
- Identifies assumptions, dependencies, obstacles, and questions for a weekly review.
- Continues an existing plan without starting over when its history is available.

The Open Window 64 has 81 cells: one central goal, eight supporting areas in the central grid, eight repeated area labels, and 64 surrounding action cells. It is a planning map, not a commitment to tackle everything at once. When information is missing, the skill marks open questions rather than inventing details.

## Installation

Git is required for the commands below. Choose a destination supported by your agent; the destination directory must be named `harada-goal-decomposition` and contain `SKILL.md` directly. If it already exists, review it before replacing it. Restart the agent or start a new session if the skill does not appear.

### Shared directory: Codex, Hermes Agent, and OpenCode

Codex and OpenCode discover `~/.agents/skills` by default. Hermes Agent can use this directory when configured as described below. Some installations use a different home directory.

**macOS and Linux:**

```bash
mkdir -p ~/.agents/skills
git clone https://github.com/wh1tespirit/harada-goal-decomposition.git ~/.agents/skills/harada-goal-decomposition
```

**Windows PowerShell:**

```powershell
New-Item -ItemType Directory -Force "$HOME\.agents\skills" | Out-Null
git clone https://github.com/wh1tespirit/harada-goal-decomposition.git "$HOME\.agents\skills\harada-goal-decomposition"
```

### Hermes Agent configuration

To share the installation above with Hermes, add the directory to `skills.external_dirs` in `~/.hermes/config.yaml` (merge it with existing settings):

```yaml
skills:
  external_dirs:
    - ~/.agents/skills
```

Alternatively, install directly into Hermes' native `~/.hermes/skills/harada-goal-decomposition` directory. A configured Hermes home or profile may change these paths. See the [Hermes skills documentation](https://github.com/NousResearch/hermes-agent/blob/main/website/docs/user-guide/features/skills.md).
### Claude Code

Use Claude Code's personal skills directory:

**macOS and Linux:**

```bash
mkdir -p ~/.claude/skills
git clone https://github.com/wh1tespirit/harada-goal-decomposition.git ~/.claude/skills/harada-goal-decomposition
```

**Windows PowerShell:**

```powershell
New-Item -ItemType Directory -Force "$HOME\.claude\skills" | Out-Null
git clone https://github.com/wh1tespirit/harada-goal-decomposition.git "$HOME\.claude\skills\harada-goal-decomposition"
```

Local Claude Code skills are for local sessions; Claude cloud and Cowork sessions have separate skill availability. See [Claude Code's skill documentation](https://code.claude.com/docs/en/skills) for details.

### Other agents and locations

Place the repository in a skill directory your agent scans, or follow its instructions for importing an Agent Skills-compatible folder. Project-local locations and trust or permission settings vary by agent. Consult the documentation for [Codex](https://learn.chatgpt.com/docs/build-skills), [Hermes Agent](https://github.com/NousResearch/hermes-agent/blob/main/website/docs/user-guide/features/skills.md), or [OpenCode](https://opencode.ai/docs/skills). The optional `agents/openai.yaml` file provides Codex interface metadata; the portable instructions are in `SKILL.md` and do not depend on it.

## How to use it

Ask your agent to use the skill and describe your goal:

```text
Use the harada-goal-decomposition skill to break down this goal
with the Harada Method: I want to launch a useful product within
six months. I can spend five hours per week and have no team yet.
```

Depending on the agent, you can also invoke the skill by name: Claude Code and Hermes Agent support `/harada-goal-decomposition`; in Codex, select or mention `$harada-goal-decomposition`. Invocation and discovery depend on the agent and its configuration.

Include the outcome you want, your desired timeline, your current situation, available time, and known constraints when you can. The skill asks for important missing information or labels assumptions when you request a draft.

For a full breakdown, ask for an **Open Window 64** matrix. For a lighter start, ask for the central goal, eight supporting areas, and a short plan. The skill responds in your language.

To revisit an existing plan, continue the conversation or provide the previous plan and an update:

```text
Use the harada-goal-decomposition skill to review my plan.
Here is what I completed, what got stuck, and how much time
I have next week: ...
```

## Scope and limitations

This is an independent practical adaptation of the Harada Method. It is not an official Harada Institute product, a diagnostic assessment, or a guarantee of achieving a goal. The skill does not create external tasks or reminders unless you separately request and authorize those actions. Compatibility depends on the agent's skill support and configuration.

## Learn more

- [Harada Institute of Education: overview of the method's tools](https://harada-educate.jp/admin/wp-content/uploads/2017/11/61be463c5aeb1b3104a937873850a20d.pdf)
- [The Harada Method: five forms](https://theharadamethod.com/)