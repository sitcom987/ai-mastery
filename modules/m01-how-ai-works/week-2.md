# Week 2: How an assistant is made, and the limits of its reasoning

About 6 hours.

| Part | What | Time |
| --- | --- | --- |
| Learn | Reading below, Karpathy post-training section, 3Blue1Brown Chapter 6, Anthropic "Tracing the thoughts" | 2.5 h |
| Try | E1.3 explain it back | 40 min |
| Try | E1.4 failure prediction | 1 h |
| Build | Customer and audience hypotheses | 1.5 h |
| Check-in | Send me your hypotheses and notes | 30 min |

## Learn

### From text predictor to assistant

Last week's model, trained only to predict the next token of internet text, is called a **base model**. Ask it "What's a good book for a club?" and it might continue with more questions, as if it were writing a forum page. It isn't trying to help; it's continuing a document.

Turning it into Claude takes a second stage, **post-training**:

1. **Supervised fine-tuning.** The model is trained further on many example conversations written to show a helpful assistant. It learns the *shape* of being an assistant: answer the question, use a friendly tone, format things clearly.
2. **Reinforcement learning.** The model produces answers, and those answers are scored, by people's preferences, by other models applying written principles, or by automatic checks such as "did the code run?". The model is nudged towards higher-scoring behaviour. This is where much of the step-by-step reasoning ability now comes from.

What this means for you:

- **The knowledge comes from pretraining; the manners come from post-training.** Post-training doesn't add much new knowledge. If a fact wasn't in the training data, a polite assistant won't know it either.
- **It has a knowledge cutoff.** The training data stops at a date. Anything after that, such as a new podcast, a price change or a new law, is unknown unless you give it the information or it searches the web.
- **It's trained to be helpful, which can make it agreeable.** It may go along with a premise in your question rather than challenge it. "Why is my book club the best in town?" invites an answer that assumes it is. Ask neutral questions when you want a real assessment.

### Attention and the context window

**Attention** is how each token's numbers get updated using the other tokens. In "the club meets at the library because it is free", attention is what lets "it" pick up meaning from "library" rather than "club". Every layer does this many times in parallel, each looking for different kinds of relationship.

Practical consequences:

- **More context isn't free.** Everything in the window competes for attention. Long chats with lots of side-tracks can make answers worse ("context rot", week 3 reading). Start a fresh chat for a new task, and put the important material in clearly.
- **Position matters somewhat.** Models often handle the beginning and end of a long document better than the middle. You'll test this yourself in week 3 (E1.6).
- **Be explicit about what matters.** If one constraint is critical ("prices must include VAT"), say so plainly and near your actual request, rather than relying on Claude to spot it in a long paste.

### Sampling, and why you can't see the dial

Each next token is drawn from the probability list. A setting called **temperature** controls how adventurous the draw is: low means it nearly always picks the most likely token; higher means more variety. In claude.ai you can't change it. What you *can* do is press regenerate (the retry arrow) and compare. If three regenerations give three different "facts", none of them is reliable.

### Reasoning, and why explanations can mislead

Current Claude models can "think" before answering, writing out working that you can sometimes see. This genuinely improves results on multi-step problems.

But Anthropic's interpretability research ([S18](../../SOURCE_REGISTER.md)) found that a model's description of *how* it reached an answer doesn't always match what happened inside it. In one example, the model added numbers with internal shortcuts but, when asked, described the school method of carrying the one. Its written reasoning is a useful view, not a guaranteed record.

What this means for you: judge the answer by checking the answer, not by how convincing the reasoning sounds. A neat chain of logic leading to a wrong revenue figure is still a wrong revenue figure.

### Now watch and read

- Karpathy, post-training section (75 min). Watch for: where conversation training data comes from, his explanation of hallucinations, and "models need tokens to think".
- 3Blue1Brown, Chapter 6, attention (30 min). The maths can wash over you; watch for the idea of words updating each other.
- Anthropic, "Tracing the thoughts of a large language model" (20 min). Focus on the sections on planning ahead (the rhyming poem) and on the mental maths example.

## Try: E1.3 explain it back (40 minutes)

Write about 300 words, in your own words and without looking anything up, explaining how Claude produces an answer and why that means you should check its facts. Then ask Claude for feedback using the prompt in [E1.3](../../exercises/m01/exercises.md#e13-explain-it-back). This isn't marked. Explaining something is the quickest way to find the bits you don't yet understand.

## Try: E1.4 failure prediction (1 hour)

Fifteen prompts about running a book club, each one designed to probe a weakness from this week or last. For each, predict whether Claude will get it right, then run it and record what happened. Steps and prompts are in [E1.4](../../exercises/m01/exercises.md#e14-failure-prediction).

The goal isn't to catch Claude out. It's to calibrate your gut feeling about when to trust it, which is the most useful skill in this module.

## Build: customer and audience hypotheses (1.5 hours)

A business plan is only as good as its understanding of who pays. This week you write down who you *think* your members and listeners are and why they come, and you mark honestly how sure you are of each point. Template: the "Customer and audience hypotheses" section of [projects/p1-book-club-podcast/README.md](../../projects/p1-book-club-podcast/README.md#customer-and-audience-hypotheses).

**How to do it with Claude:**

1. In your "AI course" project, attach last week's business snapshot.
2. Ask:

   > Using my business snapshot, help me write customer and audience hypotheses for the book club and the podcast. Ask me questions to draw out what I already know from members and listeners. For every hypothesis, record the evidence I gave and label it: "known" (I have data), "heard" (members told me), or "guess". Don't add hypotheses I haven't supported unless you label them "Claude's suggestion, untested".

3. Aim for 8 to 12 hypotheses covering: who comes, why they come, what they'd pay more for, why people stop coming, how they found you, and how podcast listeners relate to members.
4. Pick the three that matter most for profitability and write one sentence each on how you could test them cheaply (a question at the next meeting, a Stripe export, a short poll). You'll run tests in later weeks.

Notice where Claude was agreeable rather than useful. Did it challenge any of your assumptions? If not, try asking: "Which of these hypotheses would you most expect to be wrong, and why?"

## Check-in (30 minutes)

Send me:

1. Your hypotheses table and the three tests.
2. Your E1.4 results table.
3. Your E1.3 explanation and the feedback Claude gave.
4. Anything from the readings you want to talk through, and how long the week took.
