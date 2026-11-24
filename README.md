# EcoTrack — Campus Sustainability & Environmental Impact Platform

**Track actions. Measure impact. Build a greener campus.**

EcoTrack is a single-page web application that helps college students track sustainability activities, monitor environmental impact, join eco-friendly challenges, report campus environmental issues, and visualize progress — all without a backend.

Built as a practical Environmental Studies college project. Open `index.html` in any modern browser and it works immediately.

---

## Features

### Dashboard (Overview)
- Personalized welcome message and current date
- Six summary cards: Waste Recycled, Water Saved, Energy Saved, Trees Planted, Plastic Avoided, Eco Points
- Illustrative Campus EcoScore (0–100) with circular progress
- Level progress bar and quick-action buttons
- Recent activity feed

### Eco Activity Tracker
- Log activities across 6 categories:
  - Waste Management
  - Water Conservation
  - Energy Conservation
  - Plantation
  - Plastic Reduction
  - Sustainable Transport
- Automatic unit selection and point calculation
- Edit / delete activities
- Search, category filter, and sort
- **CSV export** of all logged activities

### Sustainability Goals
- Pre-loaded demo targets (waste, water, energy, trees, plastic)
- Progress bars that update when relevant activities are logged
- Add, edit, and delete custom goals

### Eco Challenges
- Six ready-to-join challenges (Plastic-Free Day, Green Commute, Lights Out, etc.)
- Join → mark progress → complete → earn reward points
- Prevents double-rewarding the same challenge

### Analytics
- Activity trends (line chart)
- Category distribution (doughnut)
- Waste composition (pie — demo)
- Weekly activity frequency (bar)
- Range filters: 7 / 30 / 90 days
- Charts update with user-logged data

### Environmental Issue Reporting
- Categories: water leakage, waste overflow, plastic pollution, electricity wastage, etc.
- Severity levels and status workflow (Reported → Under Review → In Progress → Resolved)
- Local-only storage — clearly labelled that reports are **not** sent to campus authorities
- Search and filter by category/status

### Achievements & Badges
- 8 unlockable badges (First Step, Recycler, Water Guardian, Energy Saver, Tree Friend, Eco Streak, Planet Protector, Challenge Champion)
- Live progress tracking and unlock notifications

### Leaderboard
- Demo student rankings (clearly labelled as sample data)
- Weekly and All-time views
- Your profile appears when you earn points

### Eco Tips
- 20+ practical tips across Water, Energy, Waste, Transport, Biodiversity, Plastic
- Category filters, favorites, random tip, tip of the day

### Campus Map
- Stylized CSS campus layout (no external map API)
- Clickable locations: Main Block, Library, Canteen, Computer Lab, Garden, Parking Area, Auditorium
- Shows activities, issues, and a tip for the selected location

### Profile & Settings
- Edit display name and avatar initial
- Impact summary (points, activities, challenges, badges)
- Dark mode toggle (persisted)
- Reset Demo Data (with confirmation)

### Notifications
- Generated on activity log, badge unlock, challenge join/complete, issue report
- Unread badge, mark-as-read, clear all

---

## How to Run

1. Download or copy `index.html`
2. Open it in **Chrome, Firefox, Edge, or Safari**
3. No installation, no server, no internet required after the first load (CDN fonts/icons/charts are loaded once)

> **Note:** Charts use Chart.js via CDN and icons use Lucide via CDN. An internet connection is needed the first time the page loads those resources. After that, the app runs fully offline for data and interaction.

---

## Technical Overview

| Aspect              | Detail                                      |
|---------------------|---------------------------------------------|
| Architecture        | Single-file SPA (`index.html`)              |
| Storage             | `localStorage` (no backend / database)      |
| Charts              | Chart.js 4.x (CDN)                          |
| Icons               | Lucide (CDN)                                |
| Font                | Inter (Google Fonts)                        |
| Styling             | Custom CSS (CSS variables + dark theme)     |
| Responsiveness      | Desktop, tablet, and mobile layouts         |

### LocalStorage Keys
- `ecotrack_activities`
- `ecotrack_reports`
- `ecotrack_challenges`
- `ecotrack_goals`
- `ecotrack_notifications`
- `ecotrack_profile`
- `ecotrack_preferences`
- `ecotrack_favorites`
- `ecotrack_achievements`

Demo data is loaded **only** when a key does not already exist, so user data is never overwritten on refresh.

---

## Eco Points & Levels

| Activity type              | Points          |
|----------------------------|-----------------|
| Waste recycling / segregation | 10           |
| Water conservation         | 10              |
| Energy saving              | 10              |
| Composting                 | 15              |
| Plastic avoidance          | 15              |
| Sustainable transport      | 15              |
| E-waste collection         | 20              |
| Tree planting              | 25 per tree     |

| Points range | Level             |
|--------------|-------------------|
| 0 – 99       | Eco Starter       |
| 100 – 299    | Green Explorer    |
| 300 – 599    | Eco Champion      |
| 600 – 999    | Nature Guardian   |
| 1000+        | Planet Protector  |

---

## Important Disclaimers (for evaluators)

- All statistics and the **EcoScore** are **illustrative** and based on logged (or demo) activities. They are **not** scientifically validated environmental measurements.
- The leaderboard uses **simulated student data**.
- Issue reports are stored **only in the browser** and are **not** transmitted to any campus authority or server.
- A persistent banner reminds users: *“Demo Mode — All data is stored locally in this browser.”*

---

## Browser Compatibility

Tested conceptually for:
- Google Chrome (recommended)
- Mozilla Firefox
- Microsoft Edge
- Safari

Requires a modern browser with support for:
- ES6+ JavaScript
- CSS custom properties
- `localStorage`
- Canvas (for charts)

---

## Project Structure

```
EcoTrack/
├── index.html      # Complete application (HTML + CSS + JS)
└── README.md       # This file
```

No build tools, no `node_modules`, no backend.

---

## Suggested Demo Flow (for viva / presentation)

1. Open the dashboard — show demo metrics and EcoScore  
2. Log a new activity (e.g. “Waste recycled – 5 kg”)  
3. Watch the dashboard numbers, points, and level update  
4. Go to Analytics and refresh the charts  
5. Join a challenge and mark progress  
6. Submit an environmental issue report and change its status  
7. Unlock an achievement  
8. Export activities as CSV  
9. Toggle dark mode  
10. Refresh the page to prove data persistence  
11. Optionally reset demo data from the Profile page  

---

## Credits

- **Chart.js** — https://www.chartjs.org  
- **Lucide Icons** — https://lucide.dev  
- **Inter font** — Google Fonts  

Designed and developed as a college Environmental Studies assignment project.

---

## License

This project is provided for educational purposes. You may freely use, modify, and present it as part of academic work.
