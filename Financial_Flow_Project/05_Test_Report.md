# Test report 

## Overview

| Item | Description |
|-----------|-------|
| Application Type |  Embedded kiosk system  |
| Test Type | Manual functional |


## Test scope

- Authentication & session management
- Identity verification (required before first transfer)
- Money deposit
- Money withdrawal
- Money transfer
- Transaction history (with the possibility to filter or search)
- Notifications/messages


## Execution result 
- Total test cases: 12
- Executed: 12
- Passed: 11
- Failed: 1

## Executed test 

| Module | Total Tests | Passed | Failed |
|--------|-------------|--------|--------|
| Authentication | 2 | 2 | 0 |
| Identity verification | 2 | 2 | 0 |
| Amount validation | 2 | 1 | 1 |
| Deposit | 1 | 1 | 0 |
| Withdrawl | 2 | 2 | 0 |
| Transfer | 3 | 3 | 0 |
| History | 1 | 1 | 0 |
| **Total** | **12** | **11** | **1** |  


## Requirement Coverage

| Status | Count |
|--------|-------|
| Total requirements | 5 |
| Covered | 5 |
| Coverage Rate | 100% | 


## Bug report

| Defect ID | Title | Severity |
|-----------|-------|----------|
| BUG-001 | Deposit amount over 10000 EUR | High |


