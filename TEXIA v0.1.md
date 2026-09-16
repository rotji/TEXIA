# TEXIA V0.1

This document is the current authoritative specification for TEXIA V0.1. It preserves the original manual methodology and incorporates the validated lessons discovered during early testing, without introducing a separate V0.2 designation.

The version remains:

> TEXIA V0.1

The specification is intentionally constrained to the original framework and the requirements confirmed as necessary during testing. It does not expand the method beyond the validated foundation already established in the project.

---

# 1. Purpose

TEXIA is a manual intelligence method for transforming fragmented, noisy, inconsistent, or contradictory information into structured, evidence-linked understanding.

The system is designed to help answer:

* What is happening?
* Who or what is involved?
* What is claimed?
* What is observed?
* What is evidence?
* What is inferred?
* What is disputed?
* What remains unknown?
* How do we know each of these things?

TEXIA is not a summary engine. It is a disciplined process for reconstructing states, relationships, events, claims, evidence, and uncertainty from raw information and source material.

---

# 2. Core Operating Principle

TEXIA should never analyze information without first defining the environment of analysis.

The manual workflow is:

```text
REAL-WORLD INFORMATION
        ↓
     COLLECT
        ↓
     SEGMENT
        ↓
    EXTRACT
        ↓
CLASSIFY EPISTEMIC STATUS
        ↓
PRESERVE MODALITY
        ↓
RESOLVE ENTITIES
        ↓
RESOLVE RELATIONSHIPS
        ↓
    EXTRACT EVENTS
        ↓
      BIND TIME
        ↓
   MAP EVIDENCE
        ↓
RECONSTRUCT INSTITUTIONAL PATHWAYS
        ↓
 RECONCILE CLAIMS
        ↓
HANDLE NEGATIVE EVIDENCE
        ↓
 RECONSTRUCT STATE
        ↓
  DETECT CHANGE
        ↓
     ANALYZE
        ↓
      INFER
        ↓
   HYPOTHESIZE
        ↓
      VERIFY
        ↓
     REPORT
```

This workflow preserves the original manual architecture while integrating the core controls discovered during real-world testing.

---

# 3. First: Create a TEXIA Monitor

Before analyzing anything, define the environment and the question being asked.

Use this template:

```text
TEXIA MONITOR

Monitor ID:
Date:

MONITOR NAME:
[Name]

OBJECTIVE:
[What are we trying to understand?]

DOMAIN:
[Leave broad/general]

SCOPE:
[What is included?]

ENTITIES OF INTEREST:
1.
2.
3.

EVENTS OF INTEREST:
1.
2.
3.

QUESTIONS:
Q1.
Q2.
Q3.
Q4.

TIME WINDOW:
[Start → End]

SOURCES:
1.
2.
3.
```

This is important because TEXIA should never analyze information without knowing the question, scope, and environment.

---

# 4. Collect the Raw Information

Suppose we have 20 documents.

Do not immediately ask:

> "Summarize these documents."

Instead, preserve the raw material as source-level evidence.

```text
SOURCE 001
SOURCE 002
SOURCE 003
...
SOURCE 020
```

Each source gets:

```text
SOURCE ID
TITLE
AUTHOR / ORGANIZATION
DATE
SOURCE TYPE
URL / ORIGIN
```

This becomes the Source Register.

---

# 5. Segment the Information

A complete document is too large to treat as one unit.

We break it into meaningful pieces, such as paragraphs, statements, annexes, or evidence-bearing units.

```text
DOCUMENT 001

P1
P2
P3
P4
...
```

We do not necessarily analyze every sentence independently. We identify information-bearing units that may contain:

* an observation
* a claim
* an event
* a forecast
* a causal assertion
* a description of a state
* a change
* a qualification

---

# 6. Build the Observation Record

For every important piece of information, ask:

> What was actually observed or reported?

Manual template:

```text
OBSERVATION ID:

Source:
Document:
Location in document:

Observation:

Entity:
Time:

Directly observed?
YES / NO

Measurement:
If applicable:

Original wording:
```

We preserve the original wording. This becomes critical later when claims are compared, reconciled, and tested.

---

# 7. Extract Entities

Now ask:

> Who or what is this information about?

Create an Entity Register:

```text
ENTITY REGISTER

E001
Name:
Type:
Aliases:
Description:

E002
Name:
Type:
Aliases:
Description:
```

Do not create an entity simply because a name appears.

The required pathway is:

```text
MENTION
   ↓
CANDIDATE
   ↓
ENTITY
```

If the identity is uncertain, record:

```text
ENTITY STATUS:
Unresolved
```

rather than pretending certainty.

## 7.1 Entity Identity Uncertainty

TEXIA must not force uncertain entities into a single identity.

Two names may represent:

* the same entity
* probably the same entity
* possibly the same entity
* related but distinct entities
* renamed entities
* historical versions of the same entity
* entities with overlapping functions
* entities incorrectly identified as the same
* entities whose relationship remains unresolved

The system must preserve uncertainty where the available evidence does not establish the relationship.

Required states include:

* confirmed same
* probable same
* possible same
* related but distinct
* renamed
* historical relationship
* contradicted
* unresolved

---

# 8. Extract Events

Next ask:

> What happened?

Create:

```text
EVENT REGISTER

EV001

What happened:
Who:
Where:
When:
Previous state:
Resulting state:
Source:
Confidence:
```

This is where TEXIA moves beyond ordinary text extraction and begins constructing a timeline of events.

## 8.1 Event vs. Claim About an Event

TEXIA must distinguish:

```text
CLAIM ABOUT EVENT
        ≠
EVENT ITSELF
```

A source may assert an event without establishing that the event occurred.

The claim records what was asserted.
The event record represents what the available evidence supports.

---

# 9. Extract Claims

Now ask:

> What is somebody asserting?

For example:

```text
CLAIM C001

Claimant:
Organization A

Claim:
"X will happen."

Claim type:
Forecast

Source:
Document 004

Time:
...

Evidence supplied:
...

Status:
Unverified
```

This prevents the silent conversion of a statement into a fact.

## 9.1 Claim Modality and Linguistic Strength

TEXIA must preserve the linguistic strength and modality of a claim as expressed by its source.

It must distinguish between expressions such as:

* confirmed
* established
* stated
* reported
* alleged
* claimed
* reportedly
* apparently
* appears to
* may have
* could have
* is believed to
* is suspected of
* according to
* denied
* rejected
* disputed
* unverified
* preliminary
* provisional

These expressions must not be silently strengthened or weakened during extraction, normalization, reconciliation, inference, or reporting.

The original modality must remain attached to the claim throughout extraction, reconciliation, inference, and reporting.

### Example

Source:

> The committee said the accounts may have been used for unauthorized transactions.

TEXIA must not convert this into:

> The accounts were used for unauthorized transactions.

---

# 10. Separate Five Things

This is one of the most important TEXIA rules.

Whenever we encounter information, classify it:

```text
1. OBSERVATION
2. CLAIM
3. EVIDENCE
4. INFERENCE
5. HYPOTHESIS
```

Example:

```text
Observation:
Sales declined 15%.

Claim:
Management says the decline was temporary.

Evidence:
Quarterly financial report.

Inference:
The company may be experiencing temporary weakness.

Hypothesis:
Demand weakness is responsible for the decline.
```

These are five different epistemic objects, and the distinction is a core safeguard of the system.

## 10.1 Epistemic Status Preservation

TEXIA must explicitly preserve the epistemic status of information.

The following must not be treated as equivalent:

```text
OBSERVATION
CLAIM
INSTITUTIONAL ASSERTION
ALLEGATION
INVESTIGATION FINDING
EVIDENCE
INTERPRETATION
INFERENCE
CAUSAL HYPOTHESIS
CAUSAL CONCLUSION
PREDICTION
QUALIFICATION
UNKNOWN
```

A newspaper report stating that a committee alleged diversion is not the same as the underlying event having occurred.

---

# 11. Extract Time

For every event or claim, ask:

```text
WHEN?

Event time:
Publication time:
Reference period:
Effective time:
Forecast period:
```

For example:

```text
Article published:
September 8

Event:
September 3

Policy effective:
October 1
```

Never collapse those into one date.

Temporal binding is required for every event, claim, and state.

---

# 12. Build the Evidence Chain

Now ask:

> What supports this?

We create:

```text
CLAIM
  ↓
EVIDENCE
  ↓
SOURCE
  ↓
ORIGINAL DOCUMENT
```

Example:

```text
Claim C004
     ↓
Evidence E009
     ↓
Source S003
     ↓
Paragraph 17
```

This allows every important conclusion to be traced back to its sources and evidence.

## 12.1 Evidence Rules

Evidence must remain distinct from claims.

The following must not automatically count as independent evidence:

```text
SOURCE A reports SOURCE B.
SOURCE C repeats SOURCE B.
SOURCE D repeats SOURCE C.
```

This may represent repeated information rather than independent corroboration.

TEXIA must therefore track:

* directness
* authority
* independence
* specificity
* temporal relevance
* consistency
* completeness
* provenance

Evidence quality is not the same as repetition.

---

# 13. Compare Sources

Suppose five sources discuss the same event.

We make:

| Claim | Source A | Source B | Source C | Source D |
| --- | --- | --- | --- | --- |
| Event occurred | ✓ | ✓ | ✓ | ✓ |
| Date | Sept 3 | Sept 3 | Sept 4 | Sept 3 |
| Cause | X | X | Y | unknown |
| Effect | A | A | B | unknown |

Now we can see:

### Agreement
The event itself is strongly supported.

### Conflict
The cause is disputed.

### Uncertainty
The effect is not established.

This is much more valuable than a generic summary.

---

# 14. Watch for Source Independence

This is a critical rule.

Suppose:

```text
Source A reports X.

Source B reports X.

Source C reports X.

Source D reports X.
```

We must ask:

> Are A, B, C and D actually independent?

Maybe:

```text
Original report
      ↓
Reuters
      ↓
Newspaper A
      ↓
Newspaper B
      ↓
Blog C
```

That is not five independent confirmations. It may be one information lineage appearing in multiple forms.

So we record:

```text
SOURCE LINEAGE
```

---

# 15. Reconstruct the State

Now ask:

> Given everything we've collected, what is the state of the environment?

A state reconstruction must distinguish between:

```text
WHAT IS OBSERVED
WHAT IS CLAIMED
WHAT IS SUPPORTED
WHAT IS DISPUTED
WHAT IS INFERRED
WHAT IS UNKNOWN
```

A state should never be built solely from the most repeated or most authoritative-sounding claim. It must remain evidence-linked.

---

# 16. Detect Change

TEXIA must identify change over time.

A detected change must distinguish between:

```text
OBSERVED CHANGE
REPORTED CHANGE
INFERRED CHANGE
EXPECTED CHANGE
PREDICTED CHANGE
```

A reported change is not equivalent to an independently verified change.

A change record should retain:

* previous state
* current state
* change
* source
* evidence
* time
* epistemic status
* confidence
* causal explanation
* causal uncertainty

---

# 17. Relationship Precision

TEXIA must distinguish between different relationship types rather than collapsing them into a generic concept such as "connected to" or "associated with."

Examples include:

* linked to
* associated with
* affiliated with
* represented by
* controlled by
* owned by
* operated by
* managed by
* funded by
* financed by
* appointed by
* approved by
* established by
* authorized by
* created by
* registered by
* registered with
* employed by
* contracted by
* advised by
* investigated by
* accused by
* reported by
* mentioned by

The specific relationship must be preserved according to the evidence.

## 17.1 Relationship Semantics Preservation

Confidence in a relationship must not change the semantic meaning of that relationship.

```text
Relationship Type:
LINKED_TO

Confidence:
HIGH
```

must not automatically become:

```text
Relationship Type:
OWNED_BY
```

A high-confidence weak or indirect relationship must not be silently converted into a stronger relationship merely because confidence is high.

---

# 18. Negative Evidence and Absence Handling

TEXIA must explicitly model absence.

The system must distinguish between:

```text
NO EVIDENCE FOUND
        ≠
EVIDENCE OF ABSENCE
        ≠
AUTHORITATIVE DENIAL
```

### No evidence found
Means the search did not locate supporting evidence within the examined material. It does not prove that the event did not happen.

### Evidence of absence
Means evidence exists indicating that the event or state did not occur.

### Authoritative denial
Means a relevant authority explicitly states that the event or state did not occur or did not exist.

The denial itself remains a claim or institutional assertion and must be treated according to its epistemic status.

---

# 19. Institutional Pathway Reconstruction

TEXIA must reconstruct how an entity, document, claim, decision, authorization, resource, or action moves through an institutional system.

A real-world outcome may pass through multiple institutional stages.

```text
CLAIM
  ↓
DOCUMENT
  ↓
SUBMISSION
  ↓
REVIEW
  ↓
APPROVAL
  ↓
ADMINISTRATIVE PROCESSING
  ↓
BUDGET ENTRY
  ↓
FINANCIAL CLEARANCE
  ↓
RELEASE
  ↓
PROCUREMENT / PAYMENT
  ↓
ACTUAL EXPENDITURE
  ↓
OPERATIONAL ACTIVITY
```

TEXIA must distinguish these stages.

Important distinctions:

* budget appropriation ≠ financial release
* financial release ≠ expenditure
* expenditure ≠ operational activity
* institutional recognition ≠ legal establishment
* public representation ≠ lawful appointment

## 19.1 Institutional Pathway Principle

TEXIA must reconstruct the sequence of institutional actions and states through which an entity, document, decision, resource, or event moves, without assuming that one institutional state implies another.

---

# 20. Inference Containment and Lineage

The system must maintain a clear boundary between:

```text
SOURCE
   ↓
OBSERVATION
   ↓
INTERPRETATION
   ↓
INFERENCE
   ↓
CAUSAL HYPOTHESIS
   ↓
CAUSAL CONCLUSION
   ↓
PREDICTION
```

Each inferential step must retain lineage.

An inference must identify:

* conclusion
* observations used
* claims used
* evidence used
* assumptions
* context
* alternative explanations
* confidence
* status

Rule:

> An inference must remain explicitly marked as an inference unless new evidence changes its epistemic status.

AI-generated interpretation must never silently become source-level fact.

---

# 21. Core Object Model

TEXIA works with distinct information objects. These must remain separate and must not be silently converted into one another.

```text
ENTITY
   ≠
EVENT
   ≠
CLAIM
   ≠
RELATIONSHIP
   ≠
STATE
```

## 21.1 Entity
An entity represents a thing, actor, institution, location, or identifiable object.

## 21.2 Event
An event represents something that happened or is proposed to happen.

## 21.3 Claim
A claim should support:

* claim ID
* claimant
* claim text
* normalized claim
* claim type
* epistemic status
* modality
* linguistic strength
* source
* document
* location
* event/reference time
* publication time
* evidence
* supporting claims
* contradicting claims
* status
* confidence

## 21.4 Relationship
A relationship should support:

* relationship ID
* subject entity
* relationship type
* object entity
* source
* evidence
* confidence
* status
* start time
* end time
* temporal validity
* qualification

## 21.5 Entity Relationship
An entity relationship should support:

* entity A
* entity B
* relationship type
* relationship status
* confidence
* evidence
* source
* temporal context
* notes

## 21.6 Absence / Negative Evidence
An absence record should support:

* absence ID
* proposition tested
* subject
* search scope
* search date
* sources checked
* institutions checked
* coverage
* absence type
* evidence
* limitations
* confidence
* status

## 21.7 Institutional Pathway
An institutional pathway should support:

* pathway ID
* subject
* step
* previous step
* next step
* actor
* institution
* action
* input
* output
* timestamp
* evidence
* source
* status
* uncertainty

---

# 22. Definition of State

A state reconstruction must distinguish between:

```text
WHAT IS OBSERVED
WHAT IS CLAIMED
WHAT IS SUPPORTED
WHAT IS DISPUTED
WHAT IS INFERRED
WHAT IS UNKNOWN
```

The state must be evidence-linked.

---

# 23. Definition of Change

A detected change must distinguish between:

```text
OBSERVED CHANGE
REPORTED CHANGE
INFERRED CHANGE
EXPECTED CHANGE
PREDICTED CHANGE
```

A Change Record should retain:

* previous state
* current state
* change
* source
* evidence
* time
* epistemic status
* confidence
* causal explanation
* causal uncertainty

---

# 24. What Happened?

TEXIA must distinguish between:

> What a source says happened.

and:

> What the available evidence supports happened.

and:

> What TEXIA infers happened.

Therefore an intelligence output should be capable of presenting:

```text
SOURCE REPORT
      ↓
CLAIM
      ↓
EVIDENCE
      ↓
RECONCILIATION
      ↓
SUPPORTED STATE
      ↓
INFERENCE
```

---

# 25. Safeguards and Rules of Use

TEXIA must not silently convert:

* allegation into fact
* claim into event
* relationship into stronger relationship
* uncertainty into certainty
* evidence into inference without lineage
* repeated reporting into independent corroboration
* institutional representation into confirmed fact
* budget entry into expenditure
* appearance into legal existence

The system must preserve:

* claim modality
* evidence provenance
* source independence
* temporal distinctions
* epistemic status
* uncertainty
* relationship semantics
* inference lineage
* absence distinctions
* institutional stage distinctions

---

# 26. Definition of Done for V0.1

Before TEXIA V0.1 can be considered fully validated through manual testing, the workflow should demonstrate that it can:

* preserve claim modality;
* preserve linguistic strength;
* distinguish allegation from finding;
* distinguish institutional assertion from observation;
* distinguish evidence from claim;
* distinguish linked-to from owned-by;
* distinguish associated-with from controlled-by;
* preserve unresolved entity identity;
* represent related-but-distinct entities;
* reconstruct institutional pathways;
* distinguish legal existence from administrative recognition;
* distinguish budget appropriation from financial release;
* distinguish financial release from expenditure;
* distinguish expenditure from operational activity;
* handle negative evidence;
* distinguish no evidence found from evidence of absence;
* preserve epistemic status;
* preserve inference lineage;
* prevent inference from silently becoming fact;
* preserve temporal uncertainty;
* preserve source independence;
* maintain evidence provenance.

---

# 27. Governing Rule

> TEXIA must model what is known, what is claimed, what is observed, what is supported, what is inferred, what is disputed, what is unknown, and how the system knows each of these things.

This is a foundational requirement of TEXIA.

---

# 28. Current Status

**Version:** TEXIA V0.1
**Testing Mode:** Manual
**Status:** Authoritative specification
**V0.2:** Not yet frozen

This document is the current operational specification for TEXIA V0.1. It preserves the original manual foundation and incorporates the validated requirements discovered during testing where they are consistent with that foundation and necessary to preserve the method.
