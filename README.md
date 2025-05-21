# Accounts Receivable Reconciliation Dashboard

## Project Overview

This Power BI project simulates a real-world accounts receivable reconciliation process. It enables automatic matching between invoices and customer payments, tracking of outstanding balances, and identification of unmatched or partially paid invoices.

The goal is to provide an operational dashboard that helps accounting teams manage receivables more efficiently and support follow-up actions on overdue or incorrect payments.

## Business Objectives

- Automatically match invoices and payments
- Identify unpaid or underpaid invoices
- Track monthly changes in accounts receivable
- Provide a detailed exception list for unmatched records

## Data Model

This project uses the following data tables:

- `Invoices`: Invoice records including invoice ID, amount, customer ID, and invoice date
- `Payments`: Payment records with payment amount, payment date, and related invoice ID
- `Customers`: Master customer table with names, regions, and credit ratings
- `Calendar`: A full date dimension table for time intelligence and filtering

## Key DAX Measures

- `TotalPaid`: Total payment received for each invoice
- `Difference`: Invoice amount minus total payments
- `IsMatched`: Returns "Matched" if payment difference is within tolerance, otherwise "Unmatched"
- `OpeningBalance`: Receivables carried forward into the current period
- `InvoicedThisPeriod`: Total value of invoices issued in the current period
- `PaidThisPeriod`: Total value of payments received during the current period
- `EndingBalance`: Opening balance + new invoices - payments

## Dashboard Features

- Year and month slicers for period-based analysis
- KPI cards for total invoiced, paid, and ending balances
- Line chart showing monthly ending balance trends
- Exception report listing all unmatched or underpaid invoices

## Skills and Tools Demonstrated

- Power BI Desktop
- Data modeling with relationships between multiple tables
- DAX measure creation and time intelligence
- Financial logic implementation in a BI environment
- Interactive report design

## File Information

- File name: `AccountsReceivable_Reconciliation.pbix`
- Format: Power BI Desktop (.pbix)
- Contains: Simulated invoice, payment, customer, and calendar data
