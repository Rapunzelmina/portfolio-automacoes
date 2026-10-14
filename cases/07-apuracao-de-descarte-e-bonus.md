# Waste tracking and team bonus

> **Area:** Operations & control · **Status:** In production · runs at month close

## Problem

Measuring product loss per store, comparing it to sales and computing each team's bonus meant gathering dozens of spreadsheets and PDFs and applying the rules by hand every month.

## Solution

A pipeline copies the files from the month's cloud folder, reads the stock reports and the weekly controls (waffle batter, in-house production, coffee, cake and gelato sold vs used), consolidates waste, compares it with sales, applies the bonus rules and produces the consolidated spreadsheet and print-ready PDFs, store by store. A scheduled task checks the calendar and only runs on the right closing day, and every run ends with a summary and a diagnostic checklist: missing files and out-of-curve values become visible instead of going unnoticed. The bonus rules (a sales target as the gate, points per category and an adjustment by waste band) are documented, and I prepared decision documents for management comparing alternative rules.

## Tech

- Python
- pandas
- OpenPyXL
- pdfplumber
- Geração de PDFs e documentos Word
- Windows Task Scheduler

## Result

A reproducible monthly close, with the rules documented in code and the same numbers for every store. The latest close ran with warnings about missing files, which the summary itself pointed out and which were completed the same morning. The bonus rule is being validated with management.

## What I did

I gathered the bonus rules with management, turned them into code and documented where every number comes from so anyone can check the result. When the rule had to be decided, I prepared documents comparing the alternatives for management, and made each close's summary point out what was missing.

---
*Source code is private: it contains integrations and information from the corporate environment. See the privacy note in the [main README](../README.en.md).*
