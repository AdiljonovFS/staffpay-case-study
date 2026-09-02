# StaffPay — HR, attendance and payroll system

**[staffpay.uz](https://staffpay.uz/)** · a commercial product for companies in Uzbekistan

Face-terminal attendance, a formula-driven payroll engine, and Telegram notifications in one system — replacing the spreadsheet-and-paper workflow most small companies still run on.

---

## The problem

Small and mid-sized companies track attendance on paper or in Excel, then recalculate salaries by hand every month. The result is slow, easy to dispute, and impossible to audit. Employees have no visibility into their own hours or how their pay was calculated.

## What the system does

**Face-terminal attendance** — employees check in and out at a face-recognition terminal. Late arrivals, early departures, and absences are recorded automatically.

**Payroll engine** — salaries are computed from configurable formulas and work policies rather than hardcoded rules, so each company can encode its own rates, bonuses, and deductions.

**Telegram integration** — announcements and payroll notifications reach employees through a bot. The dashboard flags anyone not yet connected, since they would silently miss every notification.

**HR workflows** — hiring and departure tracking, departments, leave and absence reasons, work policies, holidays, birthdays, and applicant handling.

**Audit trail** — every change is logged with actor and timestamp: who edited a work policy, who recalculated a salary, who marked an absence reason.

---

## Frontend work

- **Role-based interfaces** — separate views for superuser, HR admin, and employees, each seeing a different slice of the same data
- **Dashboard** — headcount and daily status cards, a 30-day attendance trend chart, department rankings, and a live activity feed
- **Payroll configuration UI** — building and editing salary schemes without touching code
- **Report generation** — attendance and payroll exports
- **Uzbek and Russian localisation**

## Design decisions worth noting

The dashboard surfaces problems rather than waiting to be asked. If employees are not connected to the Telegram bot, that appears as a warning with a direct link to the list — because a notification system that silently fails for part of the staff is worse than no notification system.

Payroll is formula-based rather than hardcoded. It costs more upfront, but it means onboarding a new company is configuration rather than a code change.

---

## Stack

`React` `Telegram Bot API` `Face recognition terminals`

---

*Source code is private — this repository documents the work. No screenshots are included because the system holds real employee data.*
