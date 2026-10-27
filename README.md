# Mortality and Life Insurance Valuation

**Actuarial modeling, mortality forecasting and life insurance valuation**

## Overview

This project develops an actuarial framework for mortality analysis and life insurance valuation. It uses historical mortality data to construct life tables, forecast future mortality rates with the Lee-Carter model, and calculate the actuarial present values of life insurance and annuity contracts.

## Objectives

- Analyze historical mortality trends by age and year.
- Construct mortality tables and estimate death and survival probabilities.
- Implement the Lee-Carter model to forecast future mortality rates.
- Value term life insurance and life annuity contracts.
- Evaluate forecast accuracy and assess the sensitivity of actuarial values to key assumptions.
- Build an interactive Streamlit application for mortality analysis and life insurance valuation.

## Data

The project primarily uses data from the Human Mortality Database (HMD), focusing on French mortality statistics, subject to data availability and access conditions.

The analysis relies on historical mortality rates, deaths and population exposures by age and year.

Data source: [Human Mortality Database](https://www.mortality.org/)

See [`data/README.md`](data/README.md) for data provenance, access instructions, variable definitions and preprocessing conventions.

## Methodology

1. Exploratory analysis of historical mortality data.
2. Construction of mortality tables and calculation of death and survival probabilities.
3. Estimation of the Lee-Carter model using singular value decomposition (SVD).
4. Forecasting of the mortality index and reconstruction of future mortality rates.
5. Actuarial valuation of term life insurance and life annuity contracts.
6. Out-of-sample forecast validation and sensitivity analysis.

## Evaluation

The analysis considers mortality forecast errors, including RMSE and MAE, the accuracy of projected mortality rates, and the stability of forecasts across age groups and time horizons.

Actuarial valuation results are assessed through sensitivity analyses involving interest rates, mortality assumptions and alternative projection scenarios.

## Application

The Streamlit application allows users to explore historical mortality trends, visualize mortality projections, calculate survival probabilities and evaluate the actuarial present values of life insurance and annuity contracts under different assumptions.

## Installation

```bash
git clone https://github.com/YOUR-PSEUDO/mortality-life-insurance.git
cd mortality-life-insurance
python -m venv .venv
pip install -r requirements.txt
```

Activate the virtual environment before installing dependencies. See the setup instructions for your operating system.

## Project structure

- `notebooks/`: mortality exploration, model development and valuation experiments
- `src/`: reusable mortality, forecasting and actuarial valuation modules
- `tests/`: automated tests
- `app/`: interactive Streamlit application
- `reports/`: results, figures and analysis
- `docs/`: methodology, assumptions and limitations

## Limitations

Mortality forecasts are subject to statistical uncertainty, structural changes and model assumptions. The Lee-Carter model does not capture every possible source of mortality variation.

Actuarial values depend on the selected mortality table, discount rate, payment timing and contract assumptions. The project is educational and does not constitute regulated actuarial advice or a complete insurance valuation framework.

## Author

Toussaint B., Fathnelle M.

## License

See [`LICENSE`](LICENSE).
