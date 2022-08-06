# Loan Data from Prosper Exploration
## by IBRAHIM SALMAN


## Dataset

This data set contains 113,937 loans with 83 variables (2 new variables on `YearlyIncomeEstimate`(derived from `StatedMonthlyIncome`) and `IncomeRange`(derived from `YearlyIncomeEstimate`) to better stratify the data set) on each loan, including loan amount, borrower APR, borrower rate (or interest rate), current loan status, borrower income, and many others. The data set can be found [here](https://docs.google.com/document/d/e/2PACX-1vQmkX4iOT6Rcrin42vslquX2_wQCjIa_hbwD0xmxrERPSOJYDtpNc_3wwK_p9_KpOsfA6QVyEHdxxq7/pub) and feature documentation [here](https://docs.google.com/spreadsheets/d/1gDyi_L4UvIrLTEC6Wri5nbaMmkGmLQBk-Yx3z0XDEtI/edit#gid=0)


## Required Modules
* numpy
* pandas
* matplotlib.pyplot
* seaborn

## Installations
The modules listed in the section above can be downloaded in the anaconda IDE (recommended software to run the ipynb files) using `conda install module_name` or the conventional `pip install module_name`

## Setup
The recommended way to run the ipynb files is by setting up a virtual environment with conda and running the files in a jupyter notebook. Click [here](https://docs.conda.io/projects/conda/en/latest/user-guide/tasks/manage-environments.html) to learn how to set up and manage virtual environments with conda.<br><br>
The html files that contains all the necessary codes and findings are also available in the `main` branch

## Known Bugs
The files in this repo currently have no bugs.

## Summary of Findings

In the exploration, I found that there was a strong relationship between borrower APR and credit grade.<br><br>
Here are the findings I got from the univariate explorations:
1. Most persons are on the 36-month term loan.
2. About half of the dataset are current borrowers.
3. Most borrowers are from california.
4. Most borrowers classified their occupation as "Others" followed by "Professional"
5. About 80% of borrowers are employed, About 5% are self-employed, About 1% are Not employed and About 1% are retired.
6. Most borrowers have income ranges of USD25,000-49,999 and USD50,000-74,999
7. TheStatedMonthlyIncome data has some outliers and most of the stated monthly income is from the range of 0 and 2000.
8. The DebtToIncomeRatio data has some outliers and most of the data are within the 0 and 1 range.
9. About half of the borrowers are homeowners and the other half aren't
10. About half of the borrowers took out a loan for Debt Consolidation.

Here are the findings I got from my bivariate explorations:
1. The BorrowerAPR, BorrowerRate, LenderYield have almost perfect positive correlations.
2. The borrower's APR has a negative relationship with the Prosper Principal Borrowed
3. The borrower APR negatively correlates with the Loan Original Amount
4. Generally, the higher the credit grade level, the lower the Borrower APR.
5. Compared to Not employed and Other Employment Statuses, persons that are employed, self_employed, and retired, have lower Borrower APR
6. Starting from the USD1-24,999 range, the Borrower APR generally decreases with ncreasing income range.
7. The low Borrower APR of the USD0 range might be due to that only 0.5% of the total data is in that range.
8. The Not Employed range has the highest Borrower APR average in the data set.
9. The Borrower APR is generally lower for persons who are homeowners.
10. The Borrower APR for the 36 month term is slightly lower than the Borrower APR of the other 2 term

Here are the findings I got from my multivariate explorations:
1. There is a positive correlation between the Borrower APR and Original Loan Amount when the data is grouped by credit grade.
2. The positive correlation reduces from grade AA to grade E but spikes at grade HR
3. The 36-month term generally has lower Borrower APR for the Employed, Retired, and Self-employed Employment Statuses
4. The Not employed Employment Status has lower APR for the 60-month loan term probably to offer more time to pay up since that category doesn't have a regular source of income.
5. It can also be seen that the credit grade is a more prominent factor in determining the borrower APR as borrowers with higher credit grades will always get lower borrower APR regardless of their income range.

## Key Insights for Presentation
I'll be presenting the trend that answers the question "what factors affect Borrower APR". This will be the flow of visualizations in the presentation:
1. Borrower APR Distribution
2. Credit Grade Distribution
3. Income Range Distribution
4. Borrower APR Vs. Credit Grade
5. Borrower APR Vs. Income Range
6. Borrower APR Vs. Credit Grade & Income Range <br><br>
The presentation can be found in the `main` branch tagged `Part_II_slide_deck_template.slides.html`

## Contributing
To make a contribution:
- Fork the repo
- Make Changes
- Send your pull request for review

## Show Love 💓
Show Love by giving the Repo a star...😇
