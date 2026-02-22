# Bug report

## Summary

| ID | Tittle | Value | Priority | Criticity |
|------|------|-------|----------|-----------|
| BUG-001| Deposit amount over 10000 EUR | High | Critical |


## Description

The user has the possibility to enter an amount greater than 10000 EUR.

## Steps to reproduce

1. Click on the screen 
2. Click on "login" 
3. Enter valid ID 
4. Enter valid password 
5. Click on the button "login"
6. Click on deposit 
7. Enter the amount : 10001 EUR


## Expected result

When the user enters an amount greater than 10000 EUR, the following message must be displayed "Error : Max 10000 EUR"


## Observed result 

When the user enters an amount greater than 10000 EUR, no message indicates that an amount greater than 10000 EUR cannot be deposited. 


