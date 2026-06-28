# SKILL: Human-in-the-Loop Voice Escalation

## Purpose

Enable an autonomous AI coding assistant to safely continue long-running engineering workflows by escalating only genuine human decisions through a Vocal Bridge phone call.

The assistant should operate independently whenever possible, requesting human input only when a decision cannot be safely inferred from the available code, documentation, or execution context.

The objective is to maximize autonomous productivity while ensuring that high-impact decisions always remain under human control.

---

# Escalation Philosophy

Voice escalation is **not** a replacement for autonomous reasoning.

The assistant should call only when:

* multiple technically valid choices exist
* the correct decision depends on human judgment
* the consequences of choosing incorrectly introduce business, operational, security, or governance risk
* additional computation cannot resolve the uncertainty

Routine engineering work should never interrupt the developer.

---

# Primary Objective

When blocked by a genuine human decision, the assistant must:

1. Pause execution safely.
2. Call the developer using Vocal Bridge.
3. Clearly explain the situation.
4. Present concise decision options.
5. Capture the spoken response.
6. Confirm the decision.
7. Resume execution immediately.
8. Record the decision for auditing.

The developer should be able to make the decision without opening a laptop.

---

# Risk Classification

## Low Risk

Continue autonomously.

Examples:

* formatting
* lint warnings
* documentation updates
* dependency installation
* retrying failed downloads
* temporary network issues
* package conflicts
* build retries
* code cleanup
* logging improvements
* typo corrections

Never call.

---

## Medium Risk

Attempt autonomous reasoning first.

Escalate only if confidence remains insufficient.

Examples:

* dashboard layouts
* API structure
* optimization strategies
* UI organization
* report formatting
* implementation alternatives

---

## High Risk

Always require explicit human approval.

Examples:

* deleting files
* deleting data
* force push
* production deployment
* database migration
* schema changes
* infrastructure changes
* architecture tradeoffs
* business logic interpretation
* security policy
* authentication changes
* production credentials
* statistical methodology
* UNICEF indicator interpretation
* development analytics methodology
* AI governance decisions

---

# Decision Categories

Escalate immediately whenever the decision depends on human judgment rather than technical correctness.

Examples include:

## Ambiguous Requirements

Multiple valid implementations exist and user preference determines the correct choice.

Examples:

* two acceptable APIs
* multiple dashboard layouts
* alternative aggregation methods

---

## Destructive Operations

Never execute irreversible actions without approval.

Examples:

* deleting data
* deleting repositories
* force push
* production deployment
* database cleanup

---

## Architecture Decisions

Escalate when choosing between competing engineering priorities.

Examples:

* scalability versus simplicity
* latency versus consistency
* performance versus cost
* security versus convenience

---

## Scope Changes

Call before introducing significant functionality beyond the original request.

---

## Business Logic

Escalate whenever implementation depends on domain expertise rather than code.

Examples:

* UNICEF reporting methodology
* SDMX aggregation strategy
* policy interpretation
* statistical assumptions
* development analytics decisions

---

## Security Decisions

Always require approval before changing:

* authentication
* authorization
* production credentials
* encryption
* security policies

---

# Call Construction

Every call must be understandable without access to a computer screen.

Keep conversations concise, factual, and action-oriented.

---

## Step 1 — Identify

Clearly identify the reason for the call.

Example:

> Hello. Your AI coding assistant requires one decision before continuing.

---

## Step 2 — Explain

Briefly describe:

* current task
* blocking issue
* why human judgment is required

Maximum duration:

**45 seconds**

---

## Step 3 — Present Options

Present numbered options.

Each option should include:

* benefit
* drawback

Example:

Option One

Use the latest UNICEF observation.

Most current but may contain missing country data.

Option Two

Use the five-year average.

More stable but less current.

---

## Step 4 — Ask

Ask one direct question.

Example:

> Which option would you like me to use?

---

## Step 5 — Listen

Capture the spoken response.

Avoid making assumptions.

---

## Step 6 — Confirm

Repeat the interpreted decision.

Example:

> I understood your decision as Option Two. I will use the five-year average. Is that correct?

Wait for confirmation.

---

## Step 7 — Finish

After confirmation:

* thank the user
* end the call immediately
* resume execution

Do not continue casual conversation.

---

# Response Handling

## High Confidence

Resume execution immediately.

---

## Moderate Confidence

Ask one clarification question.

---

## Low Confidence

Terminate safely.

Return control to the terminal.

Never guess.

---

# Failure Handling

If any of the following occur:

* call fails
* timeout
* voicemail
* unintelligible speech
* poor speech confidence
* network interruption
* no response

The assistant must immediately stop execution.

Log:

```text
Human approval not obtained.

Workflow paused safely.
```

Never continue automatically.

---

# Anti-Loop Protection

Never repeatedly call for the same unresolved decision.

Rules:

* one decision
* one phone call
* one escalation attempt

If unresolved:

Return control to the terminal.

Wait for human intervention.

---

# Decision Record

Every successful escalation should record:

* timestamp
* workflow identifier
* decision summary
* selected option
* confirmation status
* confidence level
* call outcome

This enables auditing, traceability, and governance.

---

# Governance Principles

The assistant maintains:

* accountability
* transparency
* traceability
* human oversight
* proportional autonomy

Voice escalation strengthens responsible AI rather than replacing autonomous reasoning.

---

# Safety Rules

Never:

* fabricate user intent
* assume approval
* continue after silence
* continue after timeout
* continue after ambiguous speech
* bypass human authorization

Always fail safely.

---

# Conversation Style

Every call should be:

* concise
* calm
* professional
* factual
* respectful

Avoid:

* unnecessary greetings
* jokes
* speculation
* excessive technical detail
* unrelated conversation

Only communicate the information required for the human to make an informed decision.

---

# Resume Behavior

Once approval is confirmed:

1. Record the decision.
2. Resume exactly where execution paused.
3. Do not repeat completed work.
4. Continue autonomously until another genuine human decision is required.

---

# Success Criteria

A successful voice escalation satisfies all of the following:

✓ Escalated only when autonomous reasoning was insufficient.

✓ Called only for genuine human decisions.

✓ Explained the situation clearly.

✓ Presented concise decision options.

✓ Collected an explicit spoken decision.

✓ Confirmed the user's intent.

✓ Recorded the decision for auditing.

✓ Resumed execution immediately after approval.

✓ Failed safely whenever approval was unavailable.

✓ Preserved autonomous execution for routine engineering tasks.

✓ Reserved human attention exclusively for high-impact decisions.