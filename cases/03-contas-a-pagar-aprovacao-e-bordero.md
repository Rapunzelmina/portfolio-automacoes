# Accounts payable: from extraction to approval and payment batch

> **Area:** Finance · **Status:** In production

## Problem

Accounts payable lived inside the ERP, with no clear approval queue and no consolidated view of what to pay and when.

## Solution

A scheduled bot extracts accounts payable (a 90-days-back, 90-days-ahead window) and writes them to a PostgreSQL database without duplicating records. After exporting, it checks that every expected unit is in the file, because a partial file once reached the database unnoticed. On top of that data I built the approval queue, supplier-based routing rules, automatic categories for new suppliers and the payment batch, all with role-based access enforced in the database itself (row level security).

## Tech

- Python
- Playwright
- PostgreSQL / Supabase (REST, triggers, RLS)
- SQL
- Windows Task Scheduler

## Result

What used to be a list inside the ERP became a workflow with approver, history and payment batch, refreshed every day with no intervention.

## What I did

I worked out how payments were actually approved and turned that flow into tables, routing rules and per-role permissions inside the database, researching how to apply row-level security (RLS) and triggers. When I found that the exported file could arrive incomplete, I added a coverage check before upload.

---
*Source code is private: it contains integrations and information from the corporate environment. See the privacy note in the [main README](../README.en.md).*
