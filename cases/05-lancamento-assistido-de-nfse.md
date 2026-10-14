# Assisted posting of service invoices

> **Area:** Finance · **Status:** In use · assisted (a person reviews and saves)

## Problem

Service invoices arrive as photos or PDFs and had to be read and typed into the ERP's accounts payable, choosing supplier and ledger account.

## Solution

The bot fetches pending invoices, opens the invoice and payment-slip images, extracts data with OCR (date, provider, number, amount and barcode), suggests supplier and ledger account and leaves the ERP form pre-filled. A person reviews and saves. Once posted, the invoice is flagged and the supplier is remembered for next time.

## Tech

- Python
- Playwright
- OCR via Google Drive/Docs API
- PostgreSQL / Supabase (REST)

## Result

Typing was reduced to reviewing and saving, and the system improves with every invoice because it learns suppliers.

## What I did

I mapped how a service invoice is posted in accounts payable, defined which fields the OCR must extract and how the system remembers suppliers and ledger accounts to improve with each invoice.

---
*Source code is private: it contains integrations and information from the corporate environment. See the privacy note in the [main README](../README.en.md).*
