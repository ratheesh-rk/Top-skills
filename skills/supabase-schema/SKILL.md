---
name: supabase-schema
description: Design Supabase Postgres tables, relations, indexes and Row Level Security policies for an app. Use when planning a database, adding tables, or writing RLS policies.
---
# Supabase Schema

## Ask first (only if missing)
- What the app does and the main things it stores
- User roles (admin, staff, customer...)
- Single business or multi-tenant (many businesses in one app)

## Steps
1. List entities and how they relate (one-to-many, many-to-many).
2. Write tables:
   - `id uuid primary key default gen_random_uuid()`
   - `created_at timestamptz default now()`
   - foreign keys with `on delete` rules
   - `org_id` on every table if multi-tenant
3. Add indexes on foreign keys and columns used in filters.
4. Enable RLS on every table and write policies per role.
5. Add helpful views or functions if queries repeat.

## Output
- A simple diagram (text or mermaid) of tables
- Full SQL migration
- RLS policies with a one-line explanation each
- Example queries for the main screens

## Rules
- RLS on, always. No table left open.
- Use `auth.uid()` in policies.
- Money as `numeric(12,2)`, never float.
- Status fields as text with a check constraint (or enum).
