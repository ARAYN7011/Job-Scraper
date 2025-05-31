# 🔎 Job Scraper That Actually Works 🚀

This is a **no-code job scraper built using n8n** that successfully bypasses the common issues faced by traditional web scrapers like CAPTCHA challenges, IP bans, or detection by LinkedIn and other platforms.

Unlike traditional scrapers, which are often blocked, **this workflow fetches job listings from trusted, API-friendly sources** like Google Jobs and LinkedIn jobs via aggregators. It also includes a **data cleaning pipeline** and exports jobs directly to **Google Sheets**.

## 📸 Preview

![image](https://github.com/user-attachments/assets/c2ac4a0f-b3fa-444f-a772-47617af903e4)


---
## ⚙️ Features

- ✅ Bypasses CAPTCHA and bot-detection issues
- ✅ Extracts job listings from LinkedIn, Indeed, and other platforms via trusted sources
- ✅ Filters and cleans job data (e.g., removes duplicates, handles empty salary fields)
- ✅ Automatically updates a Google Sheet with job details
- ✅ Built with **n8n**, no code required to maintain it

---

## 📊 Data Flow

1. **Trigger**: Manual or scheduled trigger
2. **Input**: JSON or API containing job listings
3. **Function Node**: Breaks job list into individual entries
4. **Data Cleaning**: Filters out incomplete or malformed jobs
5. **Google Sheets Node**: Maps and appends jobs to your sheet

---

## 🧹 Data Cleaning

Before inserting into the sheet, the workflow:

- Removes jobs with missing titles or company names
- Converts salary field to a standard format (if needed)
- Optionally removes duplicates (based on title + company + location)

---

## 📁 Google Sheet Format

Make sure your sheet has these columns in row 1:

Job Title | Company | Location | Salary | Job Type | Apply Link


The automation will append new rows below this.

---

## 🧠 Why This Works (When Traditional Scraping Fails)

Most job boards and LinkedIn aggressively block bots using:
- CAPTCHA
- IP detection
- Bot fingerprinting

This workflow bypasses those problems by:
- Using **approved aggregators** that don’t require scraping
- Sending structured, clean data to Google Sheets
- Avoiding direct requests to job sites’ protected frontends

---

## 🚀 Getting Started

1. Clone this repo
2. Import the `n8n` workflow (included in `workflow.json`)
3. Connect your Google Sheets credentials in n8n
4. Run the workflow or schedule it as a cron job

---

## 📌 Requirements

- n8n (self-hosted or cloud)
- Google Sheets account with a sheet prepared
- API source or JSON with job listings

---

## 📷 Adding an Image

![image](https://github.com/user-attachments/assets/e835fa6e-ed6a-441d-8298-2b397db99478)


---

## 🤝 Contributing

Pull requests are welcome. For major changes, please open an issue first to discuss what you would like to change.

---

## ✨ Result

This is a **fully working job scraping solution** that doesn't break, doesn't get blocked, and is easy to extend for other platforms and use cases.


