# 📊 E-Commerce A/B Testing & Revenue Optimization

Welcome to my A/B Testing analysis project! 👋 

In this project, I step into the shoes of a Data Analyst at a large online store. The marketing department compiled a list of hypotheses to boost revenue, and my job was to prioritize these ideas, analyze the results of a month-long A/B test, and make a data-driven business decision.

## 🎯 Project Objectives

This project is divided into two main parts:
1. **Hypothesis Prioritization:** Using both **ICE** (Impact, Confidence, Effort) and **RICE** (Reach, Impact, Confidence, Effort) frameworks to determine which marketing idea to test first.
2. **A/B Test Analysis:** Analyzing transaction and visit logs to evaluate if the new webpage version (Group B) actually outperformed the old one (Group A) in terms of conversion rate and average order size.

## 🛠️ Tools & Technologies Used
* **Python** 
* **Pandas & NumPy** (Data cleaning, aggregation, cumulative metrics)
* **SciPy** (Statistical significance testing / Mann-Whitney U test)
* **Matplotlib** (Data visualization & scatter plots)

## 🔍 Key Steps & Methodology

### Part 1: Prioritizing Hypotheses
* Calculated both ICE and RICE scores for 9 different hypotheses.
* Discovered how the **Reach** parameter drastically changes priorities. An idea that affects 100% of users easily overtook an idea that had a high impact but only reached 10% of the audience.

### Part 2: A/B Test Analysis
* **Data Preprocessing:** Identified and completely removed 58 anomalous users who were mistakenly exposed to both Group A and Group B, ensuring the statistical independence of our test groups.
* **Cumulative Metrics:** Plotted cumulative revenue, average order size, and conversion rates to observe how the metrics stabilized over time.
* **Anomaly Detection:** Used scatter plots and calculated the 95th and 99th percentiles to find extreme outliers (e.g., abnormally large orders). 
* **Statistical Testing:** Applied the non-parametric **Mann-Whitney U test** on both the *raw data* and the *filtered data* (with outliers removed) to prove statistical significance.

## 💡 Final Business Conclusion

After rigorous filtering and testing, here is what the data told us:
* **Conversion Rate:** Group B showed a statistically significant and stable advantage over Group A (an uplift of ~19% in the filtered data).
* **Average Order Size:** There was no statistically significant difference between the groups once extreme outliers were removed. The initial massive spike in Group B's revenue was purely an artifact of 1-2 extremely expensive orders.

**The Verdict:** 🛑 **Stop the test and declare Group B the leader.** 
Even though the average order size didn't increase, Group B successfully and consistently converted more visitors into buyers. Applying these changes will confidently drive more purchases and increase overall revenue for the business!

---
*Feel free to explore the Jupyter Notebook in this repository to see the detailed python code, visualizations, and step-by-step statistical reasoning.*
