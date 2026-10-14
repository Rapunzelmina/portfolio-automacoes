# Goods-receipt invoices with AI assistance

> **Area:** Purchasing & inventory · **Status:** In use · assisted (a person reviews and saves)

## Problem

For every goods invoice received, the receipt had to be acknowledged in the tax system and entered manually in the ERP, converting each item to the stock unit.

## Solution

Stores scan the invoice key from their phones; the bot picks up the queue, acknowledges receipt, opens goods entry, imports the e-invoice and fills the fields. Quantity conversion follows an order: previously learned conversions, then text rules and only last the Claude API (AI). The bot respects the tax authority's hourly query limit and **stops before saving** so a human can review. At the end it prominently lists which invoices have not yet appeared in the ERP, making clear it is not a bot failure and that it just needs to run again later.

## Tech

- Python
- Playwright
- PostgreSQL / Supabase
- API da Anthropic (Claude) para inferir conversões de unidade
- Expressões regulares

## Result

Less typing and fewer unit errors, with the final decision always in a person's hands.

## What I did

I found out the tax authority's rules, such as the hourly query limit, and designed the conversion order (learned table, rules, AI last), guiding the AI with precise instructions and always leaving a person with the final decision. I also diagnosed live a bug in how selected rows were counted on the ERP screen (the header's "select all" box counted as a ticked row and blocked legitimate invoices) and fixed it.

---
*Source code is private: it contains integrations and information from the corporate environment. See the privacy note in the [main README](../README.en.md).*
