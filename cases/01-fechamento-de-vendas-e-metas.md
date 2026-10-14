# Weekly sales close and targets

> **Area:** Sales & targets · **Status:** In production · runs unattended every day

## Problem

Sales-versus-target tracking, store by store, was manual: download ERP reports, total by category, update spreadsheets and build PDFs for management and for each store. Each close could take a full working week.

## Solution

A bot logs into the ERP on its own, downloads each store's sales report, totals by category, updates the target spreadsheets and produces the PDFs (one for management, one per store). It rolls the month over automatically, sends a phone notification when done and creates a calendar event for approval. More recently it also pushes the same numbers to a cloud database that feeds a targets dashboard, and a one-off history load was added to populate it.

## Tech

- Python
- Playwright
- OpenPyXL / Excel
- LibreOffice (PDF)
- Google Calendar API
- PostgreSQL via API REST
- Windows Task Scheduler

## Result

A process that could take a full working week now runs automatically in about 5 minutes. See also the [original public case](https://github.com/Rapunzelmina/Sales-Closing-Automation).

## What I did

I identified the bottleneck in the weekly sales reports and inspected the ERP screens (buttons, filters and the path to each report) to work out how to automate a system with no API. I turned the closing rules (categories, checkpoints, month rollover) into code and tested with real numbers before letting it run unattended.

---
*Source code is private: it contains integrations and information from the corporate environment. See the privacy note in the [main README](../README.en.md).*
