I build AI systems for work where a wrong answer costs something, such as compliance, safety and cloud operations.

My background is solutions architecture, customer-facing engineering and engineering management at startups and enterprise organizations. My most recent role was software engineer and compliance manager on a SOC 2 program.

## The pattern

My current projects use the same four rules:

1. **Ground.** Facts come from a deterministic source that a person has reviewed.
2. **Bound.** Code, not the prompt, sets how much authority the AI has. The AI decides what to do. Code decides whether it may.
3. **Prove.** Every output shows its source, or the system refuses.
4. **Measure.** I evaluate the AI and publish the misses.

## Projects

| Project | Domain | What it shows | Status |
|---|---|---|---|
| [grounded-context](https://github.com/cdevarenne/grounded-context) | Retrieval for agents | Exact facts are looked up, never ranked. Gaps refuse. Elasticsearch, MCP. | Prototype, [write-up](https://medium.com/@claude.devarenne/a-grounded-context-layer-for-agents-and-three-things-hybrid-search-wont-tell-you-e71fdc334773) |
| [okf-grc-skill](https://github.com/cdevarenne/okf-grc-skill) | Compliance evidence | Scanner findings mapped to SOC 2, ISO/IEC 42001 and EU AI Act controls, only through reviewed rules. OSCAL output, CI gate. | Work in progress at v1.8.1 |
| [okf-grc-demo-boutique](https://github.com/cdevarenne/okf-grc-demo-boutique) | Adoption on real code | okf-grc applied to Google's demo app Online Boutique: 422 findings, 47 gaps triaged for $0.04, an AI draft and its review. | Worked example |
| [okf-drone-skill](https://github.com/cdevarenne/okf-drone-skill) | Civil drone missions | Flight plans checked against EASA SORA 2.5. GO, NO-GO or HOLD. A person signs. | Work in progress at v1 |
| [agentic-patterns-catalog](https://github.com/cdevarenne/agentic-patterns-catalog) | Agent design | Picks design patterns for a task, with provenance on every field. MCP server with a policy layer. | Work in progress |
| Cloud patching with Pulumi | Cloud operations | An agent patches workloads within a policy, with preview, rollback and an audit trail. | Next |

okf-grc-skill and okf-drone-skill include a 'How this was built' page with the specs, the human review gates and the failures.

## Writing

- [A Grounded Context Layer for Agents](https://medium.com/@claude.devarenne/a-grounded-context-layer-for-agents-and-three-things-hybrid-search-wont-tell-you-e71fdc334773)
- Ground, Bound, Prove, Measure: a pattern for AI where a wrong answer costs something *(coming soon)*

## Contact

[LinkedIn](https://www.linkedin.com/in/cdevarenne) · Based in the San Francisco Bay Area


<!---
cdevarenne/cdevarenne is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
