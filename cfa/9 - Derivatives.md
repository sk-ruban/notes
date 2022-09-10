# Derivative Markets & Instruments
* derivatives are a 0 sum game
* rights = contingencies
* obligation = commitments
* In efficient financial markets, risk-free arbitrage opportunities ==may exist temporarily==

## Structure
1) Exchange traded - Futures / options
	* standardised contracts
	* no counter-party risk - clearinghouse takes the opposite side (investors post margin)
	* ==daily settlement - mark to market==
	* transparent & high regulation
2) OTC - Forwards / swaps
	* dealer markets (banks)
	* customisation of contracts - lack of liquidity
	* ==Dodd-Frank -> OTC contracts which can be standardised have to be==

## Forwards
* OTC contract where both parties are obligated to perform
* $ does not change hand on inception of contract
* not all assets are delivered -> NDF, cash settled forwards & contract for differences
* If futures prices are ==positively correlated with interest rates, futures contracts are more desirable== to holders of long positions than are forwards. Opposite is true

## Futures
* Exchange traded which has mark to market settlement (ie. daily settlement)
* when margin call triggered, need to post back up to **initial margin**
* ==trades can only occur within bands==
* offsetting -> closing position before delivery
* open interest -> # of outstanding contracts
* ==short must deliver==
* future and spot prices converge on last day

## Swaps
* swap variable rate for variable (typically Libor) / fixed rate
* fixed for floating (vanilla swap)
* value of swap @ inception = 0, value dependent on floating rate changes

## Options
* Buyer has the right and seller has the obligation
* American style - exercise anytime
* European style - only on expiration date
* When strike = spot price, at the money

## Credit Derivatives
* avoids many regulatory constraints of insurance
* CDS seller provides compensation in the case of credit losses
* once default occurs, payments stop until CDS settled
* ==total return swaps, credit spread options, credit linked notes==

![[d-cds.png|600]]

## Purposes
1) Information discovery - prices reflected faster + more strategies
2) Lower transaction costs - more liquid than spot
3) Market efficiency - less costly to trade / hedge

# Derivative Pricing & Valuation
## Replication
* creation of asset from another asset
* Position in underlying + opposite position in derivative = risk free asset
* ==LONG Asset + SHORT Derivative = RF bond==
* without arbitrage, replication will not produce excess return

![[d-pricing.png|400]]

* ==risk aversion is not a factor== for derivative pricing since S0 already accounts for it
* derivative prices assume **risk neutrality / arbitrage free**

## Valuation
* forwards / futures do not require cash outlay at t0

## FRA
![[d-fra.png|600]]

## Swaps
* Swap = Long a floating rate bond and short a fixed rate bond

## Options
1) Call value is directly proportional to St
2) Call value is inversely proportional to Exercise Price
3) ==Call options directly proportional to int rate==
4) Call options value directly proportional to time
5) more volatility more prices for both call and puts
6) ==options receive no benefits and pay no costs - worth less if there are benefits==

* Payments, such as dividends, reduce the value of the underlying which increases the value of a European put option

## Put-Call Parity
* Same underlying + European Options
* Long call + 0 CP bond = Long put + Long stock

## Put-Call Forward Parity
* Long call + Long 0 CP bond = Long put + Long Forward  + Long 0 CP Bond

## American vs European
* Dividends are good for American
* European call option is worth less the more dividends are paid by the underlying.
![[d-america.png|600]]