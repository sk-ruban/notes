# Portfolio Management Overview
* systematic risk = market risk
* non-systematic risk -> diversifiable (up to 50 securities)
* asset class weighting / selection more important than security selection

1) Planning -> KYC - objectives & constraints (IPS)
2) Execution -> Asset class allocation, security analysis & Portfolio Construction
3) Feedback -> dynamic (get back from price drift) vs tactical (intentional deviation)

## Investors (Buy Side)
* Pension plans
	* Defined benefit (employer pays)
	* Defined contribution (employee contributes %) -> dependent on length, performance

![[pm-investors.png]]

## Investments
### Mutual Funds
* ==all income (dividends) flows to unit holders==
* Open Ended -> issue new units @ NAV, redeem @ NAV (Must be liquid)
* Close Ended -> Fixed # shares, exchange traded, +/-/= NAV
* **Priced once a day**
* Load Funds -> annual fee + buy / sell fees
* No-Load Funds -> annual fee only
* MM MFs can be tax tree / taxable
* **No brokerage costs**
* **Long only**

### ETFs
* stays ==close to NAV==
* lower Mgmt Expense Ratio but ==has brokerage costs==
* continuous trading
* **can short / margin**
* **tax advantage**

### SMA (separately managed accounts)
* not pooled -> client owns the assets
* more control but higher buy-in

# Risk & Return 1
* holding period return **rooted** = geometric mean = time weighted
* money-weighted return = IRR -> accurate **but lacks comparability** (use CFs!!)
* gross returns = TR - trading fees
* net returns = Gross - mgmt / admin fees
* long term and dividends (Not interest) have pref. tax treatment
* nominal = RF x Inflation x ERP

### Risk Aversion
* Risk aversion - take the sure thing (Utility curve -> investors able to rank & be consistent)
* risk seeking - seeks risk
* risk neutral - just seeks higher returns regardless of risk

![[pm-riskaversion.png|300]]

### Minimum Variance Portfolio

![[pm-minvarianceport.png|500]]

# Risk & Return 2
* homogeneity of expectations -> only 1 optimal risky portfolio
* beta is the amount of **systematic risk** compared to market
* CML - CAL where the **optimal risky portfolio is the market portfolio**
	* slope is the mkt price of risk
* When leveraging, weight of Rf asset < 0
* non-systematic risk is not rewarded -> systematic risk is priced

### CAPM Assumptions
1) investors are risk adverse and rational
2) markets are frictionless and no transactional costs + taxes
3) homogeneous expectations
4) investors are price takers
5) investments are infinitely divisible

* SML - expands to inefficient portfolios unlike CML
* SML - x-axis is B rather than sd
* CML / CAL - only for efficient portfolios

### Portfolio evaluation
* M2 & Sharpe -> Total Risk & for anything
* Treynor & Jensen's alpha -> Systematic Risk & for fully diversified portfolios


# Portfolio Planning & Construction (Revise)
1) Introduction
2) Purpose
3) Duties & Responsibilities
4) Procedures - to keep IPS up to date + contingencies
5) Objectives - absolute or relative / pre or post fees
6) Constraints - liquidity, time horizon, tax concerns, legal + unique considerations
7) Guidelines - ==how to execute and exclusion==
8) Execution & Review - feedback
9) Appendix - ==Strategic asset allocation (% in each asset class) + rebalancing==

* IPS should be reviewed and updated regularly
* If low ability talk client down
* Core (Passive) - Satellite (Active) approach -> Tactical asset allocation
* corr between asset class > corr within asset class

# Behavioural Biases of Individuals

# Risk Management
* is about minimising unacceptable risks, not all risks
* top-down process
* board of directors -> Risk mgmt committee defines risk appetite
	* deliberates risk policies @ operational level
* should provide a sense that the worst loss can be managed

1) Identification - identify risks + potential drivers
2) Assessment - which risks unable to accept, should ignore personal beliefs
3) Mitigation - communication, feedback loop
4) Monitoring

* single dimensional measure - VaR
* multi dimensional measure - portfolio margining

### Sources of Risk
#### Financial
1) Market Risk - changes in interest rates, prices, forex due to fundamental economic conditions
2) Credit Risk - counterparty risk due to economic weakness
3) Liquidity Risk - having to sell asset below fair value

#### Non-Financial
1) Solvency Risk - running out of cash (Operational Risk)
2) Settlement Risk - party fails to deliver after payment

### Measures & Modifications
* VaR subject to model error
* scenario / stress testing used to complement VaR
* risk shifting -> changing the distribution of risk outcomes (derivatives)
* risk transfer -> insurance

![[pm-deltagamma.png|400]]

# Technical Analysis
## Assumptions 
1) Markets are **not efficient**
2) Prices reflect all information - no point doing fundamental analysis
3) Price / vol lead fundamental information

* once resistance is breached, it becomes support and vice versa

## Patterns
* head - new $ high but not new vol high

![[pm-hns.png|300]]

* double tops & double bottoms (no triple)
* Long term - Rectangle / Triangle
* Short term - Flag / Pennant

### Technical Indicators
 1) Moving averages - closing price over a number of periods
	 * exponential - recent prices given more weightage 

![[pm-movavg.png|300]]

2) Bollinger Bands - Bands are Moving average bands of +/- 1 SD
3) Rate of Change Oscillator

![[pm-rocoscil.png]]

4) Relative Strength Index 

![[pm-rsi.png|500]]

5) MACD

![[pm-macd.png|500]]

# Fintech
* big data = traditional + alternative sources
	* volume
	* velocity - real time
	* variety - many sources (structured - SQL / semi-structured - HTML / unstructured - Videos)
* supervised learning - based on labeled data
* unsupervised learning - no labels
* permission networks - controlled and may restrict members
* permissionless networks - open to any user, once transaction is added cannot be changed; trust not a requirement