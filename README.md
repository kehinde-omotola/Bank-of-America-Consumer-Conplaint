# Bank of America Consumer Complaint Analytics
# Project overview
This project analyses 62,516 consumer complaint records associated with
Bank of America. The data covers May 2017 to August 2023 

I used the data to understand which banking products and issues
generated the most complaints, how complaint volumes changed over time,
how complaints were handled, and how timely the recorded responses were.
## Project objectives
- Track complaint volumes over time.
- Identify products with the highest complaint counts.
- Find the most frequently reported customer issues.
- Review company response outcomes.
- Measure the recorded timely response rate.
- Examine CFPB forwarding intervals and identify unusually long
  intervals.
### Tools used
- Excel
- Power BI
### Dataset
The original workbook contains 62,516 rows and 12 columns:
- Complaint ID
- Submitted via
- Date submitted
- Date received
- State
- Product
- Sub-product
- Issue
- Sub-issue
- Company public response
- Company response to consumer
- Timely response?
The cleaned dataset contains the original 12 columns plus six additional
fields:
- Complaint Year
- Complaint Month
- Complaint Quarter
- Complaint Year-Month
- Forwarding Interval Days
- Data Quality Flag
## Data cleaning and quality checks
I checked the data before using it for the dashboard.
1. Checked the complaint IDs for missing values and duplicates.
2. Checked the date fields for missing or invalid dates.
3. Standardised spaces in text fields.
4. Converted dates to a consistent date format.
5. Standardised valid Timely response? values to Yes and No.
6. Created year, month, quarter, and year-month fields from Date
   submitted.
7. Calculated Forwarding Interval Days as Date received minus Date
   submitted.
8. Added a Data Quality Flag to identify unusual records.
9. Kept the original records and did not fill missing values with
   assumptions.
### Data quality results
- Total records: 62,516
- Distinct complaint IDs: 62,516
- Duplicate complaint IDs: 0
- Exact duplicate rows: 0
- Invalid or missing date pairs: 0
- Negative forwarding intervals: 0
- Forwarding intervals above 30 days: 435
Missing values
  Field                       Missing records   Percentage
  Sub-issue                            10,858       17.37%
Company public response               2,175        3.48%
Timely response?                      1,494        2.39%
Sub-product                               7        0.01%

I left missing values blank rather than filling them with guessed
information. All 1,494 blank Timely response? records were marked In
progress. I did not classify them as No.
# Dashboard pages and visuals
The Power BI report contains four pages.

## 1. Consumer Complaint Overview
This page gives a general view of the complaints. It includes total
complaints, timely response percentage, average forwarding days,
in-progress complaints, complaint trends, and complaints by product.
<img width="599" height="370" alt="Consumer Complaint Overview" src="https://github.com/user-attachments/assets/d6a51b58-4eab-44c9-a7ad-f86e82cd9d93" />

## 2. Product and Issues Analysis
This page compares complaints by product, sub-product, and issue. It
helps identify the products and customer problems that appear most often
in the records.
<img width="602" height="341" alt="Product & Issues Analysis" src="https://github.com/user-attachments/assets/ffc5908b-7a45-48b8-b2cd-3a3748debdc3" />

## 3. Company Response Analysis
This page shows company response outcomes, timely and untimely
responses, and company public response categories.

<img width="609" height="365" alt="Company Response Analysis" src="https://github.com/user-attachments/assets/31b76ea6-c651-4990-812f-21ae4ee7a9af" />


## 4. Complaint Timeline Analysis
This page focuses on complaint trends over time and the forwarding
interval between the CFPB intake date and the date the complaint was
forwarded to the company. It includes annual totals, forwarding interval
bands, average forwarding days by product, and a complaint detail table.
<img width="606" height="371" alt="Complaint Timeline Analysis" src="https://github.com/user-attachments/assets/780bc963-4a9c-4d58-8ce3-d2e1d28a01c5" />


# Key findings
  Measure                                   Result
  Total complaints                          62,516
Timely response rate                      96.06%
Timely complaints (Yes)                   58,619
Untimely complaints (No)                   2,403
In-progress complaints                     1,494
Average forwarding interval            1.22 days
Median forwarding interval                0 days
Forwarding intervals above 30 days           435
## Complaint volume by product
  Product                             Complaints
  Checking or savings account             24,814
Credit card or prepaid card             16,197
Credit reporting                         7,710
Mortgage                                 6,601
Money transfer                           3,453
Debt collection                          2,736
Vehicle loan or lease                      633
Payday, title, or personal loan            333
Student loan                                39
## Most reported issues
- Managing an account: 15,109
- Incorrect information on your report: 4,931
- Problem with a purchase shown on your statement: 4,415
- Closing an account: 2,953
- Trouble during payment process: 2,827
## Complaint totals by year
  Year     Complaints
  2017          5,394
2018          7,872
2019          7,075
2020          8,942
2021         11,149
2022         12,953
2023          9,131

2022 had the highest annual total. The data starts in May 2017 and ends
in August 2023, so 2017 and 2023 are partial years.
## Company response outcomes
  Response outcome                    Complaints
  Closed with explanation                 41,044
Closed with monetary relief             14,697
Closed with non-monetary relief          5,273
In progress                              1,494
Closed                                       8
# Business questions answered
## 1. Which product received the most complaints? 
Checking or savings accounts, with 24,814 complaints.
## 2. What was the most common issue? 
Managing an account, with 15,109 complaints.
## 3. Which year had the highest complaint volume? 
2022, with 12,953 complaints.
## 4. What was the most common response outcome?
Closed with explanation, with 41,044 complaints.
## 5. What was the timely response rate? 
96.06%, calculated using only Yes and No records.
## 6. How long did forwarding take on average?
1.22 days, with a median of zero days.
## 7. Which state had the most complaints? 
California, with 13,709 complaints.
# Recommendations
- Review checking and savings account processes because this product
  group had the highest complaint volume.
- Investigate account-management issues, especially deposits and
  withdrawals, debit or ATM card use, and account access.
- Review credit card and credit reporting complaints as other
  important areas.
- Monitor the 2,403 complaints marked No for timely response and track
  the 1,494 in-progress complaints separately.
- Investigate the 435 forwarding intervals above 30 days to understand
  the reasons for the delays.
- Use the dashboard regularly to monitor complaint patterns by year,
  product, issue, and response outcome.
Important notes and limitations
- The dataset covers May 2017 to August 2023. The first and last years
  are partial.
- Complaint records show issues reported by consumers; they do not
  independently prove wrongdoing.
- The average forwarding interval is the time between Date submitted
  and Date received. It is not the company's response or resolution
  time.
- The dataset does not provide a company response timestamp, so
  company response duration cannot be calculated.
- Blank public response values should not automatically be treated as
  evidence that no response was made.
- The timely response rate excludes records marked In progress because
  their timeliness value is blank.
## Conclusion
This project helped me practise data cleaning, data quality checks,
analysis, KPI reporting, and dashboard development. The dashboard
provides a simple way to explore consumer complaint patterns and
identify areas that may need further attention.
