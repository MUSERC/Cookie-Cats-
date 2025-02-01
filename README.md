 Project Overview

This project presents an A/B testing analysis conducted on a mobile game, Cookie Cats, to evaluate the impact of different game versions on player retention.

The experiment compares two versions of the game:

-Gate 30
-Gate 40

The primary objective is to determine which version leads to higher player engagement and retention through statistical analysis and data-driven insights.

 Methodology & Key Steps

1 Data Exploration & Preprocessing
The dataset contains 90,189 user records, including information on game version, total play rounds, and retention status (Day 1 and Day 7).
An initial data quality check was performed to identify missing values and validate data integrity.

Key Observation:

The dataset is complete, with no missing values.

2 Retention Rate Analysis
Player retention is measured based on the percentage of users who return to the game after installation:

Day 1 Retention: Percentage of players who return after 1 day.
Day 7 Retention: Percentage of players who return after 7 days.
Game Version	Day 1 Retention	Day 7 Retention
Gate 30	44.82%	19.02%
Gate 40	44.23%	18.20%
Key Finding: Gate 30 exhibits higher player retention over a 7-day period.

3 Hypothesis Testing (A/B Test Validation)
To determine whether the observed differences in retention rates are statistically significant, the following tests were conducted:

Chi-Square Test: To evaluate the independence of retention rates across game versions.
Z-Test for Proportions: To measure the statistical difference in retention rates between Gate 30 and Gate 40.
Results:

Day 1 Retention: The p-value is 0.0744, indicating that the difference is not statistically significant.
![image](https://github.com/user-attachments/assets/cb5eade7-0c89-4430-bdb5-5f7e44b29f07)

Day 7 Retention: The p-value is 0.0016, indicating that Gate 30 significantly outperforms Gate 40 in long-term retention.
![image](https://github.com/user-attachments/assets/3c80a9ef-15ec-49fa-9c23-be6e13a81cab)

Conclusion: There is a statistically significant difference in player retention after 7 days, favoring Gate 30.
4 Power Analysis & Minimum Detectable Effect (MDE)
To assess the statistical power of our analysis, we calculated:

Minimum Detectable Effect (MDE): The smallest effect size that can be detected.
Z-Effect & Power Calculation: Determines the robustness of our results.
Results:

Retention Period	Power Score (1 - β)
Day 1	0.43 (Low Power) 
Day 7	0.89 (High Power) 
Conclusion: The Day 7 test has strong statistical power, whereas the Day 1 test requires a larger sample size for a conclusive result.

5 Outlier Detection & Impact on Analysis
Outliers in player behavior (e.g., users who played an unusually high number of rounds) were identified and removed using Z-score analysis.
![image](https://github.com/user-attachments/assets/80c5de2c-9480-4bad-ab01-60b5476d36c8)

Before outlier removal: The correlation between playtime and retention was positive.
After outlier removal: The correlation remained consistent, confirming that outliers did not significantly impact our conclusions.
![image](https://github.com/user-attachments/assets/0e05133b-96f1-4d56-8e51-23896e1e0707)

Key Finding: Players who engaged in longer play sessions had higher retention rates.

6 User Segmentation (Cohort Analysis)
Players were segmented based on:

Retention Behavior:
Day 1 Only: Players who returned on Day 1 but not on Day 7.
Day 7 Only: Players who did not return on Day 1 but engaged later.
Both: Players who stayed active on both days.
None: Players who did not return.
Total Play Rounds (sum_gamerounds):
0–10 rounds
10–50 rounds
50–100 rounds
100–500 rounds
500+ rounds
Key Insights from Cohort Analysis:


Players who played 100–500 rounds exhibited the highest retention rates.
Most long-term retained players fell within the 500–1000 rounds range.

![image](https://github.com/user-attachments/assets/124d1cb7-93a1-4083-bc77-5b5f24cd626d)


Business Recommendation:

Players with high engagement (100+ rounds) should be incentivized with in-game promotions to increase revenue.
Casual players (<50 rounds) may benefit from a lower difficulty curve in early stages to enhance retention.
7 Strategic Recommendations for Peak Games
Final Conclusion: Gate 30 is the more effective game version for retaining players.

Recommended actions:

Implement Gate 30 as the default version to maximize player retention.
Introduce in-game promotions and engagement incentives for users who play over 100 rounds.
Enhance the onboarding experience for users with low playtime (<50 rounds) to reduce early drop-off.
Conduct further A/B tests to refine in-game mechanics affecting player engagement.
