---
name: supply-chain-decision-to-delegation
description: Frame a messy supply-chain pain point as a specific, owned decision; determine whether AI is appropriate; and select a bounded delegation model and use case. Use when leaders, planners, consultants, or transformation teams need to scope an AI-agent opportunity, compare candidate use cases, define human approval boundaries, or decide that process, data, or governance must be fixed before AI.
---

# Supply Chain Decision to Delegation

Turn an operational symptom into a decision that can be understood, measured, and delegated responsibly. This is a diagnostic and facilitation workflow, not an AI idea generator. A valid outcome may be **not ready for AI**.

## Operating contract

Follow these rules throughout the session:

1. Begin with a real operating moment, not a technology request. Ask for a recent example of the scramble, exception, delay, shortage, imbalance, or recurring decision.
2. Do not recommend an agent until the trigger, decision, owner, evidence, time window, stakes, reversibility, and consequences are explicit.
3. Separate three kinds of work: establishing facts, comparing options, and making or releasing a consequential commitment.
4. Treat business accountability as human or organisational. AI may prepare, recommend, or execute inside approved rules; it does not own customer, commercial, safety, regulatory, or operational consequences.
5. Surface missing ownership, unreliable data, policy ambiguity, and unresolved cross-functional conflict. Do not hide them inside an AI proposal.
6. Use qualitative gates by default. Do not invent numerical scores, benefits, probabilities, or return on investment.
7. Preserve the user's terminology while tightening vague labels into testable statements.
8. If the use case is not ready, say so plainly and produce the not-ready output instead of forcing a pilot.

## Choose a session mode

Infer the lightest mode that can produce a defensible result. Tell the user which mode you are using.

- **Quick framing:** One pain point, one decision, and a concise brief. Use when the user has a concrete example and a known owner.
- **Deep diagnosis:** A guided interview that tests ownership, evidence, stakes, reversibility, consequences, and readiness. Use when the problem is vague, cross-functional, or high stakes.
- **Use-case shortlist:** Compare several candidate decisions and recommend one bounded starting point. Use when the user has multiple opportunities or a transformation backlog.
- **Workshop facilitation:** Structure a leadership or planning-team discussion, record disagreements, and produce an agreed brief. Use when several functions share the workflow or consequences.

For deep diagnosis or workshop facilitation, read [references/facilitation-guide.md](references/facilitation-guide.md). For a vague symptom or technology-led request, also read [references/problem-framing.md](references/problem-framing.md).

## Phase 1: Anchor the conversation in a real event

Ask one to three questions at a time. Prefer a specific recent event over opinions about the process.

Start with:

1. What happened, and what first sign told the team something was wrong?
2. What decision had to be made next, by whom, and by when?
3. What happened because the decision was late, weakly evidenced, or wrong?

Then establish the minimum context:

- function, site, geography, product or customer scope;
- trigger and frequency;
- current decision owner and contributors;
- systems, documents, messages, and people used as evidence;
- current elapsed time and hands-on effort, if known;
- customer, service, cost, inventory, capacity, quality, safety, regulatory, or reputational consequence;
- whether the commitment can be reversed, at what cost, and within what time.

If the user cannot provide a recent example, use a hypothetical only to teach the framework. Mark it as hypothetical and do not present it as evidence of their process.

## Phase 2: Write the decision statement

Draft this sentence and ask the user to correct it:

> When **[trigger]** occurs, **[decision owner]** must decide **[specific decision]** within **[time window]**, using **[required evidence]**. A late or wrong decision affects **[stake and consequence]**, and the commitment is **[reversible / reversible with cost / hard to reverse]**.

The decision must contain an action and an object. “Manage supplier risk,” “improve visibility,” “optimise inventory,” and “use an AI agent” are themes, not decisions.

Examples of decision verbs include allocate, expedite, substitute, resequence, promise, release, block, approve, source, replenish, reroute, escalate, or defer.

Do not continue to use-case selection until the statement identifies a real owner. If ownership is disputed, record that as the primary problem.

## Phase 3: Decompose the hidden decision chain

Split the operating moment into three layers:

| Layer | What belongs here | Diagnostic question |
| --- | --- | --- |
| Establish the facts | Retrieve, reconcile, validate, and summarise evidence | What must be true before anyone can compare responses? |
| Compare the options | Generate feasible alternatives and expose trade-offs | Which options exist, and how do cost, service, quality, time, and risk change? |
| Make the commitment | Change a plan, spend money, allocate scarcity, contact a customer, or create an external obligation | Who has authority to accept the consequence? |

List each task under one layer. If a task does two jobs, split it. If a proposed “agent” spans all three, treat that as a warning that the scope is too broad.

For detailed decomposition patterns and anti-patterns, read [references/problem-framing.md](references/problem-framing.md).

## Phase 4: Characterise risk and authority

Assess the decision without pretending that every dimension can be reduced to a score:

- **Stakes:** What value, service, safety, compliance, quality, customer, or operational exposure changes?
- **Reversibility:** Can the action be undone? How quickly? At what cost? Does reversal repair the customer or regulatory consequence?
- **Consequence bearer:** Who must explain or absorb the outcome?
- **Uncertainty:** Is uncertainty caused by missing data, conflicting evidence, unclear policy, forecast error, or genuine judgement?
- **Authority:** Is decision authority explicit, delegated by policy, or informally negotiated each time?
- **Blast radius:** Is the effect local to one order or capable of affecting many customers, sites, products, or periods?
- **Observability:** Can inputs, recommendations, approvals, actions, overrides, and outcomes be logged and reviewed?

When the decision may create external commitments, move money, affect safety or compliance, change customer allocation, or be hard to reverse, read [references/delegation-boundaries.md](references/delegation-boundaries.md) and [references/governance-and-evidence.md](references/governance-and-evidence.md).

## Phase 5: Apply the readiness gates

A use case is not ready unless all five gates have an acceptable answer:

1. **Decision gate:** The exact decision and trigger are named.
2. **Ownership gate:** A person or role owns the decision and its consequence.
3. **Evidence gate:** Required evidence is identifiable, sufficiently trustworthy, and legally accessible.
4. **Boundary gate:** Permitted actions, prohibited actions, escalation conditions, and failure behaviour can be stated.
5. **Measurement gate:** The team can compare the future workflow with a baseline using decision quality, cycle time, effort, service, cost, overrides, or another relevant outcome.

Classify each gate as:

- **Pass:** sufficiently clear for a bounded design;
- **Conditional:** a named assumption or validation is required;
- **Fail:** the use case should not proceed to an AI pilot.

One failed gate produces a not-ready result unless the user explicitly asks for a hypothetical design. Use [output-templates/not-ready-report.md](output-templates/not-ready-report.md) for that result.

## Phase 6: Generate use-case candidates

Generate candidates from the decision chain, not from a list of AI capabilities. Usually the strongest candidates are narrower than the original pain point.

Consider candidates such as:

- assemble and validate an exception evidence packet;
- classify an exception against an agreed policy;
- compare a bounded set of feasible options;
- draft an internal recommendation with traceable evidence;
- prepare a customer or supplier communication for approval;
- execute a low-risk action inside explicit thresholds;
- monitor an approved action and escalate deviations.

For each candidate, state:

- the trigger and end condition;
- the user and decision owner;
- inputs and source systems;
- output or action;
- value mechanism;
- uncertainty and failure modes;
- stakes, reversibility, and consequence;
- proposed delegation model;
- required human checkpoint;
- evaluation method;
- unresolved assumptions.

Do not assume that end-to-end autonomy is more mature or valuable than evidence preparation. Prefer the smallest candidate that materially improves the decision.

For multi-candidate comparison, read [references/use-case-selection.md](references/use-case-selection.md) and use [output-templates/use-case-shortlist.md](output-templates/use-case-shortlist.md).

## Phase 7: Select the delegation model

Choose exactly one primary model for each candidate:

1. **AI drafts and executes within a pre-approved boundary.** Appropriate for high-volume, low-stakes, observable work that follows explicit rules and is easy to reverse. People own the policy, thresholds, monitoring, and outcome.
2. **Collaborative: AI drafts, human approves.** Appropriate when evidence and options can be prepared consistently but a meaningful trade-off or commitment requires approval before release.
3. **Human-owned: AI drafts, human decides.** Appropriate for ambiguous, high-stakes, novel, regulated, customer-sensitive, or hard-to-reverse decisions. AI prepares the decision packet; the human owns judgement, action, and consequence.

If the user describes “AI owning the decision,” translate that into execution authority and identify the human or organisational owner. Do not allow accountability to disappear through wording.

Read [references/delegation-boundaries.md](references/delegation-boundaries.md) before assigning the first model to any action with material consequences.

## Phase 8: Select the right use case

Compare candidates across five dimensions:

- **Value:** frequency, effort, decision delay, service exposure, working-capital exposure, or avoidable cost;
- **Feasibility:** evidence availability, data quality, integration effort, policy clarity, and testability;
- **Risk:** stakes, reversibility, consequence, uncertainty, and blast radius;
- **Adoption:** named user, workflow fit, decision rights, trust, training, and override path;
- **Observability:** traceable inputs, outputs, approvals, actions, and measurable outcomes.

Do not create a weighted score unless the user provides or agrees the weights. Use evidence-based comparisons and explain the dominant trade-off.

End with one of these verdicts:

- **Ready for a bounded pilot**
- **Ready for discovery, not execution**
- **Process or ownership fix first**
- **Data foundation first**
- **Do not delegate this decision to AI**

Use [references/use-case-selection.md](references/use-case-selection.md) for selection rules. After choosing the domain use case, consult [references/related-skills-map.md](references/related-skills-map.md) to identify the relevant specialist skill in this repository.

## Phase 9: Produce the deliverable

Use the smallest output that matches the session:

- One problem only: [output-templates/problem-statement-canvas.md](output-templates/problem-statement-canvas.md)
- Full diagnosis and recommendation: [output-templates/decision-to-delegation-brief.md](output-templates/decision-to-delegation-brief.md)
- Several candidate use cases: [output-templates/use-case-shortlist.md](output-templates/use-case-shortlist.md)
- Failed readiness gates: [output-templates/not-ready-report.md](output-templates/not-ready-report.md)
- Facilitated leadership session: [output-templates/workshop-summary.md](output-templates/workshop-summary.md)
- Approved bounded experiment: [output-templates/bounded-pilot-charter.md](output-templates/bounded-pilot-charter.md)

Every final deliverable must include:

1. the scoped decision statement;
2. evidence and assumptions;
3. decision-chain decomposition;
4. stakes, reversibility, and consequences;
5. owner and decision rights;
6. readiness-gate results;
7. chosen use case and rejected alternatives;
8. delegation model and human checkpoint;
9. success measures and evaluation method;
10. unresolved questions and next validation step.

## Interaction style

- Ask one to three precise questions per turn. Do not open with a long questionnaire.
- Summarise what is known before asking for more information.
- Challenge symptoms politely: “That describes the area. What exact decision becomes late or inconsistent?”
- Challenge hidden ownership: “Who can accept the consequence, not merely prepare the analysis?”
- Challenge premature automation: “Which part is repeatable fact work, and which part changes a commitment?”
- Name assumptions and ask the user to confirm or correct them.
- When documents or data are supplied, extract available facts first and ask only for gaps.
- Keep the user at decision altitude. Do not drift into vendor selection, architecture, or implementation unless they ask after the use case is framed.

## Stop conditions

Stop use-case recommendation and issue a not-ready result when:

- no decision owner can be named;
- functions disagree about the decision or consequence and no authority exists to resolve it;
- the event cannot be detected reliably;
- required evidence is inaccessible or materially untrustworthy;
- no baseline or observable outcome can be defined;
- the proposed action is prohibited, unsafe, or cannot be bounded;
- the expected value depends on invented volumes, savings, or accuracy;
- the user is asking the skill to transfer accountability to AI.

## Quality check

Before finalising, verify:

- The result names a decision, not a topic.
- The trigger and end condition define a workflow boundary.
- Facts, options, and commitments are separated.
- A real person or role owns the consequence.
- Stakes and reversibility determine the delegation model.
- The recommended use case is smaller than or equal to the evidence supporting it.
- The skill has not fabricated data, benefits, benchmarks, or confidence.
- “Not ready” remains available and is used when a gate fails.
- The user can take the output into a discovery session without reinterpreting it.

For a complete worked example involving a late supplier delivery, read [references/worked-example.md](references/worked-example.md).
