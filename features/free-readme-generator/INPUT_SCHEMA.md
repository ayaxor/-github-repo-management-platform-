
# Input Schema — README Auto-Generator

This document defines the **input fields** required to generate
a structured README file using the Free README Auto-Generator.

The schema is designed to be simple, minimal, and device-independent.

---

## Required Inputs

### 1. Project Name
- Type: Text
- Description: The name of the repository or project.
- Example: `wirelight-platform`

---

### 2. Project Type
- Type: Enum
- Allowed Values:
  - AI
  - Security
  - Documentation
  - Platform
  - Library
  - Other
- Description: Determines the base README structure.

---

### 3. Short Description
- Type: Text
- Description: One or two sentences describing the project.
- Example: `An ADR-first documentation platform for multi-agent systems.`

---

## Optional Inputs

### 4. Features List
- Type: List of text items
- Description: Key features or capabilities.
- Example:
  - ADR-first architecture
  - Multi-tenant support
  - Observability by design

---

### 5. Installation Instructions
- Type: Text block
- Description: Basic setup or installation steps.
- Example: `npm install` or `pip install package-name`

---

### 6. Usage Example
- Type: Text block
- Description: Basic usage or example commands.

---

### 7. License
- Type: Enum
- Allowed Values:
  - MIT
  - Apache-2.0
  - GPL-3.0
  - None
- Default: MIT

---

## Validation Rules

- Project Name MUST NOT be empty.
- Project Type MUST be one of the allowed values.
- Description SHOULD be concise (max 300 characters).
- Optional fields MAY be omitted.

---

## Output Guarantee

Given valid inputs, the generator MUST produce:
- A valid Markdown README
- A consistent section order
- No empty placeholder sections

