# Table of Contents

- [Project Title](https://github.com/briarholmes/Hello-World/edit/main/README.md#project-title)
- [Project Description](https://github.com/briarholmes/Hello-World/edit/main/README.md#project-description)
- [How to Run Program](https://github.com/briarholmes/Hello-World/edit/main/README.md#how-to-run-program)
- [Data Used in Program](https://github.com/briarholmes/Hello-World/edit/main/README.md#data-used-in-program)

## Project Title

***Iowa Sales Tax Esimator 2023***

## Project Description

This program can calculate the taxes owed from individuals and those filing married jointly for 2023.

## How to Run Program

```text
income = float(input("How much is your annual income: "))


mfj = bool(input("If you are married filling jointly, type 'True',otherwise press ENTER "))


if mfj == True:
    spouse_income = float(input("Please insert the income of your spouse: "))
    income = income + spouse_income
    
else:
    spouse_income = 0 
    income = income + spouse_income
    
max_tax_mfj_1 = 528.00
max_tax_mfj_2 = 2841.60
max_tax_mfj_3 = 7971.60

max_tax_single_1 = 264.00
max_tax_single_2 = 1420.80
max_tax_single_3 = 3985.80

if mfj == True:
    
    if income <= 12000:
        state_tax = 0 + income * 0.0440
        
    elif (income > 12000) and (income <= 60000):
        state_tax = max_tax_mfj_1 + (income - 12000)*0.0482
        
    elif (income >60000) and (income <= 150000):
        state_tax = max_tax_mfj_2 + (income-60000)*0.0570
        
    else:
        state_tax = max_tax_mfj_3 + (income - 150000)*0.0600
        
else:
    
    if income <= 6000:
        state_tax  = 0
        
    elif (income > 6000) and (income <= 30000):
        state_tax = max_tax_single_1 + (income - 6000)*0.0482
        
    elif (income > 30000) and (income <= 75000):
        state_tax = max_tax_single_2 + (income - 30000)*0.0570
        
    else:
        state_tax = max_tax_single_3 + (income - 75000)*0.0600
        
print("Your state tax owed for Iowa in 2023 was $",round(state_tax))

```

### Data Used in Program

[***Data Used in Program***](https://tax.iowa.gov/idr-announces-2023-interest-rates-deductions-income-tax-brackets)
