# 🎮 Cookie Cats: A/B Testing & Player Retention Analysis

![Python](https://img.shields.io/badge/Python-3.8%2B-blue) ![Stat_Test](https://img.shields.io/badge/Test-Mann--Whitney_U-orange) ![Status](https://img.shields.io/badge/Status-Completed-success)

## 🕹️ Introduction

**Cookie Cats** is a hugely popular mobile puzzle game. This project focuses on analyzing an A/B test where the first "gate" in the game was moved from **Level 30 to Level 40**. In mobile games, gates force players to wait or make a purchase to progress. This study aims to discover how this change affects player engagement and long-term retention.

## 🎯 Project Objectives

* **EDA:** Analyze the distribution of game rounds and handle extreme outliers.
* 
* **Statistical Analysis:** Perform normality and variance checks to select the most robust hypothesis test.
* 
* **Retention Analysis:** Use **Bootstrapping** to calculate the statistical probability of which gate location performs better for 1-day and 7-day retention.
* 
* **Business Recommendation:** Provide a data-driven suggestion on optimal gate placement.

## 📊 Dataset Summary

* `userid`: Unique player ID.
  
* `version`: Group (Control: `gate_30`, Variant: `gate_40`).
  
* `sum_gamerounds`: Total rounds played in the first 14 days.
  
* `retention_1`: Did the player return 1 day after installing?
  
* `retention_7`: Did the player return 7 days after installing?

## 🛠️ Methodology & Statistical Workflow

1. **Data Cleaning:** Removed extreme outliers.
   
2. **Assumptions:** Checked for Normality (Shapiro-Wilk) and Variance Homogeneity (Levene).
   
3. **Hypothesis Testing:** Used **Mann-Whitney U** test due to non-normal distribution.
   
4. **Bootstrapping:** Conducted 500 iterations for retention rate confidence intervals.

## 🚀 Key Findings

* **1-Day Retention:** 97% probability that `gate_30` (Control) is better.
  
* **7-Day Retention:** **100% probability** that `gate_30` is better.
  
* **The "Hedonic Adaptation" Theory:** Forcing a break at Level 30 keeps the game "fresh" and significantly improves long-term retention.

## 💡 Final Recommendation

**Do not move the gate to Level 40.** The evidence clearly shows that keeping the first gate at **Level 30** maximizes player retention and long-term engagement.
