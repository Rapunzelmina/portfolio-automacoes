# Receiving and finance app (PWA)

> **Area:** Finance & store operations · **Status:** In production

## Problem

Stores received invoices and payment slips on paper, WhatsApp and e-mail, with no single record. Payment approval, payment batches, bank reconciliation and target tracking lived in separate spreadsheets.

## Solution

An installable phone app in one place, with per-user login and access roles. In the store: scanning the invoice barcode (44-digit key) and photographing the invoice and payment slip. For finance: an approval queue with routing rules, a payment batch, **treasury** (imports the bank statement in OFX and reconciles it against what the ERP marked as paid, separating what matched, what is only in the bank and what is only in the ERP) and a **targets dashboard** (each store sees its target, management enters new ones).

## Tech

- HTML, CSS e JavaScript puro (PWA)
- Supabase (Auth, PostgreSQL, Storage, row level security)
- zxing-wasm (código de barras)
- PDF.js e SheetJS
- Vercel

## Result

A single record of invoices, approval with history, bank reconciliation and targets on the phone, with each person seeing only what their role allows.

## My role

Understanding the real process, defining the business rules, development, testing, failure handling and reliability tuning.

---
*Source code is private: it contains integrations and information from the corporate environment. See the privacy note in the [main README](../README.en.md).*
