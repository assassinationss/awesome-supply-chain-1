# Worked example: late supplier delivery

Use this example to demonstrate the method or calibrate an output. Do not copy its assumed values into a real engagement.

## Initial symptom

> “Supplier delays create too much firefighting. We need an AI agent to manage exceptions.”

This is not yet a decision or use case.

## Recent operating moment

At 6:12 a.m., a supplier moves the committed delivery of a critical component from Thursday to Monday. The component is required by several production orders. Planners begin collecting purchase-order, inventory, production, transport, and customer information through multiple systems and messages.

## Scoped decision statement

> When a supplier moves a confirmed delivery beyond the material-required date inside the frozen production window, the materials planning manager must decide within two hours whether to expedite, use qualified substitute supply, resequence production, or escalate customer allocation. The decision requires confirmed supplier quantity and date, on-hand and in-transit inventory, production consumption, qualified substitutes, expedite feasibility and cost, and affected customer commitments. A late or wrong decision can create premium freight, lost production, missed customer promises, or poor allocation of scarce stock. Some internal planning changes are reversible; customer allocation and external commitments are harder to reverse. The supply-chain planning organisation remains accountable.

This statement is illustrative. A real session must confirm the owner, time window, evidence, and consequences.

## Decision-chain decomposition

### Establish the facts

- detect the committed-date change;
- confirm whether the new date is firm or estimated;
- retrieve affected purchase-order lines and quantities;
- reconcile part, plant, supplier, and unit identifiers;
- calculate on-hand and in-transit stock by location;
- identify production orders and dates consuming the part;
- identify affected customer orders and promise dates;
- retrieve qualified substitutes and constraints;
- record missing or conflicting evidence.

### Compare the options

- accept the new date and resequence production;
- expedite a full or partial shipment;
- transfer stock from another location;
- use a qualified substitute;
- change production allocation;
- escalate a customer-priority decision;
- compare service, cost, quality, capacity, and timing effects.

### Make the commitment

- approve premium freight;
- authorise a stock transfer;
- release a production schedule change;
- allocate scarce inventory;
- change a customer promise;
- communicate an external commitment.

## Risk and authority

| Dimension | Example finding |
| --- | --- |
| Stakes | Production continuity, premium freight, and customer service are affected. |
| Reversibility | Evidence packets are reversible; approved spend or customer commitments may not be. |
| Consequence bearer | Planning and commercial leadership absorb the service and cost outcome. |
| Uncertainty | Supplier confirmation, inventory accuracy, transit estimates, and substitution constraints may conflict. |
| Blast radius | One component may affect multiple production orders and customers. |
| Observability | Inputs and recommendations can be logged; offline customer conversations may be harder to capture. |

## Readiness gates

| Gate | Illustrative result | Evidence needed |
| --- | --- | --- |
| Decision | Pass | Confirm exact option set and deadline. |
| Ownership | Conditional | Confirm who may approve expedite, resequence, and allocation. |
| Evidence | Conditional | Test supplier confirmation and inventory-data reliability. |
| Boundary | Pass for evidence preparation; conditional for action | Define thresholds and prohibited commitments. |
| Measurement | Conditional | Establish current cycle time, effort, and outcome baseline. |

Overall verdict: **Ready for discovery, not execution.**

## Candidate use cases

### Candidate A: Exception evidence packet

- Trigger: supplier committed date crosses material-required date.
- Output: traceable packet of affected supply, demand, production, customer, and evidence gaps.
- Delegation: AI drafts; planner validates.
- Value mechanism: reduce reconciliation and waiting time.
- Risk: missed or incorrectly matched evidence.
- Evaluation: completeness, source accuracy, preparation time, and planner corrections.

### Candidate B: Option comparison

- Trigger: planner accepts a validated evidence packet.
- Output: feasible response options with explicit assumptions and trade-offs.
- Delegation: AI drafts; human approves or decides.
- Value mechanism: faster and more consistent comparison.
- Risk: infeasible option, hidden constraint, or misleading ranking.
- Evaluation: feasibility rate, missing constraints, recommendation acceptance, and override reasons.

### Candidate C: Autonomous exception resolution

- Trigger: all late-supplier events.
- Output: spend, schedule, allocation, and customer actions.
- Delegation: proposed end-to-end execution.
- Finding: reject as the first use case. It spans facts, options, and commitments; ownership and boundaries are not yet proven.

## Recommended starting point

Recommend Candidate A for discovery and shadow evaluation. It is narrower, keeps commitments human-owned, and creates the evidence needed to decide whether Candidate B is justified.

Do not claim savings until the organisation measures current volume, effort, waiting time, corrections, and outcomes.

## Human checkpoint

The planner must validate:

- supplier confirmation status;
- material and order matching;
- inventory exceptions;
- missing evidence;
- affected production and customers.

No external communication, spend, allocation, substitution, or schedule release occurs in this first scope.

## Success and stop criteria

Possible success measures:

- reduced evidence-packet preparation time;
- high completeness against an agreed checklist;
- low rate of incorrect entity matching;
- explicit capture of missing or conflicting evidence;
- planner trust based on traceable sources;
- no unauthorised action.

Stop or redesign if:

- source data cannot be reconciled reliably;
- the packet omits material consequences;
- provenance is unavailable;
- planners repeatedly rebuild the analysis outside the workflow;
- the candidate expands into commitments without a separate approval.

## Final lesson

The useful first use case is not “manage supplier delays.” It is a bounded improvement to a specific decision. Evidence preparation earns the right to consider recommendation; recommendation does not automatically earn the right to execute.
