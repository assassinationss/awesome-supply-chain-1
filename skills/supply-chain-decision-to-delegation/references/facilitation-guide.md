# Facilitation guide

Use this reference when the skill must interview a leader, facilitate a cross-functional session, or reconcile conflicting descriptions of the same decision.

## Facilitation principles

- Ask for one recent event before asking for opinions about the whole process.
- Ask one to three questions at a time.
- Reflect the current understanding in plain language and invite correction.
- Distinguish disagreement about facts from disagreement about policy, priorities, or authority.
- Keep a visible list of assumptions, open questions, and decisions made during the session.
- Do not reward confident but unsupported claims with false precision.
- Allow “not ready” to be a useful result.

## Quick framing session: 15 minutes

Use when one leader or planner has a concrete example.

### Minute 0–3: The event

Ask:

1. Describe the last time this problem happened.
2. What first signal started the scramble?
3. What decision was still missing?

### Minute 3–7: Ownership and evidence

Ask:

1. Who prepared the analysis?
2. Who could actually approve or commit the response?
3. Which facts took the longest to find or reconcile?

### Minute 7–11: Stakes and reversibility

Ask:

1. What happened while the decision waited?
2. What would a wrong decision change?
3. Could the action be reversed without leaving a customer, cost, quality, or compliance consequence?

### Minute 11–15: Candidate and verdict

Draft the decision statement, decompose facts/options/commitment, test the five readiness gates, and state one verdict. Do not promise a pilot if evidence is missing.

## Deep diagnosis session: 45–60 minutes

Use when the problem crosses functions, the owner is unclear, or the decision is consequential.

### 1. Establish the operating moment

Capture:

- trigger;
- scope;
- sequence of handoffs;
- decision deadline;
- current workaround;
- consequence of delay.

Ask each participant to describe what they saw and did during the same event. Differences often expose the real data or ownership problem.

### 2. Build the decision chain

Create three columns: establish facts, compare options, make commitment.

Place each current task in one column. Split tasks that cross columns. Mark waiting time, repeated work, missing evidence, and informal approvals.

### 3. Map decision rights

For each commitment, record:

- recommender;
- approver;
- executor;
- accountable owner;
- consulted functions;
- escalation path;
- policy or threshold that grants authority.

Do not accept “the team decides” without naming a final authority.

### 4. Test stakes and reversibility

Ask participants to describe a plausible wrong outcome, not only the expected one.

Probe:

- customer promise changes;
- financial exposure;
- safety, quality, and compliance;
- contractual effects;
- inventory or capacity displacement;
- downstream decisions affected;
- time and cost to reverse;
- whether reversal repairs trust or service.

### 5. Generate and compare candidates

Generate candidates at different layers. Include at least one evidence-preparation candidate before considering execution.

For each candidate, test value, feasibility, risk, adoption, and observability. Record the reason for rejecting broader candidates.

### 6. Close with a decision

The session must end with one of:

- a bounded candidate for further validation;
- a discovery-only candidate;
- an ownership or process action;
- a data-foundation action;
- an explicit decision not to delegate.

## Multi-use-case workshop: 75–90 minutes

Use when a leadership team has an opportunity backlog.

### Before the session

Request one example for each candidate. Ask participants to bring current volume, cycle-time, consequence, source-system, and ownership information where available.

### Workshop sequence

1. **Set the rule:** the workshop selects decisions, not technologies.
2. **State each operating moment:** one minute per candidate.
3. **Reject themes:** convert “forecasting,” “visibility,” or “supplier risk” into a trigger and decision.
4. **Run the five gates:** record pass, conditional, or fail.
5. **Map delegation:** bounded execution, human approval, or human-owned decision.
6. **Compare candidates:** value, feasibility, risk, adoption, observability.
7. **Select one next action:** pilot, discovery, process fix, data fix, or no-go.
8. **Name the owner and validation date.**

Use `output-templates/workshop-summary.md` to document the result.

## Question bank

### Event and scope

- What happened on the last occasion?
- Which site, product, customer, lane, supplier, or period was affected?
- What is inside and outside this decision?
- How often does this event occur, based on observed data rather than memory?

### Trigger

- What exact signal starts the work?
- Is the signal a confirmed event, an estimate, or an inference?
- Can it be detected consistently?
- How much time remains after the trigger before the decision loses value?

### Decision

- What verb describes the decision?
- What object or commitment changes?
- Which decision is being delayed by evidence collection?
- Which part is analysis and which part is authority?

### Ownership

- Who is paged or alerted?
- Who does the analysis?
- Who can accept the cost or service consequence?
- Who explains the outcome to the customer, regulator, or executive?
- What happens if the owner is unavailable?

### Evidence

- Which facts are needed before options can be compared?
- Where does each fact live?
- Which source is authoritative?
- What is often missing, stale, or inconsistent?
- How are estimates distinguished from confirmations?
- Can a recommendation cite its evidence?

### Options

- Which responses are genuinely feasible?
- Which constraints eliminate an option?
- Which trade-offs matter to the owner?
- Does policy already rank or prohibit options?
- Where is judgement required because the policy is incomplete?

### Stakes and reversibility

- What is the smallest plausible consequence?
- What is the largest credible consequence?
- What changes outside the local team?
- Can the action be undone before it affects a customer or operation?
- Does reversal recover cost, service, or trust?

### Measurement

- How long does the decision take today?
- How much of that time is analysis, waiting, and rework?
- How often is the recommendation overridden?
- Which outcome shows that the decision improved?
- What would demonstrate that the proposed workflow is unsafe or unhelpful?

## Useful pushback

Use calm, evidence-seeking language:

- “That describes the area. What exact decision becomes late or inconsistent?”
- “Who owns the consequence, not merely the alert?”
- “Is that a source-of-truth fact, an estimate, or a judgement?”
- “If we removed AI from the sentence, what business decision would remain?”
- “What does this candidate improve that a simpler workflow rule would not?”
- “Which action is hard to reverse?”
- “What evidence supports the expected volume or value?”
- “A failed ownership gate means the next step is governance, not automation. Is that acceptable?”

## Handling disagreement

Classify disagreement before resolving it:

| Disagreement type | Response |
| --- | --- |
| Facts differ | Identify source authority, freshness, and reconciliation rule. |
| Policy differs | Name the policy owner and record the unresolved rule. |
| Priorities differ | Escalate to the role authorised to accept the trade-off. |
| Ownership differs | Fail the ownership gate until a final authority is named. |
| Benefit differs | Request baseline evidence and avoid a numerical claim. |
| Risk tolerance differs | Record thresholds and prohibited actions explicitly. |

Do not average contradictory positions into a vague compromise.

## End-of-session readback

Read back:

1. the trigger and scoped decision;
2. the owner and decision deadline;
3. evidence required and gaps;
4. stakes, reversibility, and consequences;
5. candidate use case and delegation model;
6. readiness verdict;
7. assumptions and next validation action.

Ask: “What have I stated that your team would challenge?” Incorporate the answer before finalising.
