# Harada Goal Decomposition

A reusable Codex skill for turning an ambitious goal into a concrete plan using the Harada Method and its Open Window 64 matrix.

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

### macOS and Linux

Clone this repository into your personal Codex skills directory:

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/wh1tespirit/harada-goal-decomposition.git ~/.codex/skills/harada-goal-decomposition
```

### Windows PowerShell

```powershell
New-Item -ItemType Directory -Force "$env:USERPROFILE\.codex\skills" | Out-Null
git clone https://github.com/wh1tespirit/harada-goal-decomposition.git "$env:USERPROFILE\.codex\skills\harada-goal-decomposition"
```

If you use a custom `CODEX_HOME`, place the repository in its `skills/harada-goal-decomposition` directory instead. If the destination already exists, review it before replacing it. Restart Codex or start a new session if the skill does not appear immediately.

## How to use it

Invoke the skill in a Codex conversation and describe your goal:

```text
$harada-goal-decomposition
Help me break down this goal using the Harada Method:
I want to launch a useful product within six months.
I can spend five hours per week, and I am starting without a team.
```

Include the outcome you want, your desired timeline, your current situation, available time, and known constraints when you can. The skill asks for important missing information or labels assumptions when you request a draft.

For a full breakdown, ask for an **Open Window 64** matrix. For a lighter start, ask for the central goal, eight supporting areas, and a short plan. The skill responds in your language.

To revisit an existing plan, continue the conversation or provide the previous plan and an update:

```text
$harada-goal-decomposition
Review my Harada plan. Here is what I completed, what got stuck,
and how much time I have next week: ...
```

## Scope and limitations

This is an independent practical adaptation of the Harada Method. It is not an official Harada Institute product, a diagnostic assessment, or a guarantee of achieving a goal. The skill does not create external tasks or reminders unless you separately request and authorize those actions.

## Learn more

- [Harada Institute of Education: overview of the method's tools](https://harada-educate.jp/admin/wp-content/uploads/2017/11/61be463c5aeb1b3104a937873850a20d.pdf)
- [The Harada Method: five forms](https://theharadamethod.com/)