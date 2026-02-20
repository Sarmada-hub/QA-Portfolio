# Requirements 

## Requirement identification 

Requirements are identified using the following format:

REQ-XXX

Where:
- REQ = Requirements
- XXX = Sequential number
---

## Functionnal requirements 

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

### REQ-005 : No double execution
- Double click / refresh must not create duplicated transactions.
- Every transaction has a unique ID (e.g., TX-YYYYMMDD-xxxxx).

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

## Sample Test Users
- User 1: balance 1000 EUR, Identity VERIFIED
- User 2: balance 2000 EUR, Identity VERIFIED
- User 3: balance 3000 EUR, Identity NOT_STARTED
- User 4: balance 4000 EUR, Identity PENDING
