---
name: ambition
description: >-
  Lift the ambition of whatever the user is working on before doing it. First understands who the
  user is and what they want (from existing context, a short interview, or neither), then runs the
  task through four lenses from Felix Rieseberg's "How to be more ambitious" (Speed, Altitude,
  Depth, Range), checks the lifted version against what matters to them, and hands back a sharper
  brief at the level they choose. Over time keeps a map of what they truly care about (their
  Ikigai), built from the choices they make across runs. Use for "/ambition", "lift the ambition",
  "aim higher", "what's the bigger version of this", "be more ambitious with this", "ikigai", or
  "/ambition life". Not for routine tasks the user has not asked to lift.
---

# /ambition

Invoke with:
- `/ambition <task>`: lift one task (code, work or life), then do it at the chosen level.
- `/ambition` alone: lift whatever is being worked on in this chat.
- `/ambition life`: build or refresh the Ikigai map. Read `references/life.md`.
- `/ambition review`: read the record of past runs, find the pattern, update the map. Read `references/record.md`.
- `/ambition context`: build, check or update the user's context on purpose. Read `references/context.md`.

Source article: https://felixrieseberg.com/how-to-be-more-ambitious-a-tutorial-for-humans-with-models/ (Oct 2026). The lenses are in `references/lenses.md`. Read it on every task run.

## What this skill believes

1. **Ambition means a better outcome, not more effort.** A lift that quietly costs the user's health, family or the limits they have set has failed, however impressive it looks. The best lifts make the work bigger and the user's share of it smaller.
2. **Know the person, but hold it loosely.** Context makes the lift fit. But notes about a person are partial, dated and often written in one hard season. Treat every piece of context as a guess with a date, never as who they are. The current request beats stored context. (Full rules in `references/context.md`.)
3. **The model goes first.** Most people react to a sharp draft better than they answer open questions. Do the thinking, show it briefly, and ask only what only the user can answer.
4. **Choices reveal more than statements.** What someone picks from three concrete versions tells the truth about what they want. Every pick goes in the record. Over months the record shows their real direction better than any interview.
5. **People are limited by what they think is possible.** Each run names proof that the bigger version can be done: something the user has already done, and someone else who did the bigger thing.
6. **The model does not mark its own homework.** Every lifted brief names an outside judge: a test, real data, a customer, a number, a fresh reader.
7. **Never stall the original task.** The plain version stays available. A lift that turns into weeks of indecision is worse than shipping the plain one.

## Where things live

Look for `~/.ambition/config.md`. It can name:
- the **data folder** (default `~/.ambition/`);
- the user's **context sources** (files or folders that describe them, in reading order);
- **house rules** (places never to read, topics to handle with care, style rules).

The data folder holds:
- `profile.md`: the user's context as this skill understands it (only if they chose to save one).
- `map.md`: the Ikigai map.
- `record.md`: one entry per run.

If there is no config, use `~/.ambition/` and create it only when there is something to save.

## Task run: the flow

### 1. Understand the user (always first)
Follow `references/context.md`. In short:
- **Find context.** Read the config, `profile.md`, the listed context sources, and whatever the agent already has loaded (memory files, CLAUDE.md, AGENTS.md, project docs). Read only what this task needs.
- **If there is enough:** say in one line what you are going on and how old it is, for example "Going on your profile (June) and north star (March): family time and income come first." This lets the user correct you before anything is built on it.
- **If there is none or too little:** offer three routes with AskUserQuestion: a five-minute interview saved as a profile (and a pointer added to their agent context if they want), the same interview used for this run only, or skip and get a less personal version.
- **If it matters and looks stale or shaky:** ask one "is this still true?" question before relying on it.

### 2. Size the run
Judge the stakes. Say the size in one line.
- **Small** (a feature, an email, a doc): lenses inline, about two minutes. Recommend Plain by default. Recommend higher only when the lift costs the user no extra time and clearly changes the result; then add that one lift to the plain work rather than enlarging the job.
- **Large** (a product, a role, a launch, big money, anything touching career or family): full flow, fresh-context red team (step 6), up to three questions.
- If the task is huge and vague ("fix my life"), switch to life mode.

### 3. Say what the task really does
Rewrite the task as a verb sentence (Range, noun to verb). "A quarterly review deck" becomes "getting busy people to believe a story about cause and effect and decide in 30 minutes." Show this first. It often reframes the work on its own.

### 4. Run the four lenses
Follow `references/lenses.md`. In short:
- **Speed:** the plain version, done fast. One line. The floor and the fallback.
- **Altitude:** ask "and then what?" up a ladder of four to six rungs, from the task to a life outcome. Recommend the highest rung that can start this week and that an agent could keep running. Name the setup change that takes the user out of the loop.
- **Depth:** what a top practitioner would do that the user did not ask for. Rawest material, real instruments, the belief to test against raw data, the new knowledge to produce, an unreasonable target stated as normal, and the outside judge.
- **Range:** three to five fields that do the verb well, each with what it *does* (never role-play). Always one red-team field and one field from far away.

### 5. Check the lift against the person
Drop or reshape any lift that fails.
- **What matters to them:** does it respect their stated limits and priorities?
- **Hours:** if the user has said how much time they have, every estimate of their time must fit inside it. If the lift does not fit, cut it until it does and list the rest as "later", or recommend Plain. Never present a version that needs more of their hours than they have. If no limit is known, say the hours.
- **Outside the profile:** if a profile or stored context shaped the lift, also sketch one version that ignores it entirely. If it is better, offer it. This is how the skill avoids boxing someone into old notes. In a skipped run there is nothing to step outside, so leave this out.
- **Blind spots:** is the lift serving the outcome or a need to look impressive? Is it a way to avoid a smaller, harder conversation? If the context lists known patterns, check the obvious one, once, without lecturing.
- **Every path:** prefer lifts that pay off whichever way their bigger decisions go.
- **Proof:** one thing they have already done that is close (with source), and one public example of someone doing the bigger version. If nothing is known about the user, give only the public example and say their own proof is unknown. If there is no honest proof at all, call it a long shot.

### 6. Outside judge on the plan (large runs only)
Spawn one fresh-context agent with `references/red-team.md`. Give it only the original task, the lifted brief and a short list of the user's limits as they stated them, never the chat transcript or your reasoning. Fold its findings in and say what changed. In a client without subagents, run the red-team brief as a separate pass after clearing your framing.

### 7. Ask the user (one round)
Use AskUserQuestion (or the client's equivalent). Question budget for the whole run, not counting the context question in step 1: one or two on small runs, up to three on large runs. Put them in one round. Each must be something only the user can answer: appetite, values, what a win means, a limit you do not know. Never ask about implementation.
- **Always ask the level.** Three options, each one line saying what they get and what it costs:
  - Plain: the task as asked, done well.
  - Ambitious: the recommended rung with depth and range applied.
  - Unreasonable: the specific, hard goal, stated as normal.
  Mark one "(Recommended)": on small runs, Plain unless step 2 says otherwise. On large runs, if the record shows they usually pick one level, recommend one notch above their habit, and say so.
- In a skipped run, the second question is "What would make this a win for you?" Otherwise add a second question only when an answer changes the work, for example "Which of these would count as a win?" with concrete outcomes. Use option previews to show a concrete picture (a Tuesday in that life, the first screen, the email that lands).
- If the user said "just go" or gave the level up front, skip the questions and say what you picked.

### 8. Hand back the work
When the task is a piece of work (an email, a letter, a spec, a plan), the finished work comes first and stands on its own. Keep the ladder, lenses, proof and your reasoning out of it: the user reads and uses the work, not how you got there. Add at most one line saying which lift you applied.

At plain, just do the task well and skip the brief. At ambitious or unreasonable, put a short brief after the work (at most five lines on small runs), in this order, skipping what adds nothing:
1. **What this really is:** the verb sentence.
2. **The ladder:** the rungs, with the chosen one marked.
3. **The lifted brief:** a rewritten prompt or plan the user (or an agent) can run as is. It names the material, tools, target, crew and outside judge.
4. **What it costs:** time, money, the user's hours, risk.
5. **Proof:** the two examples.
6. **What stays plain:** the fallback.

When the task is the plan itself (a launch, a role, a life decision), the brief is the work: give it in full.

Work inside the authority the user already gave. The lift never grants new authority: messages, publishing, spending, commits and deploys keep their own rules.

### 9. Record it and learn
If the user has a data folder, append an entry to `record.md` (format in `references/record.md`) and confirm in one line. If they chose a session-only or skipped context, record nothing unless they ask, and do not use stored context to personalise the run.

When the user picks against what the context predicted, or says "that's not me any more", note it in the record and offer to update the profile. Context should get more accurate with use, not more fixed.

When a later chat shows how an earlier lift went, add the outcome. The record of ambitious bets that worked is the proof file that lets the next run aim higher.

## Voice
Follow the user's own style instructions if they have them. Otherwise: plain English, short sentences, no hype, no therapy language, no motivational lines. Be direct about long shots. On family, health and legal matters, plain sentences only.

## Do not
- Do not run uninvited on routine tasks.
- Do not treat stored context as the whole person, or as current, without checking.
- Do not role-play experts. Use what the field does.
- Do not ask people to rate abstract values. Show concrete choices.
- Do not lift by adding the user's hours.
- Do not let the model judge its own work.
- Do not read anything the config's house rules put off limits.
