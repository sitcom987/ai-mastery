# Week 1: What an LLM actually does

About 6 hours. Spread it over three or four sessions rather than one long one.

| Part | What | Time |
| --- | --- | --- |
| Setup | Privacy setting and a Claude Project for the course | 15 min |
| Try | E1.1 starting-point snapshot | 45 min |
| Learn | Reading below, then 3Blue1Brown Chapter 5 and the first hour of Karpathy | 2 h |
| Try | E1.2 tokenizer lab | 45 min |
| Build | Book club business snapshot | 2 h |
| Check-in | Send me your snapshot and your notes | 30 min |

## Setup (15 minutes)

1. **Choose your privacy setting.** In claude.ai go to Settings → Privacy and look at "Help improve Claude". When it is on, your chats can be used to train future models and are kept for up to five years. When it is off, deleted chats are removed from Anthropic's systems within 30 days ([S20](../../SOURCE_REGISTER.md)). Either choice is fine. You'll be talking about your business, so pick the one you're comfortable with and make it a conscious choice.
2. **Create a Claude Project** called "AI course". Projects keep files and instructions together, so you don't re-explain yourself every chat. Add this as the project instructions:

   > I'm Adam. I run a book club with a podcast, and I'm taking a six-month course to get much better at using AI. When I give you figures about my business, use only what I give you. If something is missing, ask me; never fill a gap with a typical or assumed number. When you state a fact about the outside world, tell me how confident you are and whether I should check it.

3. Add this repo's folder for the week (or paste the files) whenever you want Claude to see the course material.

## Try: E1.1 starting-point snapshot (45 minutes)

Before learning anything, record where you are now, so that in week 9 you can see how far you've come. Full instructions are in [E1.1](../../exercises/m01/exercises.md#e11-starting-point-snapshot). In short: give yourself 30 minutes to use Claude however you normally would to find five book clubs or book podcasts similar to yours, with their prices and audience size. Save the chat and your list exactly as they are. Don't fix them.

## Learn: what happens when you press Enter

Read this first, then watch the videos. The videos will make more sense with this map in your head.

### The one-sentence version

A large language model (LLM) is a very large mathematical function that reads text and outputs a probability for every possible next piece of text, and it writes answers by doing that over and over.

### The steps, in order

1. **Your text is cut into tokens.** A token is a chunk of text: often a whole common word, sometimes part of a word, a space, or punctuation. "Book club" might be two tokens; an unusual surname might be four. The model never sees letters directly, only token numbers.
2. **Each token becomes a long list of numbers** (an *embedding*). Tokens with related meanings end up with similar lists. This is how "novel" and "book" come to be treated as related without anyone writing that rule.
3. **The lists pass through many layers.** In each layer, every token "looks at" the other tokens and updates its numbers based on them (this is *attention*, the subject of week 2). After dozens of layers, the numbers for the last position hold a compressed sense of everything relevant so far.
4. **The model outputs probabilities for the next token.** Not one answer: a ranked list over its whole vocabulary of tens of thousands of tokens. "The meeting is on" might put "Tuesday" at 8%, "the" at 6%, and so on.
5. **One token is picked**, usually not always the top one. A little randomness (*sampling*) makes the writing less robotic. That's why the same question can get a different answer each time.
6. **The chosen token is added to the text, and the whole thing repeats** until the model produces a "stop" token. A 500-word answer is roughly 700 rounds of this.

### What follows from this

These consequences matter more than the mechanics. Each one changes how you should use Claude.

- **Fluent isn't the same as true.** The model is trained to produce likely-sounding text. A confident, well-formatted answer tells you the model has seen lots of text shaped like that, not that the facts are right.
- **It can't look things up unless it is given a tool.** Without web search, everything it "knows" comes from patterns in its training data, which stops at a cutoff date. Ask about a book club that started last year and it may describe one that sounds plausible.
- **Tokens explain some strange failures.** Counting letters in a word, reversing text, or exact arithmetic on long numbers are hard because the model sees chunks, not characters. This is why you check Claude's sums for your business plan, or ask it to use a calculation tool.
- **Everything it works with is in the context window.** The context window is the text the model can see at once: your project instructions, files, the whole conversation so far, and its own replies. It has no memory beyond that, except features that put saved notes back into the context for you.
- **The first words of an answer steer the rest.** Because each token is chosen based on the ones before, an answer that starts down a wrong path tends to keep going. Asking it to think step by step, or to check before concluding, gives it room to get there.
- **Same prompt, different answer.** Sampling means one good answer doesn't prove the next will be good. For anything important, regenerate once or twice and compare.

### Now watch

- 3Blue1Brown, Chapter 5 (30 min). Watch for: the "predict, sample, repeat" loop, and embeddings as directions in space.
- Karpathy, first hour (60 min). Watch for: where the training text comes from, his tokenizer demo, and what a "base model" does before it's turned into an assistant.

Links and dates are in [readings.md](readings.md). Pause and jot down anything that surprised you. Bring those notes to the check-in.

## Try: E1.2 tokenizer lab (45 minutes)

See tokens for yourself. Full steps are in [E1.2](../../exercises/m01/exercises.md#e12-tokenizer-lab). You'll paste pieces of your own book club text into a free online tokenizer and predict, before you look, which will use the most tokens.

One caveat: the free tokenizer is OpenAI's. Claude uses its own tokenizer, which splits text differently and doesn't have a public web demo. The lesson carries over (text is chunks, unusual words cost more), but the exact counts won't match Claude's.

## Build: book club business snapshot (2 hours)

This is the first piece of your book club plan. The aim is one honest page describing the business today and what "profitable" means for you. Template: [business-snapshot.md](../../projects/p1-book-club-podcast/business-snapshot.md).

**How to do it with Claude:**

1. In your "AI course" project, start a new chat and paste in the template.
2. Ask Claude to interview you to fill it in, one question at a time. Use something like:

   > Interview me to fill in this business snapshot, one question at a time. Use only my answers. If I don't know a figure, write "unknown" and add it to the list of things to find out. Don't suggest typical figures. At the end, show the completed snapshot and list every calculation you did so I can check it.

3. Answer from your real records: Stripe payouts, past events, your own costs. Rough is fine; label it "estimate".
4. **Check every calculation yourself**, with a calculator or a spreadsheet. This is deliberate practice in the habit from today's reading: the arithmetic is where a fluent answer can be quietly wrong.
5. Save the finished file as `projects/p1-book-club-podcast/business-snapshot.md` in your copy of the repo (or keep it in the Claude Project, and send it to me at check-in).

Things to notice while you do it: did Claude ever slip in a number you didn't give it? Did it ask good questions? Note both.

## Optional: flashcards (5 minutes, a few times a week)

Import [flashcards.csv](flashcards.csv) into Anki (File → Import) or any app that reads CSV. The week 1 cards are tagged `w1`. Trying to recall an answer before you look is one of the two study habits with the strongest evidence behind them ([S11](../../SOURCE_REGISTER.md)). Skip it if it doesn't suit you.

## Check-in (30 minutes)

Send me in this thread:

1. Your business snapshot.
2. Your E1.1 list and chat (as they are; no tidying).
3. Two or three things from the videos that surprised you or didn't make sense.
4. How long the week actually took.

I'll give you feedback on the snapshot, answer your questions, and adjust week 2 if needed.
