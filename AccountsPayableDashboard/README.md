📘 **README — Accounts Payable Dashboard for Uniliver EMEA**
🔖 Project Title:
Vendor Risk & Payment Performance Monitoring
Accounts Payable Analytics — EMEA Region (Uniliver)

**📂 File:**
AP_Dashboard_Uniliver_EMEA.pbix

**🏢 Organization:**
Uniliver — Consumer Products (EMEA region)
Target users: Finance Operations, Procurement, Compliance, and AP Management

**📊 Dashboard Overview:**
This Power BI report is built to monitor and analyze accounts payable activities across EMEA company codes, with a focus on:

AP Liablities

Payment Term Compliance

Currency & Region-wise Breakdown

**📈 Key KPIs Tracked:**
Total Outstanding Amount

Total Outstanding

Average Payment Cycle

Vendor Aging Report

Paid in Full, Partially Paid

Top Payables by vendor

**🔍 Risk Indicators:**
High Outstanding Flag: Invoices unpaid and overdue by more than 90 days

**🧮 Calculated Columns & Logic:**

See Dax.txt

**🌍 Dataset Details:**
Company Codes: CH01, GB01, FR01, NL01, ES01, BE01

Currencies: CHF, GBP, EUR

Date Range: Jan 2023 – April 2025

Vendors: Dummy vendor master dataset (vmd) linked to transactional AP data


**🧰 Tools & Tech Stack:**
Power BI for reporting and modeling

⚠️ Assumptions & Limitations:
Dummy data generated for simulation — not from live ERP

Vendor payment behavior is randomized for testing

Some logic (e.g., EOM+Days) is simplified and may need adjustment for regional calendars/holidays

**🧾 Datasets:**
1. accounts_payable_data
Transaction-level AP data with invoice, status, due dates, and payment dates.

2. vmd (Vendor Master Data)
Contains VendorID, VendorName, PaymentTerms (Immediate, Net, EOM), and DueDays.

3. Overdue_Sort_Order
Used for aging buckets like "0–30 Days", with a numeric sort order.

**🔗 Relationships (as per data model)**
accounts_payable_data[VendorID] → vmd[VendorID] (Many-to-One, Single Direction)

accounts_payable_data[OverdueCategory] → Overdue_Sort_Order[OverdueCategory] (Many-to-One, Single Direction)


