# Parabank – Functional Requirements Specification

## Overview
This document defines the **functional requirements** for the Parabank application.  
These requirements serve as the basis for systematic test design and test case derivation using formal techniques such as parameter analysis, equivalence partitioning, and decision tables.

---

## 1. Registration Module

### FR-REG-01  
The system shall allow a new user to register by providing required personal and account information.

### FR-REG-02  
The system shall validate mandatory registration fields and display appropriate error messages for missing or invalid data.

### FR-REG-03  
The system shall display a confirmation message after successful registration.

---

## 2. Login & Authentication

### FR-AUTH-01  
The system shall allow a registered user to log in using valid username and password credentials.

### FR-AUTH-02  
The system shall redirect authenticated users to the Account Overview page after successful login.

---

## 3. Open New Account

### FR-ACC-01  
The system shall allow authenticated users to open a new bank account.

**Conditions**
- The user must be authenticated  
- The account type must be selected  
- An existing account must be selected for funding  
- The Open Account action must be triggered  

### FR-ACC-02  
The system shall create the new account and display it in the Account Overview.

---

## 4. Account Overview

### FR-OV-01  
The system shall display a summary of all accounts associated with the logged-in user.

### FR-OV-02  
The system shall display account numbers and corresponding balances.

---

## 5. View Account Details

### FR-VIEW-01  
The system shall allow users to view detailed information for a selected account.

### FR-VIEW-02  
The system shall display the transaction history for the selected account.

---

## 6. Transfer Funds

### FR-TF-01  
The system shall allow users to transfer funds between their own accounts.

### FR-TF-02  
The system shall validate the transfer amount and selected accounts.

### FR-TF-03  
The system shall update account balances after a successful transfer.

---

## 7. Bill Pay

### FR-BP-01  
The system shall allow users to submit bill payments to selected payees.

### FR-BP-02  
The system shall validate bill payment details before submission.

### FR-BP-03  
The system shall display a confirmation message after a successful bill payment.

---

## 8. Update Profile

### FR-UP-01  
The system shall allow users to update their personal profile information.

---

## 9. Request Loan

### FR-LOAN-01  
The system shall allow users to submit a loan request.

### FR-LOAN-02  
The system shall validate loan request details.

### FR-LOAN-03  
The system shall display loan approval or rejection status.

---

## 10. Logout

### FR-LOG-01  
The system shall allow users to securely log out.

### FR-LOG-02  
The system shall terminate the user session after logout and prevent access to secured pages.

---


