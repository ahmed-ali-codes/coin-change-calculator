# 📘 Coin Change Calculator

## 🔍 Purpose
This C program allows a user to select a currency (US Dollar, Australian Dollar, or Euro), enter an amount (between 1 and 95 cents), and calculates the optimal distribution of coins needed to make that amount using a greedy algorithm.

## 🧑‍💻 How It Works

### Currency Selection
The user chooses one of the three supported currencies:
- **US$** (Denominations: 50¢, 25¢, 10¢, 1¢)
- **AU$** (Denominations: 50¢, 20¢, 10¢, 5¢)
- **Euro** (Denominations: 20¢, 10¢, 5¢, 1¢)

### Amount Input
- The user is asked to enter a value between 1 and 95.
- If the selected currency is **AU$**, the amount must be a multiple of 5.
- Invalid amounts prompt the user to re-enter a valid value.

### Coin Distribution Calculation
The program uses fixed coin denominations based on the selected currency and calculates the minimum number of each coin needed to make the entered amount using a greedy algorithm (starting from the largest coin).

### Display Results
The program outputs the exact number of coins for each denomination used.

### Repeat or Exit
After displaying the results, the user is asked: `Do you want to continue? (y/n):`
- Entering `y` restarts the program.
- Entering `n` gracefully exits the program.

## ⚙️ Core Functions Used
- `SelectCurrency()` – Prompts the user to choose a currency.
- `GetAmountInput(currencyChoice)` – Asks and validates the amount based on the selected currency.
- `SetCurrencyDenominations(currencyChoice, denominations)` – Sets coin values for the selected currency.
- `CalculateCoins(amountInput, denominations, coinCount, size)` – Calculates the number of coins for each denomination.
- `DisplayCoinResults(coinCount, denominations, size)` – Displays the final coin breakdown.
- `CheckContinueOrExit()` – Prompts the user to run the program again or exit.

## 📌 Notes
- The program restricts inputs to a maximum of 95 cents and a minimum of 1 cent.
- Built-in validation ensures that user-friendly error messages are displayed for incorrect inputs.
