# FB Stochastic Analysis

## Overview

This open-source script provides a complete framework for estimating levelized cost of storage (LCOS) across eight asymmetric flow-battery chemistries via deterministic ranking and 10 000-run Monte-Carlo risk analysis.

## Features

• Ready-to-run – only numpy, pandas, scipy, matplotlib required

• Compares V-V baseline vs. V-H₂, V-Zn, V-Br, V-Ce, V-Mn, V-Fe, V-O₂ (15–65 Wh L⁻¹)

• Validates against DOE target (0.05 USD kWh⁻¹ cycle⁻¹) and 20 % reduction threshold

• Outputs Markdown tables and publication-ready figures that can be pasted directly into papers or reports


## Methodology

NREL-style LCOS model coupled with log-normal Monte-Carlo simulation (10 000 runs, 95 % CI) to generate VaR(95 %) and risk-adjusted returns; bubble sizes scale with energy density.

## Applications

• Research institutions: Benchmark novel electrolyte formulations

• Industry stakeholders: Screen chemistries for MW-scale cost-down studies

• Policy makers: Assess cost-target feasibility for long-duration storage

• Investors: Risk-return evaluation under price uncertainty


## Contributing

We welcome contributions! Please see our Contributing Guide for code style, testing, and pull-request process.

## License

This project is licensed under the MIT License – see the LICENSE file for details.

## Citation

If you use this code in an academic work, please cite:

Khaje, K. (2026). Asymmetric FB Stochastic LCOS (v1.0). https://github.com/kourosh-khaje/FB-Stochastic-Analysis.git

## Contact

For questions or suggestions:

• Create an Issue

• Email: kourosh.khaje@outlook.com

• Discussion forum: GitHub Discussions

