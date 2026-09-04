# AI EduCoach

AI EduCoach is a front-end prototype for an AI-powered tutoring platform. It pairs a student-facing chat tutor with a set of admin/management dashboards for monitoring the AI system, reviewing content, and analyzing usage — all built as static HTML/CSS/JS pages with mock data.

> This is a UI prototype: all data (chat replies, sessions, metrics, logs) is simulated in-browser with JavaScript. There is no backend, database, or real AI integration.

## Features

**Student experience**
- `chat_interface.html` — Chat-based AI tutor with LaTeX/math rendering (MathJax), adaptive follow-up prompts, thumbs up/down feedback, a recent-sessions table, and a study-insights modal with a Chart.js time-spent chart.
- `login_page.html` — Sign-in / account entry screen.

**Admin & operations**
- `admin_dashboard.html` — System KPIs (model accuracy, response time, satisfaction, active sessions), emotion-distribution and accuracy-trend charts, and a searchable/filterable system events log.
- `analytics_dashboard.html` — Usage and engagement analytics/reporting.
- `content_editor.html` — Interface for authoring or editing tutoring content.
- `review_queue.html` — Queue for reviewing flagged or pending content/responses.
- `monitoring_dashboard.html` — Live system/model health monitoring.
- `log_viewer.html` — Browsable system/event log viewer.

## Tech stack

- Plain HTML, CSS, and vanilla JavaScript (no build step, no framework)
- [Bootstrap 5](https://getbootstrap.com/) for layout and components
- [Font Awesome 6](https://fontawesome.com/) for icons
- [Chart.js](https://www.chartjs.org/) (+ zoom plugin) for charts
- [SweetAlert2](https://sweetalert2.github.io/) for dialogs/alerts
- [MathJax 3](https://www.mathjax.org/) for LaTeX/math rendering
- Google Fonts (Poppins)

All dependencies are loaded via CDN — no `npm install` is required.

## Project structure

```
AI-EduCoach/
├── chat_interface.html / .css        # Student chat tutor
├── login_page.html / .css            # Login screen
├── admin_dashboard.html / .css       # Admin KPIs & system events
├── analytics_dashboard.html / .css   # Usage analytics & reports
├── content_editor.html / .css        # Content authoring
├── review_queue.html / .css          # Content review queue
├── monitoring_dashboard.html / .css  # System/model monitoring
├── log_viewer.html / .css            # Event/log viewer
├── style.css                         # Shared global theme
└── .vscode/                          # Editor settings
```

## Getting started

No build tools or server are required.

1. Clone the repository:
   ```bash
   git clone https://github.com/Taniiie/AI-EduCoach.git
   cd AI-EduCoach
   ```
2. Open any page directly in a browser, e.g. `chat_interface.html`, or serve the folder locally for cleaner relative-path loading:
   ```bash
   python3 -m http.server 8000
   ```
   then visit `http://localhost:8000/chat_interface.html`.

Use the **Navigate** dropdown in the top nav bar (or the sidebar) on any page to jump between the chat tutor and the various admin/management dashboards.

## Notes

- Chat replies, KPIs, chart data, session lists, and log entries are all mocked with static JS arrays and `setTimeout`-simulated delays — swap in real API/backend calls to make this production-ready.
- Since pages are static HTML, styling (`style.css`) is shared globally while each page has its own companion stylesheet for page-specific styles.

## License

No license has been specified for this project yet. Add a `LICENSE` file to clarify usage terms.
