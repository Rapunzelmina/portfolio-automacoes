# Receiving and finance app (PWA)

> **Area:** Finance & store operations · **Status:** In production

## Problem

Stores received invoices and payment slips on paper, WhatsApp and e-mail, with no single record. Payment approval, payment batches, bank reconciliation and target tracking lived in separate spreadsheets.

## Solution

An installable phone app in one place, with per-user login and access roles. In the store: scanning the invoice barcode (44-digit key) and photographing the invoice and payment slip. For finance: an approval queue with routing rules, a payment batch, **treasury** (imports the bank statement in OFX and reconciles it against what the ERP marked as paid, separating what matched, what is only in the bank and what is only in the ERP) and a **targets dashboard** with three views: cycles per store, a panel with ranking, category mix, year-over-year comparison and attention points, and a projection tab only for management, where monthly targets per store and category are entered and **flow back to the sales robot**, which writes them into the spreadsheets and PDFs.

## Tech

- HTML, CSS e JavaScript puro (PWA)
- Supabase (Auth, PostgreSQL, Storage, row level security)
- zxing-wasm (código de barras)
- PDF.js e SheetJS
- Vercel

## Result

A single record of invoices, approval with history, bank reconciliation and targets on the phone, with each person seeing only what their role allows.

## What I did

I designed the screens and roles from the real routine of the stores and finance, and researched and implemented barcode scanning, OFX statement import for reconciliation and the targets dashboard, closing the loop between the app and the sales robot.

---
*Source code is private: it contains integrations and information from the corporate environment. See the privacy note in the [main README](../README.en.md).*
