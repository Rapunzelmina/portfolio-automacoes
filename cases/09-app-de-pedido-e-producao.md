# Ordering and production app

> **Area:** Operations & control · **Status:** In development · ordering and production in testing

## Problem

Ordering of supplies and recording of what was produced in the kitchen had no single flow, and nothing linked production to stock.

## Solution

An app with three roles (administrator, store and pastry chef). The store places the order; the chef records production with quantity, kilos and a photo of the scale. The full design covers purchasing, replenishment, automatic stock deduction and posting production to the ERP by an agent; those steps are still being studied.

## Tech

- Python (FastAPI) e SQLite no protótipo local
- JavaScript + Supabase no front-end publicado
- PWA
- Vercel / PythonAnywhere

## Result

Ordering and production already work in testing; purchasing, stock and ERP integration are the next steps.

## My role

Understanding the real process, defining the business rules, development, testing, failure handling and reliability tuning.

---
*Source code is private: it contains integrations and information from the corporate environment. See the privacy note in the [main README](../README.en.md).*
