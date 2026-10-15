# SME Cash Flow Crisis Analyzer - Kampala

## Problem Statement
Why profitable SMEs in Kampala show profit but have no cash in bank? 

Real case: Lake View Services - May 2026
- Cash Book: 4,860,000 UGX
- Bank Statement: 5,745,000 UGX
- Corrected Cash: 4,775,000 UGX
- Difference: 875,000 UGX unexplained (Owner drawings not recorded)

This violates **Entity Concept** - mixing personal & business money kills SMEs in Uganda/DRC.

## Root Causes Analyzed
1. Receivables up (clients don't pay)
2. Inventory stuck (FIFO not applied)
3. Owner drawings unrecorded
4. No bank reconciliation

## Solution
Python automation for bank reconciliation + Power BI Cash Flow Dashboard

### Tools Used
- Python (Pandas)
- Excel
- Power BI
- IAS 1 / IFRS for SMEs

### Code Preview
```python
# Auto-reconciliation
import pandas as pd
cash_book = 4860000
bank_statement = 5745000
corrected_cash = 4775000 # After adjusting owner drawings
difference = bank_statement - corrected_cash
print(f"Unexplained: {difference} UGX - Investigate owner drawings")
