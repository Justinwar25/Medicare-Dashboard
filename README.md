Overview:


This Power BI dashboard compares hospital quality and cost efficiency using CMS Provider Data. It helps identify where spending is higher/lower than expected (MSPB) and how that relates to readmission performance (ERR + readmission rate/volume).

Data Sources (CMS Provider Data)

CSV exports used:

Hospital General Information (hospital attributes + location)
Hospital Readmissions Reduction Program (HRRP) – FY 2026 (ERR, predicted vs expected, discharges/readmissions)
Medicare Spending Per Beneficiary (MSPB) (spending score)
HCAHPS (Patient Experience) (survey fields; included for possible expansion)
Data Model
Hub table: Hospital_General_Information
Key: Facility ID
Star-style layout: General Info filters the other datasets.
Key Metrics (KPIs)
Hospitals: distinct count in the current filter context
Avg ERR: average Excess Readmission Ratio
Readmission Rate: readmissions ÷ discharges (volume-adjusted)
Visuals Included
Facility-level table: Facility ID, Facility Name, MSPB Score, Avg ERR
Top 10 worst states by Avg ERR: highlights states with the highest Avg ERR (worst performance)
MSPB vs Readmissions scatter (by state): Avg MSPB vs total readmissions with trendline + filters
Interpretation Notes
ERR (Excess Readmission Ratio)
~1.0 = in line with national expectations
> 1.0 = higher-than-expected readmissions (worse)
< 1.0 = lower-than-expected readmissions (better)
MSPB Score
~1.0 = expected spending
> 1.0 = higher spending than expected
< 1.0 = lower spending than expected

Note: Total readmissions in the scatter are influenced by state size/volume. For cleaner comparisons, use Readmission Rate or Avg ERR.

How to Use
Open the .pbix in Power BI Desktop
Use filters/slicers (ex: State) to explore regions
Hover points/bars for quick outlier comparisons
Future Improvements
Add a Patient Experience page (HCAHPS response rate + key survey measures)
Add quadrant lines at MSPB = 1.0 and ERR = 1.0
Add a Top 10 best states (lowest Avg ERR) for contrast
Screenshots

<img width="2092" height="1167" alt="Medicare powerbi" src="https://github.com/user-attachments/assets/437aae2e-c6ea-49da-9614-9be8f96b0cdc" />

