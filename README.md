# FORMULA 1 RACE INTELLIGENCE

A production-grade, single-page Formula 1 championship analytics platform built in pure **HTML5, CSS3, and vanilla JavaScript**. The project recreates the official reference design and Tableau telemetry dashboards in a strict **Formula 1 Black & Red** theme (`#0a0a0a` + `#e10600`).

---

## 🏎️ Features & Components

1. **F1 5-Light Gantry Preloader ("Lights Out")**:
   - 5 red racing lights illuminate sequentially across the gantry.
   - Suspense pause before turning off simultaneously with *"LIGHTS OUT AND AWAY WE GO!"* and fading into the hero section.

2. **Hero Section (`#home`)**:
   - Split-tone design: deep black with red horizontal scanlines on the left, blending into a dramatic high-contrast modern glass skyscraper skyline (`assets/hero-skyline.jpg`) on the right.
   - Live badge `● LIVE RACE ANALYTICS PLATFORM` (pulsing red beacon).
   - Typography: **FORMULA <span style="color:#e10600">1</span> RACE INTELLIGENCE DASHBOARD** in Orbitron.
   - Primary `[VIEW DASHBOARD]` & Secondary `[EXPLORE STORY]` buttons.
   - Glass bordered stats box with animated count-up numbers:
     - `75+` SEASONS ANALYZED
     - `1K+` RACES COVERED
     - `20` ACTIVE DRIVERS
     - `10` CONSTRUCTORS
   - Animated mouse scroll indicator.

3. **Project Overview (`#project`)**:
   - Animated SVG race circuit card:
     - Dark track surface ribbon with dashed red racing line.
     - Glowing red car dot traveling smoothly around the circuit in an infinite loop.
     - Sector markers `S1` (yellow `#ffd400`), `S2` (cyan `#00e5ff`), and `S3` (orange `#ff8000`).
     - Green `DRS` straight acceleration zone.
     - 6 pill tags: DATA ANALYTICS, TABLEAU, RACE STRATEGY, VISUALIZATION, CHAMPIONSHIP, F1 DATASET.
   - 5-item telemetry architecture list with red-tinted icon boxes:
     - Global Race Overview
     - Driver Performance Metrics
     - Constructor Championship Battle
     - Pit Stop Strategy Analysis
     - Championship Success Prediction
   - `[⚡ EXPLORE DASHBOARD]` call-to-action button.

4. **Intelligence Dimensions (`#insights`)**:
   - Section header with red diamond divider (`◆`).
   - Infinite-scrolling `LIVE DATA` marquee ticker featuring real telemetry and championship facts from the dataset (pauses on hover).
   - 3×2 grid of dimension cards with red icon tiles and `→` footer metrics:
     - Circuit Analysis (`→ 24 CIRCUITS MAPPED`)
     - Lap Time Breakdown (`→ MILLISECOND PRECISION`)
     - Tire Strategy (`→ 5 COMPOUND TYPES`)
     - Driver Head-to-Head (`→ 20 DRIVERS COMPARED`)
     - Points Progression (`→ SEASON-LONG VIEW`)
     - Weather & Safety Cars (`→ INCIDENT & SAFETY METRICS`)

5. **Race Intelligence Dashboard (`#dashboard`)**:
   - macOS window frame with red/yellow/green control dots and `TABLEAU PUBLIC` pill badge.
   - High-resolution fallback screenshot (`assets/dashboard-preview.png`) displaying the full 8-panel telemetry layout with zero cropping.
   - Live KPI summary strip: `Competing Teams: 10`, `Seasons in Play: 17`, `Race Outcomes Logged: 6,464`, `Circuits Showcased: 29`.
   - `[Open full screen ↗]` button.

6. **Formula 1 Race Intelligence: Story (`#story`)**:
   - Window frame with `● TABLEAU STORY` green pill badge (`#22c55e`).
   - High-resolution story preview (`assets/story-preview.png`).
   - 7-point interactive chapter navigator that dynamically updates narrative telemetry insights:
     1. Global Driver Distribution Across Grand Prix Nations
     2. Country-wise Race Participation
     3. Team Championship Performance Analysis
     4. Driver Reliability Analysis
     5. Podium Achievements by Driver and Team
     6. Tyre Compound Usage Distribution
     7. Team Performance Ranking

7. **Telemetry & Dashboard Gallery (`#gallery`)**:
   - Grid of reference captures and dashboard interfaces.
   - Interactive Lightbox with zoom, keyboard navigation (<kbd>←</kbd> / <kbd>→</kbd> / <kbd>Esc</kbd>), and next/prev controls.

8. **Key Findings & Charts (`#insights-data`)**:
   - 6 statistical insight cards computed from the dataset:
     - *Championship Domination*: Lewis Hamilton & Mercedes AMG (6 hybrid titles, 4,491 pts).
     - *Constructor Supremacy*: Red Bull Racing (8,006 pts).
     - *Tyre Compound Superiority*: Soft compound represents 31.52% of 3,814 telemetry laps.
     - *Pit Lane Precision*: 2.18s record stop by Scuderia Ferrari.
     - *Global Circuit Footprint*: Bahrain leads with 2,168 logged outcomes.
     - *Reliability & Attrition*: 91.4% grid completion rate.
   - 4 dark-themed Chart.js visualizations:
     - **Driver Performance Leaderboard** (Top 8 drivers bar chart matching Tableau).
     - **Team Performance Ranking** (Horizontal bar chart).
     - **Tyre Compound Share** (Doughnut chart: Soft 31.52%, Medium 30.78%, Hard 30.36%, Inter 7.34%).
     - **Driver Reliability & DNF Attrition** (Stacked bar chart by failure cause).

9. **Driver Performance Telemetry Grid (`#drivers`)**:
   - Real-time search filter by driver name or constructor.
   - Season filter dropdown (`All Seasons`, `2026`, `2025`, `2024`, `2023`, `2022`, `2021`, `2020`).
   - Sort dropdown (`Highest Points`, `Most Wins`, `Most Podiums`, `Pole Positions`, `Least DNFs`).
   - Driver cards with team-specific accent stripes, champion crown badges, points, and win/podium conversion progress bars.

10. **Race Intelligence Terminal (`#contact`)**:
    - Paddock contact information and social links.
    - Form with client-side validation, transmitting button animation, and toast feedback.

11. **Footer & Global Controls**:
    - Sticky glass navbar with active section highlighting and mobile drawer.
    - Floating back-to-top button.
    - Official FIA/F1 educational disclaimer.

---

## 📁 File Structure

```
├── index.html                   # Main production single-page application
├── style.css                    # Complete F1 black & red design system
├── script.js                    # Interactivity, Chart.js, lightbox & animations
├── data.js                      # Pre-computed telemetry object (zero-CORS offline execution)
├── process_f1_dataset.py        # Python ETL extraction script
├── F1 Racing Project Dataset.xlsx # Raw Formula 1 project dataset
├── README.md                    # Project documentation
├── assets/                      # Production image assets & reference captures
│   ├── hero-skyline.jpg         # High-contrast Moscow glass skyscraper skyline
│   ├── dashboard-preview.png    # High-res Tableau Dashboard preview
│   ├── story-preview.png        # High-res Tableau Story preview
│   ├── hero-reference.png       # Reference hero capture
│   ├── project-reference.png    # Reference project capture
│   ├── dimensions-reference.png # Reference dimensions capture
│   ├── dashboard-frame-reference.png # Reference dashboard frame
│   ├── story-frame-reference.png     # Reference story frame
│   └── track_crop_ref.png       # SVG circuit design reference
└── data/                        # JSON telemetry exports
    ├── circuits.json            # 29 circuits data
    ├── drivers.json             # Driver career & season telemetry
    ├── f1_intelligence.json     # Master KPIs & aggregates
    └── insights.json            # Computed analytical findings
```

---

## ⚡ How to Run

### Method 1: Local Server (Currently Running)
Open your browser and navigate to:
**http://localhost:3000**

### Method 2: Offline Double-Click
Simply double-click `index.html` in Windows Explorer. All data is embedded in `data.js`, so the application runs with zero CORS issues.
