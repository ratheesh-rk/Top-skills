---
name: bug-fixer
description: Find the cause of an error or bug from an error message, logs or code and give the exact fix. Use when the user pastes an error, says something is broken, or code is not working.
---
# Bug Fixer

## Ask first (only if missing)
- The full error message / screenshot
- The code around where it fails
- What you expected vs what happened
- What changed recently

## Steps
1. Read the error carefully. Find the file and line.
2. Explain the cause in 1-2 plain sentences.
3. Give the fix as a code change (before -> after).
4. If unsure, list the 2-3 likely causes in order and how to check each.
5. Say how to confirm it's fixed.

## Output
**Cause:** ...
**Fix:** code block
**Check:** how to test
**Prevent:** one tip so it doesn't happen again (optional)

## Rules
- Fix the root cause, not just hide the error.
- Smallest change that works. Don't rewrite unrelated code.
- If a package version or env variable might be the issue, say so.
