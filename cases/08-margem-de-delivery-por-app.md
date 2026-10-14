# Delivery margin per app

> **Area:** Sales & delivery · **Status:** Evolving · concept under review with management

## Problem

There was visibility of revenue and units sold per delivery app, but not of cost, so nobody knew each channel's real margin.

## Solution

Automatic cross-reference between sales by product and each product's average cost (by product code, not name), computing total cost, cost percentage and margin per app, per store and per month. The result lands in the spreadsheet management already used, with colour formatting and an interactive dashboard (store selector, KPIs and trend charts) built only with native Excel features.

## Tech

- Python
- pandas
- Excel (fórmulas, formatação condicional, gráficos)

## Result

It became possible to see each channel's margin trend, which was invisible before. The concept is still being refined with management.

## What I did

I validated the real structure of each ERP report (layout, columns and special cases) before cross-referencing sales and cost by product code, and handled the cases where a sold product has no cost posted that month.

---
*Source code is private: it contains integrations and information from the corporate environment. See the privacy note in the [main README](../README.en.md).*
