# Delegation boundaries

Use this reference after the decision is framed and before recommending that AI execute an action.

## The principle

Delegate work according to the shape of the decision, not the apparent capability of the model. Authority should narrow as stakes, uncertainty, blast radius, and irreversibility increase.

AI may hold execution authority inside a policy. A person or organisation still owns the policy and the consequence.

## Model 1: AI drafts and executes within a pre-approved boundary

Use only when all of the following are true:

- the trigger is reliably detectable;
- the action follows explicit and current policy;
- required evidence is trustworthy and available;
- stakes and blast radius are bounded;
- the action is easy to reverse within the relevant time window;
- prohibited conditions and escalation thresholds can be encoded;
- every action is logged and observable;
- safe failure means stop, hold, or escalate rather than improvise;
- an accountable owner reviews performance and exceptions.

Examples may include:

- opening an internal investigation task;
- requesting missing information using an approved message;
- applying a pre-approved classification;
- updating a non-consequential internal status;
- triggering an agreed alert or escalation;
- executing a low-value, reversible action within a delegated threshold.

Do not use this model merely because a task is frequent.

## Model 2: Collaborative, with human approval

Use when:

- evidence preparation is repeatable;
- the option set is bounded but contains meaningful trade-offs;
- policy guides the decision but does not fully determine it;
- the action creates cost, service, customer, supplier, capacity, or inventory consequences;
- a named human can review evidence and approve before release;
- the approval can occur inside the decision window.

The AI may:

- assemble a traceable evidence packet;
- identify missing or conflicting information;
- generate policy-compliant options;
- compare agreed dimensions;
- draft a recommendation and communication;
- prepare an action for approval;
- execute only after explicit approval if the system permits.

The approval interface must make the consequence visible. A button that hides assumptions is not a meaningful human checkpoint.

## Model 3: Human-owned decision, with AI drafting

Use when any of these dominate:

- high stakes or broad blast radius;
- novel conditions or sparse precedent;
- ambiguous policy;
- customer allocation or promise changes;
- safety, quality, regulatory, ethical, or contractual implications;
- hard-to-reverse action;
- conflicting objectives that require accountable judgement;
- evidence that remains uncertain or disputed.

The AI may prepare facts, alternatives, assumptions, sensitivities, and questions. The human decides and acts.

## Stakes and reversibility matrix

Use the matrix as a discussion aid, not an automatic classifier.

| Stakes | Reversibility | Default posture |
| --- | --- | --- |
| Low | Easy and fast | Consider bounded execution if all other controls pass. |
| Low | Hard or slow | Human approval; low value does not remove irreversibility. |
| Moderate | Easy and fast | Human approval until evidence, policy, and monitoring are proven. |
| Moderate | Hard or costly | Human-owned or explicit approval with narrow authority. |
| High | Easy in the system but not in customer or operational effect | Human-owned; system reversal may not repair the consequence. |
| High | Hard or impossible | Human-owned; AI supports analysis only. |

## Boundary specification

Every delegated use case needs an explicit boundary:

### Preconditions

- required data is present and fresh;
- identifiers reconcile;
- confidence or data-quality conditions pass;
- policy version is known;
- the event falls inside the approved scope.

### Permitted actions

List exact actions, systems, fields, values, and thresholds. Avoid “manage,” “optimise,” or “resolve.”

### Prohibited actions

Examples:

- change a customer promise;
- approve unbudgeted spend;
- substitute an unqualified material;
- alter a regulated record;
- allocate scarce inventory across strategic customers;
- contact an external party without approval;
- act when evidence conflicts;
- extend authority beyond one site, category, lane, or threshold.

### Escalation conditions

Escalate when:

- a threshold is exceeded;
- evidence is missing, stale, or contradictory;
- no policy-compliant option exists;
- the event is novel;
- an action would affect safety, quality, compliance, or an external commitment;
- the user overrides repeatedly;
- the expected outcome diverges from reality;
- an upstream or downstream system is unavailable.

### Safe failure

Define what happens when the workflow cannot complete:

- make no change;
- retain the last approved state;
- create an exception packet;
- notify the owner;
- preserve evidence and logs;
- prevent repeated or duplicate action.

### Observability

Record:

- trigger and timestamp;
- source evidence and versions;
- missing or conflicting data;
- generated options;
- recommendation and rationale;
- policy or threshold applied;
- approver and approval time;
- action taken;
- override or rollback;
- operational outcome;
- evaluation result.

## Consequence test

Before increasing authority, ask:

1. Who receives the benefit if the action is right?
2. Who absorbs the loss if it is wrong?
3. Who must explain the outcome?
4. Can the affected party appeal or correct it?
5. Does rollback repair the actual harm or only the system record?

If the answers point outside the team operating the AI, keep the decision human-owned or require explicit approval.

## Authority expansion

Do not expand authority because the model appears persuasive. Expand only when evidence shows:

- stable performance on representative cases;
- acceptable false-action and missed-action rates;
- reliable escalation;
- correct use of current policy;
- effective human override;
- no unobserved downstream harm;
- named owner approval;
- continued reversibility inside the expanded scope.

Increase one boundary at a time: volume, value threshold, action type, geography, product, or time window.
