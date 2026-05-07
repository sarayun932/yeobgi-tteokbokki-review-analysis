# 📊 Customer Satisfaction Analysis & Service Quality Strategy
### Yeobgi Tteokbokki Franchise — Seoul, Korea

> Translating 4,197 real customer reviews into branch-level diagnostic insights — and a working tool for franchise owners who had no data infrastructure to act on them.

---

## 🔍 Project Overview

| | |
|---|---|
| **Type** | Capstone Design · Business Data Analytics Workshop |
| **Institution** | Sookmyung Women's University |
| **Period** | Sep 2025 – Dec 2025 |
| **Team** | 5 members |
| **Role** | Data collection, preprocessing, sentiment labelling, visualisation, presentation |
| **Grade** | A+ |

---

## 🛠 Tech & Methods

`Python` `R` `KoNLPy` `Guided LDA` `ABSA` `Few-shot LLM Labeling` `CLOVA Studio` `IPA` `SERVQUAL` `ANOVA` `t-test` `Prophet` `Octoparse` `Canva`

---

## 📌 Problem

Yeobgi Tteokbokki is one of Korea's largest tteokbokki franchise chains, operating hundreds of branches nationwide. Despite a large customer base, the franchise had no systematic way to monitor service quality differences across branches — relying instead on aggregate star ratings that masked branch-level variation.

**Core question:**
> *"Which branches are underperforming, on what dimensions, and what should they prioritise fixing?"*

---

## 📂 Data

| | |
|---|---|
| **Sources** | KakaoMap + Naver Map (web scraping via Octoparse) |
| **Size** | 4,197 reviews across multiple Seoul branches |
| **Period** | Jan 2023 – Oct 2025 |
| **Variables** | Review text, date, branch ID, star rating |

> ⚠️ Raw data is not included in this repository due to privacy considerations.

---

## 🔬 Methodology

**01. Data Collection**
Scraped customer reviews from KakaoMap and Naver Map using Octoparse. Reviews were assigned unique IDs structured as `[district]_[branch]_[review number]` for traceability.

**02. Preprocessing**
- Removed duplicates, null values, and non-review content
- Corrected spelling errors and normalised text
- Tokenised using KoNLPy (Okt morphological analyser)
- Applied stopword filtering

**03. Sentiment Labelling**
- Manually labelled a subset of reviews as training data (positive / negative / neutral)
- Used few-shot prompting with CLOVA Studio to scale labelling across full dataset
- Reviewed and validated AI-generated labels for quality control

**04. Topic Modelling (Guided LDA)**
- Applied Guided LDA to identify key service dimensions from review text
- Topics mapped onto SERVQUAL framework: Reliability, Responsiveness, Assurance, Empathy, Tangibles

**05. IPA Analysis (Importance–Performance Analysis)**
- Plotted service attributes on a 2x2 matrix (importance vs. satisfaction)
- Identified priority areas for improvement per branch

**06. Statistical Analysis**
- ANOVA and t-tests to identify statistically significant differences across branches
- Cohen's d to measure effect size of service quality gaps

**07. Visualisation**
- Word clouds per branch and service dimension
- Bubble charts for branch-level performance comparison
- IPA quadrant plots

---

## 📊 Key Findings

- Statistically significant differences in customer satisfaction exist across branches (t = 3.104, p = 0.004, Cohen's d = −5.66)
- **Taste** and **staff friendliness** were consistently high-performing dimensions
- **Wait time** and **value for money** were the most common pain points
- Branch-level analysis revealed that underperforming branches shared specific structural weaknesses — not random variation

---

## 🚀 Output

- Branch-level diagnostic dashboard (Canva)
- Risk index per branch combining sentiment score + review volume + trend
- Actionable recommendations for franchise HQ
- 🔗 [View the interactive app](https://yeopdduk-reviewservice.my.canva.site/)

---

## 👤 My Contributions

- Collected review data via Octoparse (KakaoMap + Naver Map)
- Performed text preprocessing and spelling correction
- Manually labelled sentiment training data and validated AI-generated labels
- Created word cloud visualisations
- Designed and produced the full presentation deck (PPT)

---

## 📁 Repository Structure

├── README.md
├── preprocessing/
│   └── preprocessing.ipynb       # Text cleaning & tokenisation
├── visualization/
│   └── wordcloud.ipynb           # Word cloud generation
└── data/
└── README.md                 # Data description (raw data not included)

---

## 🔗 Links

- 📎 [Portfolio (Notion)](https://www.notion.so/Portfolio-356dc77303348003b532f2ed4fb72183)
- 🌐 [Interactive App](https://yeopdduk-reviewservice.my.canva.site/)
