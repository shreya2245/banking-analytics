# banking-analytics
Develop a basic understanding of risk analytics in banking and financial services and understand how data is used to minimise the risk of losing money while lending to customers.
# About Dataset -
This dataset basically contains information about bank details ,various client details which consists of multiple tables which are interlinked with each other through keys like primary key and foreign key.
The various tables are Banking Relationship, Client-Banking, Gender, Investment Advisor and Period.

# Calculated Functions -

1] Sum : 
The power bi sum function will add all the numbers in a column and the column contains numbers to sum. It returns a decimal number.
Bank Deposit = SUM('Clients - Banking'[Bank Deposits] )

2] DistinctCount :
Counts the number of distinct values in a column
Total Clients = DISTINCTCOUNT('Clients - Banking'[Client ID] )

3] Sumx :
Returns the sum of an expression evaluated for each row in a table.
Total Fees = SUMX('Clients - Banking' , [Total Loan] * 'Clients - Banking'[Processing Fees] )

4] Switch :
Evaluated an expression against a list of values and returns one of multiple possible result expressions
SWITCH(<expression>, <value>, <result>[, <value>, <result>]…[, <else>])

5] DATEDIFF :
Returns the number of interval boundaries between two dates.
Engagment Days = DATEDIFF('Clients - Banking'[Joined Bank],TODAY(), DAY )

# KPI’S: 

# 1] Total Clients : 
Total Clients KPI represents total number of clients in banking.
Total Clients = DISTINCTCOUNT('Clients - Banking'[Client ID] )
<img width="370" height="155" alt="total clients" src="https://github.com/user-attachments/assets/b5ee3a92-c3b4-457d-a18d-769be65eadc9" />

# 2] Total Loan :
Total Loan gives you information about the bank loan + Business lending + credit cards balance of particular  investor , gender.
Total Loan = [Bank Loan] + [Business Lending] + [Credit Cards Balance]
<img width="345" height="152" alt="total loans" src="https://github.com/user-attachments/assets/9e7cf6af-d421-4d07-a8d1-0aa394e9bbf7" />

# 3] Bank Loan :
Bank Loan gives you information what is the loan amount of loan to be repaid by the client to bank.
Bank Loan = SUM('Clients - Banking'[Bank Loans] )
<img width="290" height="123" alt="bank loan" src="https://github.com/user-attachments/assets/dda821c6-354c-4b8d-b8cf-6e7bbe2757ee" />

# 4] Business Lending :
Business lending gives you information about the loan amount given to small business.
Business Lending = SUM('Clients - Banking'[Business Lending] )

<img width="299" height="120" alt="buisness lending" src="https://github.com/user-attachments/assets/a6a08e5a-3741-41d7-8928-c3812437786d" />

# 5] Total Deposit 
Total Deposit gives you information about the amount deposited by particular investors in bank
Total Deposit = [Bank Deposit] + [Savings Account] + [Foreign Currency Account] + [Checking Accounts]

<img width="301" height="132" alt="total deposit" src="https://github.com/user-attachments/assets/bc947a06-601b-44e5-bffd-17207adcb299" />

# 6] Total Fees :
Total Fees is nothing but the amount charged by the bank for account set-up , maintenance charges etc.
Total Fees = SUMX('Clients - Banking' , [Total Loan] * 'Clients - Banking'[Processing Fees] )

<img width="288" height="148" alt="total fees" src="https://github.com/user-attachments/assets/07ca7358-bbf8-490e-a2ce-7bc5227f4eae" />

# 7] Bank Deposit :
Bank deposit is the money put in the bank.
Bank Deposit = SUM('Clients - Banking'[Bank Deposits] )

<img width="293" height="125" alt="bank deposit" src="https://github.com/user-attachments/assets/cb647a61-3c4b-4d7f-85b0-b7faf6a71fa8" />

# 8] Checking Account Amount :
Checking account amount  is nothing but which offers easy access to your money for daily transactional needs.
Checking Accounts = SUM('Clients - Banking'[Checking Accounts] )

<img width="289" height="118" alt="checking amt" src="https://github.com/user-attachments/assets/8b2b7766-417d-41a6-99ca-fc34c6afb222" />

# 9] Total CC Amount :
Total CC Amount is a short-term source of financing for a company by a bank.
Total CC Amount = SUM('Clients - Banking'[Amount of Credit Cards] )

<img width="289" height="131" alt="total cc amt" src="https://github.com/user-attachments/assets/8bf61af1-59e0-4568-b5ad-8d01f8f33a4f" />

# 10] Saving Account Amount :
A savings account is an interest-bearing deposit account held at a bank.
Savings Account = SUM('Clients - Banking'[Saving Accounts] ) 

<img width="291" height="138" alt="savings acc amt" src="https://github.com/user-attachments/assets/46f3a898-ab96-4f17-b101-40213b0664b6" />

# 11] Foreign Currency Amount :
Foreign Currency Account means an account held in a currency that is not the currency of India or Bhutan or Nepal.
Foreign Currency Account = SUM('Clients - Banking'[Foreign Currency Account] ) 

<img width="288" height="148" alt="foreign currency amt" src="https://github.com/user-attachments/assets/0f5981a5-3625-4e0b-b9a9-06bf2b80432f" />

# 12] Engagement Account :
Engagement Banking is nothing but puts the customer at the center and aims to deliver the digital experiences they expect.
Engagment Length = SUM('Clients - Banking'[Engagment Days])

<img width="284" height="144" alt="engagement" src="https://github.com/user-attachments/assets/ddac7e83-4748-472b-ae42-faf54d9421d1" />

# 13] Credit Cards Balance :
It is the total amount of money currently owned by a cardholder to their credit card bank.
Credit Cards Balance = SUM('Clients - Banking'[Credit Card Balance] )

<img width="298" height="125" alt="cc" src="https://github.com/user-attachments/assets/dd7fd689-4569-409f-b968-070245a4fc92" />

# Visualization And Result 

# HOME
<img width="1282" height="702" alt="home" src="https://github.com/user-attachments/assets/31f988c4-98c3-459b-b927-03dda87b1e5b" />

# LOAN
<img width="1271" height="763" alt="loan" src="https://github.com/user-attachments/assets/1d23ad7c-b895-44f3-9cab-d8bb2b8a24a1" />

# Deposit
<img width="1278" height="771" alt="deposit" src="https://github.com/user-attachments/assets/d7c54ade-cde9-4a44-838f-36e6cb7e5431" />

# Summary
<img width="1281" height="762" alt="summary" src="https://github.com/user-attachments/assets/b4844da6-0f9e-440b-b1b5-498aad0952da" />

# Conclusion –
Empowered by the latest data visualization techniques, Power BI dashboards are among the most effective resources for using in banking sector. As outlined in this write-up, a banking  operations dashboard in Power BI can be developed with key banking related metrics and KPIs.
