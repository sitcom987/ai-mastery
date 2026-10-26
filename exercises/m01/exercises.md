# Module 1 exercises

Six exercises, E1.1 to E1.6. None are marked. Each produces something you keep: notes, a table or a piece of your book club plan. Bring the results to your weekly check-in.

Save your results in `exercises/m01/results/` in your copy of the repo, or keep them in your Claude Project if you prefer.

---

## E1.1 Starting-point snapshot

**Week 1 · 45 minutes · Produces:** a record of how you work with Claude today

**Why:** in week 9 you'll repeat this task with everything you've learned. Comparing the two is the most honest measure of progress you'll get.

**Steps:**

1. Set a 30-minute timer.
2. Use Claude however you normally would (any chat, with or without search, any prompts) to produce a list of **five book clubs or book-related podcasts similar to yours**, with for each: name, location or platform, price, and audience size (members, attendees or listeners).
3. Stop when the timer ends, finished or not.
4. Save: the final list, a copy or link of the chat(s), and two lines on how confident you feel in the list.

**Don't** fix or check anything yet. The point is a true snapshot. You'll check it in week 3.

---

## E1.2 Tokenizer lab

**Week 1 · 45 minutes · Produces:** notes on how text becomes tokens

**Tool:** [OpenAI's tokenizer](https://platform.openai.com/tokenizer), free and needs no account. It isn't Claude's tokenizer (Claude's has no public demo), so counts will differ, but the patterns are the same.

**Steps:**

1. Prepare six short texts. Before pasting each, write down your guess for how many tokens it will be.
   1. A plain sentence describing your book club.
   2. The same sentence in another language you know, or translated by Claude.
   3. A list of five book titles and author names you've read recently, including at least one unusual name.
   4. A Stripe-style price and date line, such as `£12.50 · 14/11/2026 · 19:30`.
   5. A URL to your website or podcast page.
   6. A made-up word, such as a nonsense name for a new club night.
2. Paste each and record the real count. Click the option to show token boundaries and look at where the splits fall.
3. Answer in a few lines:
   - Which surprised you most?
   - What kind of text costs more tokens per word?
   - Why might counting letters in a word, or doing sums on long numbers, be harder for a model than for you?

---

## E1.3 Explain it back

**Week 2 · 40 minutes · Produces:** your own explanation, plus feedback

**Steps:**

1. Without looking anything up, write about 300 words for an intelligent friend who has never thought about AI. Explain how Claude produces an answer, and why that means you should check its facts before using them in your business.
2. In a new chat, paste your text with this prompt:

   > Here's my explanation of how large language models work, for a non-technical reader. Give me feedback, not a grade. Tell me: (1) anything factually wrong or misleading, quoting my words; (2) one important idea I left out; (3) one sentence that's especially clear. Keep it short. Don't rewrite my explanation.

3. Check Claude's feedback against the week's material. Does it agree with the videos? Did Claude make any claim you now know to be doubtful?
4. Fix anything that was wrong. Keep both versions.

---

## E1.4 Failure prediction

**Week 2 · 1 hour · Produces:** a table of predictions and outcomes

**Steps:**

1. Copy this table into a document.
2. For each prompt, **first** write your prediction: will Claude get it fully right, partly right, or wrong? Add a word on why.
3. Run each prompt in a **fresh chat with web search off**.
4. Record what happened and whether your prediction was correct. Where you can't tell if it was right, note how you'd check.

| # | Prompt | Weakness it probes | My prediction | What happened | Was I right? |
| --- | --- | --- | --- | --- | --- |
| 1 | How many letter e's are in "The Remains of the Day"? | Tokens hide letters | | | |
| 2 | Spell "bibliophile" backwards. | Tokens hide letters | | | |
| 3 | A book club charges £14.50 a ticket. Attendance over eight meetings was 17, 23, 19, 21, 14, 26, 22 and 18. Room hire was £45 a meeting. What was the total profit? Give only the number. | Arithmetic without working | | | |
| 4 | Same as 3, but add: "Show your working step by step." | Room to reason | | | |
| 5 | What were the three most popular book club picks in the UK this month? | Knowledge cutoff | | | |
| 6 | What is your knowledge cutoff date? | Self-knowledge | | | |
| 7 | List five UK book clubs that also run a podcast, with their ticket prices. | Rare, specific facts | | | |
| 8 | Give me the full reference for a peer-reviewed study on why people join book clubs, with the DOI. | Invented citations | | | |
| 9 | Quote the first sentence of a novel you know well. (Choose one, and check against your copy.) | Quotation accuracy | | | |
| 10 | Why is a £20 ticket price better than £12 for a book club? | Agreeing with a premise | | | |
| 11 | Should a book club charge £20 or £12 a ticket? What would you need to know to decide? | Neutral version of 10 | | | |
| 12 | Write a 50-word event description for a book club meeting on a classic novel of your choice. | Fluent writing (strength) | | | |
| 13 | Summarise the plot of a well-known classic novel in three sentences. | Well-documented knowledge (strength) | | | |
| 14 | Summarise the plot of a book published in the last six months. (Name one.) | Cutoff and rare facts | | | |
| 15 | Ask prompt 7 again in a new chat, and compare the two answers. | Sampling variation | | | |

Answer for prompts 3 and 4, so you can check: 160 tickets × £14.50 = £2,320, minus 8 × £45 = £360 room hire, gives £1,960 (before any Stripe fees).

5. Look at the pattern. Write three sentences: when were you right to doubt Claude, when were you too cautious, and what will you do differently?

---

## E1.5 Verification lab

**Week 3 · 2.5 hours · Produces:** your verification checklist v1, and the verified comparables table for your book club plan

**Part A: without search (45 minutes)**

1. In a fresh chat with **web search off**, ask:

   > I run a book club with a podcast. List eight book clubs or book podcasts comparable to mine, with name, location or platform, price, audience size, and how they make money. Tell me how confident you are about each fact.

   (Add a line describing your club, from your business snapshot, so the comparisons fit.)

2. Ask Claude to turn its answer into a numbered list of individual factual claims. Pick 20 (mix of names, prices, sizes, dates).
3. Before checking, mark each claim: likely right / unsure / likely wrong.
4. Check each against a **primary source**: the club or podcast's own site, its ticket page, its podcast listing. Record:

| # | Claim | My prediction | Claude's stated confidence | Result: correct / wrong / can't find | Source checked | Date checked |
| --- | --- | --- | --- | --- | --- | --- |

**Part B: with search (45 minutes)**

5. Turn web search on. Ask the same question in a new chat.
6. Pick up to 20 claims again and check them the same way, including clicking Claude's own citations to see whether they actually say what Claude claims.
7. Compare: how many were wrong or unfindable in A, and in B? Did Claude's stated confidence match reality?

**Part C: your checklist (30 minutes)**

8. Open [templates/verification-checklist.md](../../templates/verification-checklist.md). Edit it into **your** checklist v1: keep what proved useful, delete what didn't, and add a rule for each kind of error you actually saw. Save it as `templates/my-verification-checklist.md`.

**Part D: verified comparables (30 minutes)**

9. Build the comparables table in your book club plan ([projects/p1-book-club-podcast/README.md](../../projects/p1-book-club-podcast/README.md#comparable-book-clubs-and-podcasts)), including **only** entries you have verified, each with its source link and date. Aim for five or more. Mark anything partly verified as such.
10. Look back at your E1.1 list from week 1. How many entries would have passed?

---

## E1.6 Context experiment

**Week 3 · 45 minutes · Produces:** notes on how position in a long context matters

**Steps:**

1. Find a long, plain text: about 15,000 to 30,000 words. A public-domain novel from [Project Gutenberg](https://www.gutenberg.org/) works well (copy the plain-text version).
2. Make three copies. In each, insert this sentence once:

   > The secret meeting place for the Thursday club is the boathouse behind the old mill.

   Put it near the **start** of copy 1, the **middle** of copy 2, and near the **end** of copy 3.
3. For each copy, in a **fresh chat**, paste the whole text and then ask, at the end:

   > Where does the Thursday club meet? Quote the exact sentence.

4. Then repeat each with a harder question that needs the fact plus some reasoning, such as:

   > Based only on this text, if someone wanted to join the Thursday club, where should they go and what building would they pass nearby?

5. Record: found or not, quoted exactly or not, and anything odd.
6. Write two or three sentences: what does this suggest about pasting long documents into a chat, and where should you put the instruction that matters most?

Modern Claude models are good at simple retrieval, so you may find it every time. That's a useful result too. The harder question is where differences, if any, tend to show.
