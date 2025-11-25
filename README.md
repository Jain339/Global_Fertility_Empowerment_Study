# **Empowered, Yet Shrinking: How Women’s Economic Gains Are Rewriting the Demographics of Prosperity**

**Authors:** Nikita Jain & Kelsang Tsomo, 
**Date:** October 2025

---

# **Table of Contents**

* [Project Overview](#project-overview)
* [Research Motivation](#research-motivation)
* [Data Sources](#data-sources)
* [Analytical Methods](#analytical-methods)
* [Key Empirical Findings](#key-empirical-findings)
* [Repository Structure](#repository-structure)
* [Reproducibility Guide](#reproducibility-guide)
* [Generative AI Statement](#generative-ai-statement)
* [Citations](#citations)

---

## **Project Overview**

This research project examines how multiple dimensions of women’s empowerment: economic, educational, and sociocultural—interact with fertility decline and population aging across the 30 wealthiest economies globally. Using a merged panel dataset from **UNICEF’s State of the World’s Children (SOWC) 2024** and the **World Bank World Development Indicators (WDI)**, the project conducts a multi-indicator quantitative analysis that integrates:

* Temporal trend analysis (2015–2023)
* Multi-variable empowerment–fertility correlations
* Regression modeling and diagnostic assessment
* Interactive visualizations of demographic change
* Policy-relevant interpretation rooted in demographic and gender-equity scholarship

The full analysis is available in the rendered interactive HTML report.
---

## **Research Motivation**

A growing body of demographic research shows that as women gain autonomy, educational attainment, and access to labor markets, fertility tends to decline—a trend pervasive across advanced economies. However, this relationship is **nonlinear** and shaped by institutional context:

* High female autonomy does not automatically translate into higher fertility.
* Empowerment at work may be offset by gendered burdens at home, generating **time poverty**.
* Economic gains may coexist with structural constraints such as limited childcare systems, rigid labor markets, and persistent unpaid domestic responsibilities.

Motivated by this paradox, our project addresses three core empirical questions:

1. **How have fertility rates evolved over time (2015-2023) across countries by income levels?**
2. **Which dimensions of women's economic empowerment associate with fertility decline across Top 30 wealthy nations?**
3. **How do the wealthiest nations compare in terms of maternal support and complementary policies?**
4. **What is the impact of reduced fertility rates particularly across countries with extreme demographic trajectories (e.g., South Korea, Japan, Italy)?**

---

## **Data Sources**
The analysis relies primarily on the **UNICEF State of the World’s Children (SOWC 2024)** dataset, augmented with harmonized variables from the **World Bank World Development Indicators (WDI)** to create a unified panel of comparable measures for the top 30 high-income countries.

### **UNICEF State of the World’s Children (SOWC) 2024**

Indicators used include:

* Total fertility rate
* Maternal and paternal leave provisions
* Cash benefit coverage for new mothers
  **Source:** [https://www.unicef.org/reports/state-worlds-children-2024](https://www.unicef.org/reports/state-worlds-children-2024)

### **World Bank World Development Indicators (WDI)**

* Female financial account ownership
* Female labor force participation
* Educational attainment
* GNI per capita
* Old-age dependency ratio
* Unpaid Time Usage
  **Source:** [https://data.worldbank.org/](https://data.worldbank.org/)

### **Merged Research Files (in repository)**

* `final_empowerment_fertility_data.csv`
* `WorldBankData.csv`
* `wb_historical_panel_data.xlsx`
* `SOWC_tables.xlsx`
* `top30.csv`

These datasets were harmonized and merged using R, with all transformations documented in the Quarto/RMarkdown file `STA313-A2.Rmd`.

---

## **Analytical Methods**

### **1. Data Wrangling & Harmonization**

* Cleaned and merged multi-source panel data (2015–2023).
* Standardized units, recoded categorical variables, and handled missingness.
* Analyzed relative changes between economic indicators between 2015 and 2023.

---

### **2. Exploratory Visualization**

Created a suite of static and interactive figures, including:

* **Temporal fertility trends** by income classification
* **Heatmaps** of maternal support policies
* **Scatterplots** linking empowerment metrics to fertility
* **Bubble charts** showing aging severity
* **Trajectory plots** connecting 2015 vs. 2023 fertility shifts

### **3. Data Analysis**

* We conducted an exploratory, visualization-driven analysis to examine how women’s empowerment relates to fertility decline and population aging. After initial EDA on all high-income countries, we focused on the **top 30 wealthiest nations**, as this group provides the most internally comparable socioeconomic and institutional context. We analyzed temporal patterns in fertility, aging, financial inclusion, labour participation, unpaid work, and education. Rather than estimating regression models, our method emphasizes **descriptive trends, cross-national contrasts, and interactive visualizations**, supported by insights from academic literature to contextualize demographic patterns and policy implications.

### **4. Policy and Demographic Interpretation**

Model results were contextualized using literature from:

* Kabeer (2012) on empowerment and structural constraints
* Upadhyay et al. (2014) on reproductive autonomy
* OECD (2024) on delayed parenthood and care burdens
* UN Population Division on fertility transition dynamics

---

## **Key Empirical Findings**

### **1. Education is no longer the dominant driver.**

In high-income contexts, female education is near universal (80–100%), producing minimal variation. As such, it exhibits **weak correlation with fertility decline**.

### **2. Economic empowerment is more strongly associated with declining fertility.**

Countries with higher levels of financial inclusion, full-time female labor participation, gender-equal financial access show **sharper fertility declines** between 2015 and 2023.

### **3. Unpaid work is the strongest negative correlate**

Even in prosperous nations, women shoulder disproportionate care burdens. Countries with high unpaid work shares exhibit **persistently low fertility**, despite strong labor-market empowerment.

This confirms the “double burden” hypothesis: economic opportunity + domestic care work = reduced reproductive capacity due to *time poverty*.

### **4. Fertility decline is tightly linked to population aging**

Our interactive bubble chart demonstrates:

* Larger fertility declines → larger increases in old-age dependency.
* South Korea is the most extreme case (–0.52 fertility change; +8.3 aging points).
* Western Europe and East Asia show the most rapid demographic divergence.

---

## **Repository Structure**

```
├── Empowerment_Fertility.Rmd                 # Full reproducible analysis
├── Empowerment_Fertility.html                # Interactive HTML report
├── EDA.Rmd                                   # Exploratory analysis script
├── EDA.html                                  # Exploratory analysis HTML
├── style.css                                 # Custom styling for HTML output
├── final_empowerment_fertility_data.csv
├── WorldBankData.csv
├── wb_historical_panel_data.xlsx
├── SOWC_tables.xlsx
├── top30.csv
└── README.md                                 # Project documentation
```

---

## **Reproducibility Guide**

### **1. Clone the Repository**

```bash
git clone https://github.com/your-username/your-repo.git
cd your-repo
```

### **2. Install Required R Packages**

```r
install.packages(c(
  "tidyverse", "dplyr", "ggplot2", "plotly",
  "readr", "readxl", "broom"
))
```

### **3. Run the Analysis**

Open `STA313-A2.Rmd` in RStudio and click:

**Render → HTML**

This regenerates:

* All visualizations
* All statistical models
* All annotations and footnotes

---

## **Citations (APA-7th edition)**

1. **Correll, S. J., Benard, S., & Paik, I.** (2007). *Getting a Job: Is There a Motherhood Penalty?* **American Journal of Sociology, 112**(5), 1297–1339. [https://doi.org/10.1086/511799](https://doi.org/10.1086/511799)

2. **Kabeer, N.** (2012). *Women’s Economic Empowerment and Inclusive Growth: Labour Markets and Enterprise Development.* [https://www.womenindisplacement.org/sites/g/files/tmzbdl1471/files/2020-10/Womens%20Economic%20Empowerment%20and%20Inclusive%20Growth.pdf](https://www.womenindisplacement.org/sites/g/files/tmzbdl1471/files/2020-10/Womens%20Economic%20Empowerment%20and%20Inclusive%20Growth.pdf)

3. **Macrotrends.** (2025). *Sweden Fertility Rate | Historical Data | Chart | 1950–2025.* [https://www.macrotrends.net/datasets/global-metrics/countries/swe/sweden/fertility-rate](https://www.macrotrends.net/datasets/global-metrics/countries/swe/sweden/fertility-rate)

4. **Mammen, K., & Paxson, C.** (2000). *Women’s Work and Economic Development.* **Journal of Economic Perspectives, 14**(4), 141–164. [https://www.jstor.org/stable/2647079](https://www.jstor.org/stable/2647079)

5. **OECD.** (2024). *OECD Family Database.* [https://www.oecd.org/els/family/database.htm](https://www.oecd.org/els/family/database.htm)

6. **Upadhyay, U. D., Gipson, J. D., Withers, M., Lewis, S., Ciaraldi, E. J., Fraser, A., Huchko, M. J., & Prata, N.** (2014). *Women’s empowerment and fertility: A review of the literature.* **Social Science & Medicine, 115**, 111–120. [https://doi.org/10.1016/j.socscimed.2014.06.014](https://doi.org/10.1016/j.socscimed.2014.06.014)

7. **UNICEF (2024).** *State of the World’s Children 2024.* [https://www.unicef.org/reports/state-worlds-children-2024](https://www.unicef.org/reports/state-worlds-children-2024)

8. **World Bank (2023).** *World Development Indicators.* [https://data.worldbank.org/](https://data.worldbank.org/)


