# **Business Transcation Analysis**
- **Business Problem:** 
    - We have to make 'Analytical Report' for, Business sales transcation of a company.

- **Data Nomenclature :**
    1. **Transaction_ID** → Unique ID for each sale.
    2. **Transaction_Date** → When the sale happened.
    3. **Revenue**→ Total money earned from the sale.
    4. **Expenses** → Cost involved in that sale.
    5. **Profit** → Revenue – Expenses (how much was gained/lost).
    6. **Category** → Broad type of business activity (R&D, Sales, Marketing, Operations).
    7. **Region** → Where the sale happened (Europe, Africa, Asia-Pacific, etc.).
    8. **Department** → Which department handled it (HR, IT, Finance, Operations, Sales).
    9. **Product_Line** → Type of product sold (Software, Electronics, Healthcare, Clothing, Furniture).
    10. **Customer_Segment** → Type of customer (SMB = Small/Medium Business, B2B = Business-to-Business, B2C = Business-to-Consumer, Enterprise).
    11. **Payment_Method** → How customer paid (Cash, Bank Transfer, Credit Card).
    12. **Discount** → Discount given on that transaction.

# **Data Analysis Process**
## **EXTRACT**
- As, the data is already in excel we dont need to extract it.
- **Data Understanding :**
    - the data have 2000 records and 12 columns

- **Data exploration :**
    - there are,
        - 1 time-series col
        - 5 continous col
        - 6 categorical col
    - unique value in categorical col,
        - category = 5
        - region = 5
        - department = 6
        - product_line = 5
        - customer_segment = 4
        - payment_method = 4
    - there is no missing value -- if present it would be visible when we check unique value for each column as 'blank' named option.
    - no wrong data
    - no wrong datatype
    - no duplicated records
    - no outliers

## **TRANSFORM**


## **LOAD**