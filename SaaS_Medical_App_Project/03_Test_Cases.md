# Test cases

## TC-ACC-003 : Login rejected due to incorrect password

| Field | Description |
|------|-------------|
| Requirement ID | REQ-ACC-003 |
| Priority | High |
| Test Type | Functional |
| Module | Authentication |
| Preconditions | User account exists and user is not logged in |


| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Open the URL | Public homepage is displayed |
| 2 | Click on "login" | Login page is displayed |
| 3 | Enter valid email | Email is accepted |
| 4 | Enter unvalid password | Password is rejected |
| 4 | Click on the button "login" | User is not authenticated, a clear error message is displayed, no access to the dashboard |

### Execution result

| Status | 
|--------|
| PASS | 


## TC-ACC-004: Sign up with a valid password

| Field | Description |
|------|-------------|
| Requirement ID | REQ-ACC-004 |
| Priority | High |
| Test Type | Functional |
| Module | Authentification |
| Preconditions | User doesn't have account |


| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Open the URL | Public homepage is displayed, "Login/Sign up" button is visible |
| 2 | Click on "Sign up"| Sign up page is displayed |
| 3 | Enter valid email | Email is accepted |
| 4 | Enter valid password | Password is accepted |
| 5 | Click on "Create account" | A message informs the user that a confirmation email has been sent |
| 6 | Go to the mail sent| Email contains a link and inform the user that an account has been created |
| 7 | Click on the link | User is redirected to the website, account is activated, session is active |


### Execution Result

| Status | 
|--------|
| PASS |


## TC-ACC-005: Sign up with an invalid password

| Field | Description |
|------|-------------|
| Requirement ID | REQ-ACC-005 |
| Priority | High |
| Test Type | Functional |
| Module | Accessibility |
| Preconditions | No user is logged in (empty session) |


| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Open the URL | Public homepage is displayed, "Login/Sign up" button is visible |
| 2 | Click on "Sign up"| Sign up page is displayed |
| 3 | Enter valid email | Email is accepted |
| 4 | Enter unvalid password | Password is refused, a message explains the conditions that the password must meet |
| 5 | Click on "Create account" | Sign is rejected, a clear error message is displayed indicating the password does not meet the required criteria, no account is created, user remains on the sign up page |


### Execution Result

| Status | 
|--------| 
| PASS | 

---

# Appointment booking

## TC-APT-001 : Book appointment 

| Field | Description |
|------|-------------|
| Requirement ID | REQ-APT-001, REQ-APT-002 and REQ-APT-003 |
| Priority | High |
| Test Type | Functional |
| Module | Appointment booking |
| Preconditions | Available time appointment exists |


| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Open the URL | Public homepage is displayed|
| 2 | Select practitioner | Available appointment displayed |
| 3 | Select consultation reason | Reason accepted |
| 4 | Select available time appointment | Only available appointment are selectable |
| 5 | Click on "Book Appointment" | Booking page displayed |
| 6 | Enter valid email | Email is accepted |
| 7 | Enter valid password | Password is accepted |
| 8 | Confirm booking | Confirmation message displayed, email and/or SMS is send to the user with appointment date and time|
| 6 | Check appointment list | Appointment visible |
| 7 | Verify appointment availability | Appointment no longer available |

### Execution Result

| Status | 
|--------|
| PASS |


## TC-APT-002: Cancel an appointment by the patient (more than 24 hours before)

| Field | Description |
|------|-------------|
| Requirement ID | REQ-APT-002 |
| Priority | High |
| Test Type | Functional |
| Module | Appointment booking |
| Preconditions | Appointment should exists, patient is login |


| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Open the URL | Public homepage is displayed|
| 2 | Enter valid email | Email is accepted |
| 3 | Enter valid password | Password is accepted |
| 4 | Go to "My appointments" | Appointment page is displayed |
| 5 | Select the appontment to cancel | "Cancel" button is display |
| 6 | Click on the button "Cancel" | Following message is displayed "Are you sure you want to cancel this appointment?", buttons "Confirm" and "Cancel" are dispayed |
| 7 | Click on the button "Confirm" | Confirmation message is dispplayed, email and/or SMS is send to the user to confirm the cancellation |
| 8 | Check appointment list | Appointment is gone |
| 9 | Verify appointment availability | Appointment is available |

### Execution Result

| Status | 
|--------|
| PASS |


## TC-APT-003: Cancellation rejected less than 24 hours before the appointment

| Field | Description |
|------|-------------|
| Requirement ID | REQ-APT-004 |
| Priority | High |
| Test Type | Functional |
| Module | Appointment booking |
| Preconditions | Appointment should be within 24 hours, patient is login |


| Step | Action | Expected Result |
|------|--------|----------------|
| 1 | Open the URL | Public homepage is displayed|
| 2 | Enter valid email | Email is accepted |
| 3 | Enter valid password | Password is accepted |
| 4 | Go to "My appointments" | Appointment page is displayed |
| 5 | Select the appontment to cancel | "Cancel" button is display |
| 6 | Click on the button "Cancel" | Following message is displayed "Are you sure you want to cancel this appointment?", buttons "Confirm" and "Cancel" are dispayed |
| 7 | Click on the button "Confirm" | Confirmation message is dispplayed, email and/or SMS is send to the user to confirm the cancellation |
| 8 | Check appointment list | Appointment is gone |
| 9 | Verify appointment availability | Appointment is available |


### Execution Result

| Status | Reason of failure |
|--------| ------------------|
| FAIL | User have the possibility to cancel an appointment within 24 hours before |
