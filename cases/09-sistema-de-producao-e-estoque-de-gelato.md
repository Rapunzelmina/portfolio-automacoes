# Gelato production and stock control system (IRIS)

> **Area:** Operations & control · **Status:** In operation and expanding

## Problem

Store orders to the central kitchen, production, gelato weighing and delivery container filling were tracked in separate spreadsheets. There was no record of who weighed what, nor a comparison between what was produced, what left and what was lost.

## Solution

A web app you can install, with five access roles (administrator, store, pastry chef, gelato maker and team lead). **Ordering:** each store gets a calculated suggestion of how many BAGs to order and records what was sent, with a reason when the quantity changes. **Production:** the kitchen records quantity, weight and a photo of the scale. **Gelato lab:** weighing of tubs with a photo, double-checking by a second person (whoever records a weighing does not verify their own), tolerances, tare, tasting loss and waste with a reason, producing a production map by flavour and by store, with a ranking and incidents for the control team. The month's map is also exported to a formatted Excel file, with a dashboard and charts, a heat map by flavour, a weekly ranking and one sheet per day with the calculations as formulas. **Delivery:** compares the gelato used with the containers filled and the target weight of each size. **Team and shifts:** PIN-based access with lockout after wrong attempts. There is also a monthly menu, a purchasing and stock view, and importers that bring ERP reports and spreadsheets into the database, with a scheduled daily sync.

## Tech

- JavaScript puro (módulos ES) e PWA, publicado na Vercel
- Supabase: PostgreSQL, Auth, Storage, funções e triggers, row level security (11 migrações)
- Python: importadores de relatórios e planilhas, sincronização diária agendada
- Playwright: robô que baixa relatórios do ERP
- Protótipo inicial em FastAPI + SQLite

## Result

In a few weeks the scope went from ordering and production of a single product to an operations control system, with over 11,000 lines of code and 11 database migrations, and the daily sync already runs on a schedule. Recipe costing, automatic ingredient deduction and automatic replenishment are still under study.

## What I did

I learned the routine of the kitchen and the stores (ordering, production, gelato weighing and delivery filling) and turned it into rules and screens. I designed the roles and permissions inside the database, built the importers that bring in ERP reports and spreadsheets, and kept what already works separate from what is still being studied.

---
*Source code is private: it contains integrations and information from the corporate environment. See the privacy note in the [main README](../README.en.md).*
