# Stochastic-LCOS-of-FB
A comprehensive Python visualization suite for techno-economic analysis of flow battery chemistries, focusing on Levelized Cost of Storage (LCOS) calculations with stochastic modeling and risk assessment.

## Overview

This open-source script provides a complete framework for analyzing and comparing different flow battery chemistries through:
- **Deterministic LCOS ranking** with economic benchmarks
- **Monte Carlo simulation** with 10,000-run stochastic modeling
- **Risk-return analysis** incorporating energy density metrics
- **Comprehensive visualization** with publication-ready figures

## Features

### 🔋 **Multi-Chemistry Support**
- 8 flow battery chemistries: V-H₂, V-Zn, V-Br, V-Ce, V-Mn, V-Fe, V-V (Baseline), V-O₂
- Energy density integration (15-65 Wh L⁻¹)
- Baseline comparison with V-V system

### 📊 **Advanced Economic Modeling**
- **DOE target benchmarking** (0.05 USD/kWh·cycle)
- **20% reduction threshold** analysis from baseline
- **Monte Carlo simulation** with skewed distributions
- **Value-at-Risk (VaR)** calculations at 95% confidence

### 📈 **Publication-Ready Visualizations**
- **Figure 1**: Deterministic ranking with economic thresholds
- **Figure 2**: Stochastic distributions with confidence intervals
- **Figure 3**: Risk-return bubble chart with energy density scaling
- **Sequential layout** for progressive analysis

## Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/flow-battery-lcos-analysis.git
cd flow-battery-lcos-analysis

# Install dependencies
pip install matplotlib numpy scipy
```

## Requirements

- Python ≥ 3.7
- matplotlib ≥ 3.3
- numpy ≥ 1.19
- scipy ≥ 1.5

## Usage

```python
# Import the analysis function
from flow_battery_analysis import create_sequential_lcos_analysis

# Run the complete analysis
create_sequential_lcos_analysis()
```

## Economic Parameters

**Default Assumptions:**
- **WACC**: 8%
- **Cycle frequency**: 1 cycle/day
- **System lifetime**: 20 years
- **Currency**: 2025 USD

**Key Benchmarks:**
- DOE target: 0.05 USD/kWh·cycle
- 20% reduction threshold from V-V baseline

## Output Summary

The script generates:
1. **Three sequential figures** with comprehensive LCOS analysis
2. **Summary table** with key metrics for all chemistries
3. **Risk metrics** including Sharpe ratios and VaR calculations

### Sample Output
```
COMPREHENSIVE FLOW BATTERY ANALYSIS SUMMARY
================================================================================
Chemistry        LCOS     Risk     ED (Wh/L)    Sharpe Ratio
--------------------------------------------------------------------------------
V-H₂            0.062    0.008    65           1.50
V-Zn            0.069    0.009    50           1.11
...
================================================================================
```

## Customization

### Modifying Chemistry Data
```python
# Update energy density values
energy_density = {
    'V-H₂': 65,    # Wh L⁻¹
    'V-Zn': 50,    # Wh L⁻¹
    # Add your custom values
}

# Adjust distribution parameters
dist_params = {
    'Your-Chemistry': {
        'mean': 0.070,      # Expected LCOS
        'std': 0.007,       # Standard deviation
        'skew': 0.3         # Skewness factor
    }
}
```

### Changing Economic Parameters
```python
# Modify benchmark targets
doe_target = 0.05           # USD/kWh·cycle
reduction_threshold = 0.8   # 80% of baseline (20% reduction)
```

## Methodology

### LCOS Calculation
Based on NREL methodology with:
- Capital expenditure (CAPEX) amortization
- Operational expenditure (OPEX) projections
- Efficiency degradation modeling
- End-of-life considerations

### Stochastic Modeling
- **Distribution**: Lognormal with skewness adjustment
- **Simulation**: 10,000 Monte Carlo runs
- **Confidence intervals**: 95% two-tailed
- **Risk metrics**: VaR(95%) and Sharpe ratios

## Applications

- **Research institutions**: Comparative techno-economic analysis
- **Industry stakeholders**: Technology benchmarking
- **Policy makers**: Cost target assessment
- **Investors**: Risk-return evaluation

## Contributing

We welcome contributions! Please see our [Contributing Guide](CONTRIBUTING.md) for:
- Code style guidelines
- Testing procedures
- Pull request process

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Citation

If you use this tool in your research, please cite:

```bibtex
@software{flow_battery_lcos_2026,
  title={Flow Battery LCOS Analysis Tool},
  author= Kourosh Khaje (PhD),
  year={2026},
  url={https://https://github.com/kourosh-khaje/Stochastic-LCOS-of-FB}
}
```

## Contact

For questions or suggestions:
- Create an [Issue](https://github.com/yourusername/flow-battery-lcos-analysis/issues)
- Email: kourosh.khaje@gmail.com
- Discussion forum: [GitHub Discussions](https://github.com/yourusername/flow-battery-lcos-analysis/discussions)

---

**Keywords**: flow battery, LCOS, techno-economic analysis, Monte Carlo simulation, energy storage, vanadium redox, risk assessment
