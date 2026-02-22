# Test Cases 

## Authentication 

### TC-001 : Block operations for unauthenticated user 

| Field | Description |
|------|-------------|
| Requirement ID | REQ-001 |
| Priority | High |
| Test Type | Functional |
| Module | Authentication |
| Preconditions | No user is logged in |

| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|-----------------|---------------|-----------|
| 1 | Click on the screen | Homepage is displayed | Behave as expected | Pass |
| 2 | Try to make an operation | Credentials are required | Behave as expected | Pass | 


### TC-002 : Session timeout after inactivity 

| Field | Description |
|------|-------------|
| Requirement ID | REQ-001 |
| Priority | High |
| Test Type | Functional |
| Module | Authentication |
| Preconditions | User is logged in |

| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|-----------------|---------------|-----------|
| 1 | Click on the screen | Homepage is displayed | Behave as expected | Pass |
| 2 | Click on "login" | Login page is displayed | Behave as expected | Pass
| 3 | Enter valid ID | Email is displayed | Behave as expected | Pass |
| 4 | Enter valid password | Password is hidden behind black dots | Behave as expected | Pass |
| 5 | Click on the button "login" | User is authenticated, access to the dashboard | Behave as expected | Pass |
| 6 | Wait 3 min inactivity | Homepage is displayed, session expired | Pass |


## Identity verification

### TC-003 : Transfer blocked if identity NOT_STARTED 

| Field | Description |
|------|-------------|
| Requirement ID | REQ-002 |
| Priority | High |
| Test Type | Functional |
| Module | Identity verification |
| Preconditions | User is logged in |

| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|-----------------|---------------|-----------|
| 1 | Click on the screen | Homepage is displayed | Behave as expected | Pass |
| 2 | Click on "login" | Login page is displayed | Behave as expected | Pass
| 3 | Enter valid ID | Email is displayed | Behave as expected | Pass |
| 4 | Enter valid password | Password is hidden behind black dots | Behave as expected | Pass |
| 5 | Click on the button "login" | User is authenticated, access to the dashboard | Behave as expected | Pass |
| 6 | Click on transfer | Transfer page is displayed | Behave as expected | Pass |
| 7 | Enter the amount | Amount valid | Behave as expected | Pass |
| 8 | Enter the payee's ID | ID valid | Behave as expected | Pass |
| 9 | Click on transfer | Identity verification is asked, identity is PENDING | Behave as expected |Pass |
| 10 | Wait 30 seconds | Identity is NOT_STARTED, transfer blocked | Behave as expected | Pass |



### TC-004 : Transfer allowed if identity VERIFIED 

| Field | Description |
|------|-------------|
| Requirement ID | REQ-002 |
| Priority | High |
| Test Type | Functional |
| Module | Identity verification |
| Preconditions | User is logged in |

| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|-----------------|---------------|-----------|
| 1 | Click on the screen | Homepage is displayed | Behave as expected | Pass |
| 2 | Click on "login" | Login page is displayed | Behave as expected | Pass
| 3 | Enter valid ID | Email is displayed | Behave as expected | Pass |
| 4 | Enter valid password | Password is hidden behind black dots | Behave as expected | Pass |
| 5 | Click on the button "login" | User is authenticated, access to the dashboard | Behave as expected | Pass |
| 6 | Click on transfer | Transfer page is displayed | Behave as expected | Pass |
| 7 | Enter the amount | Amount valid | Behave as expected | Pass |
| 8 | Enter the payee's ID | ID valid | Behave as expected | Pass |
| 9 | Click on transfer | Identity verification is asked, identity is PENDING | Behave as expected |Pass |
| 10 | Enter the code receive by SMS | Identity is VERIFIED, SMS is send confirming the transfer | Behave as expected | Pass |


## Amount validation

### TC-005 : Deposit an amount = 0 EUR rejected  

| Field | Description |
|------|-------------|
| Requirement ID | REQ-003 |
| Priority | High |
| Test Type | Functional |
| Module | Identity verification |
| Preconditions | User is logged in |

| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|-----------------|---------------|-----------|
| 1 | Click on the screen | Homepage is displayed | Behave as expected | Pass |
| 2 | Click on "login" | Login page is displayed | Behave as expected | Pass
| 3 | Enter valid ID | Email is displayed | Behave as expected | Pass |
| 4 | Enter valid password | Password is hidden behind black dots | Behave as expected | Pass |
| 5 | Click on the button "login" | User is authenticated, access to the dashboard | Behave as expected | Pass |
| 6 | Click on deposit | Deposit page is displayed | Behave as expected | Pass |
| 7 | Enter the amount : 0 EUR | Following message is displayed "Enter an amount between 0,01 and 10000 EUR", no transaction | Behave as expected | Pass |



### TC-006 : Amount > 10,000 rejected 

| Field | Description |
|------|-------------|
| Requirement ID | REQ-003 |
| Priority | High |
| Test Type | Functional |
| Module | Identity verification |
| Preconditions | User is logged in |

| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|-----------------|---------------|-----------|
| 1 | Click on the screen | Homepage is displayed | Behave as expected | Pass |
| 2 | Click on "login" | Login page is displayed | Behave as expected | Pass
| 3 | Enter valid ID | Email is displayed | Behave as expected | Pass |
| 4 | Enter valid password | Password is hidden behind black dots | Behave as expected | Pass |
| 5 | Click on the button "login" | User is authenticated, access to the dashboard | Behave as expected | Pass |
| 6 | Click on deposit | Deposit page is displayed | Behave as expected | Pass |
| 7 | Enter the amount : 10001 EUR | Amount invalid, following message is displayed "Error : Max 10000 EUR", no transaction | Did not behave as expected | Fail |



## Deposit

### TC-007 : Deposit updates balance and history 

| Field | Description |
|------|-------------|
| Requirement ID | REQ-004 and REQ-006 |
| Priority | Medium |
| Test Type | Functional |
| Module | Identity verification |
| Preconditions | User is logged in |

| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|-----------------|---------------|-----------|
| 1 | Click on the screen | Homepage is displayed | Behave as expected | Pass |
| 2 | Click on "login" | Login page is displayed | Behave as expected | Pass
| 3 | Enter valid ID | Email is displayed | Behave as expected | Pass |
| 4 | Enter valid password | Password is hidden behind black dots | Behave as expected | Pass |
| 5 | Click on the button "login" | User is authenticated, access to the dashboard | Behave as expected | Pass |
| 6 | Click on deposit | Deposit page is displayed | Behave as expected | Pass |
| 7 | Enter the amount | Amount valid | Behave as expected | Pass |
| 8 | Click on transfer | Identity verification is asked, identity is PENDING | Behave as expected | Pass |
| 9 | Enter the code receive by SMS | Identity is VERIFIED, SMS is send confirming the transfer | Behave as expected | Pass |
| 10 | Go to balance | Balance is update | Behave as expected | Pass |
| 11 | Go to history | History is update | Behave as expected | Pass |


## Withdrawal

### TC-008 : Withdrawal updates balance and history 

| Field | Description |
|------|-------------|
| Requirement ID | REQ-004 and REQ-006 |
| Priority | High |
| Test Type | Functional |
| Module | Identity verification |
| Preconditions | User is logged in |

| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|-----------------|---------------|-----------|
| 1 | Click on the screen | Homepage is displayed | Behave as expected | Pass |
| 2 | Click on "login" | Login page is displayed | Behave as expected | Pass
| 3 | Enter valid ID | Email is displayed | Behave as expected | Pass |
| 4 | Enter valid password | Password is hidden behind black dots | Behave as expected | Pass |
| 5 | Click on the button "login" | User is authenticated, access to the dashboard | Behave as expected | Pass |
| 6 | Click on withdraw | Withdraw page is displayed | Behave as expected | Pass |
| 7 | Enter the amount | Amount valid | Behave as expected | Pass |
| 8 | Click on withdraw | Identity verification is asked, identity is PENDING | Behave as expected | Pass |
| 9 | Enter the code receive by SMS | Identity is VERIFIED, cash withdrawn | Behave as expected | Pass |
| 10 | Go to balance | Balance is update | Behave as expected |Pass |
| 11 | Go to history | History is update | Behave as expected |Pass |


### TC-009 : Withdrawal blocked when insufficient balance

| Field | Description |
|------|-------------|
| Requirement ID | REQ-004 and REQ-006 |
| Priority | High |
| Test Type | Functional |
| Module | Identity verification |
| Preconditions | User is logged in |

| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|-----------------|---------------|-----------|
| 1 | Click on the screen | Homepage is displayed | Behave as expected | Pass |
| 2 | Click on "login" | Login page is displayed | Behave as expected | Pass
| 3 | Enter valid ID | Email is displayed | Behave as expected | Pass |
| 4 | Enter valid password | Password is hidden behind black dots | Behave as expected | Pass |
| 5 | Click on the button "login" | User is authenticated, access to the dashboard | Behave as expected | Pass |
| 6 | Click on withdraw | Withdraw page is displayed | Behave as expected | Pass |
| 7 | Enter the amount | Amount invalid, following message is displayed "Insufficient funds", no transaction | Behave as expected | Pass |


## Transfer

### TC-010 : Transfer updates both balances and history 
  
| Field | Description |
|------|-------------|
| Requirement ID | REQ-002 |
| Priority | High |
| Test Type | Functional |
| Module | Identity verification |
| Preconditions | User is logged in |

| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|-----------------|---------------|-----------|
| 1 | Click on the screen | Homepage is displayed | Behave as expected | Pass |
| 2 | Click on "login" | Login page is displayed | Behave as expected | Pass
| 3 | Enter valid ID | Email is displayed | Behave as expected | Pass |
| 4 | Enter valid password | Password is hidden behind black dots | Behave as expected | Pass |
| 5 | Click on the button "login" | User is authenticated, access to the dashboard | Behave as expected | Pass |
| 6 | Click on transfer | Transfer page is displayed | Behave as expected | Pass |
| 7 | Enter the amount | Amount valid | Behave as expected | Pass |
| 8 | Enter the payee's ID | ID valid | Behave as expected | Pass |
| 9 | Click on transfer | Identity verification is asked, identity is PENDING | Behave as expected |Pass |
| 10 | Enter the code receive by SMS | Identity is VERIFIED, SMS is send confirming the transfer | Behave as expected | Pass |
| 11 | Go to balance | Balance is update | Behave as expected |Pass |
| 12 | Go to history | History is update | Behave as expected |Pass |



### TC-011 : Transfer to invalid payee 
 
| Field | Description |
|------|-------------|
| Priority | High |
| Test Type | Functional |
| Module | Identity verification |
| Preconditions | User is logged in |

| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|-----------------|---------------|-----------|
| 1 | Click on the screen | Homepage is displayed | Behave as expected | Pass |
| 2 | Click on "login" | Login page is displayed | Behave as expected | Pass
| 3 | Enter valid ID | Email is displayed | Behave as expected | Pass |
| 4 | Enter valid password | Password is hidden behind black dots | Behave as expected | Pass |
| 5 | Click on the button "login" | User is authenticated, access to the dashboard | Behave as expected | Pass |
| 6 | Click on transfer | Transfer page is displayed | Behave as expected | Pass |
| 7 | Enter the amount | Amount valid | Behave as expected | Pass |
| 8 | Enter a wrong payee ID | ID invalid, no transaction | Behave as expected | Pass |


### TC-012 : Transfer blocked when insufficient balance 

| Field | Description |
|------|-------------|
| Requirement ID | REQ-004 |
| Priority | High |
| Test Type | Functional |
| Module | Identity verification |
| Preconditions | User is logged in |

| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|-----------------|---------------|-----------|
| 1 | Click on the screen | Homepage is displayed | Behave as expected | Pass |
| 2 | Click on "login" | Login page is displayed | Behave as expected | Pass
| 3 | Enter valid ID | Email is displayed | Behave as expected | Pass |
| 4 | Enter valid password | Password is hidden behind black dots | Behave as expected | Pass |
| 5 | Click on the button "login" | User is authenticated, access to the dashboard | Behave as expected | Pass |
| 6 | Click on transfer | Transfer page is displayed | Behave as expected | Pass |
| 7 | Enter the amount | Amount invalid, following message is displayed "Insufficient funds", no transaction | Behave as expected | Pass |



## History

### TC-013 : Search by transaction ID

| Field | Description |
|------|-------------|
| Requirement ID | REQ-006 |
| Priority | High |
| Test Type | Functional |
| Module | Identity verification |
| Preconditions | User is logged in |

| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|-----------------|---------------|-----------|
| 1 | Click on the screen | Homepage is displayed | Behave as expected | Pass |
| 2 | Click on "login" | Login page is displayed | Behave as expected | Pass
| 3 | Enter valid ID | Email is displayed | Behave as expected | Pass |
| 4 | Enter valid password | Password is hidden behind black dots | Behave as expected | Pass |
| 5 | Click on the button "login" | User is authenticated, access to the dashboard | Behave as expected | Pass |
| 6 | Go to on history | History page is displayed | Behave as expected | Pass |
| 7 | Search transaction ID | Transaction is displayed | Behave as expected | Pass |



