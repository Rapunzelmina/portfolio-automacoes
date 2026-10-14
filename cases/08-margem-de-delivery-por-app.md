# Delivery margin per app

> **Area:** Sales & delivery · **Status:** Evolving · dashboard rebuilt, automation and coupons pending

## Problem

There was visibility of revenue and units sold per delivery app, but not of cost, so nobody knew each channel's real margin.

## Solution

A pipeline reads two ERP reports per store and per month (sales by product and average cost), crosses them by product code and store, counts only the delivery apps, validates the total against the sales robot's and flags anomalies (very low unit price, very high quantity). It writes total cost, average cost per unit, cost percentage and margin into each store tab without changing cell addresses, so the sales robot keeps writing in the same places. The dashboard was rebuilt using formulas only, with no hard-coded values: store selector, KPIs, monthly evolution, performance per app, a store comparison with ranking and formula-generated highlights, with conditional formatting and native charts.

## Tech

- Python
- pandas
- OpenPyXL
- pdfplumber
- Excel (fórmulas, formatação condicional, gráficos de barras, linhas e rosca)

## Result

It became possible to see each channel's margin trend, which was invisible before. After management's feedback on the dashboard, the layout was rebuilt; the calculation rules stayed. Still to do: unify everything in a single routine, automate the report extraction and include coupons and discounts.

## What I did

I validated the real structure of each ERP report (layout, columns and special cases) before crossing sales and cost, and wrote a brief with the rules, the checkpoints and what must not change so I could work with the AI safely. I rebuilt the dashboard after management's feedback without touching the addresses the robot uses.

---
*Source code is private: it contains integrations and information from the corporate environment. See the privacy note in the [main README](../README.en.md).*
