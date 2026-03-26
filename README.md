NaijaMetrics

NaijaMetrics is a simple, public-facing dashboard that presents key Nigerian economic indicators in a way that is easy to read, quick to load, and always up to date. The goal is not to overwhelm with data, but to surface the few numbers people actually care about and check regularly.

It focuses on clarity, reliability, and a clean interface that feels closer to a real product than a typical side project.

---

What it does

NaijaMetrics pulls together a small set of core macroeconomic indicators and presents them in a live dashboard format. These include:

- Inflation rate (annual CPI)
- GDP growth rate
- USD to Naira exchange rate
- Unemployment rate

Each metric is displayed as both a current value and a historical trend, so users can quickly understand not just where things are, but how they’ve been moving.

The dashboard refreshes automatically at intervals, so the data stays current without requiring manual reloads.

---

Why this exists

Most publicly available Nigerian macro data is either:

- buried in PDFs
- spread across multiple sources
- delayed or hard to interpret
- or presented in a way that is not built for everyday users

NaijaMetrics exists to fix that.

It acts as a lightweight “economic pulse” for Nigeria. Something you can open quickly and get a sense of direction without digging through reports.

---

Data sources

The project relies on a mix of public and open data sources:

- World Bank API for inflation, GDP, and unemployment
- Exchange rate API for USD/NGN

Because some of these APIs do not support direct browser requests, NaijaMetrics uses a proxy layer to fetch and normalize the data.

It also includes fallback values so the interface never breaks or shows empty states when a request fails.

---

How it works

The application is entirely frontend-based:

- Built with plain HTML, CSS, and JavaScript
- Uses Chart.js for data visualization
- Fetches data asynchronously using the Fetch API
- Uses a proxy (AllOrigins) to bypass CORS restrictions
- Auto-refreshes data on a timed interval

There is no backend, no database, and no authentication layer. Everything runs in the browser.

---

Design approach

The design is intentionally minimal.

The focus is on:

- readability over decoration
- fast load times
- clear hierarchy of information
- smooth chart rendering
- a consistent dark UI

Every element is meant to feel purposeful. Nothing is there just for the sake of it.

---

Limitations

- World Bank data is not real-time. Most indicators are updated yearly or quarterly.
- Exchange rate data depends on the availability of the external API.
- Proxy services may occasionally rate-limit or fail.
- This is not a financial tool or trading dashboard.

The goal is to provide a reliable snapshot, not a tick-by-tick market feed.

---

Future improvements

Planned additions include:

- Foreign reserves data
- Monetary policy indicators (MPR, treasury bill rates)
- Oil price tracking
- Dark/light mode toggle
- Improved mobile responsiveness
- Better error handling and caching
- Export/share features

---

Running locally

Clone the repository and open the HTML file in your browser:

git clone https://github.com/yourusername/naijametrics.git
cd naijametrics

Then open "index.html" directly.

No build steps or dependencies required.

---

Deployment

The project is designed to be hosted on:

- GitHub Pages
- Netlify
- Vercel (static deployment)

No server configuration is needed.

---

Contributing

Contributions are welcome, especially around:

- UI improvements
- better data sources
- performance optimizations
- new relevant indicators

Keep changes simple and aligned with the core idea: clarity over complexity.

---

License

MIT License

---

Final note

NaijaMetrics is meant to feel like something you can check daily without thinking about it. Open it, scan it, and move on with a clearer sense of where things stand.
