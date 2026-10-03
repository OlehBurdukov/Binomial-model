# Binomial Model
This project contains essential computation and illustration functions for valuation of call and put options by well known binomial model. 
The whole project was created as an extended version of my university project on the same topic. 
Taking this opportunity, I'd like to express my gratitude to Associate Professor Dr. Josef Leydold for conducting the course of Computing and for the clear and reasonable assignment design that inspired me to proceed my work on this project using the initial tasks as an appropriate basis. 
I'd also like to pay a tribute to my trusted peer advisor Ivan Tsots for his organisational advice on my project.

## Contents
- 'Binomial model.R' – the main R script with all functions.
- 'Binomial model.Rproj' – the RStudio file containing the project
- 'Binomial_model.Rnw' – the LaTeX document
- 'Binomial_model.pdf' – the ready-to-read PDF document with presentation of the project

## How to run
1. Clone the repository
2. Open the `.Rproj` file in RStudio
3. Run `binomial_model.R`

## Description of Functions
binomial.eu.call() --- estimates the present value of an European call. 

binomial.eu.put() --- estimates the present value of an European put.

Key inputs:
  - 'r' – risk free interest rate (p.a.)
  - 's' – volatility rate of the underlying.
  - 'S0' – current price of underlying.
  - 'E' – the exercise price.
  - 'T' – period of time to maturity date (in years).
  - 'n' – number of steps in the binomial tree.
  - 'position' – postion in the contract. Possible entries: 'long', 'short'.
  - 'show_payoff' – if 'TRUE', displays the payoff graph (incl. premium).

binomial.am.call() --- estimates the present value of an American call.

binomial.am.put() --- estimates the present value of an American put.

Additionally to the input from the previous functions, the latter 2 also have:
- 'div' – if not 'NULL', considers the given amount of dividends in the model.
- 'exdivdate' – assigns the ex-dividend date into function. Cannot be missed, if 'div' isn't 'NULL'.

binomial.path() --- helps model a sample binomial path given the input for an option.
                    The output contains all spot rates of underlying across the binomial tree as well as its pace from today till the maturity date.

Key inputs:
- 'S0' – current price of underlying.
- 'r' – risk free interest rate (p.a.).
- 's' – volatility rate of the underlying.
- 'n' – number of steps in the binomial tree.
- 'T' – period of time to maturity date (in years).
- 'plot' – if 'TRUE', plots a sample binomial path of the underlying.
