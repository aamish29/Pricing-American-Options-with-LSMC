# Pricing-American-Options-with-LSMC
Pricing American Put Options with Lease Squares Monte Carlo

## Introduction
American options provide holders the flexibility to exercise the option at any time before expiration, making their valuation more complex compared to European options. This project focuses on pricing an American put option using the Least Squares Monte Carlo (LSMC) method, as introduced by Longstaff and Schwartz (2001). The LSMC method combines Monte Carlo simulations with regression techniques to approximate the continuation value of the option, helping determine the optimal exercise strategy and price.

The project specifically replicates the result from the first row, 6th column of Table 1 in the Longstaff and Schwartz paper. It uses Chebyshev polynomials to fit nonlinear functions during regression, ensuring high accuracy in approximating the continuation value.

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

### Replication of Results:
The methodology is implemented to replicate the price of the American put option as presented in the Longstaff and Schwartz paper (Table 1, Row 1, Column 6).

## Objective
The primary objective of this project is to:
Apply the LSMC method to price an American put option accurately.
Demonstrate the use of Chebyshev polynomials for nonlinear regression in financial applications.
Validate the implementation by replicating results from the Longstaff and Schwartz (2001) paper.

## Significance
The project highlights a practical and computationally efficient approach to pricing American options, a key challenge in quantitative finance. By integrating Monte Carlo simulations with regression techniques, it showcases a robust framework for handling the complexities of early exercise features in financial derivatives.
