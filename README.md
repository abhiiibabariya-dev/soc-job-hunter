<h1 align="center">SOC Job Hunter</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/Automation-Job%20Search-00FF41?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Docker-Ready-2496ED?style=for-the-badge&logo=docker&logoColor=white" />
</p>

<p align="center"><b>Automated SOC Analyst job search & application bot</b></p>

---

## Overview

An automated job search and application bot specifically designed for **SOC Analyst L1** positions. Monitors LinkedIn, Indeed, Naukri, and Glassdoor for matching opportunities, auto-applies to positions, and sends outreach emails to hiring managers.

## Features

- **Multi-board monitoring** -- LinkedIn, Indeed, Naukri, Glassdoor
- **Auto-apply** to matching SOC Analyst positions (0-2 years experience)
- **Email outreach** -- automated emails to hiring teams via SMTP
- **Scheduled scanning** -- configurable scan intervals
- **Desktop notifications** for new matching jobs
- **Web dashboard** for monitoring search results
- **Dockerized** for easy deployment

## Tech Stack

| Component | Technology |
|-----------|-----------|
| Language | Python 3.10+ |
| Scraping | BeautifulSoup4, Selenium (optional) |
| HTTP | requests, fake-useragent |
| Scheduling | schedule library |
| Email | smtplib with MIME |
| Notifications | Plyer (desktop alerts) |
| Deployment | Docker, Fly.io, Render |

## Quick Start

```bash
# Clone
git clone https://github.com/abhiiibabariya-dev/soc-job-hunter.git
cd soc-job-hunter

# Setup
cp config.example.json config.json    # Edit with your credentials
pip install -r requirements.txt

# Run the hunter
python soc_job_hunter.py

# Or run with dashboard
python dashboard.py
```

## Project Structure

```
soc-job-hunter/
├── soc_job_hunter.py     # Core job hunting engine
├── dashboard.py          # Web dashboard
├── run_scan.py           # Manual scan trigger
├── service_runner.py     # Background service manager
├── config.example.json   # Configuration template
├── requirements.txt      # Dependencies
├── templates/
│   └── index.html        # Dashboard UI
├── Dockerfile            # Container config
├── fly.toml              # Fly.io deployment
└── render.yaml           # Render deployment
```

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
