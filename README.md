# 🇪🇺 The European Trade's Silent Transformation (2013–2024)

[![Language](https://img.shields.io/badge/Language-R%204.4-276DC3?style=flat&logo=r)](https://www.r-project.org/)
[![Data Source](https://img.shields.io/badge/Data%20Source-Eurostat%20API%20(ext__ser__bec01)-003399)](https://ec.europa.eu/eurostat)
[![Dashboards](https://img.shields.io/badge/BI-Tableau%20%7C%20Power%20BI-E97627?logo=tableau)](The%20European%20trade’s%20silent%20transformation.pbix)

> An empirical macroeconomic investigation into 11 years of European trade flows, exposing the structural shift toward ICT, intangible services, and high-margin exports.

---

## 📌 Executive Summary

Macroeconomic reports frequently celebrate aggregate trade volume growth while remaining blind to underlying industrial decay. Raw GDP figures hide whether an economy is exporting high-value proprietary technology or merely acting as an assembly hub for foreign components.

This project analyzes **11 years of official Eurostat trade microdata (2013–2024)** across 31 European nations, moving beyond surface growth metrics to uncover deep structural reconfigurations:
- Maps the **silent decoupling** of intangible digital services and ICT from traditional physical manufacturing.
- Applies **Broad Economic Categories (BEC)** taxonomies to isolate intermediate supply chains from final consumption.
- Visualizes **spatial trade momentum** across EU member states using multi-scale econometric visualization and executive BI dashboards.

---

## 🔍 Key Analytical Dimensions

### 1. Scale vs. Structural Composition (BEC Mapping)
Trade growth is evaluated across three synchronized axes:
- **Scale (Absolute Growth):** Trillion-euro volume progression modeled in both linear and logarithmic scales to separate natural base-size expansion from genuine momentum.
- **Structure (Sectoral Shift):** Categorization via BEC (`BEC_SERV`, `BEC121`, `BEC221`, `BEC321`) revealing how high-margin intermediate digital services outpaced physical goods in post-2016 trade balances.
- **Momentum (Relative Velocity):** Ratio analysis ($\text{Export} / \text{Import}$) tracking national competitiveness shifts across central, northern, and peripheral member states.

### 2. Spatial Econometrics & Jenks Natural Breaks
To avoid artificial choropleth distortions, trade intensity is segmented using **Jenks Natural Breaks optimization**:
- Minimizes within-class variance while maximizing between-class variance across 31 European nations.
- Eliminates misleading linear color gradients, highlighting localized industrial clusters and import-dependent zones.

---

## 💻 Multi-Modal Architecture & Deliverables

```
European_Trade_Transformation/
├── The European trade’s silent transformation.Rmd    # Complete 73KB automated ETL and visualization pipeline
├── The European trade’s silent transformation.pbix   # Executive Power BI dashboard
├── The European trade’s silent transformation.twb    # Interactive Tableau workbook
└── The European trade’s silent transformation/       # Compiled high-resolution (200 DPI) vector charts
```

### Reproducibility
```r
# Install required packages
install.packages(c("eurostat", "tidyverse", "sf", "scales", "classInt"))

# Render complete R Markdown analysis
rmarkdown::render("The European trade’s silent transformation.Rmd")
```

---

**Author:** Francesco Colombini  
[GitHub Profile](https://github.com/FRA-0023) · [LinkedIn](https://www.linkedin.com/in/francescocolombini/)