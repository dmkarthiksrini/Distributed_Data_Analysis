# Distributed Data Analysis assignment

Credit is the ability of a legal entity to borrow money or access goods or services to be paid for later under a predefined contract. Credit is fundamental for the functioning of an economy because it increases consumer spending, which leads to an increase in producer spending and, as a result, an increase in economic activity and growth.

A credit score is a 3-digit number that is used to determine an individual, business, or nation's ability to service a debt. This is used by banks and other financial institutions as a credit risk management mechanism to prevent defaults by clients on their loans, thus providing credit to clients which have a high or acceptable credit score because the higher the credit score the more trustworthy the client would honor his or her loan payment plans.

Credit default is when a legal entity is not able to repay its contractual debt within the agreed period after other measures have been taken by the financial institution and is considered a loss to the financial institution. Most major financial crises around the world, like the Greece financial crisis and the housing mortgage crisis in the US were a result of consumer credit defaults, which in turn affected other financial institutions and the overall economy, leading to job losses, inflation, and recession.

**Importance of credit score as a tool to prevent credit default**

- Credit scores serve as risk management tools to enable banks and other financial institutions to issue loans with high predictability of repayment, thus reducing the cost of servicing defaulted and bad loans.
- Credit scores promote good financial behavior from consumers given the strong positive correlation between credit scores and the ability to access a loan.
- Credit scores are used as a proxy to determine mortgage financing, leading to house ownership and eventually family shelter. Thus, it can be used as a tool to promote home ownership or discriminate against certain ethnic minorities.

Thus, we can conclude that credit scores can help significantly reduce credit defaults which in turn leads to a healthy economy and increased productivity and economic growth, and welfare.

**Research question**

Thus, given the importance of credit score and the relationship between an individual's credit score and Loan default, we would be using a bank's client’s database of past transactions and other customer details to provide a better means to the bank’s management to issue healthy credits. Thus, we would be interested in finding answers to the following research questions

- Primary research question: Given a bank's client's historic transaction and better details, how can we determine the client's ability to service his debt by either defaulting or not defaulting?
- Secondary research questions: Given a bank’s client's historic transactions and personal details, how can we provide a credit score which is reflective of the client's ability to service his or her debts?

**Data description**

| Column   _Name           | Description                                                           | Data_Type          | Is this a Factor |
|--------------------------|-----------------------------------------------------------------------|--------------------|------------------|
| ID                       | Represents a unique   identification of an entry                      | Character (Unique) |                  |
| Customer_ID              | Represents a unique   identification of the Client                    | Character (Unique) |                  |
| Month                    | Represents the month   of the year                                    | Character          |                  |
| Name                     | Represents the name   of a person                                     | Character          |                  |
| Age                      | Represents the age of   the person                                    | Numeric            |                  |
| SSN                      | Represents the social   security number of a person                   | Numeric            |                  |
| Occupation               | Represents the   occupation of the person                             | Character          | Factors          |
| Annual_Income            | Represents the annual   income of the person                          | Numeric            |                  |
| Monthly_Inhand_Salary    | Represents the   monthly base salary of a person                      | Numeric            |                  |
| Num_Bank_Accounts        | Represents the number   of bank accounts a person holds               | Numeric            |                  |
| Num_Credit_Card          | Represents the number   of other credit cards held by a person        | Numeric            |                  |
| Interest_Rate            | Represents the   interest rate on credit card                         | Numeric            |                  |
| Num_of_Loan              | Represents the number   of loans taken from the bank                  | Numeric            |                  |
| Type_of_Loan             | Represents the types   of loan taken by a person                      | Character          | Factors          |
| Delay_from_due_date      | Represents the   average number of days delayed from the payment date | Numeric            |                  |
| Num_of_Delayed_Payment   | Represents the   average number of payments delayed by a person       | Numeric            |                  |
| Changed_Credit_Limit     | Represents the   percentage change in credit card limit               | Numeric            |                  |
| Num_Credit_Inquiries     | Represents the number   of credit card inquiries                      | Numeric            |                  |
| Credit_Mix               | Represents the   classification of the mix of credits                 | Character          | Factors          |
| Outstanding_Debt         | Represents the   remaining debt to be paid (in USD)                   | Numeric            |                  |
| Credit_Utilization_Ratio | Represents the   utilization ratio of credit card                     | Numeric            |                  |
| Credit_History_Age       | Represents the age of   credit history of the person                  | Character          |                  |
| Payment_of_Min_Amount    | Represents whether   only the minimum amount was paid by the person   | Character          | Factors          |
| Total_EMI_per_month      | Represents the   monthly EMI payments (in USD)                        | Numeric            |                  |
| Amount_invested_monthly  | Represents the   monthly amount invested by the customer (in USD)     | Numeric            |                  |
| Payment_Behaviour        | Represents the   payment behavior of the customer (in USD)            | Character          | Factors          |
| Monthly_Balance          | Represents the   monthly balance amount of the customer (in USD)      | Numeric            |                  |


#### Addition Info

#####_Regarding Payment Behaviour_

* Low spent small value payments: 1 (infrequent spending and payment behavior may indicate low credit usage or creditworthiness)
* Low spent medium value payments: 2 (infrequent spending and payment behavior may indicate a lower level of financial engagement)
* Low spent large value payments: 3 (making infrequent payments can be a risk factor, but paying off large bills or making big purchases can also be a sign of financial stability)
* High spent small value payments: 4 (high spending and regular payment behavior can indicate good creditworthiness, but there may be a risk of overspending or carrying a balance)
* High spent medium value payments: 5 (frequent spending and regular payment behavior, coupled with moderate spending amounts, can indicate responsible credit usage and strong creditworthiness)
* High spent Large value payments: 6 (Frequent spending and regular payment behavior, can indicate good creditworthiness)
### Factors (Reason behind considering this columns as Factors is we can convert this a Levels)

- Occupation
- Type_of_Loan
- Credit_Mix
- Payment_Behaviour
- Payment_Of_Min_Amount

---

## Expected Output

| Column_Name | Description | Data_Type |
| --- | --- | --- |
| Credit_rating | Numerical Representation of the credit score | Quantitative |
| Credit_Score |

Represents
the bracket of credit score (Poor, Standard, Good) | Qualitative |
| Credit_Default | Credit default represents whether the client falls into the credit default category (Yes, No) | Qualitative |


## Methodology

[Placeholder for the Methodology Updates]

(Based on comments from George we should update the tasks/operations we have done during the course of Machine Learning Model building)

### Summary of Columns:

| ID               | Customer_ID      | Month            | Name             | Age              | SSN              | Occupation       | Annual_Income    | Monthly_Inhand_Salary |
|------------------|------------------|------------------|------------------|------------------|------------------|------------------|------------------|-----------------------|
| Min.   :    5634 | Length:100000    | Length:100000    | Length:100000    | Length:100000    | Length:100000    | Length:100000    | Length:100000    | Min.   :    303.6     |
| 1st Qu.: 43133   | Class :character | Class :character | Class :character | Class :character | Class :character | Class :character | Class :character | 1st Qu.: 1625.6       |
| Median : 80632   | Mode  :character | Mode  :character | Mode  :character | Mode  :character | Mode  :character | Mode  :character | Mode  :character | Median : 3093.7       |
| Mean   : 80632   |                  |                  |                  |                  |                  |                  |                  | Mean   : 4194.2       |
| 3rd Qu.:118130   |                  |                  |                  |                  |                  |                  |                  | 3rd Qu.: 5957.4       |
| Max.   :155629   |                  |                  |                  |                  |                  |                  |                  | Max.   :15204.6       |
|                  |                  |                  |                  |                  |                  |                  |                  | NA's   :15002         |

___

| Num_Bank_Accounts | Num_Credit_Card   | Interest_Rate     | Num_of_Loan      | Type_of_Loan     | Delay_from_due_date | Num_of_Delayed_Payment | Changed_Credit_Limit | Num_Credit_Inquiries |
|-------------------|-------------------|-------------------|------------------|------------------|---------------------|------------------------|----------------------|----------------------|
| Min.   :    -1.00 | Min.   :     0.00 | Min.   :     1.00 | Length:100000    | Length:100000    | Min.   :-5.00       | Length:100000          | Length:100000        | Min.   :     0.00    |
| 1st Qu.:   3.00   | 1st Qu.:   4.00   | 1st Qu.:   8.00   | Class :character | Class :character | 1st Qu.:10.00       | Class :character       | Class :character     | 1st Qu.:   3.00      |
| Median :   6.00   | Median :   5.00   | Median :  13.00   | Mode  :character | Mode  :character | Median :18.00       | Mode  :character       | Mode  :character     | Median :   6.00      |
| Mean   :    17.09 | Mean   :    22.47 | Mean   :    72.47 |                  |                  | Mean   :21.07       |                        |                      | Mean   :    27.75    |
| 3rd Qu.:   7.00   | 3rd Qu.:   7.00   | 3rd Qu.:  20.00   |                  |                  | 3rd Qu.:28.00       |                        |                      | 3rd Qu.:   9.00      |
| Max.   :1798.00   | Max.   :1499.00   | Max.   :5797.00   |                  |                  | Max.   :67.00       |                        |                      | Max.   :2597.00      |
|                   |                   |                   |                  |                  |                     |                        |                      | NA's :1965           |

___

| Credit_Mix         | Outstanding_Debt | Credit_Utilization_Ratio | Credit_History_Age | Payment_of_Min_Amount | Total_EMI_per_month | Amount_invested_monthly | Payment_Behaviour |        Monthly_Balance | Credit_Score         |
|--------------------|------------------|--------------------------|--------------------|-----------------------|---------------------|-------------------------|-------------------|------------------------|----------------------|
| Length:100000      | Length:100000    | Min.   :20.00            | Length:100000      | Length:100000         | Min.   :      0.00  | Length:100000           | Length:100000     | Length:100000          |        Length:100000 |
| Class   :character | Class :character | 1st Qu.:28.05            | Class :character   | Class :character      | 1st Qu.:   30.31    | Class :character        | Class :character  | Class :character       | Class :character     |
| Mode  :character   | Mode  :character | Median :32.31            | Mode  :character   | Mode  :character      | Median :   69.25    | Mode  :character        | Mode  :character  | Mode  :character       | Mode  :character     |
|                    |                  | Mean   :32.29            |                    |                       | Mean   : 1403.12    |                         |                   |                        |                      |
|                    |                  | 3rd Qu.:36.50            |                    |                       | 3rd Qu.:  161.22    |                         |                   |                        |                      |
|                    |                  | Max.   :50.00            |                    |                       | Max.   :82331.00    |                         |                   |                        |                      |
## Data cleaning

### Initial Findings on the Dataset

- **Empty Values in Column**
    - Name
    - Monthly_Inhand_Salary
    - Type_of_Loan
    - Num_of_Delayed_Payment
    - Changed_Credit_Limit
    - Num_Credit_Inquiries
    - Amount_invested_monthly
    - Monthly_Balance
- **Erratic Values [ “!@9#%8” , “#F%$D@*&8”, “_______”, “_(Underscore)” , “__10000__”, “__-333333333333333333333333333__”, Extreme or Empty Values]**
    - Occupation - (_______)
    - SSN - (#F%$D@*&8)
    - Age (28_  & Negative Values)
    - Annual_Income (34847.84_)
    - Num_Bank_Accounts(Negative Values, Extreme Values)
    - Num_Credit_Card (Extreme Values)
    - Interest_Rate (Extreme Values)
    - Num_of_Loan (Extreme Values)
    - Type_of_Loan (Empty Values)
    - Num_of_Delayed_Payment (Extreme Values)
    - Credit_Mix (Empty Values)
    - Outstanding_Debt (3571.7_)
    - Total_EMI_per_month (Extreme Values)
    - Amount_invested_monthly (__10000__)
    - Payment_Behaviour (!@9#%8)
    - Monthly_Balance (**-**333333333333333333333333333)
- **Column which needs conversion to the numeric value**
    - Credit_History_Age (22 Years and 1 Month → 265 Months)
- **Column With No Issues**
    - Customer_ID
    - Month
    - Credit_Utilization_Ratio
    - Payment_of_Min_Amount

## Next Steps:

- In most cases, the values are wrongly entered or not entered, please find the Example below.

| Customer_ID | Name | Age | Occupation |
| --- | --- | --- | --- |
| CUS_0xd40 | Aaron Maashoh | 23 | Scientist |
| CUS_0xd40 |  | 23 | Scientist |
| CUS_0x21b1 | Rick Rothackerj | 28_ | _______ |
| CUS_0x21b1 | Rick Rothackerj | 28 | Teacher |
- We will perform **groupby** and **replace**  option to fix these issues
- Similarly for Extreme values as well, we will validate the update.