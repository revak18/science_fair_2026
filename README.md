# AI Data Center Load Scheduling for Grid and Water Efficiency

## Overview
This project investigates whether flexible scheduling of AI workloads can reduce electricity grid stress and power-generation water consumption.

A Mixed-Integer Linear Programming (MILP) model schedules deferrable AI jobs while respecting job deadlines, grid capacity constraints, and water consumption limits.

## Methodology
- Uses historical hourly electricity demand and Water IMPACT data.
- Analyzes two PJM regions: PJME and COMED.
- Simulates AI loads at 10%, 20%, and 30% of regional peak demand.
- Optimizes scheduling over 48-hour windows using PuLP.
- Compares optimized scheduling against immediate and random scheduling.
- Runs 30 trials per scenario to evaluate consistency.
- Analyzes trade-offs between natural gas capacity requirements and peak water consumption.

## Code
`science_fair_2026_final_code.ipynb` contains the data preprocessing, workload simulation, MILP optimization, baseline comparisons, statistical analysis, and visualizations.

## Requirements
Python, NumPy, Pandas, Matplotlib, and PuLP.

The notebook runs in Google Colab and requires historical electricity load data and Water IMPACT consumption data in the configured Google Drive directory.

## Outputs
The analysis generates CSV results and visualizations showing:
- Natural gas capacity savings (MW)
- Peak water consumption (m³/h)
- Improvements relative to baseline scheduling
- Pareto trade-offs between grid capacity and water consumption
