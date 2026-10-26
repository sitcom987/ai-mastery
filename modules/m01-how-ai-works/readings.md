# Module 1 readings and videos

All links opened and checked on 2026-10-26. IDs refer to [SOURCE_REGISTER.md](../../SOURCE_REGISTER.md).

| Week | Source | What to take from it | Time | ID |
| --- | --- | --- | --- | --- |
| 1 | 3Blue1Brown, [Transformers, the tech behind LLMs (Deep Learning Chapter 5)](https://www.3blue1brown.com/lessons/gpt), 2024 | The big picture: text in, probabilities out, one token at a time | 30 min | S15 |
| 1 | Andrej Karpathy, [Deep Dive into LLMs like ChatGPT](https://www.youtube.com/watch?v=7xTGNNLPyMI), Feb 2025, 3 h 31 min. **Week 1: the first hour**, up to where he moves from pretraining to post-training | Where training data comes from, tokens, what a "base model" is | 60 min | S16 |
| 2 | Karpathy, same video, **the post-training section** (fine-tuning on conversations, hallucinations, tool use, reinforcement learning) | How the assistant persona is made, and why it still hallucinates | 75 min | S16 |
| 2 | 3Blue1Brown, [Attention in transformers, step-by-step (Chapter 6)](https://www.3blue1brown.com/lessons/attention), Apr 2024 | How words "look at" each other to build meaning in context | 30 min | S17 |
| 2 | Anthropic, [Tracing the thoughts of a large language model](https://www.anthropic.com/news/tracing-thoughts-language-model), Mar 2025 | Claude plans ahead; its explanations of its own reasoning can differ from what it actually did | 20 min | S18 |
| 3 | OpenAI (Kalai, Nachum, Vempala, Zhang), [Why language models hallucinate](https://arxiv.org/html/2509.04664v1), Sep 2025. Read the abstract and introduction only | Hallucination starts in pretraining and is rewarded by tests that punish "I don't know" | 25 min | S19 |
| 3 | Anthropic, [Effective context engineering for AI agents](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents), Sep 2025. Read up to "The anatomy of effective context" | Why long conversations degrade ("context rot") | 15 min | S01 |
| 3 | METR, [2025 developer study](https://metr.org/blog/2025-07-10-early-2025-ai-experienced-os-dev-study/) and [2026 update](https://metr.org/blog/2026-02-24-uplift-update/) | Perceived and measured AI benefit can differ a lot | 15 min | S08, S09 |
| 3 | Anthropic, [Updates to consumer terms and privacy policy](https://www.anthropic.com/news/updates-to-our-consumer-terms), Aug 2025 | What happens to your chats, and the setting that controls it | 10 min | S20 |

Optional, for curiosity only: 3Blue1Brown [How might LLMs store facts (Chapter 7)](https://www.3blue1brown.com/lessons/mlp).

## Notes on the sources

- The two video series overlap on purpose: 3Blue1Brown is visual and short, and Karpathy is detailed and practical. If one doesn't click, the other usually does.
- Karpathy's video is from February 2025. The principles are stable, but the specific models he mentions are older than the ones you'll use.
- The hallucination paper is by OpenAI researchers. It explains a mechanism that applies to all LLMs, Claude included.
- Anthropic's interpretability findings come from an older, smaller Claude model. They show what *can* happen inside models, not a full account of how today's Claude works.
