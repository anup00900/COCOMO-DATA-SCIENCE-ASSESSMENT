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
## Media Data Analysis: Answers to All Questions

---

## **1. Which marketing channels influence revenue the most? The least? How confident are you in these results?**

### **Results**:
- **Most Influential Channels**:
  - **Google Impressions (`GOOGLE_IMP`)**: Strongest feature importance, highest impact on revenue.
  - **Facebook Impressions (`FB_IMP`)**: Second-highest contributor, showing significant engagement effects.
  - **Email Impressions (`EMAIL_IMP`)**: Moderately influential, emphasizing the value of email campaigns.

- **Least Influential Channels**:
  - **Affiliate Impressions (`AFF_IMP`)**: Minimal impact on revenue.
  - **YouTube Impressions (`YT_PAID_IMP` and `YT_ORG_IMP`)**: Least influential based on low feature importance.

### **Confidence**:
- The model’s **R² score of 0.78** indicates a strong fit and reliable insights.
- A/B testing results further confirm statistically significant differences between test and control groups.

---

## **2. Is the business allocating spend across channels efficiently? If not, how would you reinvest or allocate your budget?**

### **Results**:
- **ROI Analysis**:
  - **Google Ads (`GOOGLE_SPEND`)**: Highest ROI, most efficient channel.
  - **Email Campaigns (`EMAIL_IMP`)**: High ROI, low spend, indicating untapped potential.
  - **Facebook Ads (`FB_SPEND`)**: Moderate ROI but with signs of diminishing returns at higher spend levels.
  - **Affiliate Marketing (`AFF_SPEND`)**: Lowest ROI, least efficient channel.

### **Recommendations**:
1. **Increase Spend**:
   - Reallocate budgets to **Google Ads** and **Email Campaigns** for maximum efficiency.
2. **Reduce Spend**:
   - Optimize or reduce spending on **Facebook Ads** and **Affiliate Marketing**.
3. **Experiment and Optimize**:
   - Conduct further A/B tests to identify optimal spend thresholds for underperforming channels.

---

## **3. Are there differences in channel efficiency across geos? Would you change your model to incorporate geo-level differences?**

### **Results**:
- Geo-level analysis highlighted significant regional differences:
  - **Google Ads** perform better in some geographies, while **Facebook Ads** dominate in others.
  - Certain regions underperform, suggesting targeting or messaging issues.

### **Model Insights**:
- Including geo-specific interaction terms (e.g., `GEO_GOOGLE_SPEND`) improved the model’s **R² score**, confirming the importance of regional differences.

### **Recommendations**:
1. **Geo-Specific Strategies**:
   - Allocate budgets based on regional performance.
   - Emphasize high-performing channels in regions where they dominate.
2. **Model Enhancements**:
   - Incorporate geo-specific features and explore advanced models like **Hierarchical Bayesian Models**.

---

## **4. Are there any other observations or recommendations you would make to the team?**

### **Observations**:
1. **A/B Test Results**:
   - Group B (control group) generated higher revenue despite lower Google spend, indicating diminishing returns in Group A.
2. **Seasonal Trends**:
   - Weekly revenue trends revealed high-revenue weeks where campaigns can be optimized for peak performance.
3. **Channel Synergies**:
   - Interaction effects (e.g., `GOOGLE_FB_SPEND`) suggested that combined campaigns (e.g., Google + Facebook) may amplify returns.

### **Recommendations**:
1. **Seasonal Campaign Adjustments**:
   - Focus efforts on high-revenue weeks.
   - Use targeted promotions during low-revenue weeks to stabilize performance.
2. **Optimize Spend**:
   - Avoid overspending on Facebook Ads and maintain focus on high-ROI channels.
3. **Leverage Multi-Channel Strategies**:
   - Combine Google and Facebook campaigns to enhance synergy effects.

---

## **5. A/B Testing Results**

### **Experiment Setup**:
- **Group A**: Increased Google spend by 20% and optimized targeting.
- **Group B**: Maintained current Google spend and targeting strategy.

### **Results**:
- **Average Revenue**:
  - **Group A**: $175,022
  - **Group B**: $196,326
- **Statistical Test Results**:
  - T-Statistic: **-2.54**
  - P-Value: **0.011**
  - The difference in revenue between the two groups is statistically significant (**p < 0.05**).

### **Insights**:
- Group B (control) outperformed Group A, suggesting diminishing returns on increased spend or inefficiencies in Group A’s targeting strategy.

---

## **6. Recommendations Based on A/B Test**

1. **Reassess Increased Spend**:
   - Avoid arbitrary increases in spend without considering diminishing returns.
   - Optimize targeting and ad quality instead of purely increasing spend.
   
2. **Test Alternative Strategies**:
   - Experiment with different ad creatives, keyword optimizations, and audience segmentation.
   
3. **Dynamic Budget Allocation**:
   - Use real-time performance metrics to allocate budgets dynamically to high-performing campaigns.

---

## **Summary**

This analysis provides actionable insights to improve marketing efficiency:
1. Focus on high-ROI channels (**Google Ads**, **Email Campaigns**) while reducing inefficient spend.
2. Tailor strategies regionally based on geo-specific performance.
3. Leverage seasonal trends and multi-channel synergies for maximum impact.
4. Conduct further A/B tests to refine spend thresholds and targeting strategies.

This structured approach ensures data-driven decisions to optimize marketing campaigns effectively.


## Installation and Answer to Questions

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

