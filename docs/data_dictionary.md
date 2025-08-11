Here’s your rewritten **Expense Analytics - Data Dictionary**, cleaned up for clarity, fixed formatting, and with better readability while keeping all the details intact:

---

# **Expense Analytics - Data Dictionary**

## **Dataset Overview**

* **Source**: Generated sample expense data
* **Date Range**: **From:** 2023-09-09 **To:** 2024-01-01 *(Possible typo in original — dates appear reversed)*
* **Total Records**: 1,013
* **Last Updated**: 2025-08-11

---

## **Field Definitions**

### **Core Transaction Fields**

| Field Name      | Data Type | Description                            | Example Values               | Notes                                 |
| --------------- | --------- | -------------------------------------- | ---------------------------- | ------------------------------------- |
| transaction\_id | String    | Unique identifier for each transaction | `"TXN123456"`, `"SAL789012"` | System-generated                      |
| date            | Date      | Transaction date                       | `"2024-01-15"`               | Format: `YYYY-MM-DD`                  |
| amount          | Float     | Transaction amount                     | `-67.43`, `4500.00`          | Negative = expense, Positive = income |
| category        | String    | Expense/income category                | `"Groceries"`, `"Salary"`    | Standardized categories               |
| description     | String    | Merchant or transaction description    | `"GROCERY STORE #123"`       | As shown on statements                |
| payment\_method | String    | Payment method used                    | `"Credit Card"`, `"Cash"`    | Standardized payment types            |
| merchant        | String    | Cleaned merchant name                  | `"GROCERY STORE"`            | Standardized merchant name            |

---

### **Data Quality Notes**

#### **Date Field**

* All dates converted to `YYYY-MM-DD` format
* No missing values
* Reported range: **From 2024-01-01 to 2023-09-09** *(appears reversed)*

#### **Amount Field**

* Negative values → expenses
* Positive values → income
* Currency: USD
* Precision: 2 decimal places

#### **Category Field**

* Standardized categories used
* Category counts:

  * Groceries — 268
  * Restaurants — 160
  * Shopping — 114
  * Entertainment — 113
  * Gas — 80
  * Bills\_Utilities — 78
  * Miscellaneous — 61
  * Transportation — 46
  * Healthcare — 46
  * Personal\_Care — 35
  * Salary — 12
* "Miscellaneous" = uncategorized items

#### **Payment Method**

* Standardized values:
  `[Cash, Credit Card, Debit Card, Direct Deposit, Online Transfer]`

---

## **Category Definitions**

### **Expense Categories**

| Category         | Definition                                 | Examples                      |
| ---------------- | ------------------------------------------ | ----------------------------- |
| Groceries        | Food & household items from grocery stores | Costco, Trader Joe’s, Walmart |
| Restaurants      | Dining out, takeout, coffee shops          | McDonald's, Starbucks         |
| Gas              | Fuel for vehicles                          | Shell, Chevron                |
| Shopping         | General retail purchases                   | Amazon, Target                |
| Entertainment    | Recreation and leisure                     | Netflix, Movies, Gaming       |
| Bills\_Utilities | Monthly recurring bills                    | Electric, Water, Internet     |
| Transportation   | Travel and transport costs                 | Uber, Bus fare, Parking       |
| Healthcare       | Medical expenses                           | Doctor visits, Pharmacy       |
| Personal\_Care   | Grooming and fitness                       | Haircut, Gym, Salon           |
| Miscellaneous    | Other expenses                             | ATM fees, Gifts, Donations    |

### **Income Categories**

| Category      | Definition                | Examples                         |
| ------------- | ------------------------- | -------------------------------- |
| Salary        | Regular employment income | Monthly paycheck                 |
| Bonus         | Extra employment income   | Performance bonus, Holiday bonus |
| Investment    | Investment returns        | Dividends, Interest              |
| Other\_Income | Miscellaneous income      | Refunds, Side work               |

---

## **Data Sources and Assumptions**

### **Sources**

* Generated sample expense data for 2023–2024

### **Assumptions**

1. **Currency**: USD for all transactions
2. **Timezone**: Assumed local timezone (should be explicitly stated)
3. **Categorization**: No advanced rules applied — CSV is loaded and basic EDA performed:

   * Shape & columns check
   * Data types inspection
   * Missing value counts
   * Date range check
   * Amount stats
   * Unique payment methods list
   * Sample transactions display
4. **Data Completeness**:

   * No missing dates reported
   * Date range appears reversed (potential issue)
   * "Miscellaneous" used for uncategorized items
   * Generated sample data — not reflective of real-world irregularities

---

## **Data Limitations**

* No advanced data cleaning, filtering, or transformation applied
* Analysis is descriptive only — no predictive modeling
* Sample data may lack anomalies found in real transactions

---

## **Business Rules**

* **Transaction Classification**:

  * `< 0` → Expense
  * `> 0` → Income
  * `= 0` → Ignored
* **Category Assignment**:

  * Based primarily on `category` field from dataset
  * Payment method does not affect categorization in current analysis

---

## **Change Log**

* **\[2025-08-11]** — Initial data dictionary created
* **\[Future Dates]** — Record structural or rules changes

---
