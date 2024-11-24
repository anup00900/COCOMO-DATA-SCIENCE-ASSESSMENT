# Media Data Analysis and A/B Testing

## Overview
This project analyzes media data to evaluate the impact of various marketing channels (Google, Facebook, Email, Affiliates, YouTube) on revenue. It uses machine learning models and statistical tests to determine the most influential channels, assess spending efficiency, and provide actionable recommendations. Additionally, an A/B test is conducted to evaluate the impact of increasing Google spend by 20% on revenue.

---

## Objectives
1. Identify marketing channels that most influence revenue.
2. Evaluate the efficiency of budget allocation across channels.
3. Explore geo-specific differences in channel performance.
4. Conduct an A/B test to determine the impact of increased Google spend.
5. Provide actionable recommendations for optimizing campaigns and spend.

---

## Features
### 1. **Exploratory Data Analysis (EDA)**
- Correlation matrix to explore relationships between revenue and marketing channels.
- ROI analysis to identify the most and least efficient marketing channels.
- Seasonal trend analysis to align campaigns with high-revenue periods.

### 2. **Machine Learning Models**
- **Model Used**: XGBoost Regressor.
- **R² Score**: 0.78 (indicating strong model performance).
- Feature importance analysis to determine which channels contribute the most to revenue.

### 3. **A/B Testing**
- **Groups**:
  - **Group A**: Increased Google spend by 20% with optimized targeting.
  - **Group B**: Control group with current spend and targeting strategy.
- **Statistical Results**:
  - T-Statistic: **-2.54**, P-Value: **0.011**
  - The difference in revenue between Group A and Group B is statistically significant.

### 4. **Geo-Level Analysis**
- Examined differences in channel efficiency across geographies.
- Recommended geo-specific budget allocation based on performance.

### 5. **Seasonal Campaign Analysis**
- Weekly trends identified peak and low-revenue periods.
- Recommendations provided for aligning campaigns with seasonal trends.

---

## Key Results
1. **Most Influential Channels**:
   - Google Impressions, Facebook Impressions, and Email Campaigns drive the most revenue.
2. **ROI Analysis**:
   - Google Ads and Email Campaigns show the highest ROI.
   - Affiliate Marketing and YouTube have the least impact and low ROI.
3. **A/B Test Insights**:
   - Increasing Google spend by 20% did not yield better revenue compared to the control group.
4. **Seasonal Trends**:
   - Identified high-revenue weeks for optimal campaign alignment.

---

## Recommendations
1. **Optimize Spending**:
   - Increase budgets for **Google Ads** and **Email Campaigns** (high ROI).
   - Reduce or reallocate spending on **Affiliate Marketing** and **YouTube** (low ROI).
2. **Geo-Specific Strategies**:
   - Tailor budgets and campaigns based on regional performance.
3. **Seasonal Adjustments**:
   - Focus on high-revenue weeks for maximum ROI.
   - Introduce promotions during low-revenue weeks to stabilize performance.
4. **Multi-Channel Synergies**:
   - Combine **Google Ads** and **Facebook Ads** to leverage synergies.

---

## Installation and Usage

```bash
git clone https://github.com/your-repo/media-data-analysis.git
cd media-data-analysis

pip install -r requirements.txt

├── media_data.csv           # Input dataset
├── analysis.py              # Main analysis script
├── README.md                # Project documentation
├── requirements.txt         # Python dependencies
├── feature_importance.csv   # Feature importance results
├── roi_summary.csv          # ROI analysis results
├── geo_efficiency.csv       # Geo-specific efficiency metrics

