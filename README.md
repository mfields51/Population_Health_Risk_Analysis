# Population Health Risk Analysis

## Project Overview
This repository contains an end-to-end data pipeline and interactive business intelligence dashboard modeling a self-funded employer health plan (1,336 covered members). Utilizing an automated Python preprocessing notebook and a two-page Power BI executive layout, the project isolates financial leakage points, maps clinical care risks, and evaluates demographic cost metrics to drive target wellness interventions.

## The Business Problem
The self-funded plan sponsor experienced an inflationary spike in overall healthcare claims expenditures, totaling $17.75M. 
This dashboard risk-stratifies the covered lives to find unmanaged risk factors, locate geographic cost exposure, and provide data-driven cost-containment recommendations.

## Data Pipeline & Methodology
1. Data Ingestion & Validation (Python / Pandas): Audited raw health plan datasets via a Jupyter Notebook pipeline. Successfully flagged and dropped duplicate member records to prevent the artificial inflation of financial exposure metrics.
2. Clinical Risk Stratification (Feature Engineering): Utilized vectorization techniques (`numpy.select`) to segment the population into three strategic healthcare risk cohorts:
   - Critical Risk: Plan members exhibiting high metabolic markers (BMI ≥ 30) paired with active tobacco utilization.
   - Moderate Risk: Plan members meeting either the BMI or tobacco risk criteria.
   - Low Risk: Non-tobacco-using plan members with standard metabolic markers.
3. Executive Visualization (Power BI): Created dynamic, decoupled DAX financial measures to power a 2-page report tracking total exposure, utilization correlation, and AI-driven root-cause influencers.

## Dashboard Architecture & Insights
![Page 1 Snapshot](page1_snapshot.png)
![Page 2 Snapshot](page2_snapshot.png)

### Page 1: Financial & Utilization Overview
- The Cost Disproportion: The analysis reveals that the Critical Risk tier represents just 10.85% of total plan membership (145 members), yet drives 33.9% of total plan spend ($6.02M). 
- The Claim Multiplier: Average individual claims for Critical Risk members exceed $41,500, compared to under $8,000 for Low Risk individuals.
- Visual Evidence: The scatter plot demonstrates an isolated, high-cost financial ceiling breaking away immediately after the BMI 30 threshold for active smokers.

### Page 2: Population Health & Wellness Strategy
- Geographic Risk Clusters: The Southeast territory drives the highest baseline expenditure ($5.3M), heavily influenced by a dense concentration of Moderate and Critical risk spending.
- Dependent Cost Tracking: Employees with zero dependents drive the absolute highest volume of plan spend, proving that cost-containment focus must center on primary employee wellness enrollment rather than dependent-heavy coverage tiers.
- Machine Learning Analysis: Leveraging Power BI's AI Key Influencers module, the data mathematically proves that active tobacco status is the primary root-cause driver of premium health plan spikes, increasing average member costs by an average of $23.61K.

## Strategic TPA Recommendations
1. Targeted Premium Incentives: Implement an outcomes-based premium structure pairing tobacco users with premium surcharges to offset elective financial plan risk.
2. Digital Wellness Intervention: Partner with a digital health management vendor to launch targeted metabolic and weight-management tracks in high-spend geographic sectors like the Southeast branch.

## Data Compliance & Integrity
This repository utilizes a fully anonymized public medical data model to simulate real-world TPA operations while strictly adhering to HIPAA data privacy principles and data masking guidelines.
