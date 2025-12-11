
# AI Companion Workspace Template

This template is for creating and managing **AI companion workspaces**,
including prompts, configurations, logs, evaluations, and usage guidelines.

Replace `<placeholders>` with real values.

---

## 1. Repository Identity

- **Companion Name:** `<name>`
- **Role / Function:** `<observer / assistant / tutor / analyst>`
- **Maintainer:** `<your-name>`
- **Environment:** `<local / cloud / hybrid>`

---

## 2. Purpose

Describe the purpose of this AI companion:

- What tasks is it meant to perform?
- Who uses it?
- What limitations or safety boundaries must be respected?

**Example:**

> This repository defines the workspace for “Athena,”
> a structured AI observer that supports semantic analysis tasks.

---

## 3. Recommended Folder Structure

```text
/README.md
/CONFIG/
    system-prompts.md
    policies.md
    parameters.md
/LOGS/
    session-001.md
    session-002.md
/EVAL/
    test-scenarios.md
    evaluation-notes.md
/PLAYBOOKS/
    onboarding.md
    troubleshooting.md


---

4. System Prompt Template

This goes inside: CONFIG/system-prompts.md

# System Prompt – <companion-name>

## Core Behavior
- Define personality and style.
- Define allowed and expected behavior.
- Define tone of voice.

## Stable Behavior Rules
- Must remain consistent across sessions.
- Must avoid contradictions.
- Must preserve user meaning.

## Forbidden Behavior
- Must not bypass safety limits.
- Must not generate harmful content.
- Must not produce unverified claims.


---

5. Policies Template

For CONFIG/policies.md:

# Policies – <companion-name>

## Data Handling
- How logs or transcripts are stored.

## Privacy Expectations
- What information is protected.

## Red Lines (Forbidden Behavior)
- Disallowed topics or actions.

## Update Procedure
- How configuration changes are approved.


---

6. Evaluation Template

Inside /EVAL/evaluation-notes.md:

# Evaluation Notes – <companion-name>

## Scenario Tested
Describe the test situation.

## Observations
- Behavior 1
- Behavior 2

## Improvements Needed
- Adjustment 1
- Adjustment 2


---

7. Playbooks Template

Inside /PLAYBOOKS/onboarding.md:

# Onboarding Guide

## Initial Setup
How to initialize the companion.

## Usage Instructions
How users interact with it.

## Troubleshooting
Common problems and solutions.


---

8. Definition of Done

The AI companion workspace is considered “ready” when:

[ ] Repository structure created

[ ] CONFIG folder has prompts + policies

[ ] At least one LOGS entry added

[ ] Evaluation notes exist

[ ] Playbooks folder created


---
