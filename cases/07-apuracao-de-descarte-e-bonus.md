# Waste tracking and team bonus

> **Area:** Operations & control · **Status:** In production · runs at month close

## Problem

Measuring product loss per store, comparing it to sales and computing each team's bonus meant gathering dozens of spreadsheets and PDFs and applying the rules by hand every month.

## Solution

A pipeline reads each store's stock and target reports, consolidates waste, compares it with sales, applies the bonus rules (targets met and improvement in the loss rate) and produces the consolidated spreadsheet and print-ready PDFs, store by store. A scheduled task checks the calendar and only runs on the right closing day.

## Tech

- Python
- pandas
- OpenPyXL
- pdfplumber
- Geração de PDFs
- Windows Task Scheduler

## Result

A reproducible monthly close, with the rules documented in code and the same numbers for every store.

## What I did

I gathered the bonus rules with management (targets met and improvement in the loss rate), turned them into code and documented where every number comes from so anyone can check the result.

---
*Source code is private: it contains integrations and information from the corporate environment. See the privacy note in the [main README](../README.en.md).*
