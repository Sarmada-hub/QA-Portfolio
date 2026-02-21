# Issue Report 

## BUG-001 — Duplicate transaction on double click 
Severity: Critical  
Priority: High  

Precondition: User 1 logged in, identity VERIFIED, balance 5000  
Steps:
1. Transfer 100 EUR to User 2
2. Double-click "Confirm"
   
Observed:
- Two transactions created
- Balance debited twice
  
Expected:
- Only one transaction created
- Balance debited once

## BUG-002 — FAILED operations not shown in history 
Severity: Major  
Priority: High   

Precondition: Trigger insufficient funds on withdrawal  
Steps:
1. User 2 withdraw 150 (balance 100)
2. Open History
   
Observed: no FAILED record   

Expected: FAILED entry with reason

## BUG-003 — Deposit accepts amount 0 
Severity: Major  
Priority: High   

Steps:  
1. Deposit 0 
2. Submit   

Observed: SUCCESS created  

Expected: validation error, no transaction
