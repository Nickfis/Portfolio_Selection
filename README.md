# Stochastic Modelling and Optimization: Final Project
## Portfolio Selection with Approximate Dynamic Programming

The repository holds all the different modules built and used for the final proect. Furthermore it holds the data used (including the script for getting and cleaning the data), the documentation and the different visualizations. 
Contributors to this project are Kelly Kuo, Hamed Mirsadeghi, Laurits Marschall and me. 


## Motvation
The aim of portfolio selection problem is selecting an investment strategy that maximizes the portfolio return, while minimizing the total risk of the investment. The strategy consists of selecting a subset of a set of tradable entities, like stocks, bonds, commodities and currencies and decide the time to buy or sell those assets.
This subject is of main interest for banks and asset management firms. 

Traditionally, the portfolio optimization implements Markowitz Portfolio which aims at maximizing the expected return while controlling volatility. In this method no notion of "dead-line" exists so in a sense this method is a single-time period strategy. But in the real world, the investment strategy depends heavily on the time horizon of the investment. For example, banks suggest safer assets for older clients and riskier assets to younger, more stable customers. So the risk aversion depends on the time length of the investment. For example it is reasonable to invest in riskier assets at the beginning of the investment period and toward the end of the investment period move toward safer assets. To take this aspect into account in Markowitz portfolio selection, pre-determined investment limits are set on each tradable assets which cannot be exceeded. But by using the dynamic programming approach, because of considering successive rebalancing periods, it is possible to capture the risk aversion aspect of portfolio optimization problem without pre-determining investment limits of each asset. In this way at the end of each rebalancing time period ("epoch"), depending on whether we are far or close to the investment dead-line, the portfolio adopts itself naturally to adjust the risk aversion and maximize the final expected return.

The issue with using dynamic programming for portfolio optimization the ``curse of dimensionality''. Even considering discrete states, actions, the dimensions of their spaces is huge and it is impractical to use exact dynamic programming. To overcome this issue, we used Monte-Carlo technique and piecewise linear value functions to turn this problem into a stochastic dynamic programming. This project is an implementation of the stochastic approximated dynamic programming (ADP) in portfolio selection based on the model developed by Karamanis [1] and Berthe [2]. The strategy is tested on weekly data of a selection of stocks available in S\&P500.


