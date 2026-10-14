# Monthly tax reports for accounting

> **Area:** Accounting & tax · **Status:** In production · runs unattended on the first business day

## Problem

At the start of every month someone had to log into the ERP, generate each store's fiscal receipts report and hand organised files to accounting.

## Solution

A bot detects the first business day of the month, generates the previous month's report for every unit and saves each file in the right folder with a standard name, in accounting's cloud drive. It logs every step and sends a phone notification.

## Tech

- Python
- Playwright
- Requests
- Windows Task Scheduler
- Notificações push

## Result

A monthly routine that no longer depends on anyone remembering it, with consistent names and folders.

## My role

Understanding the real process, defining the business rules, development, testing, failure handling and reliability tuning.

---
*Source code is private: it contains integrations and information from the corporate environment. See the privacy note in the [main README](../README.en.md).*
