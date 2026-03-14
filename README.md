# Team Tracker — Recruitment Pipeline Dashboard

> A live, interactive recruitment pipeline tracker built for internal team use. Provides real-time visibility into project deadlines, role fulfillment progress, and team workload across all active hiring engagements.

---

## Overview

Team Tracker is a lightweight, zero-dependency web dashboard designed to give recruitment teams an at-a-glance view of all ongoing hiring projects. It runs entirely in the browser with no backend required, and is embedded directly into the company's internal SharePoint environment via iframe.

> ⚠️ **Note:** The data currently in this repository is placeholder/demo data. Live recruitment data will be populated once the tracker is fully implemented and handed over to the team.

---

## Features

- **Live Countdown Timers** — Deadlines auto-update every minute based on today's date. No manual date management needed.
- **Role Fulfillment Tracking** — Visual progress bars show filled vs. open positions per project at a glance.
- **Status Classification** — Each project is tagged as `On Track`, `At Risk`, or `Delayed` with color-coded indicators.
- **Per-Person Workload View** — Each team member has their own card showing all assigned projects and aggregate stats.
- **Expandable Role Breakdown** — Click any project to drill down into individual role titles and their fill status.
- **Filter by Status** — Instantly filter the dashboard to show only delayed, at-risk, or on-track projects across the team.
- **Summary Bar** — Top-level KPIs: total team members, active projects, positions filled, open positions, and delayed count.
- **Fully Responsive** — Works on desktop and mobile browsers.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML5, CSS3, Vanilla JavaScript |
| Fonts | Playfair Display · IBM Plex Sans · IBM Plex Mono (Google Fonts) |
| Hosting | GitHub Pages |
| Embedding | SharePoint iframe (via Embed web part) |
| Dependencies | None — zero libraries, zero frameworks |

---

## Live Demo

🔗 **[https://kvshwork-source.github.io/team-tracker/](https://kvshwork-source.github.io/team-tracker/)**

---

## SharePoint Embed

This dashboard is designed to be embedded into SharePoint via the **Embed web part**. Use the following iframe snippet on any SharePoint modern page:

```html
<iframe
  src="https://kvshwork-source.github.io/team-tracker/"
  width="100%"
  height="900"
  frameborder="0"
  style="border:none; min-height:900px;">
</iframe>
```

> **Admin Note:** The domain `kvshwork-source.github.io` must be whitelisted in SharePoint Admin Center under **SharePoint → More Features → HTML Field Security** for the embed to render correctly.

---

## How to Update the Tracker

### Editing on GitHub (recommended)

1. Open the repository on GitHub
2. Click `index.html`
3. Click the **pencil icon (✏️)** to edit
4. Make your changes directly in the `people` data array inside the `<script>` block
5. Click **Commit changes** — the live site updates within 1–2 minutes

### What you can update

| Task | What to change |
|---|---|
| Add a new team member | Copy an existing person block and update name, role, color, projects |
| Add a project to someone | Add a new project block inside their `projects: [ ]` array |
| Update deadline | Change the number in `daysFromNow(X)` — positive = days from today, negative = overdue |
| Update filled/open counts | Change the `filled:` and `open:` values inside each role |
| Change project status | Update `"On Track"` / `"At Risk"` / `"Delayed"` |
| Remove a person or project | Delete their block from the data array |

---

## Project Structure

```
team-tracker/
└── index.html      # Entire application — HTML, CSS, JS, and data in one file
```

This is intentionally a single-file application for ease of editing, hosting, and embedding. No build tools, no package managers, no deployment pipeline.

---

## Status

| Item | Status |
|---|---|
| Dashboard UI | ✅ Complete |
| GitHub Pages hosting | ✅ Live |
| SharePoint iframe embed | ⏳ Pending IT whitelist approval |
| Live recruitment data | ⏳ Pending handover |

---

## Maintained by

**Corporate Infotech Private Limited - Kushagra Sharma (Human Resource Intern)**  
For data updates or tracker issues, edit `index.html` directly or raise a request with the team admin.
