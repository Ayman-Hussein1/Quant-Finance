# Quant-Finance
Quant Finance Boot Camp (Summer 2025)
The Erdos Institute


Summary:


Mini Project 1 – Portfolios analysis

In this mini project, we built two different portfolios of stocks of our choice using data from the previous two years. The goal was to have one portfolio being of higher risk than the other, yet both are profitable. In order to achieve this, we built the first portfolio using low volatility stocks that are of daily usage (e.g., Costco) and ensured diversification. Minimizing the volatility of this portfolio led to balanced weights, as one would expect, and the optimal volatility was 19% while the expected two-year return is 82%. On the other hand, the riskier portfolio was built without diversification by choosing stocks from the same sector, primarily the tech sector since it showed huge returns in the last two years. The weights were then calculated in order to maximize profits, which ended up giving a volatility of 33% and expected returns of 130%!



Mini Project 2 – Normality analysis

In this min project, we wanted to check if the log returns of stocks are normally distributed or not, which is a common assumption in mathematical finance. The approach we took initially to investigate this was by attempting to fit a normal distribution to the histogram of log returns of various stocks in different periods. Another way this could be done is through using direct normality tests within the python packages. It was surprising to find that some stocks showed normality in longer periods of time using the fitting methods, but not true using the tests. This wasn’t resolved by avoiding extreme points or using different/shorter periods of returns, so I attribute this lack of normality to the choices of stocks I made, they seem to have been going through wild periods in the past two years!



Mini Project 3 – Put and Call options analysis

In this mini project, we aimed to investigate the time and spot price sensitivity of the call and put option pricing under the Black-Scholes assumptions. Focusing on the call options, we found that the rate of change of the call option with respect to expiration time decreased as the time to expiration increases. This makes sense given that the option price converges to the average spot price as time to expiration increased, which implies a smaller rate of change as time goes on since we get to be more certain about the outcome later on. On the other hand, the rate of change of the call price with respect to the spot price showed a sigmoid behavior around the strike price. One can see this when thinking about the call option price for larger spot price, since at that stage the call option is guaranteed to win leading to a constant rate of change with the spot price that saturates at a maximum of spot price – strike price. The same analysis can be applied to the put option pricing.



Mini Project 4 – Variable volatility hedging

In this last project, we aimed to explore more real-world scenarios where we work with variable volatility for the stock paths and try to apply hedging strategies in those scenarios. We explored hedging under constant volatility and saw how this neutralizes the drift in stock prices, but we found that for a simple case of variable volatility this is no longer the case. Under uniform volatility distribution for each path and another time for each step, one can see the drift playing a significant role in the predicted pricing. In particular, simulating stock paths with different volatility per path gave an average price close to the Black-Scholes pricing when the drift is set to zero. However, when assuming a variable volatility (still drawn from a uniform constant distribution) for each step in each path, which is more similar to the real world, one finds that the average price for the call option is always larger than the Black-Scholes price regardless of the number of hedges. Hence, hedging helps in getting the simulated mean closer to the Black-Scholes price, but the variable volatility still shows up in their deviation.

