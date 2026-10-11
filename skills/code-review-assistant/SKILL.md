---
name: code-review-assistant
description: Review project code, scripts, configuration, or documentation changes for correctness, clarity, maintainability, and obvious risks before merge.
---

# Code Review Assistant Skill

## Purpose
Review project code, scripts, configuration, or Markdown-based automation files for correctness, clarity, maintainability, and obvious risks.

## Use This Skill When
- A feature branch needs review before merge.
- A student wants feedback on code quality.
- Configuration or automation files need a sanity check.
- A change may introduce bugs, confusing logic, or maintainability issues.

## Inputs
- The changed file or diff.
- The purpose of the change.
- Any project rules from `knowledge.md`, `AGENTS.md`, or `CLAUDE.md`.

## Procedure
1. Read the project instructions first.
2. Understand what the change is supposed to accomplish.
3. Check for syntax or structural problems.
4. Look for logic errors, edge cases, duplicated work, and unclear naming.
5. Identify unnecessary complexity or unsafe operations.
6. Check for accidentally exposed secrets or credentials.
7. Separate required fixes from optional improvements.
8. Give concise recommendations with file or section references when possible.

## Review Categories
- Correctness
- Readability
- Maintainability
- Security and privacy
- Consistency with project instructions
- Git and deployment safety

## Output Format
### Summary
One short paragraph describing overall quality.

### Required Fixes
Only issues that should be corrected before merge.

### Suggested Improvements
Non-blocking improvements.

### Verdict
Use one of: `Ready`, `Ready with minor changes`, or `Needs revision`.

## Example Request
"Review the changes on my feature branch before I merge them into main."
