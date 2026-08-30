# Problem framing reference

Use this reference when the user presents a broad problem area, a symptom, a desired technology, or several issues that have been bundled together.

## Contents

- Symptom-to-decision ladder
- Decision statement anatomy
- Decision-chain decomposition
- Evidence mapping
- Scope controls
- Common framing failures

## Symptom-to-decision ladder

Move down the ladder until the statement can be observed and owned.

| Level | Example | Diagnostic response |
| --- | --- | --- |
| Technology wish | “We need an AI agent for procurement.” | What recurring procurement decision is late, inconsistent, or expensive to prepare? |
| Strategic theme | “We need more resilience.” | During which disruption does the current response fail, and which decision becomes stuck? |
| Process area | “Supplier management is manual.” | Which supplier event triggers manual work, and what decision follows? |
| Symptom | “We get too many late confirmations.” | Which downstream commitment becomes uncertain when a confirmation is late? |
| Operating moment | “A critical PO date changes inside the production freeze window.” | Who must decide what to do, by when, using which evidence? |
| Scoped decision | “The materials planning manager must decide within two hours whether to expedite, substitute, or resequence.” | Ready for evidence, risk, and delegation analysis. |

A broad problem may contain several decisions. Do not force them into one use case.

## Decision statement anatomy

Use this complete structure:

> When **[detectable trigger]** occurs within **[scope]**, **[named role]** must decide **[verb + object]** within **[decision window]**, using **[evidence]**. A late or wrong decision affects **[stake and consequence]**. The commitment is **[reversible, reversible with cost, or hard to reverse]**, and **[role or organisation]** remains accountable.

### Trigger

A trigger should be observable without interpretation wherever possible.

Strong examples:

- supplier committed date moves beyond the material-required date;
- projected inventory falls below a service threshold inside a frozen planning horizon;
- a carrier ETA threatens a confirmed customer delivery date;
- forecast error exceeds an agreed threshold for two review cycles;
- quality status changes and blocks a production order;
- capacity demand exceeds an approved limit in a defined period.

Weak triggers:

- when supply chain risk increases;
- when the planner feels concerned;
- when the dashboard looks bad;
- whenever optimisation is needed.

### Decision

The decision must change something. Use a verb and an object.

Useful verbs:

- allocate inventory;
- approve an expedite;
- substitute a component;
- resequence production;
- revise a customer promise;
- select a supplier;
- release or hold an order;
- reroute a shipment;
- accept or reject a forecast override;
- escalate an exception.

### Owner

Distinguish among:

- the person who detects the event;
- the person who prepares analysis;
- contributors who provide evidence;
- the person authorised to decide;
- the person or organisation accountable for the consequence.

If these are unclear, ownership is part of the problem statement.

### Time window

Use the decision deadline, not the eventual process completion time. Record both when helpful:

- trigger-to-decision elapsed time;
- hands-on analysis time;
- waiting time between functions;
- time remaining before the commitment becomes harder or more expensive to change.

### Stakes and consequences

Name the mechanism, not only the metric.

Examples:

- a customer order misses its confirmed date;
- a line loses productive hours;
- scarce inventory is allocated away from a strategic customer;
- an expedite premium is incurred;
- a regulated or safety-critical material is substituted;
- working capital increases because replenishment is released unnecessarily;
- a supplier communication creates a contractual commitment.

## Decision-chain decomposition

Map the current workflow before designing the future one.

### Layer 1: Establish the facts

Typical tasks:

- detect the trigger;
- retrieve purchase orders, inventory, orders, forecasts, capacity, quality, transport, or supplier data;
- reconcile identifiers, units, dates, and versions;
- distinguish confirmed values from estimates;
- calculate exposure;
- identify missing or conflicting evidence;
- assemble an evidence packet with provenance.

Output: a traceable statement of what is known, unknown, and time-sensitive.

### Layer 2: Compare the options

Typical tasks:

- generate policy-compliant alternatives;
- test feasibility and dependencies;
- compare service, cost, quality, capacity, inventory, and timing trade-offs;
- expose assumptions and uncertainty;
- rank options only when the ranking logic is agreed;
- draft a recommendation and dissenting evidence.

Output: a bounded set of feasible options and their consequences.

### Layer 3: Make the commitment

Typical tasks:

- approve spend;
- change a plan or schedule;
- allocate scarcity;
- communicate a customer promise;
- select or reject a supplier;
- release a transaction;
- accept a regulatory, safety, quality, or contractual consequence;
- escalate outside delegated limits.

Output: an authorised action and a record of who accepted the consequence.

## Evidence map

For every important fact, record:

| Field | Question |
| --- | --- |
| Evidence item | What fact is needed? |
| Source | Which system, document, message, or person supplies it? |
| Authority | Is this a system of record, an estimate, or an opinion? |
| Freshness | How old can it be before the decision becomes unsafe? |
| Quality | Is it complete, consistent, and correctly identified? |
| Access | May the proposed workflow retrieve and use it? |
| Conflict rule | What happens when two sources disagree? |
| Provenance | Can the final recommendation link back to the source? |

Do not call a data problem an intelligence problem. If the team cannot agree which source is authoritative, the readiness gate is conditional or failed.

## Scope controls

Use these boundaries to keep the use case testable:

- one trigger family;
- one primary decision;
- one accountable role;
- one operating scope such as site, category, lane, market, or product family;
- a bounded set of inputs;
- a defined output or action;
- explicit exclusions;
- a measurable baseline and decision outcome.

The first use case should not attempt to solve planning, procurement, logistics, and customer communication simultaneously.

## Common framing failures

### Capability-first framing

“Use an LLM to monitor suppliers and resolve exceptions.”

Why it fails: it hides the trigger, decision rights, and consequences.

Correction: identify one exception and the next consequential decision.

### KPI-only framing

“Improve OTIF by five points.”

Why it fails: a lagging KPI may be influenced by many decisions and constraints.

Correction: identify the operational decision that can change the KPI and its decision window.

### Workflow-as-one-task framing

“Automate the late-supplier workflow.”

Why it fails: fact collection, option analysis, and commercial commitment have different risk profiles.

Correction: decompose the workflow and assign a delegation model to each candidate.

### Owner-by-convenience framing

“The planner owns the alert.”

Why it fails: acknowledging an alert is not the same as accepting expedite cost or changing customer allocation.

Correction: name the role with authority over the consequence.

### Benefit-by-assumption framing

“This will save thousands of hours.”

Why it fails: no baseline or validated volume supports the claim.

Correction: record current volume, touch time, elapsed time, rework, overrides, and consequence before estimating benefit.

### False-autonomy framing

“The agent owns the decision.”

Why it fails: software cannot absorb commercial, regulatory, safety, or customer accountability.

Correction: state the permitted execution authority and name the human or organisational owner.
