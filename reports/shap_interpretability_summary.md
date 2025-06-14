# 📊 Task 4: SHAP Interpretability Summary

## 🔍 Objective

Interpret the **Random Forest model** used to predict **TotalClaims** using **SHAP (SHapley Additive Explanations)** to understand which features most influenced the predictions.

## ✅ Dataset Details

- **Model Used**: Random Forest Regressor
- **Data Subset**: First 100 samples where `TotalClaims > 0`
- **Features Used**:
  - Province
  - VehicleType
  - RegistrationYear
  - make
  - SumInsured
  - CalculatedPremiumPerTerm

---

## 🔧 SHAP Results Breakdown

### 1. SHAP Beeswarm Plot

![SHAP Beeswarm](shap_beeswarm.png)

- **Explanation**: Each dot represents a SHAP value for a feature in one prediction. The horizontal spread indicates impact magnitude. Colors represent the feature value (blue = low, red = high).

- **Key Findings**:
  - Feature 43, 42, and 41 dominate influence — likely derived from encoded `make`, `Province`, or `VehicleType`.
  - Positive SHAP values push predictions **higher**, while negative SHAP values reduce them.

### 2. SHAP Feature Importance Plot

![SHAP Feature Importance](shap_feature_importance.png)

- **Explanation**: This bar plot ranks features by average absolute SHAP values.
- **Top Influencers**:
  - Feature 43, 42, 41: Encoded categorical values.
  - SumInsured and CalculatedPremiumPerTerm: Strong numeric drivers of predicted claim severity.

---

## 📘 Business Interpretation & Recommendations

- **Premium Calibration**: High `SumInsured` and `PremiumPerTerm` are associated with high claims — these should be emphasized in risk pricing.
- **Regional Pricing**: Differences among encoded `Province` or `VehicleType` indicators suggest that **regional** or **vehicle-based** pricing should be considered.
- **Actionable Insight**:
  - Refactor premium structure to emphasize most impactful variables.
  - Potentially remove low-impact variables from the pricing formula.

---

## 🗂️ Files Saved

| File Type               | Path                                             |
| ----------------------- | ------------------------------------------------ |
| SHAP Beeswarm Plot      | `outputs/task4/shap/shap_beeswarm.png`           |
| SHAP Feature Importance | `outputs/task4/shap/shap_feature_importance.png` |
| Summary Text File       | `outputs/task4/shap/shap_summary.txt`            |
