# Bug report

## Summary

| ID | Tittle | Value |
|------|------|-------|
| BUG-001| Appointment can be cancelled within 24 hours before the appointment| Appointment |


## Description

When entering invalid password, the system displays a generic message: “Epic sadface: Username and password do not match any user in this service”.

## Steps to reproduce

1. Open the URL 
2. Enter valid email 
3. Enter valid password 
4. Go to "My appointments" 
5. Select the appontment to cancel 
6. Click on the button "Cancel"
7. Click on the button "Confirm" 


## Expected result

When the user try to cancell the appointment within 24 hours before, a message should appear when he click on the button "Cancel" saying "The appointment can't be cancelled".  

## Observed result 

When the user try to cancell the appointment within 24 hours before, a the following message appears “Are you sure you want to cancell this appointment?" with the buttons "Cancel" and "Confirm". When the user click on the button "Confirm" he receive email and/or SMS to confirm the cancellation.  


## Criticity 

High critity  

## Priority 

High priority  
