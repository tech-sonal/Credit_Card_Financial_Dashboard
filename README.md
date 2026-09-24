# Credit_Card_Financial_Dashboard
Power BI Dashboard
Credit Card Weekly Status Report
1. Project objective
  To develop a comprehensive credit card weekly dashboard that provides real-time insights into key performance metrics and trends, enabling stakeholders to monitor    and analyze credit card operations effectively.  
2. Data from SQL
  Imported data to SQL database
  i. Prepared csv file 
  ii. Created tables in SQL
  iii. imported csv file into SQL
3. Data processing & DAX.
  DAX Queries
  week_num2 = WEEKNUM('public cc_detail'[week_start_date])
  Revenue = 'public cc_detail'[annual_fees] + 'public cc_detail'[total_trans_amt] + 'public cc_detail'[interest_earned]
  Current_week_Reveneue = CALCULATE(
  SUM('public cc_detail'[Revenue]),
  FILTER(
  ALL('public cc_detail'),
  'public cc_detail'[week_num2] = MAX('public cc_detail'[week_num2]))) 
  Previous_week_Reveneue = CALCULATE(
  SUM('public cc_detail'[Revenue]),
  FILTER(
  ALL('public cc_detail'),
  'public cc_detail'[week_num2] = MAX('public cc_detail'[week_num2])-1))
4. Dashboard & insights
5. Export 
