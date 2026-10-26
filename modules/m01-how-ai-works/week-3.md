# Week 3: Why models make things up, and how to check them

About 6 hours. This week ends Module 1 with a short work review.

| Part | What | Time |
| --- | --- | --- |
| Learn | Reading below, the hallucination paper (abstract and intro), context engineering article (first part), METR posts, Anthropic terms update | 1.5 h |
| Try and Build | E1.5 verification lab, which produces your fact-checked comparables | 2.5 h |
| Try | E1.6 context experiment | 45 min |
| Check-in | Module 1 work review | 45 min |

## Learn

### Why hallucinations happen

A hallucination is a confident statement that is false: an invented statistic, a book club that doesn't exist, a quote nobody said, a reference to a paper with the right style and the wrong authors.

The 2025 paper by Kalai and colleagues ([S19](../../SOURCE_REGISTER.md)) gives a clear account of why:

1. **Pretraining makes some errors inevitable.** For facts that appear rarely in the training data, such as a small business's founding date, the model has no pattern to learn from. Predicting plausible text there means producing plausible guesses.
2. **Training and testing reward guessing.** Most benchmarks score an answer as right or wrong, with "I don't know" scoring zero. A model that guesses scores higher than one that admits uncertainty, just as a student guessing on a multiple-choice test does. So models learn to bluff.

What this means for you:

- **Rare, specific facts are the danger zone.** Prices, dates, names of small organisations, exact figures, quotations and citations. General explanations of well-documented topics are much safer.
- **Make "I don't know" welcome.** Say so in your prompt: "If you're not sure, say so. An honest 'unknown' is more useful to me than a guess." Your project instructions already do this.
- **Web search helps a lot, but doesn't remove the problem.** With search on, Claude can cite pages. It can still misread them, pick weak sources or blend two sources into one claim. Click the citations for anything that matters.

### A verification workflow

For anything you'll rely on, especially numbers going into your business plan:

1. **Separate the claims.** Ask Claude to list the factual claims in its answer as a numbered list. A paragraph hides claims; a list exposes them.
2. **Triage.** Mark each claim: does it matter for a decision? Is it a rare, specific fact? Those get checked. Common knowledge that doesn't affect anything can pass.
3. **Find the primary source.** The organisation's own website, a company filing, the original study, the official price page. A blog that repeats the claim isn't a check.
4. **Record what you checked**, with the link and the date. Prices and facts change, and you'll want to know how old your evidence is.
5. **Fix or drop.** Correct the claim, mark it "unverified", or remove it.

You'll turn this into your own checklist in E1.5, starting from [templates/verification-checklist.md](../../templates/verification-checklist.md).

### Capability isn't reliability

You'll often see headlines that a model "passed the bar exam" or "beat experts". Two things to keep in mind:

- **A benchmark measures one kind of task in one setting.** Your tasks are different. The only test that tells you how Claude does on your work is trying it on your work, repeatedly.
- **Feeling faster isn't the same as being faster.** METR's 2025 study ([S08](../../SOURCE_REGISTER.md)) found experienced developers using AI tools took longer on their tasks, while believing they'd been faster. Their 2026 update ([S09](../../SOURCE_REGISTER.md)) suggests things have improved and says the evidence is weak either way. The lesson for you isn't "AI is slow". It's: measure what matters, because your impression can be wrong. That's why you'll compare against your week 1 snapshot later.

### Long context, and why fresh chats help

Anthropic's context engineering article ([S01](../../SOURCE_REGISTER.md)) describes **context rot**: as the amount of text in the context grows, the model's ability to recall and use any particular piece of it declines. Practical habits:

- Start a new chat for a new task. Bring across a short summary, not the whole history.
- Put stable material (your business snapshot, your instructions) in the Project, and keep chats focused.
- If a long chat starts going wrong, ask for a summary of decisions so far and continue in a fresh chat.

### Privacy and intellectual property basics

This is general information to help you make sensible choices, not legal advice.

- **Your setting.** You chose "Help improve Claude" on or off in week 1. Anthropic's update ([S20](../../SOURCE_REGISTER.md)) explains the difference: on means chats may be used for training and kept for up to five years; off means the 30-day retention applies to deleted chats.
- **Other people's data.** Member names and email addresses are personal data under UK GDPR. Before pasting a member list or a Stripe export into any AI tool, remove names and emails, or replace them with IDs. You rarely need them to get the analysis you want.
- **Other people's words.** Book extracts, other podcasts' content or someone's article can be pasted for your own analysis, but don't publish AI output that reproduces them.
- **Your own words.** AI-generated text you publish (marketing copy, show notes) is your responsibility. Check facts and make it sound like you.

### Now read

The four items in [readings.md](readings.md) for week 3. For the hallucination paper, the abstract and introduction are enough; the rest is maths.

## Try and Build: E1.5 verification lab (2.5 hours)

This is where the module comes together, and it produces the third piece of your book club plan: a fact-checked list of comparable book clubs and podcasts. Full steps are in [E1.5](../../exercises/m01/exercises.md#e15-verification-lab).

In short:

1. Without web search, ask Claude for comparable book clubs and podcasts with prices and audience size. Pull out 20 factual claims.
2. Predict which are right. Then check each against a primary source and record the result.
3. Repeat with web search on, and compare the error rates.
4. Write your own verification checklist (v1) based on what actually went wrong.
5. Produce the verified comparables table for your plan, with sources and dates.

Compare the result with your week 1 snapshot list from E1.1. How many of those entries would have survived this check?

## Try: E1.6 context experiment (45 minutes)

Hide the same small fact at the start, the middle and the end of a long document, and see whether Claude finds it each time. Steps in [E1.6](../../exercises/m01/exercises.md#e16-context-experiment). It takes a few minutes to set up and gives you a direct feel for how position in a long context matters.

## Module 1 work review (45 minutes)

No test. Send me the work and a short reflection, and we'll look at it together.

**Send:**

1. Your book club plan so far: business snapshot, hypotheses, and verified comparables.
2. Your verification checklist v1.
3. Your E1.5 and E1.6 results.
4. A few sentences on each of these:
   - What do you now do differently when using Claude, compared with three weeks ago?
   - Which kind of task do you trust Claude with more than before, and which less?
   - What's still fuzzy?
   - How did the time work out? Too much, too little, about right?

**What I'll look at:** whether the plan uses only real or clearly labelled figures, whether the checklist reflects mistakes you actually saw, and whether your reflection shows you can predict where Claude goes wrong. I'll write back with what's working, one or two things to focus on, and any changes to Module 2. If something needs another pass, we do it then. It's not a pass or fail.
