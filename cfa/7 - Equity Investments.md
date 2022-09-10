# Market Org & Structure
## Functions of Fin Sys
1) Facilitate Transfers
	* speculators -> expecting to earn in excess of risk
2) Price Discovery
3) Efficient allocation of capital
* complete markets require savers, borrowers, hedgers & asset exchange

## Classification
* Money markets -> <1 year maturity
* primary markets -> seller is issuer

## Securities
* Common -> entitled to discretionary dividends
* Preferred -> entitled to **fixed** dividends
* Forward -> OTC, customisable
* Futures -> Standardised, exchange traded

## Intermediaries
* Brokers fulfils orders for a client
* Dealers hold inventory, create liquidity, contract counter-parties & can act as broker
	* Primary Dealers -> buy / sell with Central Bank
* Clearing houses -> arrange for final settlement, acts as counter-party for futures

## Positions
* Long -> Purchased a contract / has rights
* Short -> Sold a contract (Deliverer) / has obligation
	* To close, initiate a buy to cover/close

![[ei-margincall.png]]

## Order
* Market -> Buy on ask, sell on bid (normal) -> guaranteed order but not price
* Limit -> guaranteed price but not order
* Can send orders with hidden size or with a 'lower' displayed size ~ Iceberg
* GTC ~ max typically is 6 months
* FOK (Fill or kill) - immediately
* good on close - execute at the close of trading
* stop-loss - stop selling if the price too low
* buy-stop - stop buying if the price too high

## Trading
* ==Call Market -> only occurs @ particular times & places (treasury auction)==
	* Uniform Pricing - same price for all trades
* Continuous Market -> anytime the market is open
	* Discriminatory Pricing - order that arrives first determines price
	1) Price precedence
	2) Display precedence
	3) Time precedence
* Quote Driven Markets - OTC (Dealer supplies)
* Order Driven Markets - Exchanges
	* Derivative pricing - midpoint of bid ask from another market
* Post trade transparency -> wider spreads + higher transaction costs

# Security Market Index

* Price Return Index - only price
	* has a divisor to make the start price look nice
	* divisor changes over time to reflect price change only (ie. ignoring stock splits & rebalancing)
* Total Return Index - assumes reinvestment of all income received **since inception**
	* total return = price change + all income
* multiple period return -> geo mean R₉ = √ [(1+R)(1+R2)....] - 1

### Index Weighting
1) Price Weighting (simplest)
	* DJIA
	* highest price stocks will have the most impact (AMZN)
	* same no. of stocks in each index
	* stock splits will affect all the weightings (D changes)
	* **No need to rebalance** because of price changes
2) Equal Weighting
	* same amt spent on each stock (ie. $2000 on)
	* large P stocks underrepresented
	* frequent rebalancing as price changes -> reduce weights of overperformers
3) Mkt-Cap Weighting
	*  SNP500
	*  Float adjusted Mkt cap (Those available to investing public)
	*  Divide Mkt Cap by sum of all mkt cap
	*  leads to overweight of overvalued stocks + big Mkt cap can move the index
	*  **No need to rebalance** unless M&A and liquidations
4) Fundamental Weighting
	*	uses fundamental value as proxy rather than mkt cap
	*	book value, revenue **ratios**
	*	contrarian effect

* Reconstitution -> changing the index to keep it representative
* change in price & mkt cap weightings; not for equal weighting

# Market Efficiency
* assumes information is timely, complete, correct & understandable

![[ei-mkttaxonomy.png]]

1) Weak-form
	* no correlation with historical data (**technical analysis doesnt work**)
2) Semi-weak form
	* cannot earn after information has been made public
	* active managers are a waste of money
3) Strong form
	*	perfect markers where information is cost free and available to all
	*	no one can consistenly achieve abnormal returns

### Anomalies
1) Calendar Anomalies
	* January - higher returns
	* Turn of the month - higher returns on the last trading day
	* Day of the week - Mon lowest
	* Holiday - day prior highest
2) Overreaction Anomalies
3) Momentum Anomalies
4) Size effect - small cap tend to outperform
5) Value effect - value outperform growth overtime

### Behavioural Finance
1) Loss aversion
2) Herding
3) Information Cascades 
4) Overconfidence


# Equity Securities
#### Common Shares
* Statutory voting - each share is 1 vote
* Cumulative voting - # shares * # directors
* Callable - issuer has the right to buy back shares at a pre-determined price
* Putable - investor has the right to sell the shares at a pre-determined price (Less risky)

#### Preferred Shares (Less risky than commons)
* no voting rights
* receive dividends before commons
* dividend can be fixed or par (usually more than commons)
	* dividend still discretionary
	* Cumulative - unpaid dividends accrue and must be paid in full before commons
	* Non-Cumulative - does not accrue, higher yield
* can be perpetual, convertible, callable and putable
* convertible to common and can be forced converted if common > conversion price

### Public vs Private
* Private placement - institutional investors, no secondary markets (More risky)
* # shareholders > 50 - considered as public company
* PIPE - get restricted stock and preferreds @discount

### Non Domestic Equity
1) Direct Investing - **exchange rate risk**
2) Depository receipts - like ordinary share, has **exchange rate risk**
	* all dividends in domestic $
	* sponsored - foreign co. has a direct involvement in issuance of receipts, investors have same rights as direct owners
	* unsponsored - depository (BANK) has the rights to ownership
	* GDR (Global) - issued outside issuer home country and US (in USD)
	* ADR (American)- in USD & trade like common shares in US
	
![[ei-deporeceipts.png]]

3) Global registered shares - traded in different currencies and mkts
4) Basket of Listed DR - ETF of DR

### Financing
* Accounting ROE = **NI - Pref Div** / avg **BV**
* high MV to BV ratio means markey is pricing future growth
* Normal ROE can be managed -> issue debts to buy back shares

# Industry & Company Analysis
### Classifications
1) By product service
	* Based on principal business activity
2) Business cycle
	* non-cyclical - consumable / non-discretionary
		* defensive - staple consumer goods
		* growth
3) Statistical similarities
	* based on correlation of past returns

1) GICS - Principal biz activity
	* Sector > Industry Group > Industry > Sub-Industry
2) RGS - basis of goods / services produced
	*	Sector > Sub Sector > Industry
3) ICB - primary revenue source
	* Industry > Supersector > Sector > Subsector
4) Gov classification - ISIC, NACE, ANZSIC, NAICS
	* gov does not disclose info about specific biz
	* commercial ones reviewed more frequently
	* comm -> only profit & publicaly traded

### Strategic Analysis
* Porter's 5 force model - lower better
	1) Threat of substitutes
	2) Bargaining power of customers
	3) Bargaining power of suppliers 
	4) Threat of new entrants
	5) Intensity of rivalry

* Automobile industry has high barriers to entry BUT low pricing power
* limited capacity -> more pricing power as demand > supply

![[ei-finratios.png]]

# Equity Valuation

### Dividends
* Stock dividend not relevant for valuation unlike normal dividend
* Stock splits not relevant for valuation
* Share splits are relevant
* shareholder must have the stock **2 days before Holder of Record Date**
	* stock will open lower by the amount of dividend 1 day before

### 1) PV (DCF)
* V0 = Sum of PV of dividends to infinity + Pn / (1 + r)
	* Pn -> terminal stock value
* r estimated using CAPM = rf + B(ERP)

![[ei-dcf.png|500]]

#### FCFE
* FCFE - free cash flow to EQ (dividend paying capacity)
* FCFE = CFO (casho flow ops) - (CAPEX + Net borrowings)
* V0 = PV of FCFE

#### Preferred Shares
* If perpetual, non callable, non convertible: V0 = D0 / r
* If maturing at time n, same as a bond

### Gordon Growth Model
* accounts for Dividend growth
* If r>g -> geometric series
* V0 = D1 / (r-g)
	* g extremely important to valuation (**use another model if its bigger than r**)
* g = earning retension rate * ROE
* earning retention rate = 1 - DPR
* assumes g is forever, r is constant and g < r

#### Multistage DMM
* makes use of 2 g - high g (terminal value DDM) and low g (perpetuity - GGM)

![[ei-multistagedmm.png|500]]

### 2) Price Multiples
* P / E - useless if EPS < 0 but strongly correlated to long term returns
	* P/ E = DPR / (r-g)
	* P / E positively related to ROE
* P / S (sales) -not influenced by acct choices but ignores cost structure
* P / CF - more difficult to manipulate and more reliable long term but ignores non Cash revenues
* P / BV - appropriate for firms in distress

* OR estimate the value of enterprise EV = MV(EQ + Pref + Debt)- Cash
* useful for comparing cos with different capital structure -> EV / EBITDA

### 3) Asset Based Valuations
* A - L / # shares