# Governance and evidence basis

Use this reference when the proposed use case involves consequential actions, agentic execution, human approval, or claims about current AI-agent practice.

## Evidence limits

Do not claim that autonomous supply-chain agents are already widespread in production unless the user supplies reliable evidence. Current public discussion is stronger on governance principles than on independently verified, scaled supply-chain deployments.

Use the sources below to support design principles, not adoption statistics or guaranteed outcomes.

## Design principles supported by the sources

### Make decision authority explicit

An operational agent needs a defined objective, permitted actions, decision authority, and escalation path. Treat those elements as part of the operating model rather than implementation detail.

Source: [Supply Chain Management Review, “How agentic AI changes supply chain operations”](https://www.scmr.com/article/how-agentic-ai-changes-supply-chain-operations/automation)

### Default to constrained access for consequential actions

Start with read-only access or scoped tools, especially when an action is difficult to reverse. Observe how delegated authority is used rather than assuming correct behaviour from a model response.

Source: [IDC, “Agentic AI is critical infrastructure”](https://www.idc.com/resource-center/blog/agentic-ai-is-critical-infrastructure/)

### Use agents for volume and preparation before transferring judgement

Exception-management agents can assemble information, perform repeatable pre-work, and maintain an audit trail. Consequential actions still need guardrails and human confirmation where appropriate.

Source: [Arman Seraji, “AI agents for supply chain exceptions”](https://armanseraji.ai/blog/ai-agents-supply-chain-exceptions)

### Treat trust and isolation as active engineering concerns

Recent general agent discussion has focused heavily on sandboxing, restricted authority, testing, verification, and the risk of excessive permissions. These are not supply-chain deployment statistics, but they reinforce the need for bounded tools and observable execution.

Context sources:

- [Docker Sandboxes](https://www.docker.com/products/docker-sandboxes/)
- [Terminal-Bench-Science](https://www.terminal-bench-science.ai/announcement)
- [AI Agent Has Root](https://infernalcode.com/posts/your-ai-agent-has-root/)

## How to cite evidence in an output

Use restrained language:

- “Recent guidance converges on explicit authority and escalation.”
- “A bounded, observable starting point is better supported than end-to-end autonomy.”
- “This is a design recommendation, not proof of widespread adoption.”

Avoid:

- “Everyone is moving to autonomous supply chains.”
- “Agents are proven to reduce exception cost by X percent” without a direct source and comparable context.
- “Human approval eliminates risk.”
- “Read-only access is safe by definition.”

## Evidence required from the organisation

Public sources cannot replace local evidence. Before recommending a use case, request or identify:

- event frequency;
- current trigger-to-decision time;
- hands-on effort and waiting time;
- examples of wrong, late, or overridden decisions;
- authoritative data sources and known quality issues;
- decision-rights policy;
- thresholds and prohibited actions;
- customer, cost, service, quality, safety, or compliance consequences;
- representative historical cases;
- baseline outcome measures.

Mark every unsupported local claim as an assumption or validation need.

## Governance minimum

A consequential workflow needs:

1. a named business owner;
2. approved scope and authority;
3. data-access approval;
4. source provenance;
5. permitted and prohibited actions;
6. escalation and safe failure;
7. approval and override mechanism;
8. logging and review;
9. evaluation and stop criteria;
10. change control for policy, model, prompt, tool, and scope updates.

The skill should expose missing governance as an output, not silently solve around it.
