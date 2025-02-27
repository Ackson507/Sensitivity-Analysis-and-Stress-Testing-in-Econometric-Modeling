# Sensitivity Analysis
![FeatureImage8](https://github.com/user-attachments/assets/f4038035-361b-471b-874c-e354e2496cbd)


# Application of Sensitivity Analysis
Sensitivity Analysis (SA) is a key tool in both econometric modeling and machine learning (ML), used to assess how changes in inputs affect outputs. It helps quantify risk and uncertainty, making models more robust and interpretable. Some of the application include;

🔹 Regression Models: Assessing the impact of different variables on GDP, inflation, or employment.

🔹 Policy Analysis: Evaluating how fiscal or monetary policy changes affect economic outcomes.

🔹 Forecasting: Testing the reliability of GDP or demand forecasts under different assumptions.

### Stress Testing & Scenario Analysis in a VAR Model: Assessing Shocks & Uncertainties
A Vector Autoregression (VAR) model is commonly used in econometrics to analyze how shocks or uncertainties impact interdependent economic indicators. Scenario analysis and stress testing help us understand how the system reacts under different condition. A VAR model treats multiple time series as endogenous and models each variable as a function of its own lags and the lags of all other variables. To carry out this project we will do it in multiple steps listed below.

1️⃣Estimating the VAR Model.

We will collect and clean sufficient macroeconomic data (e.g., inflation, interest rates, exchange rate. e.t.c ), use the ADF test to check for unit roots, and difference the data if necessary). Then we
determine the optimal lag length using AIC, BIC, or HQIC criteria and lastly estimate the VAR model using Ordinary Least Squares (OLS) regression using Eview 14 econometric software

2️⃣Identifying Structural Shocks and Risks.

Introduce Impulse Response Functions (IRFs) to analyze how each variable reacts to a shock in another variable

3️⃣Defining Economic Stress Scenarios.

We will construct hypothetical scenarios where economic conditions deviate from the norm by Simulating the impact of each shock by manipulating the error term. Examples include:
- Interest Rate Hike: A sudden 2% increase in policy rates
- A sudden 10%  kwacha depreciation against dollar
  
4️⃣Introducing the Shock into the Model.

Compute new Impulse Response Functions (IRFs) to observe how variables react

5️⃣Run the Model & Analyze the Results.

Compare variance decompositions before and after the shock.


REFERENCES

