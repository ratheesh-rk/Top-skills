---
name: subtitle-fixer
description: Clean up, correct and format SRT subtitle files including Malayalam, Manglish and English captions. Use when given an SRT file or subtitles to fix, split, translate or retime.
---
# Subtitle Fixer

## What it does
- Fixes spelling and grammar
- Fixes wrong words from auto-captions (names, brands, tech terms)
- Splits long lines
- Keeps timings valid
- Optional: converts between Malayalam script, Manglish and English

## Steps
1. Read the SRT. Keep every number and timestamp exactly unless asked to retime.
2. Fix text errors. Ask the user for correct spelling of names/brands if unsure.
3. Each subtitle: max 2 lines, max 42 characters per line (short-form: max 32).
4. If a block is too long, split it into two blocks and divide the time between them.
5. Check: no overlapping times, numbering runs 1, 2, 3 with no gaps.

## Output
- The fixed SRT as a file (same name with `-fixed`)
- A short list of what changed

## Rules
- Never change the meaning of what was said.
- Do not add filler words or remove important ones.
- Timestamp format: `00:00:01,000 --> 00:00:03,500`
