# YRBSS Data Analysis Project

## Overview
This project analyzes data from the Youth Risk Behavior Surveillance System (YRBSS), which is conducted by the Centers for Disease Control and Prevention every two years. The analysis focuses on health patterns among high school students (9th through 12th grade), examining relationships between physical activity, sleep habits, height, and weight.

## Dataset Information
- **Source**: Centers for Disease Control and Prevention (CDC)
- **Sample Size**: 13,583 high school students
- **Variables**: 13 variables including demographics, physical measurements, and health behaviors
- **Missing Data**: Some variables have missing values (e.g., 1,004 missing weight values)

## Key Variables
- `age`: Age of student (in years)
- `gender`: Gender identity (female/male)
- `height`: Height in meters
- `weight`: Weight in kilograms
- `physically_active_7d`: Number of days physically active in past week (0-7)
- `school_night_hours_sleep`: Hours of sleep on school nights
- `physical_3plus`: Derived variable indicating if student exercises 3+ days per week

## Research Questions
The analysis investigates several key research questions:

1. Is there a difference in average weight between students who exercise at least three times a week versus those who don't?
2. Is there a difference in average height between students who exercise at least three times a week versus those who don't?
3. How does sleep duration relate to student weight?

## Methods
- **Statistical Tests**: Two-sample t-tests, hypothesis testing
- **Confidence Intervals**: 90% and 95% confidence intervals
- **Randomization**: Permutation testing
- **Visualizations**: Boxplots, histograms

## Key Findings

### Physical Activity and Weight
- Students who exercise 3+ days per week weigh, on average, 1.7 kg more than those who don't
- 95% Confidence Interval: [1.08, 2.32] kg
- This counterintuitive result may be explained by increased muscle mass among active students

### Physical Activity and Height
- Students who exercise 3+ days per week are, on average, 3.76 cm taller than those who don't
- t-statistic: 19.03, p-value: extremely small (5.39 × 10^-79)
- The relationship is statistically significant and practically meaningful

### Sleep and Weight
- Students who get inadequate sleep (<8 hours) weigh approximately 2.2 kg more than well-rested students
- 95% Confidence Interval: [1.6, 2.8] kg
- This aligns with research on sleep's impact on metabolism and appetite regulation

## Assumptions Checked
- Independence of observations
- Large sample sizes (Central Limit Theorem applies)
- Equal variances where appropriate
- Random sampling

## Required Packages
```r
library(tidyverse)
library(openintro)
library(infer)
library(dplyr)
library(ggplot2)
```

## How to Use This Analysis
1. Install required R packages
2. Load the YRBSS dataset: `data('yrbss', package='openintro')`
3. Run the analyses as documented in the R Markdown file

## Limitations
- Cross-sectional data cannot establish causal relationships
- Self-reported data may contain inaccuracies
- Missing data may introduce bias
- Confounding variables not accounted for (e.g., diet, genetics)

## Conclusions
The analysis reveals significant relationships between physical activity, sleep habits, and physical measurements among high school students. Notably, more physically active students tend to be taller and heavier, while students with inadequate sleep tend to weigh more than well-rested peers. These findings highlight the complex interplay between lifestyle factors and physical development in adolescents.

## Future Work
- Investigate interactions between gender, physical activity, and physical measurements
- Analyze relationships between screen time, sleep, and weight
- Examine trends across different demographic groups
- Incorporate dietary information if available

## Author
Emmanuel Kasigazi

## License
This project is licensed under the MIT License - see the LICENSE file for details.
