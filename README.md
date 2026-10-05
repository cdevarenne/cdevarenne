I build AI systems for work where a wrong answer costs something, such as compliance, safety and cloud operations.

My background is solutions architecture, customer-facing engineering and engineering management at startups and enterprise organizations. My most recent role was software engineer and compliance manager on a SOC 2 program.

## The pattern

My current projects use the same four rules:

1. **Ground.** Facts come from a deterministic source that a person has reviewed.
2. **Bound.** Code, not the prompt, sets how much authority the AI has. The AI decides what to do. Code decides whether it may.
3. **Prove.** Every output shows its source, or the system refuses.
4. **Measure.** I evaluate the AI and publish the misses.

## Projects

| Project | Domain | What it shows | Where the AI is, and what checks it | Status |
|---|---|---|---|---|
| [grounded-context](https://github.com/cdevarenne/grounded-context) · [JVM port](https://github.com/cdevarenne/grounded-context-jvm) | Retrieval for agents | Exact facts are looked up, never ranked. Gaps refuse. Elasticsearch, MCP. | Semantic search only for exploration; below a measured relevance floor it refuses. A 20-question eval checks the answer and the route. | Complete, [write-up](https://medium.com/@claude.devarenne/a-grounded-context-layer-for-agents-and-three-things-hybrid-search-wont-tell-you-e71fdc334773) |
| [grc-evidence](https://github.com/cdevarenne/grc-evidence) | Compliance evidence | Scanner findings mapped to SOC 2, ISO/IEC 42001 and EU AI Act controls, only through reviewed rules. OSCAL output, CI gate. Code decides status. An LLM drafts prose. A person reviews. | An LLM drafts report text and proposes controls for unmapped findings. Held-out eval, cost log. The scan has no LLM. | Released v1.8; Type 2 evidence over an audit window in progress (v2.0.0) |
| [grc-evidence-boutique](https://github.com/cdevarenne/grc-evidence-boutique) | Adoption on real code | grc-evidence applied to Google's Online Boutique: 422 findings mapped to controls, a compliance gate on every PR, a nightly scan, and an agent's draft with the review that corrected it. | Claude Haiku proposed a control for each gap rule ($0.04). A person decided all 47: 42 mapped, 5 left as gaps. | Worked example |
| [drone-mission-plan](https://github.com/cdevarenne/drone-mission-plan) | Civil drone missions | Flight plans checked against EASA SORA 2.5. GO, NO-GO or HOLD. Flown in PX4 simulation. | Optional LLM steps with their own eval. The plan, the checks and the risk score have no LLM. A person signs. | Released v1.0 |
| [agentic-patterns-catalog](https://github.com/cdevarenne/agentic-patterns-catalog) | Agent design | 288 agentic design patterns served to agents over MCP, behind a policy layer, with provenance on every field. | LLM-drafted enrichment stays marked unreviewed until a person reviews it. Golden-set eval. | Active: enrichment in progress |
| Cloud DevSecOps *(name TBD)* | Cloud operations | An agent proposes patches within a policy, with preview, rollback and an audit trail. | The agent proposes. Policy code decides. A person approves. | Planned |

grc-evidence and drone-mission-plan include a 'How this was built' page with the specs, the human review gates and the failures.

## Writing

- [A Grounded Context Layer for Agents](https://medium.com/@claude.devarenne/a-grounded-context-layer-for-agents-and-three-things-hybrid-search-wont-tell-you-e71fdc334773)
- Ground, Bound, Prove, Measure: a pattern for AI where a wrong answer costs something *(coming soon)*

## Contact

[LinkedIn](https://www.linkedin.com/in/cdevarenne) · Based in the San Francisco Bay Area
