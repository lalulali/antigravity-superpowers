---
name: writing-requirements
description: Use this to gather detailed requirements, refine user stories, and define acceptance criteria (using Gherkin) before creating an implementation plan. Optional but recommended for complex features.
---
# Writing Requirements

## Overview

Gather and document detailed requirements into a single **Requirements Document**. Take input from a **Brainstorming Design Doc** OR directly from **user requirements**. 

Document everything clearly with **Glossaries**, rigid **User Stories**, and **Gherkin-style Acceptance Criteria**.

Assume the executing engineer needs absolute clarity and detailed scope.

**Announce at start:** "I'm using the writing-requirements skill to document detailed requirements."

**Save documents to:** `docs/plans/<order-number>-<feature-name>/requirements.md`

## The Process

### Step 1: Gather Information
1. Read the existing design doc (if brainstorming was performed) or parse the user's direct prompt.
2. Identify core features, constraints, and gaps in information.
3. Ask clarifying questions one at a time if details are missing.

### Step 2: Create Requirements Document
Write the output file following this rigid template:

````markdown
# [Feature Name] - Requirements Document

## Introduction
[High level introduction of the requirement]

## Glossary
- **[Term]**: [Definition/Description]

## Requirements

### Requirement 1: [Requirement Title]

**User Story:**
As a [user type], I want to [action] so that [benefit].

#### Acceptance criteria
```gherkin
Scenario: [Scenario Title]
    Given [Precondition]
    When [Action]
    Then [Postcondition]
```
````

### Step 3: Transition to Plan
- Invoke `.agent/skills/writing-plans/SKILL.md` to create an implementation plan using this document as the source of truth.

---

## Key Principles

- **Detailed and Complete:** The requirement should be as complete as possible and as detailed as possible. 
- **Gherkin format:** Use strict `Given`, `When`, `Then` syntax for all acceptance criteria.
- **No Vague Terms:** Ensure all ambiguous terms are added to the **Glossary**.
