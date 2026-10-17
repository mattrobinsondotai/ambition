# ambition

A skill for Claude Code, and any agent that reads `SKILL.md` files. Before it does a task, the assistant works out what the task is really for, finds the version a top practitioner would do, and checks it against your time and your limits. You pick the level (plain, ambitious or unreasonable), then it does the work.

Built on Felix Rieseberg's essay [How to be more ambitious: a tutorial for humans with models](https://felixrieseberg.com/how-to-be-more-ambitious-a-tutorial-for-humans-with-models/). The four lenses (Speed, Altitude, Depth and Range) are his.

## Use it for

- **A job application.** Find the one fact about the employer that turns your weakest point into a strength.
- **A product feature.** Aim at the problem behind the request, sized to the hours you actually have.
- **A launch or a campaign.** Set a measurable result, and name what will tell you whether it worked.
- **A report for a busy reader.** Answer the question they are really asking, on one page.
- **A side project.** Find the version that keeps paying off without more of your evenings.
- **A big personal decision.** `/ambition life` maps what you care about before you choose.

Small jobs stay small. On an email or a quick fix, it recommends the plain version and does it well.

## Install

**Claude Code:**

```
/plugin marketplace add mattrobinsondotai/ambition
/plugin install ambition@ambition
```

Or copy the skill in directly:

```bash
git clone https://github.com/mattrobinsondotai/ambition
cp -R ambition/skills/ambition ~/.claude/skills/
```

**Codex and other agents:** copy `skills/ambition` into the agent's skills folder.

**claude.ai:** zip `skills/ambition` and upload it as a custom skill in settings.

## Commands

- `/ambition <task>`: lift a task, then do it at the level you pick.
- `/ambition`: lift whatever you're working on.
- `/ambition life`: map what you care about.
- `/ambition review`: look back over past runs.
- `/ambition context`: set up what it knows about you.

## Licence

MIT. The lenses come from Felix Rieseberg's essay. Read the original.
