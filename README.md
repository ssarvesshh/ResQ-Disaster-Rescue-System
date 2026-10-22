# ResQ — Disaster Rescue Coordination System

> **A Data Structures & Algorithms mini-project** that simulates emergency triage, rescue-team allocation, and incident tracking through a browser-based command centre.

![ResQ command-centre dashboard](assets/resq-demo-dashboard.png)

## Overview

ResQ is a self-contained web application built with **HTML, CSS, and vanilla JavaScript**. It demonstrates how common data structures can support a disaster-response workflow: registering incidents, calculating priority scores, selecting the most urgent case, allocating available rescue teams, and tracking response progress.

This is an **academic simulation only**. It is not connected to emergency services, live GPS, or an operational dispatch system. Map pins are illustrative.

## Features

- Emergency registration with incident type, severity, location, people affected, and medical urgency.
- Automatically calculated priority scores.
- Incident board with statuses: **Pending → Assigned → In Progress → Resolved**.
- Rescue-team management and FIFO team allocation.
- Max-heap priority queue for active incidents.
- Hash-map index for looking up incidents by ID.
- Undo last action using a stack of previous application states.
- Illustrative incident map, activity log, and live dashboard counters.
- Search and status filtering.
- Local browser persistence using `localStorage`.
- Export incident and team data as JSON.
- Responsive layout for desktop and mobile screens.

## Data structures used

| Data structure | How ResQ uses it |
|---|---|
| **Binary Max-Heap / Priority Queue** | Inserts active incidents by calculated score so the highest-priority case is at the root. |
| **Circular Queue** | Keeps available rescue-team IDs and allocates them in FIFO (First In, First Out) order. |
| **Hash Map** | Maps an incident ID to its incident record for direct lookup. |
| **Stack** | Saves prior application states so the most recent change can be undone first. |
| **Arrays / Array Lists** | Store incident records, rescue teams, and activity-log entries. |
| **Searching and sorting** | Filters incidents by keyword/status and arranges the displayed incident list by priority. |

## Demo screenshots

### 1. Initial demo data

The initial dashboard loads sample incidents and rescue teams so the main features can be demonstrated immediately.

![ResQ initial demo dashboard](assets/resq-demo-dashboard.png)

### 2. Progress after adding data

This example shows a fourth incident added (**Earthquake — Kunnamkulam, Thrissur**) and the Flood incident moved through team assignment into **In Progress**. Dashboard counters, the priority heap, team availability, incident board, and activity log update as the application state changes.

![ResQ dashboard after adding and progressing data](assets/resq-progress-dashboard.png)

[View the full-page progress screenshot](assets/resq-progress-full.png)

## How to run

1. Download or clone this repository.
2. Open `index.html` in a modern browser (Chrome, Edge, or Firefox).
3. Use **Register an Emergency** to add an incident.
4. Click **Assign team**, then **Start response**, and finally **Resolve** to demonstrate the incident workflow.
5. Add rescue teams from the **Rescue Teams** section.
6. Try **Undo last action** and **Export JSON**.

No installation, framework, build step, or backend is required.

## Publish with GitHub Pages

1. Upload `index.html`, `README.md`, and the `assets/` folder to the root of a **public** GitHub repository.
2. Open the repository's **Settings → Pages**.
3. Under the build/deployment source, choose **Deploy from a branch**.
4. Select branch `main` and folder `/(root)`, then save.
5. After deployment completes, the site will be available at `https://YOUR-USERNAME.github.io/YOUR-REPOSITORY/`.

Replace `YOUR-USERNAME` and `YOUR-REPOSITORY` with your actual GitHub username and repository name. GitHub Pages may take a few minutes to publish the first time.

## Project structure

```text
ResQ/
├── index.html
├── README.md
└── assets/
    ├── resq-demo-dashboard.png
    ├── resq-progress-dashboard.png
    └── resq-progress-full.png
```

## Limitations

- Data is stored in the current browser using `localStorage`; it is not shared between different users or devices.
- The map uses sample positions and does not show real geographic coordinates.
- The app is a demonstration, not a real emergency dispatch or public-safety service.
- The priority formula is a simple educational scoring model and should not be used for real-world triage.

## Technologies

**HTML5 · CSS3 · JavaScript · Data Structures & Algorithms · Browser Local Storage**

---

Created as an educational Data Structures project.
