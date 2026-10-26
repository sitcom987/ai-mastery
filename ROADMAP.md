# Roadmap

Status: **proposed**, 2026-10-26. Awaiting Adam's approval (decisions D1–D7) and answers to Q1–Q6. Full rationale, research findings and the Module 1 outline: https://claude.ai/artifact/RFSuzp3Ppme4hQEXHp8Quz

## Shape

Four phases, three cumulative assessment gates.

| Phase | Weeks | Modules | Gate |
| --- | --- | --- | --- |
| Understand | 1–6 | M1 How AI works; M2 Prompt and context engineering | Module assessments |
| Apply to plans | 7–12 | M3 Research and knowledge work; M4 Opportunity and business design | Review 1 (week 12): plans v1 delivered |
| Build | 13–22 | M5 Coding foundations with Claude Code; M6 Workflow automation; M7 Agents and MCP | Review 2 (week 22): agent passes its evals |
| Capstone | 23–26 | M8 AI-assisted software engineering (sampler prototype) | Final (week 26): prototype demo |

Weeks 1–12 need no programming. From week 13 prerequisites are strict: coding and security before automation, automation before agents.

## Revisions after Adam's answers (2026-10-26)

- **No API spend (D8):** programmatic Claude calls use Claude Code's non-interactive mode within the Pro allowance (Pro usage is shared between Claude and Claude Code); HTTP practice uses free APIs including Stripe test mode; the agent loop runs on a free local model via Ollama.
- **Environment:** macOS 26.5.1 on a 2022 M2 MacBook Pro; everything runs locally.
- **Priorities:** book club profitability first, album second. With no release date set, the jazz plan becomes a release framework you can date later.
- **P3 automation candidates:** Stripe payment, then attendee list, then a confirmation email drafted for approval, then a calendar entry; reminders; feedback form.
- **P4 sampler:** foley instrument with several banks and XY-pad blending; targets VST3 and AU on macOS first (Cubase and Ableton), with Windows and Linux later. Week 25 target is one playable bank; XY blending is stretch.
- **P5 toothpaste:** design-led statement brand in a striking pump dispenser; discovery tests this concept.

- **Book club plan from week 1 (D1 approved with this change):** every week's independent slot builds part of the P1 plan; one-page v0.5 in week 6, full v1 in week 9. Light, just-in-time business concepts first; Module 4 covers them properly.

## Week by week

Hours are core hours split as Concept / Guided / Independent / Review. Stretch tasks are optional (up to ~3 h).

| Wk | Module | Focus | Project | Hours C/G/I/R | Stretch |
| --- | --- | --- | --- | --- | --- |
| 1 | M1 How AI works | Setup decisions, baseline assessment, tokens and next-token prediction, start of learning system. P1: business snapshot and profitability goal | P1, P6 | 2 / 2 / 1.5 / 1.5 | Tokenizer experiments |
| 2 | M1 | Training pipeline, embeddings, attention, context windows. P1: customer and audience hypotheses | P1 | 2.5 / 2 / 2 / 1 | Attention paper walkthrough |
| 3 | M1 | Hallucination and verification lab, lab vs real-world reliability, privacy and IP. P1: verified scan of comparable book clubs and podcasts. **Assessment** | P1 | 1.5 / 1.5 / 3 / 1.5 | Compare Claude with another model |
| 4 | M2 Prompt and context engineering | Specification, decomposition, structure, examples, output schemas. P1: unit economics model v0 | P1 | 2 / 2.5 / 2 / 1 | XML vs JSON schema comparison |
| 5 | M2 | Test sets, rubrics, model-as-grader, regression; separating instructions from untrusted content. P1: tested survey and feedback-analysis prompts | P1 | 2 / 2 / 2.5 / 1 | Prompt-injection red-team |
| 6 | M2 | Context for long projects, prompt library v1. P1: pricing and income-stream options, one-page plan v0.5. **Assessment** | P1, P2 | 1.5 / 1.5 / 3 / 1.5 | Port a prompt to another vendor |
| 7 | M3 Research and knowledge work | Deep research with traceable sources, source hierarchy, comparing claims | P1 | 1.5 / 2 / 3 / 1 | Source-register template |
| 8 | M3 | Long documents, structured extraction, qualitative analysis | P1, P2 | 1.5 / 2 / 3 / 1 | Survey design |
| 9 | M3 | Evidence vs inference vs assumption, decision memos. **Book club and podcast plan v1. Assessment** | P1 | 1 / 1.5 / 4 / 1.5 | Measurement dashboard spec |
| 10 | M4 Opportunity and business design | Problem discovery, jobs to be done, segments, value propositions, customer-research design | P2, P5 | 2 / 2 / 2.5 / 1 | Interview guide |
| 11 | M4 | Business models, unit economics, competitive maps, validation experiments. **Jazz release plan v1, toothpaste opportunity brief. Assessment** | P2, P5 | 1.5 / 1.5 / 4 / 1 | Supplier long-list |
| 12 | Review 1 | Cumulative assessment 1, **personal-development system v1**, roadmap adjustment | P6 | 0.5 / 1 / 4 / 2 | Toothpaste competitor teardown |
| 13 | M5 Coding foundations | Terminal, git and GitHub, Claude Code install, explore-plan-implement loop | All | 2 / 3 / 1.5 / 1 | Git branching drills |
| 14 | M5 | Python essentials with tests; reading code; CLAUDE.md | P3 | 2 / 2.5 / 2 / 1 | Tests first for one script |
| 15 | M5 | HTTP, JSON, APIs, secrets (Stripe test mode), programmatic Claude calls via `claude -p`, structured outputs, usage budgeting, LLM security. **Episode-notes extractor. Assessment** | P3 | 2 / 2 / 2.5 / 1 | Batch processing and caching |
| 16 | M6 Workflow automation | Workflow mapping, scoring candidates, platform comparison with fresh pricing | P3 | 2 / 1.5 / 3 / 1 | Value estimate for top 5 |
| 17 | M6 | Automation 1 in n8n: triggers, transforms, errors, retries, logs, human approval | P3 | 1 / 2 / 3.5 / 1 | Same flow in Python |
| 18 | M6 | Automation 2 with approval step; idempotency, monitoring, docs. **Assessment** | P3 | 1 / 1.5 / 4 / 1 | Release-calendar automation |
| 19 | M7 Agents and MCP | Workflows vs agents; tool-calling loop on a local model (Ollama); permissions and stop conditions | P3 | 2 / 2.5 / 2 / 1 | Compare one agent framework |
| 20 | M7 | MCP server over the research library; embeddings, retrieval, RAG | P1, P6 | 2 / 2 / 2.5 / 1 | Vector vs keyword search |
| 21 | M7 | Bounded agent with eval suite, tracing, cost caps, injection tests, oversight. **Assessment** | P2, P3 | 1 / 1 / 4.5 / 1 | Second agent design review |
| 22 | Review 2 | Cumulative assessment 2; Claude Code skills, hooks, subagents; sampler spec interview; C++ warm-up | P4 | 1 / 1.5 / 3 / 2 | Toothpaste plan v2 |
| 23 | M8 AI-assisted software engineering | Sampler spec and architecture, C++ essentials, JUCE and CMake, empty plugin builds | P4 | 2 / 2.5 / 2.5 / 0.5 | Read JUCE examples with Claude |
| 24 | M8 | Audio fundamentals, real-time thread rules; load a sample, play from MIDI | P4 | 2 / 2 / 3 / 0.5 | Unit tests for sample loading |
| 25 | M8 | One foley bank playable as an instrument: gain and envelope, basic UI, tests, validation in Ableton and Cubase (VST3 and AU), reviewing AI-written C++ | P4 | 1 / 2 / 4 / 0.5 | Two-bank XY blend |
| 26 | Final review | Capstone demo, final assessment, extension plan | All | 0.5 / 0.5 / 3 / 3.5 | |

Projects: P1 book club and podcast plan · P2 jazz album release · P3 book club and podcast automations · P4 sampler plugin · P5 toothpaste business plan · P6 personal-development system.

## Feasibility flags

1. **Sampler plugin:** prototype by week 25 at best; a sellable product needs 8–12 extension weeks and likely specialist review.
2. **Toothpaste plan:** an evidence-backed desk draft by week 22; real validation needs calendar time and outside experts.
3. **Advanced level:** realistic for evaluation, research and prompting; *Independent* is the realistic target elsewhere.
4. **Jazz release date:** if it is within four months, the jazz plan moves ahead of the book club plan.

## Open decisions (D1–D7)

| # | Decision | Recommendation |
| --- | --- | --- |
| D1 | Sequence and week table | **Approved 2026-10-26**, with the book club plan starting in week 1 |
| D2 | End targets | Sampler prototype plus extension; toothpaste plan as draft |
| D3 | Main language | **Decided 2026-10-26: Python** |
| D4 | Automation platform | n8n self-hosted, compared with Make, Zapier, plain code |
| D5 | File home | **Done: this GitHub repository** |
| D6 | Time policy | 5–6 core hours plus optional stretch |
| D7 | Feedback rhythm | Weekly check-in |
| D8 | Spending | Stay within Claude Pro: no API credits or extra usage; free local tools fill the gaps |
