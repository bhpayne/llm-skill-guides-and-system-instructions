---
name: sourcecode-review-gaps
description: Analyzes sourcecode to identify logic gaps, security flaws, architectural inconsistencies, and areas of improvement. Use when asked to review, audit, check, or find gaps in sourcecode files.
---

Use this skill to systematically analyze files, pull requests, or code snippets to find bugs, security concerns, architectural violations, and logic gaps.

## Trigger Criteria
Activate this skill when the user asks you to:
- "Review this software" or "Audit this code"
- "Identify gaps in my implementation"
- "Check if this PR is ready"
- "Analyze this folder for architectural consistency"

## Evaluation Workflow

When performing a review, follow these steps in order:

1. **Understand Context**: Read the entire file and identify its language, framework, and architectural patterns.
2. **Scan for Core Issues**:
   - **Security**: Look for hardcoded secrets, SQL injection risks, unsafe deserialization, or missing authorization checks.
   - **Performance**: Identify redundant loops, missing database indexes, unoptimized queries, or unnecessary re-renders.
   - **Logic & Edge Cases**: Check for unhandled null/undefined values, unhandled promise rejections, or missing try-catch blocks.
   - **Architectural Gaps**: Check if the file misses required patterns (e.g., missing error boundaries, lack of input validation, or failure to follow separation of concerns).
3. **Formulate constructive recommendations**: Focus on specific, actionable code changes.


### If Applicable create a Refactored Snippet
*Provide a concise rewrite of the most critical sections, clearly highlighting what was changed and why.*

## Constraints & Guardrails
- **No Style Nitpicking**: Do not mention linting, spacing, or semi-colon style choices unless explicitly asked. Assume standard formatters (like Prettier/ESLint) handle this.
- **Keep Code Contextual**: When providing refactored snippets, only show the modified portions rather than rewriting a large file.


