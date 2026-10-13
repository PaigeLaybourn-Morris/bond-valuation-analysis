
# Bond Valuation and Interest Rate Sensitivity Analysis

## Project Overview

This project uses Python to explore bond valuation and investigate how changes in interest rates affect bond prices. It applies mathematical and financial concepts to a computational model, using numerical analysis and data visualisation to understand the relationship between bond yields, prices and maturity.

The project was developed as an extension of university-level actuarial mathematics, with a focus on applying quantitative reasoning and Python programming to a practical financial problem.

**[Open the Google Colab Notebook](https://colab.research.google.com/github/PaigeLaybourn-Morris/bond-valuation-analysis/blob/main/bond_valuation.ipynb)**

## Objectives

- Implement a bond pricing model using Python.
- Calculate theoretical bond prices under different yield assumptions.
- Investigate the relationship between bond yields and prices.
- Compare the interest rate sensitivity of bonds with different maturities.
- Present findings using data tables and visualisations.
- Interpret the financial implications of the results.

## Tools and Technologies

- **Python** – Implementing the bond pricing model and performing calculations.
- **NumPy** – Generating numerical ranges of interest rates.
- **pandas** – Organising calculated bond prices into structured data tables.
- **Matplotlib** – Visualising the relationship between bond yields, prices and maturities.
- **Google Colab** – Developing and executing the Python notebook.
- **GitHub** – Version control and project documentation.

## Methodology

### 1. Bond Pricing Model

A bond's theoretical price is calculated as the present value of its future coupon payments plus the present value of the repayment received at maturity.


The model uses the following formula:

```math
P = \sum_{t=1}^{n} \frac{C}{(1+i)^t} + \frac{N}{(1+i)^n}
```

Where:

- $P$ = theoretical bond price
- $C$ = annual coupon payment
- $N$ = face value repaid at maturity
- $i$ = annual yield
- $n$ = number of years until maturity
- $t$ = year in which a payment is received



A reusable Python function was developed to calculate bond prices from the face value, coupon rate, yield and maturity.

### 2. Yield Sensitivity Analysis

The model calculates bond prices across a range of yields from 1% to 10%, holding the face value, coupon rate and maturity constant.

The results are stored in a pandas DataFrame and visualised using Matplotlib, with a reference line indicating the bond's face value.

This analysis investigates how changes in the yield used to discount future cash flows affect the theoretical price of a bond.

### 3. Maturity Sensitivity Analysis

The model is extended to compare bonds with maturities of 2, 5, 10 and 20 years.

By varying the yield while keeping other assumptions constant, the analysis compares how the prices of bonds with different maturities respond to interest rate changes.

This helps illustrate the relationship between maturity and interest rate sensitivity.

## Key Findings

The initial yield sensitivity analysis demonstrates that bond prices decrease as yields increase, assuming all other factors remain constant.

For a bond with a face value of £1,000, an annual coupon rate of 5% and a maturity of five years, the model produces the following results:

| Annual yield | Theoretical bond price |
|---:|---:|
| 1% | £1,194.14 |
| 3% | £1,091.59 |
| 5% | £1,000.00 |
| 7% | £918.00 |
| 10% | £810.46 |

These results illustrate three key principles:

- **Inverse relationship:** Bond prices generally fall as yields rise because future fixed payments are discounted at a higher rate.
- **Price at face value:** When the annual yield equals the coupon rate, the bond is priced at its £1,000 face value under the model's assumptions.
- **Premium and discount pricing:** When the yield is below the coupon rate, the bond trades above face value; when the yield is above the coupon rate, it trades below face value.

The maturity comparison further investigates how the size of price movements differs between shorter- and longer-term bonds.

## Assumptions and Limitations

The model uses simplified assumptions to focus on the mathematical relationship between bond prices and yields:

- Coupon payments are made annually.
- The annual yield is applied consistently to discount future cash flows.
- Coupon payments and the face value repayment are fixed.
- The initial analysis uses hypothetical bond parameters rather than observed market prices.
- The model does not account for transaction costs, taxes, credit risk, inflation or changes in market liquidity.

Consequently, the calculated prices are theoretical values under the specified assumptions and should not be interpreted as live market valuations or investment recommendations.

## How to Run the Project

1. Open the notebook using the Google Colab link above.
2. Select **Runtime → Run all** to execute the notebook cells.
3. Review the calculated bond prices, data tables and visualisations.
4. Modify the model inputs to investigate alternative yields, coupon rates or maturities.

The required libraries are NumPy, pandas and Matplotlib. These are commonly available in Google Colab.

## Skills Demonstrated

- Mathematical modelling and financial calculations
- Python programming and reusable functions
- Numerical analysis and sensitivity analysis
- Data manipulation using pandas
- Data visualisation using Matplotlib
- Interpretation and communication of quantitative results

## Future Improvements

Potential extensions include:

- Incorporating real-world bond market data.
- Comparing theoretical prices with observed market prices.
- Investigating the effect of different coupon rates on price sensitivity.
- Exploring additional bond valuation measures, such as duration.
- Developing an interactive tool to calculate bond prices under user-defined assumptions.

## Author

**Paige Laybourn-Morris**

Mathematics and Statistics undergraduate student interested in data analysis, quantitative modelling and financial applications of Python.
