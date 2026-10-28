---
name: simple-code-review
description: Review code for bugs, security issues, messy parts and simple improvements before shipping. Use when asked to review, check or clean up code.
---
# Simple Code Review

## What to check
1. **Bugs** - wrong logic, missing null checks, async mistakes, off-by-one
2. **Security** - exposed keys, missing auth checks, unvalidated input, SQL/XSS risk
3. **Errors** - what happens when the API fails or data is empty
4. **Readability** - unclear names, huge functions, repeated code
5. **Performance** - obvious waste only (loops of DB calls, huge re-renders)

## Output
| Severity | File / line | Issue | Fix |
|----------|-------------|-------|-----|
Severity: Must fix / Should fix / Nice to have.

Then: **Good things** (1-2 lines) and **Overall**: ship / fix first.

## Rules
- Must-fix items first.
- Show the fixed code for anything Must fix.
- Don't nitpick formatting if a formatter exists.
- Explain in plain words; no lectures.
