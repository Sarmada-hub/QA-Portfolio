# Test cases

## TC-ACC-001 : Access homepage without authentification

| Field | Description |
|------|-------------|
| Requirement ID | REQ-ACC-001 |
| Priority | High |
| Test Type | Functional |
| Module | Authentication |
| Preconditions | No user is logged in |


| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|-----------------|---------------|-----------|
| 1 | Open the URL | Public homepage is displayed | Behave as expected | Pass |   




## TC-ACC-002 : Login with valid credentials 

| Field | Description |
|------|-------------|
| Requirement ID | REQ-ACC-002 |
| Priority | High |
| Test Type | Functional |
| Module | Authentication |
| Preconditions | User account exists and user is not logged in |


| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|-----------------|---------------|-----------|
| 1 | Open the URL | Public homepage is displayed | Behave as expected | Pass |
| 2 | Click on "login" | Login page is displayed | Behave as expected | Pass
| 3 | Enter valid email | Email is displayed | Behave as expected | Pass |
| 4 | Enter valid password | Password is hidden behind black dots | Behave as expected | Pass |
| 4 | Click on the button "login" | User is authenticated, access to the dashboard | Behave as expected | Pass |



## TC-ACC-003 : Login rejected due to incorrect password

| Field | Description |
|------|-------------|
| Requirement ID | REQ-ACC-003 |
| Priority | High |
| Test Type | Functional |
| Module | Authentication |
| Preconditions | User account exists and user is not logged in |


| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|-----------------|---------------|-----------|
| 1 | Open the URL | Public homepage is displayed | Behave as expected | Pass |
| 2 | Click on "login" | Login page is displayed | Behave as expected | Pass
| 3 | Enter valid email | Email is accepted | Behave as expected | Pass |
| 4 | Enter unvalid password | Password is hidden behind black dots | Behave as expected | Pass |
| 4 | Click on the button "login" | User is not authenticated, the following message is displayed "Incorrect password", no access to the dashboard | Behave as expected | Pass |



## TC-ACC-004: Sign up with a valid password

| Field | Description |
|------|-------------|
| Requirement ID | REQ-ACC-004 |
| Priority | High |
| Test Type | Functional |
| Module | Authentification |
| Preconditions | User doesn't have account |


| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|----------------|----------------|-----------|
| 1 | Open the URL | Public homepage is displayed, "Login/Sign up" button is visible | Behave as expected | Pass |
| 2 | Click on "Sign up"| Sign up page is displayed | Behave as expected | Pass |
| 3 | Enter valid email | Email is displayed | Behave as expected | Pass |
| 4 | Enter valid password | Message explaining the criteria that the password must meet, password is hidden behind black dots | Behave as expected | Pass |
| 5 | Click on "Create account" | Message informing the user that a confirmation email has been sent | Behave as expected | Pass |
| 6 | Go to the mail sent| Email contains a link and inform the user that an account has been created | Behave as expected | Pass |
| 7 | Click on the link | User redirecting to the website, account is activated, session is active | Behave as expected | Pass |  



## TC-ACC-005: Sign up with an invalid password

| Field | Description |
|------|-------------|
| Requirement ID | REQ-ACC-005 |
| Priority | High |
| Test Type | Functional |
| Module | Accessibility |
| Preconditions | No user is logged in (empty session) |


| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|-----------------|---------------| --------- |
| 1 | Open the URL | Public homepage is displayed, "Login/Sign up" button is visible | Behave as expected | Pass |
| 2 | Click on "Sign up"| Sign up page is displayed | Behave as expected | Pass |
| 3 | Enter valid email | Email is displayed | Behave as expected | Pass |
| 4 | Enter unvalid password | Message explaining the criteria that the password must meet, password is hidden behind black dots | Behave as expected | Pass |
| 5 | Click on "Create account" | Sign is rejected, the following message is displayed "The password does not meet the criteria.", no account created, user remains on the sign up page | Behave as expected | Pass |



# Appointment booking

## TC-APT-001 : Book appointment 

| Field | Description | 
|------|-------------|
| Requirement ID | REQ-APT-001, REQ-APT-002 and REQ-APT-003 |
| Priority | High |
| Test Type | Functional |
| Module | Appointment booking |
| Preconditions | Available time appointment exists |


| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|-----------------|---------------|-----------|
| 1 | Open the URL | Public homepage is displayed | Behaved as expected | Pass |
| 2 | Select practitioner | Available appointment displayed | Behave as expected | Pass |
| 3 | Select consultation reason | Reason accepted | Behave as expected | Pass |
| 4 | Select available time appointment | Only available appointment are selectable | Behave as expected | Pass |
| 5 | Click on "Book Appointment" | Booking page displayed | Behave as expected | Pass |
| 6 | Enter valid email | Email is accepted | Behaved as expected | Pass |
| 7 | Enter valid password | Password is accepted | Behaved as expected | Pass |
| 8 | Confirm booking | Confirmation message displayed, email and/or SMS is send to the user with appointment date and time | Behaved as expected | Pass |
| 6 | Check appointment list | Appointment visible | Behaved as expected | Pass |
| 7 | Verify appointment availability | Appointment no longer available | Behaved as expected | Pass |



## TC-APT-002: Cancel an appointment by the patient (more than 24 hours before)

| Field | Description |
|------|-------------|
| Requirement ID | REQ-APT-002 |
| Priority | High |
| Test Type | Functional |
| Module | Appointment booking |
| Preconditions | Appointment should exists, patient is login |


| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|-----------------|---------------|-----------|
| 1 | Open the URL | Public homepage is displayed | Behaved as expected | Pass |
| 2 | Enter valid email | Email is accepted | Behaved as expected | Pass |
| 3 | Enter valid password | Password is accepted | Behaved as expected | Pass |
| 4 | Go to "My appointments" | Appointment page is displayed | Behaved as expected | Pass |
| 5 | Select the appontment to cancel | "Cancel" button is display | Behaved as expected | Pass |
| 6 | Click on the button "Cancel" | Following message is displayed "Are you sure you want to cancel this appointment?", buttons "Confirm" and "Cancel" are dispayed | Behaved as expected | Pass |
| 7 | Click on the button "Confirm" | Confirmation message is dispplayed, email and/or SMS is send to the user to confirm the cancellation | Behaved as expected | Pass |
| 8 | Check appointment list | Appointment is gone | Behaved as expected | Pass |
| 9 | Verify appointment availability | Appointment is available | Behaved as expected | Pass |



## TC-APT-003: Cancellation rejected less than 24 hours before the appointment

| Field | Description |
|------|-------------|
| Requirement ID | REQ-APT-004 |
| Priority | High |
| Test Type | Functional |
| Module | Appointment booking |
| Preconditions | Appointment should be within 24 hours, patient is login |


| Step | Action | Expected result | Actual result | Pass/Fail |
|------|--------|-----------------|---------------|-----------|
| 1 | Open the URL | Public homepage is displayed | Behaved as expected | Pass |
| 2 | Enter valid email | Email is accepted | Behaved as expected | Pass |
| 3 | Enter valid password | Password is accepted | Behaved as expected | Pass |
| 4 | Go to "My appointments" | Appointment page is displayed | Behaved as expected | Pass |
| 5 | Select the appontment to cancel | "Cancel" button is display | Behaved as expected | Pass |
| 6 | Click on the button "Cancel" | Following message is displayed "Are you sure you want to cancel this appointment?", buttons "Confirm" and "Cancel" are dispayed | Did not behaved as expected | Fail | - | N/A |
| 7 | Click on the button "Confirm" | Not executed | - | N/A |
| 8 | Check appointment list | Not executed | - | N/A |
| 9 | Verify appointment availability | Not executed | - | N/A |

