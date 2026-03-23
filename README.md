# Dallas Housing Needs Assessment

This repository contains a housing needs assessment for the City of Dallas using ACS PUMS data.

## Contents

- `dallas_housing_assessment.ipynb`: modular analysis workflow
- `dallas_housing_assessment_report.pdf`: summary findings and policy implications
- `charts/`: exported figures used in the report
- `tables/`: summary tables generated from the analysis

## Approach

The analysis estimates households below 60% AMI and identifies those paying more than 30% of income toward housing costs. It compares demographic characteristics and identifies key indicators of cost burden.

The workflow is structured as a set of reusable functions for:

- income classification  
- cost burden calculation  
- summary table generation  
- chart production  

This structure allows the analysis to be adapted to other cities or ACS releases.

## Notes

- AMI thresholds are based on provided inputs  
- Results are directional estimates based on PUMS sample data  

## Limitations

- AMI thresholds reflect an earlier income-limit vintage than the ACS / PUMS data; aligning vintages would improve accuracy.  
- PUMS is a sample dataset, so all results should be interpreted as estimates.  
- PUMA geography approximates, but does not perfectly match Dallas city boundaries.  
- Renter and owner housing cost measures are not directly comparable.  
- Zero or negative income cases are treated as missing for burden calculations rather than forced into extreme ratios.  
- Race / ethnicity is based on the household reference person and does not capture full household composition.  
- `SERIALNO` does not function as a reliable unique household identifier in this extract, limiting certain linkage and deduplication checks.  

## Workflow and Next Steps

The analysis is structured as a modular workflow separating:

- income classification  
- cost burden calculation  
- summary outputs  
- chart generation  

This structure supports reuse across ACS releases, adaptation to other geographies, and integration into a dashboard-based analytical tool.

In a production setting, this workflow could be extended to support automated data refreshes and interactive dashboard delivery.
