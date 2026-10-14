# Goods-receipt invoices with AI assistance

> **Area:** Purchasing & inventory · **Status:** In use · assisted (a person reviews and saves)

## Problem

For every goods invoice received, the receipt had to be acknowledged in the tax system and entered manually in the ERP, converting each item to the stock unit.

## Solution

Stores scan the invoice key from their phones; the bot picks up the queue, acknowledges receipt, opens goods entry, imports the e-invoice and fills the fields. Quantity conversion follows an order: previously learned conversions, then text rules and only last the Claude API (AI). The bot respects the tax authority's hourly query limit and **stops before saving** so a human can review.

## Tech

- Python
- Playwright
- PostgreSQL / Supabase
- API da Anthropic (Claude) para inferir conversões de unidade
- Expressões regulares

## Result

Less typing and fewer unit errors, with the final decision always in a person's hands.

## My role

Understanding the real process, defining the business rules, development, testing, failure handling and reliability tuning.

---
*Source code is private: it contains integrations and information from the corporate environment. See the privacy note in the [main README](../README.en.md).*
