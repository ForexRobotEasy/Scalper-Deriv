# Scalper Deriv

This code is a sample implementation of a scalping strategy for the MetaTrader 5 platform. It is designed to place trades based on market conditions with a focus on quick profits. The code calculates the lot size, stop loss, and take profit levels based on the account balance. 

## Input Parameters

- `AccountBalance`: The account balance to be used for lot size calculation. The default value is set to 5000.0.
- `RentPeriod`: The rent period in days. The default value is set to 30.

## Initialization

The `OnInit` function is called during the initialization of the expert advisor. It calculates the lot size based on the account balance. The lot size is determined by different ranges of the account balance. For account balances above $200,000, the lot size is set to 10.0. For account balances between $100,000 and $200,000, the lot size is set to 5.0. For account balances between $50,000 and $100,000, the lot size is set to 2.5. For account balances between $20,000 and $50,000, the lot size is set to 1.0. For account balances below $20,000, the lot size is set to 0.5. The stop loss and take profit levels are also calculated in this function.

## Trade Execution

The `OnTick` function is called on each tick of the market. It implements the scalping strategy by placing trades based on market conditions. In this code, an example trade execution is shown using the `OrderSend` function. It places a buy order with the calculated lot size at the current ask price with a fixed stop loss and take profit level.

## Utility Function

The `OnTimer` function is a utility function that is called periodically. In this code, it is used to check if the rent period is over. If the rent period is zero, trading is disabled by calling the `ExpertRemove` function. Otherwise, the rent period is decreased by one day.

---

## Product Description

Scalper Deriv is a powerful expert advisor developed by the Forex Robot Easy Team. It is designed to elevate your forex scalping strategy and help you achieve quick profits in the market.

With Scalper Deriv, you can take advantage of market conditions and place trades with precision. The expert advisor calculates the lot size, stop loss, and take profit levels based on your account balance, ensuring optimal risk management.

This expert advisor is perfect for traders who prefer the scalping strategy, aiming to profit from short-term market movements. It executes trades quickly and efficiently, allowing you to take advantage of even the smallest price fluctuations.

Scalper Deriv is easy to use and customize. You can adjust the input parameters, such as the account balance and rent period, to suit your trading preferences. The expert advisor also includes a utility function to disable trading after a specified rent period, providing flexibility and control over your trading activities.

Please note that Forex Robot Easy is not the official developer of Scalper Deriv. We only provide this code as a sample implementation that can work as described in the product. For detailed reviews and trading results of Scalper Deriv, please visit the official developer's website using the following link: [Scalper Deriv Review - Elevate Your Forex Scalping Strategy](https://forexroboteasy.com/forex-robot-review/scalper-deriv-review-elevate-your-forex-scalping-strategy/). To find the official developer of this product and obtain the official version, please refer to the MQL5 platform.
