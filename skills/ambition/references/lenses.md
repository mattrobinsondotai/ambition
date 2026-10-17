# The four lenses

From Felix Rieseberg, "How to be more ambitious: a tutorial for humans with models" (felixrieseberg.com, Oct 2026). Summarised and adapted. Each lens has the questions to answer and the test that a lens was done properly.

## 1. Speed: the floor

The same work, faster. Rieseberg skips it because it is well understood. Here it does one job: it states the plain version in one line, so the lift never blocks the task.

- Write: "Plain version: <what gets done>, about <time>."
- Test: the user could say "just do the plain one" and lose nothing.

## 2. Altitude: aim at the outcome, not the task

Ask "what do you want to happen next?" and then "and after that?". Rieseberg moved from "fix this crash" to "keep my apps crash-free".

Build a ladder of four to six rungs:
1. The task as asked.
2. The result the task is for.
3. The result that result is for.
4. ...up to a life outcome in the user's own terms (from their context if known: income, time, family, health, freedom, meaning).

Then choose the rung to recommend:
- The highest rung that can start this week.
- The rung where a loop could keep running without the user (a workflow, an agent, a schedule, a product).
- Not a rung so high it becomes "go make money". Rieseberg: that does not work yet for most businesses.

Name the setup change that makes the rung possible. Rieseberg had to make crash reports easy to fetch, map versions to commits and give Claude machines to test on. Often this is: give the agent the data, a way to check its own result, and a schedule.

Signals Altitude fits: the work has an end outcome, and it would normally take meetings. It fits creative work less well.

Example ladder:
1. Write this week's newsletter.
2. Get readers to open and finish it.
3. Grow to readers who forward it.
4. A newsletter that brings in work or income without more weekly hours.
5. Work the user chooses, on their terms.
Recommended rung: 4. Setup change: an agent that drafts from the week's notes, tracks which issues brought replies and suggests the next topic, so the user only edits and sends.

Test: the chosen rung changes what gets built, not only how it is described.

## 3. Depth: work like the best in the field

Go below the surface of the task into the raw data, tools and problems. Keep going until an expert could learn something from the result.

Answer each, in one or two lines:
- **What would a top practitioner do here that the user did not ask for?**
- **Rawest material:** the source data they would start from (logs, transactions, transcripts, the actual job ads, the actual customer messages), not a summary.
- **Instruments:** the tools and methods they would use. If the default would be a markdown table, the expert uses a database, a statistical model, a simulation, a prototype. The user does not need to know these tools. The model does.
- **Belief to test:** the thing everyone assumes. Try to reproduce it from raw data, adversarially. "We think churn is an onboarding problem: show it from the raw events."
- **New knowledge:** the blind spot the result could find. Build something that reproduces the past, then look for the earliest signal nobody knows about, then test it on data it has not seen.
- **Unreasonable target, stated as normal:** a specific hard number. 200ms not 5 seconds. If the model thinks it is impossible, say it is solvable and keep going. Locke and Latham: specific hard goals beat "do your best".
- **Outside judge:** what, other than the model or the user, checks the result. A test suite, a holdout set, a real customer, a market price, a fresh-context reader, a number that moves. Prefer something the agent can run itself for fast feedback.

Rieseberg's rewrite move: before writing the brief, state what a top professional would do that was not asked for, the rawest material, the methods and tools, and what outside the model would verify it. Then rewrite the prompt to ask for exactly that.

Test: the brief names real material, a real instrument and a real judge. If any are vague, it is not deep yet.

## 4. Range: bring in other fields

Draw on fields the user would not normally think of. Rieseberg had never thought of Blender for his homepage until he saw a colleague render interiors with it.

Steps:
1. **Nouns to verbs** (Kelley and Littman, *The Art of Innovation*). Write what the task does as a verb sentence. The verbs point to fields.
2. **Assemble the crew.** Three to five fields that are best at those verbs. For each, one line on what that field *does* that would help. Include:
   - one red-team field (short seller, forensic accountant, opposing counsel, a hostile customer, a recruiter screening 300 CVs);
   - one field from far away (game design, sports coaching, film editing, epidemiology, architecture, kitchen brigades).
3. **No role-play.** Do not write "as a short seller". Do what a short seller does to research a position. Role-play makes the work weirder, not better.
4. For large runs, these fields can become parallel subagents, each doing its field's work on the raw material.

Test: at least one field would surprise the user, and each field changes something concrete in the brief.

## Why it matters: belief

Rieseberg's closing point: people are limited by what they believe is possible. Belief in your own ability (self-efficacy) can be built on purpose.

- After Bannister broke four minutes, others followed within weeks.
- Dantzig solved two unsolved problems because he thought they were homework.
- *The Inner Game of Tennis*: trying very hard can get in the way.

So every run shows proof (one thing the user has already done that is close, and one public example of the bigger thing done), and frames the unreasonable target as ordinary work. The record of past lifts that worked is the long-term version of this: the user's own proof file.
