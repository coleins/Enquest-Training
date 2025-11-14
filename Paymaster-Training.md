# PAYMASTER TRAINING

## PAYSLIP
1. Taxable Income = Gross Salary - Statutory Deductions
2. Net Pay = Gross Salary - (Statutory Deductions + PAYE)
3. PAYE = 

## SHIF = Employee contributes 2.75% of gross salary; minimum KSh 300/month; no cap

## NHIF = From 1 Feb 2025 tiered contributions: Tier I (6% of first KSh 8,000 gross) and Tier II (6% of gross between KSh 8,001 and KSh 72,000) — maximum employee contribution KSh 4,320/month.

## NHDF = Employee contributes 1.5% of gross salary (and employer also contributes)

## Gross Pay is the total monthly pay before any statutory or voluntary deductions

1. Taxable income = Gross Pay - Allowable Deductions (Statutory deductions)

### after calculating Gross Pay calculate the statutory deductions, other deductions and PAYE to be filled in the deductions column

2. Contribution = NSSF + Pension
3. PAYE = Tax Chargeable - Personal Relief
4. Net Pay = Gross Pay - (PAYE + NSSF + SHIF + Housing Levy)

## GRATUITY CALCULATION

1. Import service gratuity from paymster desktop after it has calculated
2. In the new system use Yearly Tax Table
3. No of years to be included in the computation of gratuity should be provided by the client
4. In the gratuity table contribution is NSSF + Pension
5. Gratuity formula provided by client to be input in the service gratuity setting in payroll settings(Minimum No. Of Year(s) For Gratuity, Gratuity Calculated On, )

| Year | Previous Gross (A) | Contribution (B) | Prev. Taxable Gross (C = A - B) | Service Gratuity (D) | New Gross (E = A + D) | New Taxable Gross (F = E - B) | New Tax Amount (G) | Tax Relief (H) | Previous Tax Paid (I) | Taxable Pay (J = G - H - I) |
| ---- | -----------------: | ---------------: | ------------------------------: | -------------------: | --------------------: | ----------------------------: | -----------------: | -------------: | --------------------: | --------------------------: |
| 2025 |          1,200,000 |           60,000 |                       1,140,000 |              100,000 |             1,300,000 |                     1,240,000 |            372,000 |         28,800 |               350,000 |                      -6,800 |
| 2024 |          1,100,000 |           55,000 |                       1,045,000 |               95,000 |             1,195,000 |                     1,140,000 |            342,000 |         26,400 |               320,000 |                      -4,400 |
| 2023 |          1,050,000 |           50,000 |                       1,000,000 |               90,000 |             1,140,000 |                     1,090,000 |            327,000 |         25,200 |               305,000 |                      -3,200 |
| 2022 |            950,000 |           45,000 |                         905,000 |               85,000 |             1,035,000 |                       990,000 |            297,000 |         22,800 |               280,000 |                      -5,800 |
| 2021 |            900,000 |           40,000 |                         860,000 |               80,000 |               980,000 |                       940,000 |            282,000 |         21,600 |               265,000 |                      -4,600 |

| Column                      | Description                                                                                                                                    | Computation Formula / Logic                                                             |
| :-------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------------------------------------- |
| **Year**                    | The financial or calendar year the computation refers to.                                                                                      | — _(Manually entered/ System generated(by default last 5 years of employees))_          |
| **Previous Gross (A)**      | The total gross income from the previous year before any deductions. This includes all earnings such as basic salary, allowances, and bonuses. | — _(Manually entered/System generated(for the whole year))_                             |
| **Contribution (B)**        | The total statutory or voluntary deductions from the gross (e.g., NSSF, pension contribution).                                                 | — _(Manually entered/System generated(nssf + pension))_                                 |
| **Prev. Taxable Gross (C)** | The taxable income after deducting contributions from the previous gross pay.                                                                  | `C = A - B`                                                                             |
| **Service Gratuity (D)**    | A lump-sum or periodic benefit paid (e.g., at end of service or contract renewal).                                                             | — _(Manually entered/System generated(depending on clients formula e.g [Basic]\*0.33))_ |
| **New Gross (E)**           | The adjusted gross income after adding the gratuity to the previous gross.                                                                     | `E = A + D`                                                                             |
| **New Taxable Gross (F)**   | The taxable amount for the current computation period after subtracting contributions from the new gross.                                      | `F = E - B`                                                                             |
| **New Tax Amount (G)**      | The total tax computed based on the **income tax table** or system tax logic applied to `F`.                                                   | _(System computed — based on yearly IT table)_                                          |
| **Tax Relief (H)**          | The allowable reduction in tax liability (e.g., monthly or annual personal relief).                                                            | — _(System computed or fixed amount)_                                                   |
| **Previous Tax Paid (I)**   | The total tax paid previously, before recalculation or adjustments.                                                                            | — _(Manually entered/System generated)_                                                 |
| **Taxable Pay (J)**         | The net tax payable or refundable after considering relief and previously paid tax. A negative value means an overpayment/refund.              | `J = G - H - I`                                                                         |

## NON CASH BENEFIT CALCULATION

Under the Income Tax Act (Cap 470) and KRA PAYE regulations,
Non-Cash Benefits (also called fringe benefits or benefits-in-kind) that an employer provides to an employee are considered part of gross taxable income.

Examples include:

Free or subsidized housing, Company car, Meals, fuel, utilities, airtime, etc.

Employer-paid personal bills

However, there’s a de minimis (minimum) threshold — that is, small benefits below a certain total value per month don’t need to be taxed.
