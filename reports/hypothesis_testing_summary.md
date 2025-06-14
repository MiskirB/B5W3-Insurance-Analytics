Task 3 - Hypothesis Testing Summary
This analysis evaluates whether certain policyholder attributes lead to statistically significant differences in insurance risk, measured through:

Claim Frequency: Proportion of policies that resulted in at least one claim.

Claim Severity: Average size of claims when they occur.

Margin: Total Premium minus Total Claims.

We tested four null hypotheses using A/B segmentation and two-sample t-tests.

🧪 Hypothesis Test Results
Test Metric Group A (Mean) Group B (Mean) p-value Decision
Province (Gauteng vs WC) Claim Frequency 0.00 0.00 0.0000 Reject H₀
Province (Gauteng vs WC) Claim Severity 22,244 28,096 0.0306 Reject H₀
Zip Code (1459 vs 8001) Claim Frequency 0.00 0.00 0.3177 Fail to Reject H₀
Zip Code (1459 vs 8001) Claim Severity N/A 17,275 N/A Fail to Reject H₀
Zip Code (1459 vs 8001) Margin 73.87 -4.69 0.0087 Reject H₀
Gender (Male vs Female) Claim Frequency 0.00 0.00 0.8372 Fail to Reject H₀
Gender (Male vs Female) Claim Severity 14,859 17,875 0.5680 Fail to Reject H₀

📌 Key Insights & Recommendations
✅ Province matters: Gauteng and Western Cape have significantly different claim behavior. Consider regional premium adjustments.

✅ Profitability differs by Zip Code: Even without higher claim risk, certain zip codes show profitability differences — valuable for pricing strategy.

🚫 Gender does not impact claim risk: Supports gender-neutral pricing.

🚫 Zip Code claim risk is similar: Reinforces location-level adjustments may be more margin- than risk-driven.
