# Dallas Housing Needs Assessment

This repository contains a short housing needs assessment for the City of Dallas using ACS PUMS data.

## Contents

- `notebook.ipynb`: modular analysis workflow
- `report.pdf`: summary findings and policy implications
- `charts/`: exported figures used in the report

## Approach

The analysis estimates households below 60% AMI and identifies those paying more than 30% of income toward housing. It compares demographic characteristics and identifies key indicators of cost burden.

The workflow is structured as a set of reusable functions for:
- income classification
- cost burden calculation
- summary tables
- chart generation

This structure allows the analysis to be adapted to other cities or ACS releases.

## Notes

- AMI thresholds are based on provided inputs
- Results are directional estimates based on PUMS sample data
