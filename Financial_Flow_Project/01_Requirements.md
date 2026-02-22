# Requirements 

### REQ-001 : Authentication
- User must be authenticated to perform Deposit/Withdrawal/Transfer.
- Session expires after 10 minutes of inactivity.

### REQ-002 : Identity verification
- Identity must be VERIFIED before performing a Transfer.
- Identity status : NOT_STARTED, PENDING, VERIFIED, REJECTED
- If NOT_STARTED/PENDING/REJECTED, the transfer blocked with clear message.

### REQ-003 : Amount validation
- Amount must be strictly > 0.
- Max amount per operation: 10000 EUR.
- Currency : EUR only.

### REQ-004 : Balance
- Withdrawal/Transfer require sufficient balance.
- Balance updates immediately after a successful operation.

### REQ-005 : Anti double execution
- Double click / refresh must not create duplicated transactions.
- Every transaction has an unique ID.

### REQ-006 : Transaction history
- All operations must be recorded, successed and failed
- History includes:
  - Transaction ID
  - Type : Deposit/Withdrawal/Transfer
  - Amount in euro
  - Date, time
  - Status : SUCCESS/FAILED
  - Payee for Transfer
  - Failure reason if FAILED

---

## Test users
- User 1: balance 5000 EUR, identity VERIFIED
- User 2: balance 100 EUR, identity VERIFIED
- User 3: balance 5000 EUR, identity NOT_STARTED
- User 4: balance 5000 EUR, identity PENDING
