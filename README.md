# Ames Housing Price Prediction

This repository contains the full analysis, modeling, and results for a housing price prediction project using the **AmesHousing** dataset. The project uses multiple linear regression to identify key factors influencing residential property sale prices in Ames, Iowa.

## 📌 Project Overview

The primary goal of this project is to model and understand how various housing attributes—such as ground living area, garage area, year built, number of bedrooms, and overall quality—affect the final sale price of homes. The analysis focuses on homes with average to excellent overall quality and 2–4 bedrooms, built after 1940.

## 🧠 Key Questions

- What are the most significant predictors of home prices in Ames, Iowa?
- How does each variable (e.g., size, age, quality) influence price?
- Can a linear model offer interpretable and robust results for real-world housing data?

## 📂 Dataset

- **Source**: [`AmesHousing` R package](https://cran.r-project.org/web/packages/AmesHousing/AmesHousing.pdf) by Max Kuhn & Kjell Johnson
- **Scope**: Residential property sales in Ames, Iowa (2006–2010)
- **Size**: 2,930 observations, 80+ variables

## 🧪 Methodology

1. **Data Filtering & Preprocessing**
   - Filtered for homes with 2–4 bedrooms and average or better quality
   - Removed homes built before 1940 to avoid age-related outliers
   - Applied log transformation to `SalePrice`, `Gr_Liv_Area`, and `Garage_Area` to address skewness

2. **Exploratory Data Analysis**
   - Visualized distributions, outliers, and relationships using `ggplot2`
   - Checked for multicollinearity and data imbalance

3. **Modeling**
   - Built multiple linear regression model using `lm()` in R
   - Selected predictors using AIC and domain knowledge
   - Interpreted coefficients with confidence intervals and p-values
   - Validated assumptions using residual plots, QQ-plots, and pairwise scatter plots

4. **Performance**
   - R²: 0.819, Adjusted R²: 0.8182
   - AIC: -2184.5
   - Strong model fit and explanatory power with interpretable output

## 📊 Key Findings

- **Ground living area** is the most influential continuous variable.
- **Overall quality** significantly increases price in a consistent, tiered manner.
- **Garage area** and **year built** have positive but smaller effects.
- **Number of bedrooms** showed a counterintuitive negative relationship—possibly due to space trade-offs when controlling for total size.

## 🛠️ Tools & Packages

- **R**
  - `tidyverse` – data manipulation
  - `ggplot2` – visualization
  - `broom` – model tidying
  - `car`, `MASS` – regression diagnostics

## 📁 Repository Structure

