Yes — and I think this is the **right decision**.

We should treat **TEXIA V0.1 as a manual instrument before we automate it**. That lets us discover whether the method actually produces useful intelligence before spending time building software.

In fact, the manual version should behave almost exactly like the future software version.

# TEXIA V0.1 — Manual Operating Method

The basic workflow is:

```text
REAL-WORLD INFORMATION
        ↓
     COLLECT
        ↓
     SEGMENT
        ↓
    EXTRACT
        ↓
    STRUCTURE
        ↓
    RECONCILE
        ↓
   RECONSTRUCT
      STATE
        ↓
  DETECT CHANGE
        ↓
    ANALYZE
        ↓
 GENERATE INTELLIGENCE
        ↓
     VERIFY
        ↓
     REPORT
```

We can perform all of this manually using **ChatGPT + documents/web sources + simple tables/notes**.

---

# 1. First: Create a TEXIA Monitor

Before analyzing anything, define the environment.

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

This is important because **TEXIA should never analyze information without knowing what question/environment it is analyzing.**

---

# 2. Collect the Raw Information

Suppose we have 20 documents.

Do **not** immediately ask:

> "Summarize these documents."

Instead, we preserve the raw material.

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

This becomes our **Source Register**.

---

# 3. Segment the Information

A complete document is too large to treat as one unit.

We break it into meaningful pieces.

For example:

```text
DOCUMENT 001

P1
P2
P3
P4
...
```

But we don't necessarily analyze every sentence independently.

We identify **information-bearing units**.

An information unit might contain:

* an observation
* a claim
* an event
* a forecast
* a causal assertion
* a description of a state
* a change
* a qualification

---

# 4. Build the Observation Record

For every important piece of information, ask:

> **What was actually observed/reported?**

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

We preserve the original wording.

This becomes extremely important later.

---

# 5. Extract Entities

Now ask:

> **Who or what is this information about?**

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

Don't create an entity simply because a name appears.

We need:

```text
MENTION
   ↓
CANDIDATE
   ↓
ENTITY
```

If we're uncertain, record:

```text
ENTITY STATUS:
Unresolved
```

rather than pretending we know.

---

# 6. Extract Events

Next:

> **What happened?**

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

This is where TEXIA starts moving beyond ordinary text analysis.

We're constructing a **timeline of events**.

---

# 7. Extract Claims

Now ask:

> **What is somebody asserting?**

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

This prevents us from accidentally turning someone's statement into reality.

---

# 8. Separate Five Things

This is one of the most important TEXIA manual rules.

Whenever we encounter information, classify it.

```text
1. OBSERVATION
2. CLAIM
3. EVIDENCE
4. INFERENCE
5. HYPOTHESIS
```

For example:

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

These are **five different epistemic objects**.

This distinction is one of the strongest things we can carry forward from our earlier experiments.

---

# 9. Extract Time

For every event/claim, ask:

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

---

# 10. Build the Evidence Chain

Now ask:

> **What supports this?**

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

This means every important conclusion can eventually be audited.

---

# 11. Compare Sources

This is where TEXIA becomes much more interesting.

Suppose five sources discuss the same event.

We make:

| Claim          | Source A | Source B | Source C | Source D |
| -------------- | -------- | -------- | -------- | -------- |
| Event occurred | ✓        | ✓        | ✓        | ✓        |
| Date           | Sept 3   | Sept 3   | Sept 4   | Sept 3   |
| Cause          | X        | X        | Y        | unknown  |
| Effect         | A        | A        | B        | unknown  |

Now we can see:

### Agreement

The event itself is strongly supported.

### Conflict

The cause is disputed.

### Uncertainty

The effect is not established.

This is much more valuable than a 500-word summary.

---

# 12. Watch for Source Independence

This is another critical manual rule.

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

That's not five independent confirmations.

It's potentially **one information lineage appearing five times**.

So we record:

```text
SOURCE LINEAGE
```

This will become very important later.

---

# 13. Reconstruct the State

Now we ask:

> **Given everything we've collected, what is the state of the environment?**

Use:

```text
STATE SNAPSHOT

As of:
Date

ENTITY / SUBJECT:

Current status:
...

Known facts:
...

Active events:
...

Current relationships:
...

Current indicators:
...

Supported claims:
...

Unresolved claims:
...

Unknowns:
...
```

Then create previous snapshots:

```text
STATE T0
   ↓
EVENT
   ↓
STATE T1
   ↓
EVENT
   ↓
STATE T2
```

---

# 14. Detect Change

Now compare:

```text
PREVIOUS STATE
       vs
CURRENT STATE
```

Ask:

### What changed?

```text
Entity changed?
Relationship changed?
Status changed?
Value changed?
Policy changed?
Event occurred?
Claim changed?
Forecast changed?
Risk changed?
```

Record:

```text
CHANGE ID:

Subject:

Previous state:

Current state:

Change:

Date:

Evidence:

Confidence:

What caused the change?
Known / suspected / unknown
```

---

# 15. Identify What Matters

Not every change is important.

So we introduce a second question:

> **Why does this change matter?**

For every significant change:

```text
CHANGE
   ↓
IMPLICATION
```

But we must distinguish:

```text
Observed implication
       vs
Inferred implication
       vs
Possible implication
```

Example:

```text
Observed:
Policy changed.

Inference:
This may increase operating costs.

Hypothesis:
The policy could cause companies to relocate.

Unknown:
Whether companies actually will relocate.
```

---

# 16. Identify Contradictions

TEXIA should actively search for:

```text
CLAIM A
   ↕
CLAIM B
```

Then classify:

```text
True contradiction
Different time
Different definition
Different entity
Different measurement
Different scope
Different interpretation
Insufficient information
```

This prevents false contradictions.

---

# 17. Identify Unknowns

This is something ordinary summaries usually don't do.

Create an:

# **Unknown Register**

```text
U001:
Cause of event remains uncertain.

U002:
No independent confirmation.

U003:
Future outcome unknown.

U004:
Two sources disagree.

U005:
Data unavailable for period X.
```

This tells us:

> **What we don't know.**

That is itself intelligence.

---

# 18. Generate the TEXIA Intelligence Brief

After all that, we produce the final output.

The format should be:

```text
TEXIA INTELLIGENCE BRIEF

MONITOR:
...

DATE:
...

────────────────────────

1. CURRENT STATE

...

────────────────────────

2. WHAT CHANGED?

Change 001
...

Change 002
...

────────────────────────

3. WHY IT MATTERS

...

────────────────────────

4. SUPPORTING EVIDENCE

...

────────────────────────

5. CONFLICTING INFORMATION

...

────────────────────────

6. UNCERTAINTIES

...

────────────────────────

7. INFERENCES

...

────────────────────────

8. HYPOTHESES

...

────────────────────────

9. OPEN QUESTIONS

...

────────────────────────

10. WHAT TO WATCH NEXT

...

────────────────────────

CONFIDENCE / EVIDENCE QUALITY

...

SOURCE REGISTER

...
```

That is our **manual TEXIA output**.

---

# 19. The Most Important Part: Don't Let TEXIA Become a Summary Machine

Our workflow should be:

```text
                 DOCUMENTS
                     ↓
                 SUMMARY
                     ↓
                 ❌ STOP
```

Instead:

```text
                 DOCUMENTS
                     ↓
               INFORMATION
                     ↓
                STRUCTURE
                     ↓
       ┌─────────────┼─────────────┐
       ↓             ↓             ↓
    ENTITIES       EVENTS        CLAIMS
       │             │             │
       └─────────────┼─────────────┘
                     ↓
                  EVIDENCE
                     ↓
                    TIME
                     ↓
                   STATE
                     ↓
                  CHANGE
                     ↓
                 INFERENCE
                     ↓
               INTELLIGENCE
```

That's the difference between **document summarization** and what we're attempting with TEXIA.

---

# 20. How We Use ChatGPT as the Manual TEXIA Instrument

We don't need software.

You can give me:

```text
TEXIA MONITOR
+
SOURCE 001
+
SOURCE 002
+
SOURCE 003
...
```

And instruct me to execute the TEXIA protocol.

For example:

> **Run TEXIA V0.1 on these sources. Do not summarize first. Extract the entities, events, observations, claims, evidence and temporal information. Resolve references, compare claims across sources, reconstruct the current state, identify changes, contradictions and uncertainties, then produce the intelligence brief.**

I would then operate as the **manual processing engine**.

You remain the investigator/operator.

---

# 21. But We Should Keep a Human Verification Gate

Very important.

The manual workflow should be:

```text
TEXIA ANALYSIS
      ↓
HUMAN REVIEW
      ↓
CORRECTION
      ↓
FINAL INTELLIGENCE
```

If I make an incorrect entity resolution:

```text
TEXIA:
Company A = Company B

Human:
NO — different entities.
```

We correct it.

If I infer causation where the evidence doesn't support it:

```text
TEXIA:
A caused B.

Human:
INSUFFICIENT EVIDENCE.
```

The conclusion becomes:

```text
A preceded B.
A may be related to B.
Causation unresolved.
```

This is exactly how we make the instrument stronger.

---

# 22. Our First Real Manual TEXIA Test

I recommend we **stop creating artificial experiments now**.

Let's take one real-world information environment.

Not necessarily Nigeria.

Not necessarily finance.

Not necessarily politics.

We choose something with:

* multiple sources
* a timeline
* competing claims
* observable changes
* enough information to investigate
* meaningful consequences

Then we run the entire TEXIA V0.1 process.

### Test structure

```text
TEXIA TEST 001

MONITOR
↓
10–20 SOURCES
↓
SOURCE REGISTER
↓
ENTITY REGISTER
↓
EVENT REGISTER
↓
OBSERVATION REGISTER
↓
CLAIM REGISTER
↓
EVIDENCE MAP
↓
TIMELINE
↓
STATE T0
↓
STATE T1
↓
CHANGE REGISTER
↓
CONFLICT REGISTER
↓
UNKNOWN REGISTER
↓
INFERENCE REGISTER
↓
TEXIA INTELLIGENCE BRIEF
```

And here's the important part:

**We will judge TEXIA by whether it discovers something useful that ordinary reading/summarization would have made easier to miss.**

If it doesn't, we don't blindly proceed.

We identify the failure, modify V0.1, and run the next real-world test.

That is how the **product itself becomes our laboratory** without getting trapped in endless theoretical experiments.
