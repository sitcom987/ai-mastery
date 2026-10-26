# Verification checklist (starter)

A starting point for checking AI output before you rely on it. In [E1.5](../exercises/m01/exercises.md#e15-verification-lab) you'll turn this into your own version, based on the mistakes you actually see. Save yours as `templates/my-verification-checklist.md`.

## Before you ask

- [ ] Is this a task where a wrong fact would matter (money, a public claim, a decision)? If not, a light check is enough.
- [ ] Have I told Claude that "unknown" is an acceptable answer?
- [ ] Is web search on, if the answer depends on current or specific facts?
- [ ] Have I removed personal data (member names, emails) that the task doesn't need?

## After the answer

1. [ ] **List the claims.** Ask Claude: "List every factual claim in your answer as a numbered list."
2. [ ] **Triage.** Mark claims that matter for a decision or are rare and specific: prices, dates, names of small organisations, statistics, quotations, citations. These get checked.
3. [ ] **Check the primary source.** The organisation's own page, the original study, the official price list. Not a blog repeating it.
4. [ ] **Open the citations.** If Claude cited a page, open it and confirm it says what Claude said.
5. [ ] **Recalculate numbers** yourself or in a spreadsheet.
6. [ ] **Regenerate once** for important answers. If the facts change between versions, treat all of them as unverified.
7. [ ] **Record** the source link and the date you checked it.
8. [ ] **Fix, label or drop** each claim: corrected, "unverified", or removed.

## Warning signs

- Very precise figures with no source (for example "37.4% of book club members…")
- References that look perfect but you can't find
- An answer that agrees with how you framed the question
- Reasoning that sounds convincing but ends in a number you haven't checked
- Anything about events after Claude's knowledge cutoff, without search

## My additions (from E1.5)

-
