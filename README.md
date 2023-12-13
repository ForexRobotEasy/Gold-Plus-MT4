# Gold Plus MT4

Gold Plus MT4 is an automated Forex trading software developed by the Forex Robot Easy team. This software is designed for trading XAU/USD (Gold) pairs on the MetaTrader 4 platform. 

For detailed reviews and trading results of this product, please visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/review-gold-plus-mt4-automated-forex-software-for-xauusd-trading/).

## Input Parameters

- `lotSize`: The lot size for each trade (default: 0.01)
- `stopLoss`: The stop loss in pips (default: 100)
- `takeProfit`: The take profit in pips (default: 200)

## Global Variables

- `ticket`: The order ticket number
- `isTradeOpen`: A flag to check if a trade is open

## Initialization Function

The `OnInit()` function is the initialization function of the expert advisor. It is called once when the expert advisor is attached to a chart.

## Deinitialization Function

The `OnDeinit()` function is the deinitialization function of the expert advisor. It is called once when the expert advisor is removed from a chart.

## Tick Function

The `OnTick()` function is the main function of the expert advisor. It is called on every tick of the market. 

In this function, the EA checks if a trade is already open. If a trade is open, the function returns. Otherwise, it performs market analysis using the `PerformClusterAnalysis()` function to determine whether to enter a trade. If the conditions are met, a buy trade is opened using the `OrderSend()` function.

## Perform Cluster Analysis Function

The `PerformClusterAnalysis()` function is responsible for performing cluster analysis and determining the trading decision. This function should contain the cluster analysis code and return `true` if the conditions are met to enter a trade, or `false` otherwise.

## Close Trade Function

The `CloseTrade()` function is used to close the current trade. It closes the trade using the `OrderClose()` function with the appropriate parameters.

## Trade Event Handling Function

The `OnTrade()` function is responsible for handling trade events. It checks if the current trade has been closed by checking the `OrderSelect()` and `OrderCloseTime()` functions. If the trade has been closed, the `isTradeOpen` flag is set to `false`.

Please note that ForexRobotEasy is not the official developer of this product. We are only providing a sample code that can work as described in this product. To find the official developer of this product, please use MQL5.
