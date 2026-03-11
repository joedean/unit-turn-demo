# Unit Turn Priority Dashboard

## Project Context
A prioritized task list dashboard for property managers to track all steps in turning a unit after a resident doesn't renew their lease.

## Tech Stack
- **Frontend:** React (Vite)
- **Backend:** Node.js + Express
- **Database:** SQLite (simple, no setup required)
- **Styling:** Tailwind CSS

## Domain Context

### What is a Unit Turn?
When a resident doesn't renew their lease, the property manager must execute a series of sequential steps to close out that resident's account and prepare the unit. Missing steps costs money and creates liability.

### The Turn Pipeline
Each unit goes through these stages in order:
1. **Non-Renewal** — Resident notifies (or is notified) they won't be renewing
2. **Move-Out** — Coordinate move-out date, conduct inspection, document unit condition
3. **Financial Account Statement (FACS)** — Generate the final account statement with all charges, credits, deposits
4. **Collections** — If there's an outstanding balance after FACS, initiate collections process

### Users
- **Property Manager (Dana)** — Primary user. Manages 30+ units across a property. Needs to see what requires attention RIGHT NOW across all active turns.

### Key Design Principles
- Tasks are prioritized by urgency (overdue items float to the top)
- Each unit turn shows its current stage and next action
- Color coding: red (overdue), yellow (due today/tomorrow), green (on track)
- Dashboard view shows ALL active turns at once — not one unit at a time

## Code Conventions
- Use functional React components with hooks
- API routes under `/api/`
- Keep components small and focused
- Use descriptive variable names
