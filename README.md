# NEXUS AI

An installable personal finance app that runs entirely in your browser. It tracks income and expenses, keeps a ledger of money you have lent, and includes a rule-based assistant called JARVIS that answers questions from your own records.

**Live app:** https://leenjerry2006.github.io/nexus-ai/

## Features

- **Dashboard:** income, expenses, net, savings rate and all-time balance, with a month filter and animated figures
- **Charts:** cash flow by month and spending by category
- **Transactions:** add, edit, delete, search and filter, with custom categories and multiple currencies (INR by default)
- **Money lent:** record who you lent to, track part-payments with a progress bar, and see overdue and due-soon reminders
- **JARVIS assistant:** a daily briefing plus questions such as "how much did I spend this week", "can I afford 15000" and "who owes me money". It can also add an entry after you confirm
- **Import and export:** CSV import (DD/MM/YYYY and YYYY-MM-DD dates), CSV export, and a JSON backup and restore that includes loans
- **Installable and offline:** works as a Progressive Web App with a service worker

## Install on your phone

- **Android (Chrome):** open the live link, open the menu, then choose **Install app** or **Add to Home screen**
- **iPhone (Safari):** open the live link, tap **Share**, then **Add to Home Screen**

## How it works

- Plain HTML, CSS and JavaScript in a single `index.html`, with [Chart.js](https://www.chartjs.org/) loaded from a CDN
- Data is saved in your browser's local storage. There is no server and no account, so nothing is sent anywhere
- `sw.js` caches the app so it opens offline, and `manifest.webmanifest` makes it installable
- JARVIS is rule-based, not an AI model. Every answer is calculated from your entries

## Limits

- Data does not sync between devices. Use **Settings and data tools** to download a JSON backup and restore it on another device
- Clearing your browser data erases your records, so keep a backup
- Reminders appear when you open the app. A web page cannot send notifications while it is closed
- Money you lend is tracked separately and is not included in your balance or spending totals

## Run locally

```
python3 -m http.server 8000
```

Then open http://localhost:8000. A local server is needed for the service worker.

## Roadmap

Budgets and goals, bills and subscriptions, forecasting, a what-if simulator and unusual-spending detection.
