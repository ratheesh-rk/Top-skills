---
name: nextjs-supabase-feature
description: Add a feature to a Next.js App Router plus Supabase app, covering database, API or server actions, UI and auth. Use when building CRM, dashboard or SaaS features with Next.js and Supabase.
---
# Next.js + Supabase Feature

Add one feature end to end, the clean way.

## Ask first (only if missing)
- What the feature does (user story)
- Which tables already exist
- Who can use it (roles)
- Existing folder structure or a sample file

## Steps
1. **Data** - tables/columns needed. Write the SQL migration.
2. **Security** - RLS policies for each role. Never skip.
3. **Server** - server actions or route handlers. Validate input (zod).
4. **UI** - page/components. Loading, empty and error states.
5. **Types** - TypeScript types matching the table.
6. **Test** - list manual steps to verify it works.

## Output
- File list with path for each file
- Full code for each file
- SQL to run in Supabase
- Any env variables needed

## Rules
- App Router, TypeScript, server components by default; `"use client"` only where needed.
- Use `@supabase/ssr` for auth in server code.
- Never put the service role key in client code.
- Keep each file focused; no 500-line components.
