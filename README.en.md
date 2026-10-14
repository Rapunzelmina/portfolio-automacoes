# Projects, automation and process improvement

**Project and automation analyst.** I map the process, find the bottleneck, build the solution (robot, app or AI) and follow it until it runs in production.

*Process improvement · Automation (RPA) · Applied AI · Robots · Project management*

[Versão em português](README.md)

At a food-service retail chain I worked across several areas of the company and, in each one, found where the manual work was and built the solution. That is 9 projects with one common thread: **understand the real process, turn the rules into code and always leave the final decision to a person.**

## Highlights

- **From up to a week of work to about 5 minutes** in the weekly sales and targets close.
- **9 projects across 6 areas of the company:** finance, accounting, sales and targets, purchasing and inventory, operations and control, and delivery.
- **6 scheduled routines** on Windows running without anyone pressing a button.
- **A production and stock system with over 11,000 lines of code**, built in a few weeks and already in operation.
- **Responsible applied AI:** always after the rules and always with human review before anything is saved.
- **Role-based security inside the database** (row level security) in three systems.

## Projects

| Area | Project | Type | Status |
|---|---|---|---|
| Sales & targets | [Weekly sales close and targets](cases/01-fechamento-de-vendas-e-metas.md) | Robot (RPA) | In production |
| Accounting & tax | [Monthly tax reports for accounting](cases/02-relatorios-fiscais-mensais.md) | Robot (RPA) | In production |
| Finance | [Accounts payable: from extraction to approval and payment batch](cases/03-contas-a-pagar-aprovacao-e-bordero.md) | Robot + database | In production |
| Purchasing & inventory | [Goods-receipt invoices with AI assistance](cases/04-entrada-de-nfe-com-ia.md) | Robot + AI | In use |
| Finance | [Assisted posting of service invoices](cases/05-lancamento-assistido-de-nfse.md) | Robot + AI | In use |
| Finance & store operations | [Receiving and finance app (PWA)](cases/06-app-de-recebimento-e-financeiro.md) | App | In production |
| Operations & control | [Waste tracking and team bonus](cases/07-apuracao-de-descarte-e-bonus.md) | Data and reporting | In production |
| Sales & delivery | [Delivery margin per app](cases/08-margem-de-delivery-por-app.md) | Data and reporting | Evolving |
| Operations & control | [Gelato production and stock control system (IRIS)](cases/09-sistema-de-producao-e-estoque-de-gelato.md) | App + robots | In operation and expanding |

## Cases in their own repository

The most complete projects also have a repository of their own, with a diagram:

- [AI-assisted invoice entry](https://github.com/Rapunzelmina/AI-Assisted-Invoice-Entry): rules first, AI last, a person always decides
- [Receiving and finance app](https://github.com/Rapunzelmina/Receiving-Finance-PWA): approval, treasury (OFX reconciliation) and targets dashboard
- [Accounts payable, approval and payment batch](https://github.com/Rapunzelmina/Accounts-Payable-Approval-Workflow): from the ERP to the approval workflow, with role-based security in the database
- [Sales close automation](https://github.com/Rapunzelmina/Sales-Closing-Automation): from up to a week to about 5 minutes

## Process improvement: before and after

| Process | Before | After |
|---|---|---|
| Sales and targets close | Manual, could take a week | Automatic, about 5 minutes |
| Tax reports | Generated store by store, by hand | Generated and filed on their own on the first business day |
| Payment approval | A list inside the ERP | Approval queue with history and payment batch |
| Goods invoice entry | Typing and unit conversion by hand | Assisted, with AI only as a last resort and human review |
| Service invoices | Reading and typing | OCR with a pre-filled form and human review |
| Bank reconciliation | Statement and payments in separate spreadsheets | Statement import and automatic reconciliation |
| Waste and bonus | Dozens of spreadsheets and PDFs every month | Reproducible pipeline, with a diagnosis of what is missing |
| Production and stock | Separate spreadsheets, no idea who weighed what | System with traceability and double-checking by a second person |
| Delivery margin | Only revenue and quantity | Revenue, cost and margin per channel (evolving) |

## How I run a project

1. **I discover the process and the bottleneck** by talking to the people who run the area.
2. **I inspect the system.** When there is no API, I analyse the screens (buttons, forms, URLs and the path to each report) until I understand how to automate it.
3. **I research and choose the technology** and the way to execute it.
4. **I direct the AI with precise instructions.** I define the problem and the rules; Claude (Anthropic) is my programming partner and I review what it writes.
5. **I test with real data**, handle failures and only then let it run unattended.
6. **I follow up after delivery:** I read the logs, fix what fails and adjust to what changed in the process.
7. **I keep a person in charge of the final decision** wherever there is risk.

## Next steps (roadmap)

Under study or in progress, no finished code yet:

- Payment write-off routine, cash flow and income statement, integrated with the treasury module.
- Production and stock system: recipe costing, automatic ingredient deduction and automatic replenishment.
- Delivery margin: include coupons and discounts, automate the extraction and unify everything in a single routine.

## Skills

- **Projects and processes:** requirements gathering, process mapping, continuous improvement, prioritisation, validation with the business areas, post-delivery follow-up
- **Automation and robots (RPA):** Python, Playwright, integration with systems that have no API, scheduled routines, logging, failure handling and notifications
- **Applied AI:** OCR, unit conversion and decision support with Claude, with human review
- **Data and reporting:** pandas, advanced Excel (formulas, dashboards, charts), PDF
- **Databases and security:** PostgreSQL, SQL, triggers, row level security
- **Web apps:** installable PWA in plain JavaScript, with authentication, roles and offline support

## Privacy and security

The repositories and documents in this portfolio do not contain:

- source code of the original implementations;
- credentials, passwords, keys or tokens;
- customer, employee or personal data;
- tax IDs, store or supplier names;
- internal URLs and paths;
- company files, spreadsheets or figures.

The original code stays private because it contains integrations and information from the corporate environment. The projects are presented as technical portfolio case studies.
