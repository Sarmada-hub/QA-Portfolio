# Test report 

## Overview

| Item | Description |
|-----------|-------|
| Application Type |     |
| Environnement |  |
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
- Total test cases: 20
- Executed: 20
- Passed: 17
- Failed: 3
- Blocked: 0

## Executed test 

| Module | Total Tests | Passed | Failed |
|--------|-------------|--------|--------|
| Authentication | 1 | 1 | 0 |
| Identity verification | 3 | 3 | 0 |
| Amount validation | 3 | 3 | 0 |
| Deposit | 1 | 0 | 1 |
| Withdrawl | 2 | 2 | 0 |
| Transfer | 3 | 2 | 1 |
| Anti double execution | 2 | 0 | 0 |
| History | 4 | 3 | 1 |
| **Total** | **19** | **16** | **3** |  


## Requirement Coverage

| Status | Count |
|--------|-------|
| Total requirements | 6 |
| Covered | 6 |
| Coverage Rate | 100% | 


## Bug report

| Defect ID | Title | Severity |
|------------|-------|----------|
| BUG-001 | Duplicated transaction on double click| Critical |
| BUG-002 | Operation not shown on history | Critical |
| BUG-003 | Deposit accept amount 0| Major |

