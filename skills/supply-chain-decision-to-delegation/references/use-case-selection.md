# Use-case selection

Use this reference when comparing several AI opportunities or deciding whether a framed decision is ready for a bounded pilot.

## Selection rule

Choose the smallest use case that materially improves the decision while keeping authority, evidence, risk, and evaluation clear. Do not equate breadth or autonomy with value.

## Step 1: Apply the five gates

| Gate | Pass evidence | Conditional evidence | Fail evidence |
| --- | --- | --- | --- |
| Decision | Trigger, exact decision, deadline, and end condition are explicit. | One element needs validation. | Problem remains a topic, KPI, or technology wish. |
| Ownership | One role owns the decision and consequence. | Delegated authority requires confirmation. | Ownership is disputed or absent. |
| Evidence | Sources, authority, freshness, access, and conflict handling are known. | A limited data-quality test is needed. | Critical evidence is inaccessible, untrusted, or undefined. |
| Boundary | Permitted and prohibited actions, escalation, and safe failure are clear. | Thresholds require policy-owner confirmation. | The workflow requires open-ended or prohibited authority. |
| Measurement | Baseline and observable outcome can be defined. | Data collection must begin before evaluation. | Benefit depends on unsupported assumptions. |

One fail means no AI pilot. Recommend the prerequisite action and use the not-ready template.

## Step 2: Generate candidates at different layers

Do not generate three versions of the same broad agent. Generate candidates with meaningfully different authority.

Example candidate ladder:

1. Detect and assemble the evidence packet.
2. Validate the packet and identify missing or contradictory facts.
3. Generate a bounded option set.
4. Draft a recommendation for approval.
5. Prepare and release an action after explicit approval.
6. Execute a low-risk action inside pre-approved rules.

The right first use case is often between levels 1 and 4.

## Step 3: Compare candidates

### Value

Look for evidence of:

- recurring volume;
- long trigger-to-decision time;
- high hands-on effort;
- repeated reconciliation or rework;
- cost of delay;
- service, inventory, capacity, quality, or working-capital exposure;
- decisions that miss their useful window.

Avoid benefit claims based only on stakeholder enthusiasm.

### Feasibility

Examine:

- data availability and access rights;
- identifier and master-data quality;
- policy clarity;
- integration effort;
- latency and freshness requirements;
- representative historical cases;
- ability to run offline or shadow evaluation;
- ability to detect failure.

### Risk

Examine:

- stakes and blast radius;
- reversibility in the real world;
- customer, supplier, contractual, regulatory, safety, quality, or financial consequence;
- uncertainty and novelty;
- ease of stopping or rolling back;
- effect of a false action versus a missed action.

### Adoption

Examine:

- named daily user;
- fit with existing planning cadence and systems;
- availability of the approver inside the decision window;
- trust and transparency needs;
- override path;
- incentives and cross-functional consequences;
- training and policy ownership.

### Observability

Examine whether the team can record:

- trigger;
- inputs and provenance;
- recommendation;
- approval;
- action;
- override;
- outcome;
- reason for success or failure.

## Step 4: State the dominant trade-off

Use evidence, not a total score.

Examples:

- “Candidate A has lower direct value but is ready because the evidence and boundary are clear; Candidate B has greater theoretical value but fails the ownership gate.”
- “Recommendation drafting is feasible, but action execution is not ready because the customer consequence is hard to reverse.”
- “The process is frequent, but the signal is unreliable; data foundation work comes first.”

If stakeholders require scoring, ask them to agree weights and definitions. Show the raw evidence beside every score.

## Verdicts

### Ready for a bounded pilot

Use when all gates pass, the authority boundary is explicit, and an evaluation can compare the future workflow with the baseline.

The pilot should begin with read-only or draft-only operation unless low-risk execution is strongly justified.

### Ready for discovery, not execution

Use when the decision is clear but data quality, policy thresholds, integration, or evaluation still needs validation.

The next action is a time-bounded discovery or shadow evaluation, not a production agent.

### Process or ownership fix first

Use when the workflow lacks a final authority, functions disagree about policy, or the decision itself is unstable.

The next action is governance or process design.

### Data foundation first

Use when triggers, identifiers, authoritative sources, freshness, or evidence quality are insufficient.

The next action is data reconciliation, instrumentation, or source-of-truth agreement.

### Do not delegate this decision to AI

Use when the decision is inherently high stakes, hard to reverse, poorly observable, prohibited, or dependent on accountable judgement that cannot be bounded.

AI may still support evidence preparation if that subtask passes the gates.

## Pilot selection checks

Before issuing a bounded-pilot recommendation, confirm:

- representative cases exist for evaluation;
- the current baseline is measured or a baseline-collection period is defined;
- the output can be reviewed without executing it;
- evaluation includes both false actions and missed actions;
- escalation and safe failure are testable;
- the owner agrees the human checkpoint;
- success and stop criteria are explicit;
- scope expansion requires a separate review.

Use `output-templates/bounded-pilot-charter.md` only after these checks pass.
