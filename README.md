# Pricing-American-Options-with-LSMC
Pricing American Put Options with Lease Squares Monte Carlo

## Introduction
American options provide holders the flexibility to exercise the option at any time before expiration, making their valuation more complex compared to European options. This project focuses on pricing an American put option using the Least Squares Monte Carlo (LSMC) method, as introduced by Longstaff and Schwartz (2001). The LSMC method combines Monte Carlo simulations with regression techniques to approximate the continuation value of the option, helping determine the optimal exercise strategy and price.

## Methodologies
American Put Option Overview:
An American put option gives the holder the right, but not the obligation, to sell an underlying asset at a predetermined price (strike price) at any time before the option's maturity.
The challenge lies in identifying the optimal time to exercise the option to maximize returns.

Least Squares Monte Carlo (LSMC):

Step 1: Generate Monte Carlo price paths for the underlying asset.

Step 2: At each time step (starting from maturity), estimate the continuation value of the option using regression on Chebyshev polynomial features of the asset price.

Step 3: Compare the immediate exercise payoff to the continuation value:

If the immediate exercise value is greater, exercise the option.
Otherwise, continue holding the option.

Step 4: Discount all realized payoffs back to the present to compute the option price.

## Objective
The primary objective of this project is to:

Apply the LSMC method to price an American put option accurately.

Demonstrate the use of Chebyshev polynomials for nonlinear regression in financial applications.

## Significance
The project highlights a practical and computationally efficient approach to pricing American options, a key challenge in quantitative finance. By integrating Monte Carlo simulations with regression techniques, it showcases a robust framework for handling the complexities of early exercise features in financial derivatives.
