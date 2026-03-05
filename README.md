### Executive Summary

This analysis evaluates the performance of an advertising campaign by comparing a 'test group' that saw ads against a 'control group' that saw Public Service Announcements (PSAs). The key metric is **conversion rate** (user converted to the desired action).

The main findings are:
1.  The **advertising campaign was effective**, leading to a statistically significant increase in conversion rates compared to the PSA group.
2.  **Monday has the highest conversion rate**, while Saturday has the lowest. Weekdays generally outperform weekends.
3.  **Early morning hours (2 AM - 4 AM) have extremely low conversion rates**, while late afternoon and early evening (4 PM - 9 PM) show the highest user engagement and conversion.
4.  Users who **convert view significantly more ads** than those who do not, indicating a clear relationship between ad exposure and conversion.

Based on these insights, recommendations are provided to optimize ad spend, schedule campaigns more effectively, and refine user targeting.

---

### Detailed Insights and Recommendations

#### 1. Ad Effectiveness

*   **Insight (from cells 36 & 48):** The analysis strongly indicates that the advertising campaign was successful. The conversion rate for the **ad group (2.55%) is significantly higher** than for the **PSA group (1.79%)**. A Chi-squared test was performed, yielding a p-value of 0.00000, confirming that this difference is statistically significant and not due to random chance.

*   **Recommendation:**
    *   **Continue & Scale:** Continue running the ads, as they have a proven positive impact on conversions. Consider increasing the budget for this campaign, but do so carefully while monitoring performance to ensure the increased spend remains cost-effective.

#### 2. Optimal Days for Advertising

*   **Insight (from cells 26, 39 & 48):** The analysis of conversion rates by day of the week reveals a clear pattern.
    *   **Best Day:** **Monday** has the highest conversion rate (3.28%).
    *   **Worst Days:** **Saturday (2.11%)** and **Thursday (2.16%)** show the lowest conversion rates.
    *   The Chi-squared test (p-value 0.00000) confirms that the day of the week has a significant impact on conversion.

*   **Recommendation:**
    *   **Optimize Ad Scheduling:** Shift a higher proportion of the ad budget to **Mondays, Tuesdays, and Wednesdays** to capitalize on higher user engagement and conversion intent.
    *   **Reduce Spend on Weekends:** Significantly reduce ad spend on **Saturdays** and consider lowering it on **Thursdays and Fridays** as well, as these days underperform compared to the start of the week. Re-allocate this budget to higher-performing days.

#### 3. Optimal Hours for Advertising

*   **Insight (from cells 31, 40 & 48):** The data shows strong hourly trends in user conversion.
    *   **Best Hours:** The hours with the highest conversion rates are **16 (3.08%), 20 (2.98%), and 15 (2.97%)**. This points to late afternoon and early evening as the prime time for engagement.
    *   **Worst Hours:** The hours from **2 (0.73%), 3 (1.05%), and 1 (1.29%)** in the early morning are the absolute worst for conversions, with rates far below average.
    *   The Chi-squared test (p-value 0.00000) confirms the hour of the day is a highly significant factor.

*   **Recommendation:**
    *   **Time-of-Day Targeting:** Implement strict time-based targeting. Concentrate ad delivery between **4 PM and 9 PM** to maximize conversion efficiency.
    *   **Pause During Inactive Hours:** **Completely pause or dramatically reduce bids** during the early morning hours (midnight to 6 AM) to avoid wasting budget when users are not responsive. The slight activity during these hours is likely not cost-effective.

#### 4. Relationship Between Ad Exposure and Conversion

*   **Insight (from cells 42 & 53):**
    *   **Box Plot Analysis:** The box plots clearly show a strong positive correlation. Users who converted (`converted=True`) have a much higher median and a much wider range for the number of ads viewed compared to users who did not convert. This suggests that higher ad exposure is linked to conversion.
    *   **Statistical Testing:** The Shapiro-Wilk test confirms that the data is not normally distributed, making a non-parametric test the correct choice. The subsequent Mann-Whitney U Test (p-value = 0.0) confirms a statistically significant difference between the two groups.

*   **Recommendation:**
    *   **Focus on User Engagement:** While causality cannot be definitively proven (it could be that more interested users both see more ads and convert), the data strongly suggests that increasing a user's ad exposure is crucial. This supports strategies that aim to increase frequency and reach.
    *   **Frequency Capping:** While the goal is to increase exposure, consider implementing frequency capping to avoid ad fatigue. The analysis shows diminishing returns with very high ad counts (the upper outliers for non-converters are also very high), suggesting that beyond a certain point, showing more ads doesn't necessarily lead to conversion.

### Summary of Key Takeaways

| Feature | Top Performers | Bottom Performers | Statistical Significance |
| :--- | :--- | :--- | :--- |
| **Campaign Type** | **Ad Group** | **PSA Group** | **Yes** |
| **Day of Week** | **Monday, Tuesday, Wednesday** | **Saturday, Thursday** | **Yes** |
| **Hour of Day** | **4 PM - 9 PM** | **2 AM - 5 AM** | **Yes** |
| **Ad Exposure** | **Higher number of ads viewed** | **Lower number of ads viewed** | **Yes** |
