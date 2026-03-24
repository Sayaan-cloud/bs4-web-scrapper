# 🚗 AckoDrive Mahindra Car Scraper

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat-square&logo=python)
![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-4-brightgreen?style=flat-square)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Processing-150458?style=flat-square&logo=pandas)
![Platform](https://img.shields.io/badge/Platform-Jupyter%20Notebook-orange?style=flat-square&logo=jupyter)
![License](https://img.shields.io/badge/License-Academic%20Use-lightgrey?style=flat-square)

> Scrape, clean, and export Mahindra car listings from the AckoDrive website using BeautifulSoup — built as part of an internship mini-project.

---

## 📌 Overview

This project collects structured data on **15 Mahindra car models** listed on [AckoDrive](https://www.ackodrive.com), a new-car marketplace. Since AckoDrive lists only new cars, used-car attributes (Year, KM Driven, Owners) were not available and are excluded from the dataset.

> 📍 **Note on Location:** Mumbai location data failed to load on AckoDrive — selecting Mumbai did not change the URL or class names, so the scraper defaulted to **Delhi**, which provided complete and consistent data.

---

## 📂 Repository Structure

```
📦 ackodrive-mahindra-scraper
 ┣ 📓 TeamE_Minor_Project_IPYNB.ipynb   ← Main scraping & analysis notebook
 ┣ 🌐 raw_ackodrive.html                ← Raw HTML fetched during scraping
 ┣ 📊 AckoDrive_Mahindra_Car.csv        ← Final cleaned dataset
 ┗ 📄 README.md                         ← Project documentation
```

---

## 🔍 Data Collected

| Attribute | Description |
|---|---|
| **Car Name** | Name of the Mahindra model |
| **Fuel Type** | Petrol / Diesel |
| **Transmission** | Manual / Automatic |
| **Price Label** | Location-based pricing info |
| **Price Range** | Minimum & maximum on-road price |
| **Variants** | Total number of variants offered |

> ❌ Fields like **Year**, **KM Driven**, and **Owners** were unavailable — AckoDrive lists new cars only.

---

## ⚙️ Workflow

```
1. Fetch page HTML using Requests
2. Parse HTML with BeautifulSoup
3. Extract car attributes (name, fuel, transmission, price, variants)
4. Clean and structure data into a Pandas DataFrame
5. Export final dataset as CSV
```

---

## 🛠️ Technologies Used

| Tool | Purpose |
|---|---|
| Python 3.8+ | Core language |
| BeautifulSoup 4 | HTML parsing & data extraction |
| Requests | Fetching raw HTML from AckoDrive |
| Pandas | Data cleaning & structuring |
| Jupyter Notebook | Development environment |

---

## ⚠️ Challenges

- **Mumbai location unavailable** — AckoDrive's URL and class names did not update upon selecting Mumbai, so Delhi was used as the working location instead.
- **New cars only** — Used car fields (Year, KM Driven, Owners) were absent from all listings.
- **Dynamic class names** — Some HTML class names required manual inspection via browser DevTools to identify correctly.

Despite these, all **15 Mahindra car models** were successfully extracted.

---

## ▶️ How to Run

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-repo-url
   ```

2. **Navigate to the project folder:**
   ```bash
   cd ackodrive-mahindra-scraper
   ```

3. **Install dependencies:**
   ```bash
   pip install requests beautifulsoup4 pandas
   ```

4. **Open the notebook:**
   ```bash
   jupyter notebook TeamE_Minor_Project_IPYNB.ipynb
   ```

5. **Run all cells** to scrape, clean, and export the dataset.

---

## 👥 Team Members

| # | Name |
|---|---|
| 1 | Sai Surya |
| 2 | Aastha Das |
| 3 | Priyanshu Prakash Sharma |
| 4 | Hima Sajeesh Kumar |
| 5 | Vansh Bharadwaj |
| 6 | T J John |
| 7 | Vivek Salimath |

---

## 📄 License

This project is intended for **educational and academic purposes only**.
