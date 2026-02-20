# Test Cases 

---

## Authentication / Session

### TC-001 (High priority) : Block operations for unauthenticated user (REQ-001)
Precondition: user logged out  
Steps: 
1. Open the deposit page
2. Try to submit  

Expected: redirect to login and message "Authentication required"

### TC-002 (High priority) : Session timeout after inactivity (REQ-001)
Precondition: user logged in  
Steps: 
1. Wait 10 min inactivity
2. Click on Withdrawal  

Expected: session expired, user must login again

---

## Identity verification

### TC-003 (High priority) : Transfer blocked if identity NOT_STARTED (REQ-002)
Precondition: User 3 logged in identity NOT_STARTED  
Steps: 
1. Transfer 50 EUR to U2
2. Confirm  

Expected: Transfer blocked + message requesting identity

### TC-004 (High priority) : Transfer blocked if identity PENDING (REQ-002)  
Precondition: User 4 logged in identity PENDING  
Steps:   
1. Transfer 50 EUR to User 2  
2. Confirm  

Expected: blocked and message "identity in progress"

### TC-005 (High priority) — Transfer allowed if identity VERIFIED (REQ-002)
Precondition: U1 logged in identity VERIFIED
Steps: 
1. Transfer 50 EUR to User 2
2. Confirm  

Expected: SUCCESS and transaction ID generated

---

## Amount validation

### TC-006 (High priority) : Amount = 0 rejected (REQ-003)
Precondition: User 1 logged in  
Steps: 
1. Deposit 0 EUR
2. Submit  

Expected: error "Invalid amount" and no transaction created

### TC-007 (High priority) : Negative amount rejected (REQ-003)
Precondition: User 1 logged in  
Steps: 
1. Withdrawal 10 EUR
2. Submit  

Expected: error and no transaction

### TC-008 (High priority) : Amount > 10,000 rejected (REQ-003)
Precondition: User 1 logged in  
Step:  
Transfer 10001 EUR to U2  

Expected: error "Max 10000" and  no transaction

---

## Deposit

### TC-009 (Medium priority) : Deposit updates balance and history (REQ-004, REQ-006)
Precondition: User 2 balance 100  
Steps:  
1. Deposit 50
2. Submit  

Expected: SUCCESS, new balance 150, history contains deposit entry

---

## Withdrawal

### TC-010 (High priority) : Withdrawal updates balance and history (REQ-004, REQ-006)
Precondition: User 1 balance 5000  
Steps: 
1. Withdraw 200
2. submit  

Expected: SUCCESS, balance 4800, history contains withdrawal entry

### TC-011 (High priority) : Withdrawal blocked when insufficient balance (REQ-004, REQ-006)
Precondition: User 2 balance 100  
Steps: 
1. Withdraw 150
2. Submit  

Expected: FAILED with message "Insufficient funds", balance unchanged, history records FAILED

---

## Transfer

### TC-012 (High priority) : Transfer updates both balances and history (REQ-004, RQ-006)  
Precondition: User 1 balance 5000, User 2 balance 100, identity VERIFIED   
Steps:  
User 1 transfers 300 to User 2  

Expected: User 1 = 4700 EUR, User 2 = 400 EUR, history updated for both sides

### TC-013 (High priority) : Transfer to invalid recipient (Error handling)
Precondition: User 1 identity VERIFIED  
Steps: 
Transfer 10 to invalid recipient ID  

Expected: FAILED, message "Recipient not found", no balance change, history records FAILED

### TC-014 (High priority) : Transfer blocked when insufficient balance (REQ-004)
Precondition: User 2 balance 100, identity VERIFIED  
Steps:  
Transfer 150 to User 1  

Expected: FAILED "Insufficient funds", no balance change

---

## Anti double execution

### TC-015 (High priority) : Double click confirm creates only one transaction (REQ-005)
Precondition: User 1 identity VERIFIED  
Steps: 
1. Transfer 20 
2. Double-click Confirm  

Expected: only one transaction created, one debit only

### TC-016 (High priority) : Refresh confirmation page does not duplicate transaction (REQ-005)
Precondition: User 1 about to confirm a transfer  
Steps: 
1. Confirm 
2. Immediately refresh  

Expected: no duplicate transaction, stable status

---

## History

### TC-017 (High priority) : History includes transaction ID + status (REQ-006)
Precondition: at least one operation exists  
Step:  
Open History  

Expected: entries show transaction ID, type, amount, date, time, status

### TC-018 (Medium priority) : History sorted by most recent first (REQ-006)
Precondition: multiple operations exist  
Step:  
Open History  

Expected: newest entry on top

### TC-019 (Medium priority) : Search by transaction ID (REQ-006)
Precondition: known transaction ID  
Step:  
Search transaction ID  
Expected: matching entry displayed

### TC-020 (Medium priority) : FAILED operations appear in history (REQ-006)
Precondition: trigger a FAILED operation (e.g. insufficient funds)  
Step:  
Open History  

Expected: FAILED line visible with failure reason
