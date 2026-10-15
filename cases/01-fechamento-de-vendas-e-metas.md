# Weekly sales close and targets

> **Area:** Sales & targets · **Status:** In production · runs unattended on the weekly closes

## Problem

Sales-versus-target tracking, store by store, was manual: download ERP reports, total by category, update spreadsheets and build PDFs for management and for each store. Each closing cycle could take almost a full working day, and a month has up to five cycles.

## Solution

A bot logs into the ERP on its own, downloads each store's sales report, totals by category, updates the target spreadsheets and produces the PDFs (one for management, one per store). It rolls the month over automatically, sends a phone notification when done and creates a calendar event for approval. More recently it also pushes the same numbers to a cloud database that feeds a targets dashboard, and a one-off history load was added to populate it. To be reliable, the bot retries on its own a store that fails right after login (common when the ERP returns an error page), protects the month rollover (a unit that did not close the month is left out and the team gets a high-priority alert, instead of inheriting an incomplete month), produces a full PDF in the last cycle of the month, reads back the targets typed in the company's app to write them into the spreadsheets and PDFs, and the scheduled task wakes the computer and runs on resume when the time slot is missed.

## Tech

- Python
- Playwright
- OpenPyXL / Excel
- LibreOffice (PDF)
- Google Calendar API
- PostgreSQL via API REST
- Windows Task Scheduler

## Result

What took almost a full working day per cycle (about a week per month) now runs automatically in up to 5 minutes per cycle. See also the [original public case](https://github.com/Rapunzelmina/Sales-Closing-Automation).

## What I did

I identified the bottleneck in the weekly sales reports and inspected the ERP screens (buttons, filters and the path to each report) to work out how to automate a system with no API. I turned the closing rules (categories, checkpoints, month rollover) into code and tested with real numbers before letting it run unattended. Later, reading the logs, I investigated a recurring failure (a unit that errored on the ERP's first load), built the automatic retry and the month-rollover protection, and tuned the Windows scheduler so the task does not lose the day when the computer sleeps.

---
*Source code is private: it contains integrations and information from the corporate environment. See the privacy note in the [main README](../README.en.md).*
