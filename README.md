# Sensitivity Analysis

![uncertainty-hero-940x529](https://github.com/user-attachments/assets/34f81d91-90fc-45fb-a003-93df44701d14)


# Application of Sensitivity Analysis
Sensitivity Analysis (SA) is a key tool in both econometric modeling and machine learning (ML), used to assess how changes in inputs affect outputs. It helps quantify risk and uncertainty, making models more robust and interpretable. Some of the application include;

🔹 Regression Models: Assessing the impact of different variables on GDP, inflation, or employment.

🔹 Policy Analysis: Evaluating how fiscal or monetary policy changes affect economic outcomes.

🔹 Forecasting: Testing the reliability of GDP or demand forecasts under different assumptions.

### Stress Testing & Scenario Analysis in a VAR Model: Assessing Shocks & Uncertainties
A Vector Autoregression (VAR) model is commonly used in econometrics to analyze how shocks or uncertainties impact interdependent economic indicators. Scenario analysis and stress testing help us understand how the system reacts under different condition. A VAR model treats multiple time series as endogenous and models each variable as a function of its own lags and the lags of all other variables. To carry out this project we will do it in multiple steps listed below.

## 1️⃣Estimating the VAR Model.

We will collect and clean sufficient macroeconomic data (e.g., inflation, interest rates, exchange rate. e.t.c ), use the ADF test to check for unit roots, and difference the data if necessary). Then we
determine the optimal lag length using AIC, BIC, or HQIC criteria and lastly estimate the VAR model using Ordinary Least Squares (OLS) regression using Eview 14 econometric software. This is done in one of the project done here in one of the repositories and below were the VAR Model Estimates.

![Screenshot 2025-02-28 085804](https://github.com/user-attachments/assets/7b20ee00-7b68-41ec-b772-a35193edf9b1)


## 2️⃣Identifying Structural Shocks and Risks.

Introduce Impulse Response Functions (IRFs) to analyze how each variable reacts to a shock in another variable. Before we carry out this step we can look at key results that we need to check our model for stability. To do this we need to carry out System Stability Tests → Inverse Roots of AR Characteristic Polynomial) check for roots;

![stability](https://github.com/user-attachments/assets/5c2ebc13-cb38-4579-a7e9-5f9503a1affd)


- ✅ Since all roots are inside the unit circle → The model is stable.

### Impulse Response Function [IRF]
 IRFs show how a shock to one variable affects others over time. In a Vector Autoregression (VAR) model, the Impulse Response Function (IRF) shows how one variable responds over time to a shock in another variable. The choice of impulse (shocked variable) and response (affected variable) depends on the economic or financial system you are analyzing.
  
- Impulse Variable: Inflation
- Response Variable: Intrest Rates, Forex, Currency in Circulation and Bank of Zambia Reserves.

Below is are response graphs using Monte Carlo Method.

![irf to inflation](https://github.com/user-attachments/assets/92a91b4d-595e-4450-9ecb-6741651cee0d)

Interpretation:

### Top Left: Response of Interest Rate (IR_D) to Inflation Shock 
The interest rate increases in response to an inflation shock. The response is positive and persistent, peaking around the 6th period before stabilizing and this suggests that monetary policy (interest rates) reacts by tightening in response to inflation

Implication:

The central bank may be raising interest rates to control inflation.


### Top Right:  Response of Foreign Exchange Reserves (FOREX_K_USD_D) to Inflation Shock.

The response is negative, meaning that an inflation shock leads to a decline in forex reserves and the effect becomes stronger over time. A possible explanation is that inflation leads to depreciation of the local currency, forcing authorities to use forex reserves to stabilize the exchange rate.

### Overall Insights.
- Inflation shocks lead to higher interest rates (suggesting a monetary policy response).
  
- Forex reserves and central bank reserves decline, indicating pressure on external stability.
  
- Currency in circulation reacts sharply, showing possible liquidity constraints.

  
## 3️⃣Defining Economic Stress Scenarios.

We will construct hypothetical scenarios where economic conditions deviate from the norm by Simulating the impact of each shock by manipulating the error term. Examples include:
- Interest Rate Hike: A sudden 4% increase in policy rates
  
## 4️⃣Introducing the Shock into the Model.

Compute new Impulse Response Functions (IRFs) to observe how variables react. To simulate the interest rate shock, we will use the Impulse Response Function (IRF) analysis, applying a one-standard deviation (S.D.) shock to a variable by manually increasing the Interest Rate by 4%. To carry out this we will go to Model" → "Solve Control" in Eview. Below are responses to Iterest Rate before introducing a shock.

![b4irshock](https://github.com/user-attachments/assets/7a2edc2f-a2c8-49ab-a040-eed181d964d3)


## 5️⃣Run the Model & Analyze the Results.

Compare variance decompositions before and after the shock. We will not use this method but use visual response after 4% Interest rate is applied, below are responses after shock is applied.

![aftershock](https://github.com/user-attachments/assets/8580be7a-6379-4958-a96a-77cfcca3b87d)
 
### Key Insights:

- Foreign Exchange Reserves (FOREX_K_USD_D): The exchange rate or reserves initially strengthened but returned to baseline levels, indicating a temporary effect.
  
After Shock: FOREX_K_USD_D shows an initial increase (peaking at 2 units) but then fluctuates and declines, eventually stabilizing around 0. This suggests that the interest rate hike initially attracted foreign capital, strengthening the currency and increasing reserves. However, the effect is short-lived, and the exchange rate or reserves return to baseline levels over time.

- Inflation (INFLATION_D): The interest rate hike successfully reduced inflation over time, but the initial spike suggests potential short-term costs.

Inflation shows an initial increase (peaking at 6 units) but then declines sharply, becoming negative (-2 units) by the 10th period. This indicates that the interest rate hike initially caused a spike in inflation (possibly due to higher borrowing costs), but over time, it successfully reduced inflationary pressures, leading to deflationary effects.

## DATA REFERENCES

1: International Monetary Fund. https://www.imf.org/external/datamapper/NGDPDPC@WEO/ZMB?zoom=ZMB&highlight=ZMB

2: WORLD BANK https://data.worldbank.org/indicator/SL.UEM.TOTL.ZS?locations=ZM

3: Bank of Zambia https://www.boz.zm/statistics.htm

