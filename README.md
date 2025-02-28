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
determine the optimal lag length using AIC, BIC, or HQIC criteria and lastly estimate the VAR model using Ordinary Least Squares (OLS) regression using Eview 14 econometric software. This is done in one of the project done here in one of the repositories and below were the VAR Model Estimates.

![Screenshot 2025-02-28 085804](https://github.com/user-attachments/assets/7b20ee00-7b68-41ec-b772-a35193edf9b1)


2️⃣Identifying Structural Shocks and Risks.

Introduce Impulse Response Functions (IRFs) to analyze how each variable reacts to a shock in another variable. Before we carry out this step we can look at key results that we need to check our model for stability. To do this we need to carry out System Stability Tests → Inverse Roots of AR Characteristic Polynomial) check for roots;

![stability](https://github.com/user-attachments/assets/5c2ebc13-cb38-4579-a7e9-5f9503a1affd)


- ✅ Since all roots are inside the unit circle → The model is stable.

### Impulse Response Function [IRF]
 IRFs show how a shock to one variable affects others over time. In a Vector Autoregression (VAR) model, the Impulse Response Function (IRF) shows how one variable responds over time to a shock in another variable. The choice of impulse (shocked variable) and response (affected variable) depends on the economic or financial system you are analyzing.
  
- Impulse Variable: Inflation
- Response Variable: Intrest Rates, Forex, Currency in Circulation and Bank of Zambia Reserves.

Below is are response graphs using Monte Carlo Method.

![irf to inflation](https://github.com/user-attachments/assets/92a91b4d-595e-4450-9ecb-6741651cee0d)

  
3️⃣Defining Economic Stress Scenarios.

We will construct hypothetical scenarios where economic conditions deviate from the norm by Simulating the impact of each shock by manipulating the error term. Examples include:
- Interest Rate Hike: A sudden 2% increase in policy rates
- A sudden 10%  kwacha depreciation against dollar
  
4️⃣Introducing the Shock into the Model.

Compute new Impulse Response Functions (IRFs) to observe how variables react

5️⃣Run the Model & Analyze the Results.

Compare variance decompositions before and after the shock.


REFERENCES

