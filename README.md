# 05_API_homework_disaster
Homework unfinished for 5- API's - why isn't this due on Sunday anymore :-P



Part 1 - Personal Finance Planner
In this section of the challenge, you will create a personal finance planner application. To develop the personal finance planner prototype, you should take into account the following assumptions:


The average household income for each member of the credit union is $12,000.


Every union member has a savings portfolio composed of cryptocurrencies, stocks and bonds:


Assume the following amount of crypto assets: 1.2 BTC and 5.3 ETH.


Assume the following amount of shares in stocks and bonds: 50 SPY (stocks) and 200 AGG (bonds).




Use the starter Jupyter notebook to complete the following steps.

Collect Crypto Prices Using the requests Library


Create two variables called my_btc and my_eth. Set them equal to 1.2 and 5.3, respectively.


Use the requests library to fetch the current price in US dollars of bitcoin (BTC) and ethereum (ETH) using the Alternative Free Crypto API endpoints provided in the starter notebook.


Parse the API JSON response to select only the crypto prices and store each price in a variable.
Hint: Be aware of the particular identifier for each cryptocurrency in the API JSON response - the bitcoin identifier is 1 whereas ethereum is 1027.


Compute the portfolio value of cryptocurrencies and print the results.



Collect Investments Data Using Alpaca: SPY (stocks) and AGG (bonds)
Important: Remember to create a .env file in your working directory to store the values of your Alpaca API key and Alpaca secret key.


Create two variables named my_agg and my_spy and set them equal to 200 and 50, respectively.


Set the Alpaca API key and secret key variables, then create the Alpaca API object using the tradeapi.REST function from the Alpaca SDK.


Format the current date as ISO format. You may change the date set in the starter code to the current date.


Get the current closing prices for SPY and AGG using Alpaca's get_barset() function. Transform the function's response to a Pandas DataFrame and preview the data.


Pick the SPY and AGG close prices from the Alpaca's get_barset() DataFrame response and store them as Python variables. Print the closing values for validation.


Compute the value in dollars of the current amount of shares and print the results.



Savings Health Analysis
In this section, you will assess the financial health of the credit union's members.


Create a variable called monthly_income and set its value to 12000.


To analyze savings health, create a DataFrame called df_savings with two rows. Store the total value in dollars of the crypto assets in the first row and the total value of the shares in the second row.
Hint: The df_savings DataFrame should have one column named amount and two rows where crypto and shares are the index values:



Use the df_savings DataFrame to plot a pie chart to visualize the composition of personal savings.


Use if conditional statements to validate if the current savings are enough for an emergency fund. An ideal emergency fund should be equal to three times your monthly income.


If total savings are greater than the emergency fund, display a message congratulating the person for having enough money in this fund.


If total savings are equal to the emergency fund, display a message congratulating the person on reaching this financial goal.


If total savings are less than the emergency fund, display a message showing how many dollars away the person is from reaching the goal.





Part 2 - Retirement Planning
In this section, you will use the Alpaca API to fetch historical closing prices for a retirement portfolio and then Use the MCForecastTools toolkit to create Monte Carlo simulations to project the portfolio performance at 30 years. You will then use the Monte Carlo data to answer questions about the portfolio.
Follow the steps outlined in the starter notebook to complete the following:

Monte Carlo Simulation


Use the Alpaca API to fetch five years historical closing prices for a traditional 40/60 portfolio using the SPY and AGG tickers to represent the 60% stocks (SPY) and 40% bonds (AGG) composition of the portfolio. Make sure to convert the API output to a DataFrame and preview the output.


Configure and execute a Monte Carlo Simulation of 500 runs and 30 years for the 40/60 portfolio.


Plot the simulation results and the probability distribution/confidence intervals.





Retirement Analysis


Fetch the summary statistics from the Monte Carlo simulation results.


Given an initial investment of $20,000, calculate the expected portfolio return in dollars at the 95% lower and upper confidence intervals.


Calculate the expected portfolio return at the 95% lower and upper confidence intervals based on a 50% increase in the initial investment.



Optional Challenge - Early Retirement
The CTO of the Credit Union was really impressed with your work on this planner, but commented that 30 years seems like such a long time to wait to retire! The CTO starts wondering if the retirement plan could be adjusted to account for an earlier than normal retirement.
Try adjusting the portfolio to either include more risk (a higher stock than bond ratio) or to have a larger initial investment and rerun the retirement analysis to see what it would take to retire in 5 or 10 years instead of 30!


Hints and Considerations


To allow for quicker work during the Monte Carlo simulation, start out by running 100 simulations for one year of returns, and when you have the code worked out, run the full 500 simulations for 30 years.


Remember to add the .env files to the .gitignore configuration to avoid exposing your API keys in your GitHub repository.


A .gitignore file contains file names and extensions of files that you don't want pushed to your repository. For more information on how a gitignore works, you can read the documentation here.




Submission


Use the starter Jupyter Notebook for your Personal Finance Planner.


Submit your notebook to a new GitHub repository and create a README.md file.


Submit the link to your GitHub project to Bootcampspot for grading.


