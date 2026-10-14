# Accounts payable: from extraction to approval and payment batch

> **Area:** Finance · **Status:** In production · runs unattended every day

## Problem

Accounts payable lived inside the ERP, with no clear approval queue and no consolidated view of what to pay and when.

## Solution

Every day a bot extracts accounts payable (a 90-days-back, 90-days-ahead window) and writes them to a PostgreSQL database without duplicating records. On top of that data I built the approval queue, supplier-based routing rules, automatic categories for new suppliers and the payment batch, all with role-based access enforced in the database itself (row level security).

## Tech

- Python
- Playwright
- PostgreSQL / Supabase (REST, triggers, RLS)
- SQL
- Windows Task Scheduler

## Result

What used to be a list inside the ERP became a workflow with approver, history and payment batch, refreshed every day with no intervention.

## What I did

I worked out how payments were actually approved and turned that flow into tables, routing rules and per-role permissions inside the database, researching how to apply row-level security (RLS) and triggers.

---
*Source code is private: it contains integrations and information from the corporate environment. See the privacy note in the [main README](../README.en.md).*
