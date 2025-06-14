EDA Summary Report - Task 1 (Insurance Analytics) by Miskir Besir Abshir
📁 Dataset Overview
The dataset contains 1,000,098 insurance records and 52 columns, including customer details, vehicle information, policy attributes, and financial metrics (e.g. premiums, claims). A few notable columns include:

TransactionMonth, Province, VehicleType, Gender

TotalPremium, TotalClaims, CustomValueEstimate

CoverType, Product, StatutoryRiskType

❓ Missing Value Snapshot
Key missingness observations:

Bank: ~14.6% missing

AccountType: ~4% missing

CustomValueEstimate: ~77.9% missing

WrittenOff, Rebuilt, Converted: ~64% missing

NumberOfVehiclesInFleet: 100% missing

🔢 Data Types & Transformations
TransactionMonth converted to datetime format

LossRatio calculated as TotalClaims / TotalPremium

Binary ClaimOccurred feature derived from TotalClaims > 0

📊 Key Visual Insights

1. Histogram of Financial Variables
   TotalPremium is heavily right-skewed, with most policies having low premiums.

TotalClaims is sparsely distributed with extreme outliers.

CustomValueEstimate is concentrated near lower values with limited distribution due to missingness.

2. Boxplot of TotalClaims
   Significant outliers are present in TotalClaims, suggesting that some customers file disproportionately large claims.

Most values are tightly packed near zero.

3. Monthly Trend: Premiums vs Claims
   Premiums and claims fluctuate over time, but the volume of claims tends to lag behind premium trends.

Several periods show significant spikes in premium revenue without proportional claim growth.

4. Average Loss Ratio by Province
   Provinces like Western Cape and KwaZulu-Natal show higher average loss ratios, indicating elevated risk profiles.

Limpopo and Free State exhibit relatively lower risk based on loss ratio.

5. Heatmap of Loss Ratio by Province and Vehicle Type
   Distinct patterns emerge, such as high loss ratios for Passenger Vehicles in Western Cape.

Vehicle types and regions interact in complex ways, suggesting the need for segmented premium strategies.

✅ Key Takeaways
There is considerable class imbalance and skew in the financial data.

Some provinces consistently show higher loss ratios.

Visual analysis supports the idea of segmenting customers based on region and vehicle type.

Missing data in vehicle valuation (CustomValueEstimate) and fleet indicators should be handled cautiously in later modeling stages.
