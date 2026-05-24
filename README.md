# Medicare-Dashboard
Power BI dashboard using CMS Provider Data to compare hospital quality and cost. KPIs include hospital count, Avg ERR, and readmission rate. Visuals show Top 10 worst states by Avg ERR, a facility-level table, and an MSPB vs readmissions scatter by state with trendline and filters.

# Medicare Quality vs Cost Dashboard (Power BI)

## Overview
This Power BI report explores the relationship between **hospital cost efficiency** and **readmission performance** using CMS Provider Data. The goal is to quickly identify where spending is higher/lower than expected (MSPB) and how that relates to readmissions (ERR / readmission counts).

## Data Sources (CMS Provider Data)
This report uses CMS Provider Data exports (CSV):
- **Hospital General Information** (hospital attributes + location)
- **Hospital Readmissions Reduction Program (HRRP) – FY 2026** (ERR, predicted vs expected, discharges/readmissions)
- **Medicare Spending Per Beneficiary (MSPB)** (spending score)
- **HCAHPS (Patient Experience)** (survey response/experience fields; included for future expansion)

## Data Model
- **Hub table:** `Hospital_General_Information`
- Relationships use **Facility ID** as the key.
- Star-style layout: General Info filters the other datasets.

## Key Metrics (KPIs)
- **Hospitals**: distinct hospital count in the current filter context
- **Avg ERR**: average Excess Readmission Ratio (ERR ≈ 1.0 is “as expected”; >1.0 is worse)
- **Readmission Rate**: readmissions ÷ discharges (volume-adjusted)

## Visuals Included
- **Facility-level table**: Facility ID, Facility Name, MSPB Score, and Avg ERR for quick scanning
- **Top 10 worst states by Avg ERR**: highlights states with the highest average ERR (worse-than-expected readmissions)
- **MSPB vs Readmissions scatter (by state)**: compares average MSPB score to total readmissions with a trendline

## How to Use
1. Download/open the `.pbix` file in **Power BI Desktop**
2. Use filters/slicers (e.g., State) to explore different regions
3. Hover over points/bars to view tooltips and compare outliers

## Interpretation Notes
- **ERR (Excess Readmission Ratio)** is a risk-adjusted ratio:
  - ~**1.0** = in line with national expectations
  - **> 1.0** = higher-than-expected readmissions (worse)
  - **< 1.0** = lower-than-expected readmissions (better)
- **MSPB Score**:
  - ~**1.0** = expected spending
  - **> 1.0** = higher spending than expected
  - **< 1.0** = lower spending than expected
- The scatter using **total readmissions** is influenced by **state size/volume**. For a cleaner comparison, use **readmission rate** or **Avg ERR**.

## Future Improvements
- Add a “Patient Experience” page using HCAHPS (response rate + key survey measures)
- Add quadrant lines at **MSPB=1.0** and **ERR=1.0** to highlight best/worst regions
- Add Top 10 “best” states (lowest Avg ERR) for contrast

## Screenshots
Add screenshots here (optional):
# Medicare Quality vs Cost Dashboard (Power BI)

## Overview
This Power BI report explores the relationship between **hospital cost efficiency** and **readmission performance** using CMS Provider Data. The goal is to quickly identify where spending is higher/lower than expected (MSPB) and how that relates to readmissions (ERR / readmission counts).

## Data Sources (CMS Provider Data)
This report uses CMS Provider Data exports (CSV):
- **Hospital General Information** (hospital attributes + location)
- **Hospital Readmissions Reduction Program (HRRP) – FY 2026** (ERR, predicted vs expected, discharges/readmissions)
- **Medicare Spending Per Beneficiary (MSPB)** (spending score)
- **HCAHPS (Patient Experience)** (survey response/experience fields; included for future expansion)

## Data Model
- **Hub table:** `Hospital_General_Information`
- Relationships use **Facility ID** as the key.
- Star-style layout: General Info filters the other datasets.

## Key Metrics (KPIs)
- **Hospitals**: distinct hospital count in the current filter context
- **Avg ERR**: average Excess Readmission Ratio (ERR ≈ 1.0 is “as expected”; >1.0 is worse)
- **Readmission Rate**: readmissions ÷ discharges (volume-adjusted)

## Visuals Included
- **Facility-level table**: Facility ID, Facility Name, MSPB Score, and Avg ERR for quick scanning
- **Top 10 worst states by Avg ERR**: highlights states with the highest average ERR (worse-than-expected readmissions)
- **MSPB vs Readmissions scatter (by state)**: compares average MSPB score to total readmissions with a trendline


## Interpretation Notes
- **ERR (Excess Readmission Ratio)** is a risk-adjusted ratio:
  - ~**1.0** = in line with national expectations
  - **> 1.0** = higher-than-expected readmissions (worse)
  - **< 1.0** = lower-than-expected readmissions (better)
- **MSPB Score**:
  - ~**1.0** = expected spending
  - **> 1.0** = higher spending than expected
  - **< 1.0** = lower spending than expected
- The scatter using **total readmissions** is influenced by **state size/volume**. For a cleaner comparison, use **readmission rate** or **Avg ERR**.

## Screenshots
<img width="2092" height="1167" alt="Medicare powerbi" src="https://github.com/user-attachments/assets/437aae2e-c6ea-49da-9614-9be8f96b0cdc" />

