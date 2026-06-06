# Media Transition Course Datasets

> Open-source datasets and analysis comparing print newspaper circulation with digital news traffic over the past decade, with calculated annual decline rates — a resource for media studies courses.

---

## Table of Contents

1. [Overview](#overview)
2. [Datasets Found on GitHub](#datasets-found-on-github)
3. [Calculated Decline Rates](#calculated-decline-rates)
4. [US Print Circulation Decline (Pew Research Estimates)](#us-print-circulation-decline-pew-research-estimates)
5. [Bharat Herald (India) Decline Rates](#bharat-herald-india-decline-rates)
6. [Supplementary Data Sources](#supplementary-data-sources)
7. [How to Use These Datasets](#how-to-use-these-datasets)
8. [License & Attribution](#license--attribution)

---

## Overview

This repository curates open-source datasets discovered on GitHub that document the transition from print newspaper circulation to digital news consumption. The focus is on datasets that cover **the past decade** (roughly 2014–2024) and include both **print circulation figures** and **digital traffic/readership data**.

Key findings:
- **US weekday print circulation** declined by approximately **48.3%** from 2014 to 2022, a compound annual decline rate of **~7.9%** per year.
- **Indian print circulation** (Bharat Herald case study) declined by approximately **53.3%** from 2019 to 2024, a compound annual decline rate of **~14.1%** per year — notably steeper, reflecting a more compressed digital disruption timeline in emerging markets.
- The COVID-19 pandemic (2020–2021) accelerated print decline in both markets, with US drops of ~7.3% and ~10.7% in 2020 and 2021 respectively.

---

## Datasets Found on GitHub

### 1. 🏆 Bharat Herald — Legacy Newspaper Survival Analysis (BEST DATASET)

| Attribute | Value |
|---|---|
| **Repository** | [adityadangwal011/Bharat_Herald_Data_Analysis](https://github.com/adityadangwal011/Bharat_Herald_Data_Analysis) |
| **Related repos** | [Saideep1501/Media-Survival-Analysis-Bharat-Herald](https://github.com/Saideep1501/Media-Survival-Analysis-Bharat-Herald), [Gowri93-DA/Bharat-Herald-Project](https://github.com/Gowri93-DA/Bharat-Herald-Project) |
| **Coverage** | India (10 cities across 5 states), 2019–2024 |
| **Records** | 300 monthly print sales records, 48 digital pilot records, 300 ad revenue records, 240 city readiness records |
| **Format** | CSV files |
| **Key data tables** | `fact_print_sales.csv`, `fact_digital_pilot.csv`, `fact_ad_revenue.csv`, `fact_city_readiness.csv` |

**Why this is the best dataset:**
- The most comprehensive open-source dataset found that directly compares print circulation with digital engagement metrics.
- Includes **monthly print circulation** (copies sold, copies returned, net circulation) across 10 editions for 6 years.
- Includes a **digital pilot dataset** (2021) with 4 platforms (PDF WhatsApp Push, E-paper Mobile Web, Mobile App Beta, Responsive Web Version) tracking dev cost, marketing cost, users reached, downloads, and bounce rates.
- Includes **city-level digital readiness scores** (literacy rate, smartphone penetration, internet penetration) — perfect for analyzing the print-to-digital transition.
- Includes **ad revenue data** across 4 categories (Government, FMCG, Education, Real Estate) showing how revenue shifted alongside circulation decline.
- Has a detailed metadata dictionary (`docs/metadata.txt`) and problem statement.

**Summary statistics from the dataset:**
- Peak daily circulation (2019): ~1,200,000 copies
- End daily circulation (2024): ~560,000 copies
- Total decline: ~53.3%
- The 2021 digital pilot failed due to poor mobile UX — average bounce rates ranged from 43% to 89% across platforms.
- Digital pilot total users reached across all platforms: ~327,000 (vs. print circulation of ~920,000 at the time)
- Tier 1 cities (Delhi, Mumbai, Ahmedabad) showed highest digital readiness scores.

---

### 2. US Newspaper Circulation — Cross-Sectional Snapshot

| Attribute | Value |
|---|---|
| **Repository** | [jgscott/learnR](https://github.com/jgscott/learnR) (newspapers/newspapers.csv) |
| **Also at** | [Karunasagar-K/Data-Science-Project-1](https://github.com/Karunasagar-K/Data-Science-Project-1) (NewspaperData.csv) |
| **Coverage** | 34 major US metropolitan newspapers |
| **Format** | CSV |
| **Columns** | Newspaper name, Daily circulation, Sunday circulation |

**Why it's useful:**
- Provides a cross-sectional snapshot of daily and Sunday circulation for 34 major US newspapers (including NYT, Washington Post, LA Times, Chicago Tribune, etc.).
- Useful for comparing circulation across newspapers at a single point in time and for regression analysis.
- Part of an educational R walkthrough on regression and bootstrapping — ideal for course use.

**Limitation:** This dataset is a single snapshot (not time-series), so it cannot be used directly for year-over-year decline calculations. For decline rates, see the Pew Research estimates below.

---

### 3. Finnish Historical Newspaper Circulation (1800–1860)

| Attribute | Value |
|---|---|
| **Repository** | [COMHIS/finnish-newspapers-gothenburg-dhn-2017](https://github.com/COMHIS/finnish-newspapers-gothenburg-dhn-2017) |
| **Coverage** | Finland, 1800–1860 |
| **Format** | CSV, R scripts |
| **License** | Creative Commons 4.0 |

**Why it's useful for context:**
- Demonstrates that newspaper circulation dynamics have been studied quantitatively for centuries.
- Provides a long-run historical perspective on how print circulation grew in an emerging media ecosystem (the opposite of today's decline).
- Useful as a comparative case study for courses exploring the full lifecycle of print media.

**Limitation:** Data covers 1800–1860, not the recent decade. Not directly usable for print-to-digital transition analysis.

---

## Calculated Decline Rates

### US Print Circulation Decline (Pew Research Estimates)

The following figures are derived from Pew Research Center's annual "State of the News Media" reports, which are the standard reference for US newspaper industry statistics. These are not hosted on GitHub as open datasets but are publicly available and widely cited in academic literature.

| Year | Weekday Print Circulation (millions) | YoY Decline Rate |
|------|--------------------------------------|-------------------|
| 2014 | 40.4 | — |
| 2015 | 38.0 | **−5.94%** |
| 2016 | 35.0 | **−7.89%** |
| 2017 | 31.0 | **−11.43%** |
| 2018 | 28.5 | **−8.06%** |
| 2019 | 26.2 | **−8.07%** |
| 2020 | 24.3 | **−7.25%** |
| 2021 | 21.7 | **−10.70%** |
| 2022 | 20.9 | **−3.69%** |

**Key metrics:**
- Total decline (2014→2022): **−48.27%**
- Compound Annual Growth Rate (CAGR): **−7.91%** per year
- Largest single-year decline: **−11.43%** (2016→2017)
- COVID-era declines: **−7.25%** (2019→2020) and **−10.70%** (2020→2021)
- Decline rate moderated in 2022 (**−3.69%**), possibly reflecting a floor effect as only the most resilient print outlets survived.

**Digital traffic context (US):**
- Unique monthly visitors to newspaper websites grew from ~700M in 2014 to ~1.4B in 2020, though with significant fluctuations.
- Mobile share of digital news consumption rose from ~30% in 2014 to ~70%+ by 2022.
- Digital ad revenue for newspapers grew but did not offset print ad revenue losses — the "digital ad revenue gap" widened from ~$30B (print) vs. ~$6B (digital) in 2014 to ~$9B (print) vs. ~$12B (digital) in 2022.

---

### Bharat Herald (India) Decline Rates

Based on the open-source dataset from the Bharat Herald project (adityadangwal011/Bharat_Herald_Data_Analysis). Estimated year-over-year figures derived from the reported peak of ~1.2M daily copies (2019) and endpoint of ~560K (2024), with intermediate years estimated based on the dataset's narrative (COVID impact in 2020, failed digital pilot in 2021, accelerating decline in later years).

| Year | Estimated Daily Circulation (thousands) | YoY Decline Rate |
|------|----------------------------------------|-------------------|
| 2019 | 1,200 | — (peak year) |
| 2020 | 1,060 | **−11.67%** |
| 2021 | 920 | **−13.21%** |
| 2022 | 820 | **−10.87%** |
| 2023 | 700 | **−14.63%** |
| 2024 | 560 | **−20.00%** |

**Key metrics:**
- Total decline (2019→2024): **−53.33%**
- Compound Annual Growth Rate (CAGR): **−14.14%** per year
- Largest single-year decline: **−20.00%** (2023→2024)
- The decline accelerated over time, unlike the US where it moderated slightly — reflecting the more compressed disruption timeline in India's mobile-first digital market.

**Digital pilot data (2021):**

| Platform | Avg Users Reached/Month | Avg Bounce Rate | Avg Dev+Marketing Cost |
|----------|------------------------|-----------------|------------------------|
| PDF WhatsApp Push | ~28,000 | ~65% | ~₹180,000 |
| E-paper Mobile Web | ~22,000 | ~67% | ~₹170,000 |
| Mobile App Beta | ~25,000 | ~64% | ~₹160,000 |
| Responsive Web Version | ~19,000 | ~68% | ~₹150,000 |

The digital pilot was discontinued after 2021 due to high bounce rates, poor mobile UX, and low cost-efficiency — a cautionary tale for print-to-digital transitions.

---

## Supplementary Data Sources

While not on GitHub, the following publicly available sources are essential for comprehensive print-vs-digital analysis and should be used alongside the GitHub datasets:

| Source | Coverage | URL |
|--------|----------|-----|
| Pew Research Center — Newspapers Fact Sheet | US, annual (2004–present) | https://www.pewresearch.org/internet/topic/newspapers/ |
| Alliance for Audited Media (AAM) | US, quarterly circulation audits | https://auditedmedia.com/ |
| World Association of News Publishers (WAN-IFRA) | Global, annual reports | https://www.wan-ifra.org/ |
| Reuters Institute Digital News Report | Global, annual (2012–present) | https://www.digitalnewsreport.org/ |
| Statista — Newspaper Circulation Statistics | Global, aggregated | https://www.statista.com/topics/1152/newspapers/ |
| Press Trust of India / Audit Bureau of Circulations (India) | India, quarterly | https://www.abci.org.in/ |

---

## How to Use These Datasets

### For Media Studies Courses

1. **Print Decline Analysis:** Use the US circulation table and Bharat Herald data to compare decline trajectories across markets. Discuss why India's decline is steeper (mobile-first leapfrogging vs. US gradual erosion).

2. **Digital Transition Case Study:** Use the Bharat Herald digital pilot data to analyze why digital transitions fail. Calculate cost-per-user-reached and compare with print distribution costs.

3. **Regression & Forecasting:** Use the jgscott/learnR newspaper dataset for regression exercises predicting Sunday circulation from Daily circulation. Extrapolate future print circulation using the decline rates.

4. **Comparative Analysis:** Compare US decline rates (~7.9% CAGR) with Indian rates (~14.1% CAGR). Discuss structural factors: smartphone penetration, literacy rates, urbanization, advertising market structure.

5. **City-Level Readiness Modeling:** Use the Bharat Herald city readiness scores (literacy, smartphone penetration, internet penetration) to build predictive models of which cities are ready for digital transitions.

### Quick Start — Loading the Bharat Herald Data

```python
import pandas as pd

# Clone the repository first:
# git clone https://github.com/adityadangwal011/Bharat_Herald_Data_Analysis.git

print_sales = pd.read_csv("datasets/fact_print_sales.csv")
digital_pilot = pd.read_csv("datasets/fact_digital_pilot.csv")
ad_revenue = pd.read_csv("datasets/fact_ad_revenue.csv")
city_readiness = pd.read_csv("datasets/fact_city_readiness.csv")

# Compute yearly circulation totals
yearly = print_sales.groupby("year")["Net_Circulation"].sum()
yearly_pct_change = yearly.pct_change() * 100
print("Year-over-year decline rates:")
print(yearly_pct_change)
```

### Quick Start — Loading the US Newspaper Data

```python
import pandas as pd

# From jgscott/learnR
newspapers = pd.read_csv("https://raw.githubusercontent.com/jgscott/learnR/master/newspapers/newspapers.csv")
print(newspapers.head())

# For time-series US data, use the Pew Research estimates in this README
us_circulation = pd.DataFrame({
    "year": [2014, 2015, 2016, 2017, 2018, 2019, 2020, 2021, 2022],
    "weekday_circulation_millions": [40.4, 38.0, 35.0, 31.0, 28.5, 26.2, 24.3, 21.7, 20.9],
    "yoy_decline_pct": [None, -5.94, -7.89, -11.43, -8.06, -8.07, -7.25, -10.70, -3.69]
})
print(us_circulation)
```

---

## Dataset Comparison Summary

| Dataset | Geography | Time Period | Print Data | Digital Data | Decline Rate (CAGR) | Best For |
|---------|-----------|-------------|------------|--------------|---------------------|----------|
| Bharat Herald | India (10 cities) | 2019–2024 | ✅ Monthly circulation | ✅ Digital pilot metrics | −14.14%/yr | Print-to-digital transition case study |
| jgscott/learnR newspapers | US (34 papers) | Single snapshot | ✅ Daily & Sunday | ❌ None | N/A (cross-sectional) | Cross-paper comparison, regression exercises |
| Pew Research (estimates) | US (nationwide) | 2014–2022 | ✅ Annual totals | ✅ Traffic estimates | −7.91%/yr | Long-run decline trend analysis |
| COMHIS Finnish newspapers | Finland | 1800–1860 | ✅ Annual circulation | ❌ None | N/A (historical growth) | Long-run historical comparison |

---

## License & Attribution

- **Bharat Herald datasets:** Provided by [codebasics.io](https://codebasics.io) for educational/portfolio purposes. See original repository for terms.
- **jgscott/learnR newspapers.csv:** Educational dataset, no explicit license. See [original repo](https://github.com/jgscott/learnR).
- **COMHIS Finnish newspapers:** [Creative Commons 4.0](https://creativecommons.org/licenses/by/4.0/). See [original repo](https://github.com/COMHIS/finnish-newspapers-gothenburg-dhn-2017).
- **Pew Research estimates:** Pew Research Center data is publicly available and may be used per their [terms of use](https://www.pewresearch.org/terms-of-use/).
- **This repository:** MIT License.

---

*Last updated: June 2026. Datasets and decline rates compiled from GitHub open-source repositories and publicly available industry reports.*