# BitMEX Funding Pine Script

###### TradingView Pine script for the BitMEX XBTUSD perpetual swaps contract premium index (XBTUSDPI) and emulated predicted funding rate.

[TradingView Indicator](https://www.tradingview.com/script/RgyVwnXZ-BitMEX-Funding-R1984/)

This indicator attempts to emulate the @BitMEX predicted funding rate for the XBTUSD perpetual swaps contract. 

The indicator is most accurate on the 1-minute interval.  It can be used on higher intervals but will lose accuracy due to smoothing.

Tip: Right-click the scale and enable the "Indicator Last Value" option.

**Change Log**
- First commit: Fork it if you wanna fork. (GNU GPL v3)
- Increased default transparency of funding payout markers.
- Moved payout marker symbol ($) to bottom of indicator.  Tried to create an input to let the user choose top or bottom, but TV pine script does not allow series of strings.

**Previous Changes**
- Tweaked MA algorithm to be more accurate shortly after funding payout.
- Added 8-hour funding payout markers (can be disabled from Inputs menu).
- Added final 8-hour funding rate plot.
- Added labels to plots for easier identification in Style menu.

**Reference**
https://www.bitmex.com/app/contract/XBTUSD
https://www.bitmex.com/app/perpetualContractsGuide#Funding-Rate-Calculations
*Funding Rate (F) = Premium Index (P) + clamp(Interest Rate (I) - Premium Index (P), 0.05%, -0.05%)*
Positive funding rate means longs pay shorts. Negative funding rate means shorts pay longs.

**Indicator Key**
- Green/Red area: Raw values of the calculated funding rate based on the XBT/USD Premium Index (.XBTUSDPI)
- White line: Time-Weighted Average Price (TWAP) of the calculated funding rate
- Lime/Red thick line: Predicted funding rate
- White dotted line: Adjustable EMA of raw funding rate values
- Aqua/Orange line: Final 8-hour funding rate
- Midline value set to interest rate (static 0.01% as of April 21, 2017)

