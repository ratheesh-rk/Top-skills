---
name: scroll-motion
description: Build scroll-triggered animation sections for websites using GSAP ScrollTrigger or CSS such as reveal, pin, parallax, horizontal scroll and image sequences. Use when asked for scroll animations, motion website, or Apple-style scroll effects.
---
# Scroll Motion

Add smooth scroll-based animation that feels premium, not distracting.

## Ask first (only if missing)
- Which section(s) and what should move
- Feel: subtle, bold, or product-showcase
- Plain HTML or React/Next.js

## Effects menu
- **Fade/slide reveal** - elements appear as you scroll
- **Stagger** - cards come in one by one
- **Pin + steps** - section sticks while content changes (great for "how it works")
- **Parallax** - background moves slower than foreground
- **Horizontal scroll** - cards move sideways while scrolling down
- **Image sequence** - product rotates/opens frame by frame on scroll
- **Number counter** - stats count up when visible

## Tech
- GSAP + ScrollTrigger from cdnjs for complex effects.
- CSS + IntersectionObserver for simple reveals (no library).
- For React: use `useEffect` / `useGSAP` and clean up on unmount.

## Rules
- Animate `transform` and `opacity` only (smooth on phones).
- Respect `prefers-reduced-motion`: turn effects off for those users.
- Content must still be readable if JavaScript fails.
- Lighter effects on mobile; skip heavy pinning under 768px if it feels janky.
