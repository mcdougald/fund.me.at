<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/hero-dark.png">
    <img src=".github/assets/hero.png" alt="fund.me.at landing page" width="880">
  </picture>
</p>

<h1 align="center">fund.me.at</h1>

<p align="center"><strong>What the market did, and what your decisions did.</strong></p>

<p align="center">
  <img src="https://img.shields.io/badge/status-in%20development-171717?style=flat-square" alt="Status: in development">
  <img src="https://img.shields.io/badge/license-source--available-404040?style=flat-square" alt="License: source-available">
  <img src="https://img.shields.io/badge/self--host-supported-525252?style=flat-square" alt="Self-host: supported">
  <img src="https://img.shields.io/badge/part%20of-me.at-737373?style=flat-square" alt="Part of me.at">
</p>

<p align="center">
  <a href="#features">Features</a> ·
  <a href="#how-it-works">How it works</a> ·
  <a href="#screenshots">Screenshots</a> ·
  <a href="#built-with">Built with</a>
</p>

Most net-worth trackers show today's balance and a single return figure, so you cannot tell what the market did from what your own timing did. I built fund.me.at as a portfolio ledger and net-worth tracker for one owner: accounts, holdings and transactions are recorded over time, and every figure is replayed from those transactions on decimal arithmetic, so the history is the point rather than today's balance. Time-weighted and money-weighted returns sit side by side, research briefs argue in the open, and an optional model reads only the prose you hand it, never your balances. It is self-hostable.

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/overview-dark.svg">
    <img src=".github/assets/overview.svg" alt="fund.me.at at a glance: market and timing apart, a ledger not totals, research that argues, AI with the rails on" width="880">
  </picture>
</p>

## Why fund.me.at

| The usual net-worth tracker | fund.me.at |
| --- | --- |
| Today's balance | The full history, replayed from transactions |
| One return figure | Time-weighted and money-weighted returns side by side |
| A missing price counts as zero | A holding with no usable price is reported as unpriced |
| Your balances sent to an AI | An optional model sees only the prose you hand it |
| Sharing means showing dollar amounts | A public page with percentage change and milestones only |

## Features

- **Returns that tell market and timing apart**: time-weighted return, money-weighted return (XIRR) and Modified Dietz for partial periods, computed over the same series.
- **A ledger, not running totals**: balances are derived by replaying transactions against price history, with FIFO cost basis lot by lot and fixed-point decimal arithmetic. Amending an old transaction corrects every month after it.
- **Performance and portfolio views**: net worth, drawdown, allocation and income yield over any window. A holding with no usable price is reported as unpriced rather than valued at zero.
- **Daily price feed with provenance**: closes and FX rates are pulled from a public feed for held and watched symbols, and never overwrite a number the owner typed for the same day.
- **Data sources in the open**: a public page lists every market and macro data source that was bound, considered or refused, with each one's terms review.
- **Research briefs written as a debate**: rule-based analysts put weighted evidence on the table, a bull and a bear argue it in turns, and each brief is later scored against what the price actually did. Indicators (moving averages, RSI, MACD, Bollinger bands and more) follow textbook definitions.
- **AI with the rails on**: an optional, off-by-default model may write the fundamentals and news lenses only from prose you supplied, only with a citation, and never with more weight than the arithmetic. Your holdings and amounts are never sent.
- **Journal, commitments and monitors**: a paper trade journal that keeps the decision yours, recurring charges tracked as obligations, and scheduled monitors that can note an event or write a brief and nothing more. Nothing trades on its own.
- **Public journey, without dollar amounts**: an opt-in public page shows only percentage change and milestones the owner chose to publish.

## How it works

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset=".github/assets/flow-dark.svg">
    <img src=".github/assets/flow.svg" alt="How fund.me.at works: record, price, replay, measure, decide" width="880">
  </picture>
</p>

You record accounts, holdings and transactions, and a daily feed adds closes and FX rates without touching any figure you typed yourself. Every balance is then replayed from the ledger with FIFO lots on fixed-point decimals, so correcting an old transaction corrects every month after it. Returns, drawdown, allocation and yield are measured over that replayed series, and briefs, the journal and monitors help you decide without ever placing a trade.

## Screenshots

<table>
  <tr>
    <td width="50%"><picture><source media="(prefers-color-scheme: dark)" srcset=".github/assets/hero-dark.png"><img src=".github/assets/hero.png" alt="Landing page"></picture><br><sub>The landing page and its drawn product previews.</sub></td>
    <td width="50%"><picture><source media="(prefers-color-scheme: dark)" srcset=".github/assets/sources-dark.png"><img src=".github/assets/sources.png" alt="Data sources"></picture><br><sub>Sources: every market and macro data source bound, considered or refused, with its terms review.</sub></td>
  </tr>
</table>

## Built with

<p>
  <img src="https://img.shields.io/badge/Next.js-16-000000?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js 16">
  <img src="https://img.shields.io/badge/React-19-171717?style=flat-square&logo=react&logoColor=white" alt="React 19">
  <img src="https://img.shields.io/badge/TypeScript-5-262626?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript">
  <img src="https://img.shields.io/badge/Tailwind%20CSS-4-404040?style=flat-square&logo=tailwindcss&logoColor=white" alt="Tailwind CSS 4">
  <img src="https://img.shields.io/badge/Drizzle-Postgres-525252?style=flat-square&logo=drizzle&logoColor=white" alt="Drizzle ORM and Postgres">
  <img src="https://img.shields.io/badge/oRPC-TanStack%20Query-737373?style=flat-square" alt="oRPC with TanStack Query">
</p>

- Next.js 16 (App Router), React 19, TypeScript
- Tailwind CSS 4
- Drizzle ORM with Postgres
- oRPC with TanStack Query
- Better Auth
- Optional LLM provider (Anthropic or an OpenAI-compatible endpoint)
- next-intl

## Part of the me.at family

fund.me.at is one of my [`*.me.at`](https://me.at) apps. They share one design system, account, and app shell. Development happens in a private monorepo; this repository is the project's public-facing home.

## License

Source-available. See [LICENSE](LICENSE).
