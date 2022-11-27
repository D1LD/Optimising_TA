# Optimising_TA
Optimising Technical Indicators for Stock Market Trading 
What We can offer--ROI &PL

# Calculate the total profit/loss for 100 share size orders
total_profit_loss = round(fntk_df["cost/proceeds"].sum(), 2)

# Print the profit/loss metrics
print(f"The total profit/loss of the trading strategy is ${total_profit_loss}.")
# Initialize the variable to hold the value of the invested capital
invested_capital = 0

# Calculate the invested capital by adding the cost of all buy trades
for index, row in fntk_df.iterrows():
    if row["trade_type"] == "buy":
        invested_capital = invested_capital + row["cost/proceeds"]


# Calculate the return on investment (ROI)
roi = round((total_profit_loss / -(invested_capital)) * 100, 2)

# Print the ROI
print(f"The trading algorithm resulted in a return on investment of {roi}%")




