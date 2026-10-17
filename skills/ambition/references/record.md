# The record, the map and review mode

All three files live in the data folder (see SKILL.md, Where things live). Profile format is in `context.md`.

## record.md: one entry per run

Append at the bottom. Newest last. Dates in the user's time zone.

```markdown
### 2026-10-15 · Cover letter for a product lead role
- **Kind:** task (large) | life bet
- **Where:** <project or area>
- **Really:** <the verb sentence>
- **Ladder:** 1 <task> → 2 ... → 5 <life outcome>
- **Offered:** plain / ambitious (rung 4, recommended) / unreasonable
- **Picked:** ambitious
- **Why (their words if given):** ...
- **Against the profile?** no | yes: <what the profile predicted>
- **Top rung touched:** <which life outcome the ladder ended at, in the user's own terms>
- **Red team changed:** <one line, or "not run">
- **Outcome:** open | shipped <date> | dropped <date>, because ... | worked: <evidence> | flopped: <evidence>
```

For a life bet, replace Ladder, Offered and Picked with:
```markdown
- **Experiment:** <what>
- **Signal:** <what to watch>
- **Check on:** <date>
```

## map.md: the Ikigai map

```markdown
# Ikigai map

Version: 2026-10-15 · Confidence: low | medium | high

## Best guess
<Name> does X, for Y, paid by Z, in a way that keeps W.

## Loves
- <claim> · shown · <source, date> · high

## Good at
- ...

## Paid for
- ...

## Needed for
- ...

## Overlaps
- <what sits in more than one circle>

## Gaps (stated vs shown)
- Says <x> (<source>), but does <y> (<source>).

## The ring (hard limits)
- <the limits they won't trade>

## What the notes don't cover
- <areas the evidence is silent on>

## Live experiments
- <experiment> · check <date> · see record

## Previous versions
<older best guesses with dates, newest first>
```

## Review mode (`/ambition review`)

Run monthly, or when the user asks. Read `record.md` in full and `map.md`.

Work out, with numbers:
1. **How high they aim.** Count picks by level. If most are plain, say so.
2. **Hit rate.** Of ambitious and unreasonable picks with an outcome, how many worked. A high hit rate with mostly plain picks means they are aiming too low. Say that plainly with the count.
3. **The recurring top rung.** Which life outcome the ladders end at across unrelated tasks. The one that keeps appearing is a real driver, whatever their stated goals say.
4. **Picks against the profile.** Claims the user keeps choosing against. Offer to change or drop them.
5. **Drops.** Which lifts they dropped and why. Repeated drops for the same reason show a hidden limit or a fear. Name it once, without judgement.
6. **Life bets due.** Any experiment past its check date without an outcome: ask for the signal in one question.

Then:
- Add new `shown` evidence to the map and move stale claims down. Mark profile claims older than a year for a check.
- Set the default push for the next month (for example: "recommend one notch above plain").
- Report: three lines of findings, one change to the map, the push level, any bets due.
- If the review has run by hand twice, offer once to schedule it monthly.
