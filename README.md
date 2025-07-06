# Phone_analysis

# A/B Test Analysis: Mobile Checkout Theme

## Objective

This project analyzes the results of an A/B test experiment aimed at improving the design of a product payment page. The goal is to determine if a new mobile checkout theme (`mobile_checkout_theme_new`) performs better than the old theme (`mobile_checkout_theme_old`) in terms of user engagement and conversion.

## Data

The analysis is based on the data provided in `experiment_raw.csv`. This file contains records of user interactions with both versions of the checkout page, including:

*   User ID
*   Date of interaction
*   Country
*   Operating System (OS)
*   The checkout theme shown to the user (test or control)
*   Whether a purchase was attempted
*   Whether a purchase was successful

## Methodology

The analysis was conducted using Python with the `pandas`, `scipy`, `matplotlib`, and `seaborn` libraries. The following tasks were performed:

1.  **Statistical Significance:** A **Chi-Squared test of independence** was used to determine if there is a statistically significant difference between the two themes in terms of:
    *   Purchase attempts
    *   Successful purchases

2.  **Operating System Segmentation:** The analysis was repeated for each major operating system (Android and iOS) to check if the new theme's performance varies across platforms.

3.  **Effect Stability Over Time:** The daily conversion rates (successful purchases / total users) for both themes were calculated and plotted over time to assess the stability of the observed effects.

## Files in this Project

*   `analysis.py`: The Python script that performs the complete analysis, including data loading, statistical tests, and plot generation.
*   `experiment_raw.csv`: The raw data file containing the experiment results.
*   `conversion_rates.png`: A visualization of the daily purchase success rates for both the new and old themes.

## How to Run the Analysis

1.  **Install Dependencies:**
    ```bash
    pip install pandas scipy matplotlib seaborn
    ```

2.  **Run the Script:**
    ```bash
    python analysis.py
    ```
    This will print the statistical results to the console and generate the `conversion_rates.png` image file.

## Summary of Findings

*   The new checkout theme shows a **statistically significant improvement** in both purchase attempts and successful purchases compared to the old theme.
*   This positive effect is consistent across both **Android and iOS** operating systems.
*   The improvement in conversion rates is **stable over time**, as shown in the daily performance plot.

## Conclusion

Based on the data, the new mobile checkout theme is a clear winner. It is recommended to **fully launch the new theme to all users** to increase conversions and improve the overall user experience.
