# -time_series_hepB_analysis.R
# Time Series Analysis on Hepatitis B Infection in the Ashanti Region

## 📊 Project Overview
This repository contains the statistical framework and data workflows developed for my final-year undergraduate dissertation in **BSc Statistics at Kwame Nkrumah University of Science and Technology (KNUST)**. The project constructs a predictive model for monthly epidemiological trends of Hepatitis B transmission using historical clinical surveillance datasets sourced from the **Komfo Anokye Teaching Hospital (KATH)**.

## 🔬 Methodology & Statistical Framework
The modeling workflow follows the strict **Box-Jenkins methodology** alongside exponential smoothing diagnostic checks:
*   **Stationarity Transformation:** Diagnosed via the Augmented Dickey-Fuller (ADF) test, requiring a structural first-differencing (\(d=1\)) to stabilize volatile mean variances.
*   **Model Selection Criteria:** Candidate configurations were evaluated using Maximum Likelihood Estimation and optimized using the **Akaike Information Criterion (AIC)** to balance parsimony and explanatory precision.

### 📈 Model Optimization Metrics Evaluated:

| Candidate Model Tier | Log-Likelihood | AIC Value | Selection Status |
| :--- | :--- | :--- | :--- |
| **SARIMA(0,1,1) × (0,1,0)₁₂** | **-170.62** | **345.25** | **Selected / Optimal** |
| SARIMA(1,1,0) × (0,1,0)₁₂ | -167.44 | 358.88 | Rejected |
| ARIMA(1,1,0) | -221.10 | 446.20 | Rejected |

*   **Residual Diagnostics:** Residual validations were systematically verified using the **Ljung-Box Portmanteau test** to confirm independence (ensuring white noise behavior) and **Shapiro-Wilk calculations** to confirm residual normality.
*   **Forecasting Variant:** Comparative projection metrics were cross-evaluated alongside a parallel additive **Holt-Winters exponential smoothing model** using Mean Square Error (MSE) and Mean Absolute Percentage Error (MAPE).

## 🛠️ Core Toolkit
*   **Language:** R
*   **Primary Packages:** `forecast`, `tseries`, `ggplot2`
*   **Alternative Systems:** SPSS, MS Excel (Data Analysis Toolpak)
