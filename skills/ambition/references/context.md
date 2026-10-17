# Understanding the user

Step 1 of every run, and the whole of `/ambition context`. The aim: know the person well enough that the lift fits them, without pinning them to notes that are partial, dated or written in one hard season.

## 1. Find what already exists

Read, in this order, stopping when you have enough for the task in hand:
1. `~/.ambition/config.md`: the data folder, context sources and house rules.
2. `profile.md` in the data folder.
3. The context sources the config lists (for example a north star doc, a notes vault, an about-me page).
4. What the agent already has: memory files, global and project CLAUDE.md or AGENTS.md, the project's README or vision doc.
5. The last 10 entries of `record.md`, if it exists.

Small task: the profile summary and anything directly about the task is enough. Large or life run: read more.

Respect the house rules. Never read a place they rule out, even if it looks relevant.

## 2. Decide if it is enough

Enough means you can answer, for this task:
- What is the person trying to achieve beyond this task?
- What will they not trade away (time, health, family, money, integrity, location)?
- What have they already done that shows they can do the bigger thing?

If you can answer two of the three, proceed and ask about the third only if it changes the work.

## 3. If there is not enough: offer three routes

Use AskUserQuestion with these options:
- **Short interview, saved (Recommended for repeat use):** about five minutes. Saved to `profile.md`. Offer to add a one-line pointer to their agent context (global CLAUDE.md, AGENTS.md or the client's memory) so other agents can find it. Ask before writing to any agent context file.
- **Short interview, this run only:** nothing saved.
- **Skip:** run a less personal version. Use the generic lenses, recommend from the task alone, and ask only "What would make this a win for you?"

Also mention once: "Or point me at notes you already have." Reading what exists beats asking again.

## 4. The interview

Five to seven questions, one round where the client allows, choice-based where possible, free text where not. People answer concrete questions better than abstract ones. Adjust to the task; drop any question the context already answers.

1. **Direction:** "In 12 months, what would make you say this year worked?" (free text)
2. **The bigger picture:** "Which matters most right now?" Options built from what you know, for example: income, freedom over time, family, health, craft, recognition, meaning. Allow two picks.
3. **Limits:** "What won't you trade for a bigger result?" Multi-select: evenings and weekends, health, time with family, where you live, money at risk, your name on something you don't believe in. Plus "Other".
4. **A great week:** "Describe a week you'd happily repeat for five years." (free text, two or three lines)
5. **Proof:** "What's something you did that you weren't sure you could?" (free text)
6. **Energy:** "Which kind of work leaves you with more energy than it took?" Options built from the task area.
7. **What's in the way:** "What usually stops you aiming higher?" Options: time, money, confidence, not knowing how, other people, haven't tried. Plus "Other".

## 5. Write the profile (if saving)

```markdown
# Profile

Built: 2026-10-15 from an interview · Last checked: 2026-10-15

> These are working guesses about a person, not a definition of them. Newer requests beat this file.

## Going for
- <claim> · said <date> · confidence medium

## Won't trade
- ...

## Proof (done before)
- ...

## Energy
- gives: ... · takes: ...

## Usually in the way
- ...

## Changes seen
- <date>: picked against the profile on <task>; said <why>.
```

Every claim carries where it came from and when. Keep it under a page. If the context sources already hold this, the profile should point to them rather than copy them.

## 6. Do not over-fit

The trap is honing in too tightly on context that is not absolute and does not show the whole person. Rules:

- **Guesses, not facts.** Every claim about who the user is has a source and a date. Facts about the world (a dose, a deadline, an amount) come from their source; never guess one.
- **Seasons pass.** Goals and fears written during a crisis, a job loss, an illness or a breakup may not hold a year later. When a claim from a hard season decides the recommendation, check it.
- **The request wins.** If today's request points somewhere the profile does not, follow the request and note the gap.
- **One outside-the-profile option.** Every run sketches one version that ignores the stored context. If it is stronger, offer it.
- **Check the claim the recommendation rests on.** If one piece of context decides the outcome and it is older than six months or medium confidence or lower, ask "Is this still true?" in one question.
- **Never build identity from one data point.** One project, one comment or one bad week is not a pattern.
- **Notes are partial.** People write about problems more than what is going well, and about work more than play. Ask about what is missing before concluding.
- **Learn from disagreement.** When the user picks against the profile, record it. Two picks against the same claim: offer to change the profile.

## 7. Saying what you are going on

At the start of each personalised run, one line: what you are relying on and how old it is. This invites correction before anything is built on it. In a skipped run, one line: "Running without your context, so this is less tailored."
