# IPL Analysis Dashboard (2008–2026) | Power BI

An interactive Power BI dashboard analyzing IPL (Indian Premier League) data from 2008 to 2026 — covering team performance, top run-scorers, top wicket-takers, and match statistics.

![Status](https://img.shields.io/badge/tool-Power%20BI-F2C811?logo=powerbi&logoColor=black)
![Status](https://img.shields.io/badge/status-complete-brightgreen)

## 📊 Overview

This dashboard brings together 18 seasons of IPL data into a single-page interactive report, letting users filter by team/season and instantly see updated stats across every visual.

## 📂 Data Source

Match and ball-by-ball data sourced from [Cricsheet](https://cricsheet.org/) — a free, open ball-by-ball dataset for international and T20 league cricket matches, including the IPL.

## 🗂️ Data Model

The dashboard is built on 4 connected tables, modeled in Power BI:

| Table | Description | Rows |
|---|---|---|
| `ball_by_ball_data_new.csv` | Ball-by-ball delivery data — batter, bowler, runs, extras, wicket details | ~295,700 |
| `ipl_matches_data_new.csv` | Match-level data — teams, venue, toss, result, player of the match | ~1,240 |
| `players-data-updated.csv` | Player profiles — batting/bowling style, full name, image | ~775 |
| `teams_data.csv` | Team names, short codes, and logos | 16 |

**Relationships:** `ball_by_ball_data` and `ipl_matches_data` are linked on `match_id`; player and team details are joined in via `batter`/`bowler` and `team_batting`/`team_bowling`.

## 🔑 Key Features

- **Point Table** — season-wise team standings
- **Orange Cap Stats** — leading run-scorers
- **Purple Cap Stats** — leading wicket-takers
- **Total Sixes & Total Fours** — boundary-hitting stats across teams/players
- **Interactive Slicer** — filter the entire dashboard by team/season
- **Detail Table** — drill into underlying match/player data

## 🖼️ Screenshot

![Dashboard](screenshots/dashboard.png)

## 🛠️ Tools & Skills Used

- **Power BI Desktop** — data modeling, DAX measures, report design
- **Power Query** — data cleaning and transformation
- **DAX** — calculated measures for cards (sixes, fours, cap stats)

## 📁 Repository Structure

```
ipl-powerbi-dashboard/
├── IPL.pbix                       # Power BI report file
├── README.md                      # Project documentation
├── data/                          # Source CSV files (from Cricsheet)
│   ├── ball_by_ball_data_new.csv
│   ├── ipl_matches_data_new.csv
│   ├── players-data-updated.csv
│   └── teams_data.csv
└── screenshots/                   # Dashboard preview images
    └── dashboard.png
```

## ▶️ How to View

1. Download `IPL.pbix` from this repository
2. Open it in [Power BI Desktop](https://www.microsoft.com/en-us/power-platform/products/power-bi/downloads) (free)
3. Explore the interactive slicers and visuals

## 👤 Author

**Vyshnav P S**
Data Analyst

---
*This project is part of my data analytics portfolio.*

