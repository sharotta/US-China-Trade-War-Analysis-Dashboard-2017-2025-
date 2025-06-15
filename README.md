# US-China-Trade-War-Analysis-Dashboard-2017-2025-
Visualizes tariff escalation, trade imbalances, and inflation trends during the US–China trade war using public economic datasets.

## Project Overview

This analysis investigates:
- How tariffs between the U.S. and China evolved from 2018 to 2025
- Which sectors were most impacted by trade restrictions
- How bilateral trade flows shifted over time
- The real-world effects on U.S. consumer prices (CPI)

## Tools & Technologies

- **Power BI** (data modeling, DAX, Smart Narrative)
- **Microsoft Excel** (data prep & transformation)
- **DAX** (calculated columns, YoY/MoM %, time intelligence)

## Data Sources
  - U.S. Census Bureau (Trade data) https://usatrade.census.gov/
  - World Bank WITS https://wits.worldbank.org 
  - US Bureau of Labor Statistics https://data.bls.gov
  - Office of the U.S. Trade Representative (USTR) https://ustr.gov
  - WTO Tariff Database (For China’s retaliatory tariffs) https://www.wto.org

## Datasets 
  - U.S. Census Bureau—for historical import/export values by HS Code
  - World Bank (WITS)—for China’s trade data
  - USITC Tariff Timeline—to track tariff implementation events and affected sectors
  - U.S. Bureau of Labor Statistics (BLS)—for monthly Consumer Price Index (CPI) data per category
  - WTO Tariff Database (For China’s retaliatory tariffs) https://www.wto.org

## Data Processing Highlights
- Standardized tables and cleaned descriptions
- Appended trade data (imports + exports) and CPI by sector
- Created custom columns: Flow Direction, Trade Period
- Built a unified Date Table (Year, Month, Quarter)
- Managed many-to-many relationships (Tariff ↔ CPI ↔ Sector)
![Data Model](https://github.com/user-attachments/assets/6c8bb840-5599-4d78-88c0-dc7dcbc077a4)
  - Used `DAX` for:
  - YoY and MoM % Change
  - Tariff escalation tracking
  - Event count filtering

## Data Analytics & Visualization

### Page 1: Tariff Timeline (2018–2025)
![Tariff Timeline](https://github.com/user-attachments/assets/e3575e78-b0be-48ed-a6f8-3119b5ed0f86)
- 15 major tariff events recorded
- USA initiated 67% of tariff actions
- Avg U.S. tariff rate peaked at 67% in 2025
- China’s responses were more targeted but impactful in sectors like agriculture and consumer goods
- Key sectors affected: Technology, Apparel, Consumer Goods
- A strategic escalation timeline emerged:
   - 2018: Trade War Begins
   - 2019: Escalation Peaks
   - 2020: Phase 1 Deal offers partial relief
   - 2025: New wave of U.S. tariffs at 145%

### Page 2: U.S. Trade Flow
![USA TRADE](https://github.com/user-attachments/assets/57d14364-5588-4ba2-9609-5aa5827dc12e)
1. Decline in Bilateral Trade Post-Tariffs
- Total U.S. imports from China dropped sharply from $115B (pre-tariff) to $68.7B (post-tariff), a ~40% decline.
- U.S. exports to China also fell, but less severely, from $82B (pre-tariff) to $12B (post-tariff), an ~85% drop.
- The trade imbalance narrowed slightly, but the U.S. maintained a persistent deficit.
- Pre-Tariff (2017–2018): High trade volume in apparel, automotive, and technology.
- Post-Tariff (2019–2024): Significant contraction, especially in apparel and automotive imports.
2. U.S. Imports from China (Most Affected Sectors)
- Apparel (Knit & Woven)—Massive decline (e.g., from $0.51B to $0.07B in some categories).
- Automotive & Technology—Also saw sharp reductions, suggesting supply chain shifts.
- Telecommunications—Data indicates lower reliance on Chinese imports post-tariffs.
U.S. Exports to China 
- Agriculture & Automotive—Heavily impacted, with exports shrinking.
- Technology—declined, though less severely than other sectors.
3. U.S. Trade Balance: Limited Improvement Despite Tariffs
- Pre-Tariff Deficit (2017): -$98B
- Post-Tariff Deficit (2024): -$56B (a ~43% reduction but still substantial).
- U.S. demand for Chinese goods remains (despite tariffs).
- China reduced purchases of U.S. exports (e.g., agriculture, autos).
- Trade volumes stabilized in 2024 but at much lower levels than pre-tariff years.
- No major recovery in key sectors (apparel, automotive, tech), indicating lasting supply chain diversification.

### Page 3: China Trade Flow
![China ](https://github.com/user-attachments/assets/41734dba-93bd-4348-82d1-039bc838db06)
- China consistently held a trade surplus, exporting $491M and importing only $151M.
- Top exports post-2018 were electronics, apparel, and automotive.
- The trade balance remained positive every year, peaking in 2018 and stabilizing around $40M by 2024
- China maintained a strong surplus, exporting $491M to the U.S. while importing only $151M.

### Page 4: CPI Impact on U.S. Consumers
![CPI](https://github.com/user-attachments/assets/332cc270-644e-428a-a5a6-a28c7eee3b05)
1. Tariffs Drove Significant Price Increases in Key Sectors- Post-Tariff CPI Surges (2018–2025 vs. Pre-Tariff 2017)
- Apparel: +11.4% (Avg CPI rose from 125.61 → 139.91)
- Electronics: -4.3% (Avg CPI fell from 7.62 → 7.29), likely due to tech deflation trends outweighing tariffs.
- Energy Commodities: +27.6% (Avg CPI jumped from 216.28 → 276.11.)
- Motor Vehicles & Parts: +13.4% (Avg CPI up from 143.04 → 162.24)
- Key Inflation Peaks:
  - 2019 “Escalation Peaks” as tariffs took full effect.
  - 2025 New 145% tariffs on all goods led to another inflationary spike.
2. Sector-Specific CPI Trends
- Biggest Price Increases:
- Energy Commodities (27.6%)—Fuel and energy costs surged, partly due to trade disruptions.
- Apparel (11.4%)—Heavy tariffs on Chinese textiles drove up clothing prices.
- Motor Vehicles (13.4%)—Auto parts became more expensive as tariffs hit supply chains.
- Despite tariffs, electronics prices dropped (-4.3%), likely due to:
- Overproduction & tech deflation (e.g., cheaper chips, economies of scale).
- Substitution effects (U.S. buyers sourcing from Vietnam and Mexico).
3. The “145% tariffs on all goods” in 2025 suggest:
- Further price hikes in apparel, autos, and energy.
- Potential reversal in electronics deflation if alternative suppliers can’t keep up.
- The Phase 1 Deal (2020) temporarily eased prices, but 2025’s extreme tariffs could reignite inflation.
- Energy and apparel are most vulnerable to further trade restrictions.

## Challenges Encountered
- Could not extract from UN Comtrade; used U.S. Census instead
- Chinese trade data lacked product-level granularity
- Understanding HS Code classifications for mapping
- Building accurate many-to-many model relationships
- Backtracking to document cleaning steps mid-project

## Skills Demonstrated

- Power BI dashboard building (4 pages)
- Data modeling (1:* and *:* relationships, normalized structure)
- DAX measures (YoY %, MoM %, rolling averages, conditional logic)
- Time intelligence (using custom Date Table)
- Data cleaning (unpivoting, joining, column mapping in Power Query)
- Smart narrative writing & timeline annotations
- Sectoral analysis using HS Codes and CPI categorization

## Conclusion
- Tariff escalation doesn’t always shrink trade. U.S. imports stayed high even at 67%+ rates
- China’s export strategy pivoted but didn’t collapse. in fact, electronics exports grew
- Consumers felt the pinch, especially in energy and apparel

## Want to understand the full workflow, insights, and challenges?
- [Read the full Medium article here](https://medium.com/@sharon_dolapo_johnson/trade-wars-real-costs-how-i-visualized-the-impact-of-us-china-tariff-era-2017-2025-35f6ea0bf76c)
- [Connect with me on LinkedIn](https://www.linkedin.com/in/sharon-dolapo-johnson/)
  
## Final Reflection
This dashboard wasn’t just about policy and numbers; it was about building a bridge between data and real-world impact. It helped me refine my Power BI skills, navigate messy datasets, and communicate findings with clarity and context.

It’s also proof that data can humanize global economic decisions and tell stories that matter. From Policy to Prices: Linking Trade Actions to Real-World Inflation.

