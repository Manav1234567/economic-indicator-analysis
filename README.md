# Relationship Between Inflation Rates and Unemployment

## A B S T R A C T

This project aims to investigate the relationships between inflation, unemployment, and GDP
growth in the United States from December 2019 to December 2024 and analyse the validity of the
Phillips Curve and Okun's Law. The results provide strong evidence for the Phillips Curve, indicating a
significant inverse relationship between inflation and unemployment. However, the findings suggest
a weaker and less robust validation of Okun's Law. The combined model highlights inflation as a
stronger determinant of GDP growth than unemployment. These findings underscore the importance
of monitoring inflation-unemployment dynamics for effective policy-making and economic stability.

## Introduction

The interplay between key macroeconomic variables—such as inflation, unemployment, and GDP growth—has long
been a cornerstone of economic analysis and policy formulation. These relationships are central to understanding the
dynamics of economic performance and the trade-offs policymakers face when addressing competing priorities like
price stability, employment, and growth. Two critical theoretical constructs in this domain, the Phillips Curve and
Okun's Law, provide valuable frameworks for examining these dynamics.
The Phillips Curve gives an inverse relationship between inflation and unemployment, suggesting that policymakers
may face a trade-off between achieving low unemployment and controlling inflation. Conversely, Okun's Law
establishes a link between changes in unemployment and real GDP growth, indicating that economic output is tightly
connected to labour market conditions. Despite their historical relevance, the strength and robustness of these
relationships have been the subject of significant debate.
This project aims to empirically analyse these macroeconomic relationships using recent data from December 2019 to
December 2024. By utilizing monthly data sourced from the Federal Reserve Economic Data (FRED), this paper
examines the validity of the Phillips Curve and Okun's Law, as well as their combined influence on economic
performance.

## Theoretical Framework

### Phillips Curve
The Phillips Curve, first introduced by A.W. Phillips in 1958, highlights an inverse relationship between unemployment
and inflation. It suggests that when unemployment is low, increased demand for labour pushes wages upward,
subsequently driving prices higher. Conversely, higher unemployment suppresses wage growth and reduces
inflationary pressures.

### Okun's Law
Okun's Law, named after economist Arthur Okun, establishes a relationship between changes in real GDP and the
unemployment rate. This relationship reflects the economic output lost due to unemployment and is often used to
measure economic slack. However, Okun's Law is not a strict causal mechanism but an empirical regularity, with the
strength of its relationship varying across time periods and economic conditions.

### Combined Model
The combined model seeks to evaluate the simultaneous impact of inflation and unemployment on GDP growth,
effectively combining insights from Phillips Curve and Okun’s Law. This approach accounts for the broader
macroeconomic context and shows how inflation and unemployment influence economic output collectively.

## Data set

The data used for this project was sourced from the **Federal Reserve of Economic Data**, provided by the Federal Reserve Bank of St. Louis. The variables listed below were included:

- **Real GDP Growth Rate**
  - The dependent variable in this project is the **Brave-Butters-Kelley Monthly GDP Growth Index (BBKI)**, which provides an estimate of monthly GDP growth for the U.S. economy. This measure:
    - Is derived from a dynamic factor analysis of 490 real economic activity indicators and quarterly real GDP data.
    - Includes cycle, trend, and irregular components, allowing for a nuanced view of economic fluctuations.
    - Is indexed to align with the quarterly estimates of real GDP from the U.S. Bureau of Economic Analysis.
  - This variable represents the overall economic performance and serves as the foundation for analyzing its relationship with inflation and unemployment rates.

- **Inflation Rate**
  - The independent variable for inflation is the **10-Year Breakeven Inflation Rate**, which:
    - Is calculated from the spread between 10-Year Treasury Constant Maturity Securities and 10-Year Treasury Inflation-Indexed Constant Maturity Securities.
    - Reflects the forward-looking nature of inflation expectations, making it a vital indicator of economic sentiment.

- **Unemployment Rate**
  - The unemployment data is sourced from the **Current Population Survey (CPS)**, which represents:
    - The percentage of the labor force actively seeking employment but unable to find work.
    - A monthly indicator that provides insight into labor market conditions.
  - It is a widely used measure for evaluating economic slack and its impact on other economic variables.


## Research Methodology and Design

We initially plot a scatter plot between variables to see for the validity of Phillips curve and Okun’s law, followed by a
more detailed analysis wherein we use Ordinary Least Squared (OLS) to model the relationships between variables.
We also test for the assumptions of linear regression, including normality, multicollinearity, and homoskedasticity.
Model Specification
1. Phillips Curve Model: 𝐼𝑛𝑓𝑙𝑎𝑡𝑖𝑜𝑛 𝑅𝑎𝑡𝑒𝑡 = 𝛽0 + 𝛽1(𝑈𝑛𝑒𝑚𝑝𝑙𝑜𝑦𝑚𝑒𝑛𝑡 𝑅𝑎𝑡𝑒) + 𝜖𝑡
2. Okun's Law Model: 𝐺𝐷𝑃 𝐺𝑟𝑜𝑤𝑡ℎ 𝑅𝑎𝑡𝑒𝑡 = 𝛽0 + 𝛽1(𝑈𝑛𝑒𝑚𝑝𝑙𝑜𝑦𝑚𝑒𝑛𝑡 𝑅𝑎𝑡𝑒) + 𝜖𝑡
3. Combined Model: 𝐺𝐷𝑃 𝐺𝑟𝑜𝑤𝑡ℎ 𝑅𝑎𝑡𝑒𝑡 = 𝛽0 + 𝛽1(𝐼𝑛𝑓𝑙𝑎𝑡𝑖𝑜𝑛 𝑅𝑎𝑡𝑒) + 𝛽2(𝑈𝑛𝑒𝑚𝑝𝑙𝑜𝑦𝑚𝑒𝑛𝑡 𝑅𝑎𝑡𝑒) + 𝜖𝑡

- **Testing for assumptions**
  - Normality: Scaling/Transformation of variables
  - Multicollinearity: Variance Inflation Factor (VIF)
  - Homoskedasticity: Visual inspection of Residual plot, Breusch-Pagan Test, White's Test

## Technical Analysis

Using VIF, we saw no severe multicollinearity with any variable.
For normal distribution, we Log-transformed Unemployment Rate and Inflation Rate and Cube-Root transformed GDP
Growth Rate. The distribution of the resulting variable is shown in Figure 5.
### Multiple Regression Analysis
- **Model 1: Phillips Curve**
  - 𝛽1 = −1.3019 which is statistically significant at 95% confidence interval.
  - 𝐴𝑑𝑗𝑢𝑠𝑡𝑒𝑑 𝑅2 = 0.604
  - P-value for Breusch-Pagan and White’s test statistics are 0.50 and 0.52 respectively which proves
homoskedasticity.
- **Model 2: Okun's Law**
  - 𝛽1 = −0.8034 which is not statistically significant at 95% confidence interval.
  - 𝐴𝑑𝑗𝑢𝑠𝑡𝑒𝑑 𝑅2 = 0.026
  - P-value for Breusch-Pagan and White’s test statistic are 2.35e-06 and 9.46e-06 respectively which
shows heteroskedasticity.
- **Model 3: Combined Model**
  - 𝐴𝑑𝑗𝑢𝑠𝑡𝑒𝑑 𝑅2 = 0.128
  - 𝛽1 = 3.5385 which is statistically significant at 95% confidence interval.
  - 𝛽2 = 0.8557 which is not statistically significant at 95% confidence interval.
  - P-value for Breusch-Pagan and White’s test statistic are 1.13e-06 and 1.01e-05 respectively which
shows heteroskedasticity.

## Findings and Results

By looking at the time series plots, we can suggest that the first quarter of 2020 was a period of significant recessionary gap
as unemployment increased, inflation decreased (in other words price came down), and the output decreased (shown
by negative growth in real GDP).
  - Phillips Curve: Strong support for an inverse relationship between inflation and unemployment.
  - Okun's Law: Weak evidence suggests it holds during this period, but the relationship is not robust.
  - Combined Model: Inflation seems to be a bigger influence on GDP growth then Unemployment rate.
The reason for the weak statistical significance in Model 2 and 3 potentially arises due to omitted variable bias

## Research Results and Interpretation

  - Inflation and Unemployment: Clear evidence of the Phillips Curve; policymakers can use unemployment to
predict inflation trends.
  - GDP Growth and Unemployment: Okun's Law is less apparent, suggesting other factors influence the
relationship.
  - Policy Implications: The results underline the importance of monitoring inflation-unemployment dynamics for
economic stability.

## Bibliography and References

  - Phillips, A. W. (1958). "The Relationship Between Unemployment and the Rate of Change of Money Wages."
  - Okun, A. M. (1962). "Potential GNP: Its Measurement and Significance."
  - Data Sources: U.S. Bureau of Economic Analysis (BEA), Bureau of Labor Statistics (BLS).
