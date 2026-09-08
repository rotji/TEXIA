# TEXIA V0.1

## Temporal Evidence eXtraction, Intelligence & Analysis

**Status:** V0.1 Product Specification
**Product type:** General-purpose intelligence and change-monitoring system
**Domain:** Domain-agnostic
**Primary objective:** Convert distributed information into an evidence-linked, time-aware representation of what is happening, what changed, what is claimed, and what remains uncertain.

---

# 1. Product Thesis

TEXIA exists to solve a simple problem:

> People and organizations cannot continuously read, compare, reconcile, and interpret all the information relevant to their environment.

TEXIA transforms information from multiple sources into a structured intelligence layer.

Instead of primarily answering:

> "What does this document say?"

TEXIA focuses on:

> "What do all the available sources collectively tell us about the current state, what has changed, and how certain are we?"

---

# 2. Core Product Loop

```text
DEFINE
  ↓
MONITOR
  ↓
COLLECT
  ↓
EXTRACT
  ↓
RESOLVE
  ↓
RECONCILE
  ↓
RECONSTRUCT STATE
  ↓
DETECT CHANGE
  ↓
ANALYZE
  ↓
GENERATE INTELLIGENCE
  ↓
MONITOR AGAIN
```

TEXIA is therefore not a one-time document summarizer.

It is a **continuous information-to-intelligence system**.

---

# 3. V0.1 Scope

V0.1 will support:

### Input

* User-provided documents
* Web pages / supported web sources
* Reports
* Statements
* Articles
* PDFs
* Text
* Structured data where supported

### Processing

* Document parsing
* Text segmentation
* Entity extraction
* Event extraction
* Claim extraction
* Temporal extraction
* Reference resolution
* Basic entity resolution
* Claim normalization
* Evidence linking
* Contradiction detection
* State reconstruction
* Change detection
* Basic inference

### Output

* Current State
* What Changed
* Evidence
* Timeline
* Conflicts
* Uncertainty
* Inferences
* Open Questions
* Alerts
* Intelligence Reports

---

# 4. What V0.1 Is NOT

V0.1 will deliberately NOT attempt to build:

* a universal autonomous agent
* an automatic truth machine
* perfect causal inference
* autonomous decision-making
* universal prediction
* a giant global knowledge graph
* every possible data connector
* real-time monitoring of everything
* fully autonomous investigations
* sophisticated proprietary ML research
* automatic trading or financial decisions

These capabilities may eventually exist, but they are outside V0.1.

---

# 5. The Fundamental TEXIA Object Model

TEXIA is built around a small number of universal objects.

```text
SOURCE
DOCUMENT
ENTITY
EVENT
CLAIM
OBSERVATION
EVIDENCE
TIME
RELATIONSHIP
STATE
CHANGE
INFERENCE
HYPOTHESIS
PREDICTION
QUESTION
```

The system should not treat these as interchangeable.

For example:

```text
Claim ≠ Evidence
Evidence ≠ Observation
Observation ≠ Inference
Inference ≠ Causation
Event ≠ Claim
Mention ≠ Entity
Publication Time ≠ Event Time
Confidence ≠ Truth
```

These distinctions are fundamental system constraints.

---

# 6. Monitor

The **Monitor** is the top-level user object.

A user does not tell TEXIA:

> "Analyze everything."

The user creates a specific monitoring environment.

```text
MONITOR

ID
Name
Objective
Domain
Scope

Entities of Interest
Events of Interest
Indicators of Interest
Questions of Interest

Sources
Time Horizon
Update Frequency

Alert Conditions
Status
Created At
Updated At
```

Example:

```text
Monitor:
"Company X Competitive Environment"

Objective:
Track significant developments affecting Company X.

Entities:
Company X
Competitor A
Competitor B
Regulator Y

Events:
Acquisitions
Product launches
Regulatory decisions
Leadership changes

Questions:
What changed?
Who is gaining influence?
What new risks appeared?
Which claims conflict?
```

The same engine could then be used for:

```text
Business
Finance
Science
Politics
Regulation
Supply Chain
Technology
Geopolitics
Research
Media
Custom Domains
```

The domain is configuration.

The intelligence engine remains universal.

---

# 7. Source Layer

Every piece of information entering TEXIA must have provenance.

```text
SOURCE

source_id
source_type
name
publisher
url
authority
collection_method
created_at
```

Examples:

```text
Official document
News article
Government report
Research paper
Company statement
User document
Dataset
Interview transcript
Web page
```

A source is not automatically evidence.

It is the origin from which information is obtained.

---

# 8. Document Layer

```text
DOCUMENT

document_id
source_id
title
author
publisher
publication_time
retrieval_time
document_type
language
version
content
hash
```

Important distinction:

```text
Publication Time
      ≠
Event Time
```

A document published today may describe something that happened years ago.

---

# 9. Entity Layer

TEXIA identifies entities mentioned in information.

Possible entity classes:

```text
PERSON
ORGANIZATION
GOVERNMENT
INSTITUTION
LOCATION
PRODUCT
ASSET
POLICY
INDICATOR
FINANCIAL INSTRUMENT
EVENT
OTHER
```

But:

```text
Mention
  ↓
Candidate Entity
  ↓
Resolved Entity
```

The system must not assume that two identical names represent the same entity.

Entity resolution therefore includes:

* aliases
* abbreviations
* titles
* roles
* descriptions
* identifiers
* relationships
* contextual evidence

Uncertainty must be retained.

---

# 10. Event Layer

Events describe things that happened or are expected to happen.

```text
EVENT

event_id
event_type
entities
description

start_time
end_time
reference_time
publication_time
effective_time

location
status
source_ids
confidence
```

Example:

```text
EVENT

Type:
Policy Decision

Entity:
Organization A

Event Time:
July 21, 2026

Publication Time:
July 22, 2026

Effective Time:
July 25, 2026
```

TEXIA must preserve these distinctions.

---

# 11. Claim Layer

A claim is something asserted by a source.

```text
CLAIM

claim_id
subject
predicate
object

claim_type
source_id
document_id

event_id
time
status
confidence
```

Example:

```text
Subject:
Company A

Predicate:
increased

Object:
production

Time:
Q2 2026
```

Claim types can include:

```text
FACTUAL ASSERTION
INSTITUTIONAL ASSERTION
OBSERVATION
EXPERT ASSESSMENT
FORECAST
INTERPRETATION
CAUSAL CLAIM
SPECULATION
```

This classification is important because:

> "Company A increased production"

is epistemically different from:

> "Analysts expect Company A to increase production."

---

# 12. Observation Layer

An observation represents information directly reported or measured.

```text
OBSERVATION

observation_id
content
source_id
document_id
time
entities
event_id
measurement
unit
provenance
```

Example:

```text
Observation:
Revenue increased 12%.

Measurement:
12%

Reference Period:
Q2 2026
```

Observation should remain separate from interpretation.

---

# 13. Evidence Layer

Evidence connects information to claims.

```text
EVIDENCE

evidence_id

supports_claims
contradicts_claims
qualifies_claims

source
document
observation

directness
authority
independence
specificity
temporal_relevance
consistency
completeness

provenance
```

TEXIA must distinguish:

```text
Someone says X
        ≠
Evidence that X is true
```

---

# 14. Temporal Engine

Time is a first-class component of TEXIA.

The system tracks:

```text
Event Time
Reference Time
Publication Time
Effective Time
Forecast Time
Duration
Temporal Precision
```

Example:

```text
Document published:
September 8

Describes event:
September 1

Policy becomes effective:
October 1

Forecast:
October–December
```

These must never be collapsed into one timestamp.

### Temporal rule

> Preserve the temporal precision contained in the source. Never manufacture precision that the source does not provide.

---

# 15. Claim Resolution

Different sources may express essentially the same claim.

Example:

```text
Source A:
Inflation declined.

Source B:
Price growth slowed.

Source C:
The inflation rate fell.
```

TEXIA should identify that these may refer to the same underlying proposition.

Conversely:

```text
Source A:
Inflation declined in July.

Source B:
Inflation declined during Q3.
```

These may be related but are not necessarily identical claims.

Therefore TEXIA performs:

```text
CLAIM EXTRACTION
       ↓
CLAIM NORMALIZATION
       ↓
CLAIM COMPARISON
       ↓
CLAIM RELATIONSHIP
```

Possible relationships:

```text
EQUIVALENT
SUPPORTS
CONTRADICTS
QUALIFIES
EXTENDS
NARROWS
UNCLEAR
```

---

# 16. Evidence Reconciliation

When multiple sources discuss the same subject, TEXIA compares them.

The system should identify:

```text
Agreement
Contradiction
Partial Agreement
Different Time Period
Different Definition
Different Measurement
Different Entity
Different Version
Unresolved Conflict
```

Critically:

```text
10 articles repeating Source A
```

must not automatically become:

```text
10 independent pieces of evidence.
```

TEXIA should trace information lineage.

---

# 17. State Reconstruction

This is one of the most important parts of the product.

TEXIA does not only store events.

It reconstructs the state of monitored entities or environments.

```text
STATE(t0)
    ↓
EVENT
    ↓
STATE(t1)
    ↓
EVENT
    ↓
STATE(t2)
```

Example:

```text
January:
Policy = A

March:
Policy announced to change

April:
Policy officially changed

May:
Implementation begins

June:
Observed effect appears
```

The user can therefore ask:

> What is the current state?

and:

> How did we get here?

---

# 18. Change Detection Engine

TEXIA compares states across time.

```text
PREVIOUS STATE
       ↓
      Δ
       ↓
CURRENT STATE
```

Changes can include:

```text
VALUE CHANGE
STATUS CHANGE
RELATIONSHIP CHANGE
ENTITY CHANGE
POLICY CHANGE
EVENT CHANGE
RISK CHANGE
TREND CHANGE
BELIEF CHANGE
FORECAST CHANGE
```

The central output is:

# WHAT CHANGED?

---

# 19. Intelligence Layer

TEXIA converts structured information into intelligence.

The primary intelligence object:

```text
INTELLIGENCE

id
title
summary

subject
change
previous_state
current_state

evidence
claims
events
entities
timeline

conflicts
uncertainty

inferences
open_questions

confidence
provenance
created_at
```

---

# 20. Intelligence Output

The main dashboard should answer four questions.

```text
┌────────────────────────────────────┐
│            TEXIA                   │
│                                    │
│        WHAT CHANGED?               │
│                                    │
│        WHAT MATTERS?               │
│                                    │
│        WHAT IS UNCERTAIN?          │
│                                    │
│        WHAT SHOULD WE WATCH?       │
└────────────────────────────────────┘
```

This becomes the primary user experience.

---

# 21. Intelligence Item

Every important change can be opened.

```text
CHANGE DETECTED

Subject:
Entity A

Change:
Status changed from X → Y

When:
Date / time

Previous State:
X

Current State:
Y

Evidence:
Source A
Source B
Source C

Supporting Claims:
...

Contradictory Claims:
...

Timeline:
...

Inference:
...

Alternative Explanations:
...

Confidence:
...

Open Questions:
...
```

The user should be able to move from:

```text
INTELLIGENCE
   ↓
CHANGE
   ↓
STATE
   ↓
EVENT
   ↓
CLAIM
   ↓
EVIDENCE
   ↓
SOURCE
```

This creates the audit trail.

---

# 22. Inference Engine

TEXIA can generate inferences, but must clearly label them.

Example:

```text
OBSERVATION
Investment declined.

        ↓

INFERENCE
The policy change may have contributed.

        ↓

CAUSAL HYPOTHESIS
The policy change caused part of the decline.

        ↓

PREDICTION
Further policy tightening may reduce investment further.
```

These are not equivalent.

Every inference must retain:

```text
Conclusion
Observations Used
Claims Used
Assumptions
Context
Alternative Explanations
Confidence
Provenance
Status
```

### Core rule

> TEXIA must never silently promote an inference into a fact.

---

# 23. Hypothesis Layer

Hypotheses represent explanations that remain unresolved.

```text
HYPOTHESIS

hypothesis_id
statement

supporting_evidence
contradicting_evidence

assumptions
alternative_hypotheses

confidence
status
created_at
updated_at
```

Possible status:

```text
OPEN
SUPPORTED
WEAKENED
REJECTED
CONFIRMED
UNRESOLVED
```

"Confirmed" should be used conservatively.

---

# 24. Prediction Layer

Predictions are future-oriented claims.

```text
PREDICTION

prediction_id
statement
basis

prediction_time
horizon

expected_outcome
confidence

created_at
status
```

Later:

```text
PREDICTION
     ↓
OUTCOME
     ↓
BACKTEST
     ↓
PERFORMANCE
```

This allows TEXIA to eventually learn which forecasting patterns are reliable.

V0.1 only needs basic prediction tracking.

---

# 25. Question Engine

Questions are first-class objects.

Examples:

```text
What changed?

Why did it change?

Which entities are becoming more influential?

Which claims conflict?

Which assumptions are changing?

What risks are emerging?

Which forecasts are failing?

What remains unknown?

What should we monitor next?
```

This prevents TEXIA from becoming only a passive database.

---

# 26. User Workflow

The V0.1 user journey:

```text
SIGN UP
   ↓
CREATE MONITOR
   ↓
DEFINE OBJECTIVE
   ↓
DEFINE SCOPE
   ↓
ADD ENTITIES / QUESTIONS
   ↓
ADD SOURCES
   ↓
INGEST INFORMATION
   ↓
TEXIA PROCESSES INFORMATION
   ↓
REVIEW EXTRACTED OBJECTS
   ↓
STATE CREATED
   ↓
CHANGES DETECTED
   ↓
INTELLIGENCE GENERATED
   ↓
USER INVESTIGATES
   ↓
USER ADDS / REMOVES SOURCES
   ↓
TEXIA UPDATES STATE
```

---

# 27. V0.1 Screens

The initial interface should remain small.

## 1. Dashboard

```text
Overview
What Changed
What Matters
Uncertainty
Watchlist
Recent Intelligence
```

## 2. Monitors

```text
My Monitors

Monitor A
Monitor B
Monitor C

+ Create Monitor
```

## 3. Monitor Detail

```text
Overview
Changes
Entities
Events
Claims
Evidence
Timeline
Questions
Sources
```

## 4. Intelligence Detail

```text
Change
Previous State
Current State
Evidence
Timeline
Conflicts
Inference
Uncertainty
Open Questions
```

## 5. Sources

```text
Sources
Documents
Collection status
Last updated
Source reliability metadata
```

## 6. Investigation View

A deeper exploration interface:

```text
Entity
   ↓
Events
   ↓
Claims
   ↓
Evidence
   ↓
State
   ↓
Changes
```

---

# 28. V0.1 Architecture

```text
                    TEXIA
                      │
              ┌───────┴────────┐
              │                 │
           FRONTEND          BACKEND
              │                 │
       React + TypeScript   Node + TypeScript
              │                 │
              └────────┬────────┘
                       │
                 API / Services
                       │
        ┌──────────────┼──────────────┐
        │              │              │
    Ingestion       Intelligence    Storage
        │              │              │
        ↓              ↓              ↓
   Documents       Analysis       Database
        │              │
        └───────┬──────┘
                ↓
           TEXIA CORE
                │
 ┌──────────────┼──────────────────────┐
 ↓              ↓                      ↓
Entity        Event                  Claim
Resolution    Resolution             Resolution
 │              │                      │
 └──────────────┼──────────────────────┘
                ↓
         Temporal Engine
                ↓
         Evidence Engine
                ↓
          State Engine
                ↓
         Change Engine
                ↓
        Inference Engine
                ↓
       Intelligence Engine
```

---

# 29. Proposed Technical Stack

The initial implementation can use:

```text
Frontend
Vite
React
TypeScript
CSS Modules

Backend
Node.js
Express
TypeScript

Processing
Python where specialized NLP/data processing is useful

Database
PostgreSQL or MongoDB

Object/File Storage
S3-compatible storage

Search
PostgreSQL full-text initially
Dedicated search engine later if required

AI/NLP
Model abstraction layer
```

The important architectural decision is:

> AI models must be replaceable components, not the identity of TEXIA.

---

# 30. Core Backend Services

```text
/services

ingestion
document
entity
event
claim
temporal
evidence
state
change
inference
intelligence
monitor
question
source
```

Each service should have a clear responsibility.

---

# 31. Processing Pipeline

A document entering TEXIA follows:

```text
RAW SOURCE
    ↓
DOCUMENT INGESTION
    ↓
TEXT EXTRACTION
    ↓
SEGMENTATION
    ↓
ENTITY EXTRACTION
    ↓
EVENT EXTRACTION
    ↓
CLAIM EXTRACTION
    ↓
TEMPORAL EXTRACTION
    ↓
ENTITY RESOLUTION
    ↓
EVENT RESOLUTION
    ↓
CLAIM RESOLUTION
    ↓
EVIDENCE LINKING
    ↓
STATE UPDATE
    ↓
CHANGE DETECTION
    ↓
INFERENCE
    ↓
INTELLIGENCE
```

Every stage should retain provenance.

---

# 32. Provenance

Every important piece of generated knowledge should be traceable.

```text
INTELLIGENCE
    ↓
INFERENCE
    ↓
OBSERVATIONS / CLAIMS
    ↓
DOCUMENT
    ↓
SOURCE
```

The user should never have to ask:

> "Where did TEXIA get this?"

The system should already provide the answer.

---

# 33. Confidence

Confidence should never be presented as truth probability unless the underlying methodology actually supports that interpretation.

V0.1 can use confidence as an analytical signal based on factors such as:

```text
Source quality
Evidence directness
Evidence independence
Temporal relevance
Agreement
Contradiction
Completeness
Resolution certainty
```

Example:

```text
Confidence: Medium

Why:
- 2 sources
- same underlying source lineage
- event directly reported
- no independent confirmation
```

This is much more useful than simply showing:

```text
Confidence: 82%
```

without explanation.

---

# 34. Conflict Representation

Conflicts should be visible rather than silently resolved.

```text
CONFLICT

Claim A:
Entity X announced Y.

Claim B:
Entity X has not announced Y.

Status:
Unresolved

Possible explanation:
Different publication times.

Evidence:
Source A
Source B
```

TEXIA should preserve disagreement.

---

# 35. The Minimum Viable Intelligence Unit

The smallest useful TEXIA intelligence item is:

```text
WHO / WHAT
+
WHAT HAPPENED
+
WHEN
+
WHAT CHANGED
+
EVIDENCE
+
CURRENT STATE
+
UNCERTAINTY
```

Everything else can be added around this.

---

# 36. V0.1 Success Criterion

V0.1 does not need to understand the entire world.

It needs to demonstrate one thing extremely well:

> Given a defined monitoring environment and a collection of documents, TEXIA can identify meaningful changes and show the evidence and reasoning behind them.

A successful test would look like:

```text
50 documents
      ↓
TEXIA
      ↓
structured information
      ↓
10 meaningful changes
      ↓
each change linked to evidence
      ↓
current state reconstructed
      ↓
conflicts identified
      ↓
uncertainty displayed
```

The user should be able to understand the environment significantly faster than by reading the documents manually.

---

# 37. V0.1 Product Boundary

The first version therefore has one central promise:

> **TEXIA helps users understand what changed in an information environment, why the system thinks it changed, what evidence supports that conclusion, and what remains uncertain.**

That is the product.

Not:

> "AI that knows everything."

Not:

> "An autonomous intelligence."

Not:

> "A machine that discovers the truth."

---

# 38. Development Principle

The development loop becomes:

```text
PRODUCT
   ↓
REAL USER
   ↓
REAL INFORMATION
   ↓
REAL FAILURE
   ↓
IDENTIFY GAP
   ↓
TARGETED EXPERIMENT
   ↓
DISCOVERY
   ↓
ENGINEERING
   ↓
PRODUCT IMPROVEMENT
```

This replaces the earlier endless-experimentation model.

The foundational research phase is complete.

From this point forward:

> **The product becomes the laboratory.**

---

# 39. V0.1 Definition of Done

TEXIA V0.1 is complete when a user can:

1. Create a Monitor.
2. Define its objective and scope.
3. Add entities/questions of interest.
4. Add or ingest multiple sources.
5. Process documents.
6. Extract entities, events, claims and time.
7. Resolve basic references.
8. Link claims to evidence.
9. Identify conflicting claims.
10. Construct a current state.
11. Compare previous and current states.
12. Detect meaningful changes.
13. Generate an intelligence item.
14. Inspect its evidence.
15. Follow provenance back to the original document.
16. See uncertainty and unresolved issues.
17. Ask monitoring questions.
18. Continue adding information and update the state.

If those capabilities work reliably, **TEXIA V0.1 exists.**

---

# 40. TEXIA's Core Identity

The architecture can ultimately be summarized as:

```text
                 TEXIA

        INFORMATION ENVIRONMENT
                  ↓
             OBSERVATION
                  ↓
         ENTITY / EVENT / CLAIM
                  ↓
                TIME
                  ↓
              EVIDENCE
                  ↓
                STATE
                  ↓
               CHANGE
                  ↓
              INFERENCE
                  ↓
             INTELLIGENCE
                  ↓
              DECISION
```

TEXIA's responsibility ends primarily at the **intelligence layer**.

The human or organization remains responsible for decisions.

---

# 41. V0.1 North Star

> **Turn fragmented information into an evidence-linked understanding of changing reality.**
