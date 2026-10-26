# Glossary

Plain-English definitions of terms used in the course. Grows with each module. The module where a term first appears is in brackets.

| Term | Meaning |
| --- | --- |
| Agent (M7) | An AI system that takes a series of actions with tools, deciding the next step itself, rather than answering once. |
| Attention (M1) | The step inside a model where each token updates its meaning using the other tokens in the context. |
| Base model (M1) | A model after pretraining only. It continues text rather than acting as an assistant. |
| Benchmark (M1) | A standard set of test questions used to compare models. Scores show performance on that test, not on your work. |
| Citation (M1) | A link or reference Claude gives for a claim. It still needs opening: it may not say what Claude says it does. |
| Context engineering (M1, M2) | Deciding what information goes into the context window, and how, so the model has what it needs and little else. |
| Context rot (M1) | The decline in how well a model uses information as the context gets longer. |
| Context window (M1) | Everything the model can see at once: instructions, files, the conversation and its own replies. It has no other memory. |
| Embedding (M1) | The long list of numbers that represents a token's meaning inside the model. Similar meanings have similar lists. |
| Fine-tuning (M1) | Further training of a pretrained model on a smaller, chosen set of examples, such as helpful conversations. |
| Hallucination (M1) | A confident statement from a model that is false or made up. |
| Interpretability (M1) | Research into what is actually happening inside a model when it produces an answer. |
| Knowledge cutoff (M1) | The date the training data ends. The model doesn't know later events unless it's given them or can search. |
| Large language model, LLM (M1) | A model trained on huge amounts of text to predict the next token, used to generate text. |
| Layer (M1) | One of the many repeated processing stages a token's numbers pass through inside the model. |
| MCP, Model Context Protocol (M7) | An open standard for connecting AI applications to tools and data sources. |
| Parameters (M1) | The billions of numbers inside a model that are adjusted during training. They hold what the model has learned. |
| Personal data (M1) | Information about an identifiable person, such as a member's name or email. Protected by UK GDPR. |
| Post-training (M1) | The training after pretraining that turns a base model into a helpful assistant: fine-tuning and reinforcement learning. |
| Pretraining (M1) | The first, largest training stage: learning to predict the next token across a vast amount of text. |
| Primary source (M1) | The original source of a fact: the organisation's own site, the study itself, the official document. |
| Project (Claude) (M1) | A workspace in claude.ai that keeps files and instructions together across chats. |
| Prompt (M1) | The text you give a model, including any instructions and material. |
| Reasoning, extended thinking (M1) | A model writing out its working before answering. Improves multi-step tasks, but the written reasoning may not reflect exactly how the answer was reached. |
| Reinforcement learning (M1) | Training by scoring the model's outputs and nudging it towards higher-scoring behaviour. |
| Retrieval practice (M1) | Studying by trying to recall something before looking at the answer, as with flashcards. |
| Sampling (M1) | Choosing the next token from the model's probability list, with some randomness. |
| Sycophancy (M1) | A model's tendency to agree with the user or the premise of a question rather than give an independent view. |
| Temperature (M1) | A setting that controls how random sampling is. Not adjustable in claude.ai. |
| Token (M1) | A chunk of text (a word, part of a word, a space or punctuation) that the model reads and writes. |
| Tokenizer (M1) | The tool that splits text into tokens. Each model family has its own. |
| Transformer (M1) | The model design behind modern LLMs, built around attention. |
| Verification (M1) | Checking AI output against primary sources before relying on it. |
| Web search (Claude) (M1) | A tool that lets Claude look up current pages and cite them. Reduces, but doesn't remove, made-up facts. |
