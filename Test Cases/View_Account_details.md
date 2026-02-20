# Test Suite: View Account Details

## Feature Overview

This test suite covers functional and validation testing for the **Parabank View Account Details** feature. Test cases are derived to validate account selection, transaction history display, and handling of missing inputs.

---

## Requirements Covered

* **FR-VIEW-01**: The system shall allow users to view detailed information for a selected account.
* **FR-VIEW-02**: The system shall display transaction history for the selected account.

---

## Test Suite: View Account Details

### TC-VIEW-01 – View details of selected account

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-VIEW-01                                                                   |
| Preconditions        | User is authenticated and has at least one account                            |
| Test Data            | A specific account selected                                                  |
| Steps                | 1. Log in as a valid user<br>2. Navigate to Account Overview<br>3. Select an account |
| Expected Result      | Account details are displayed correctly                                      |
| Priority             | High                                                                         |
| Type                 | Functional                                                                  |
| Automation Candidate | Yes                                                                          |

---

### TC-VIEW-02 – No details shown when no account is selected

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-VIEW-01                                                                   |
| Preconditions        | User is authenticated                                                        |
| Test Data            | No account selected                                                          |
| Steps                | 1. Log in as a valid user<br>2. Navigate to Account Overview<br>3. Do not select any account |
| Expected Result      | No account details are displayed; error or prompt to select an account      |
| Priority             | Medium                                                                       |
| Type                 | Negative                                                                    |
| Automation Candidate | Yes                                                                          |

---

## Transaction History Display

### TC-VIEW-03 – Display transaction history (Rule 1 – Accepted)

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-VIEW-02                                                                   |
| Preconditions        | User is authenticated, account selected, transactions exist, activity period and type selected |
| Test Data            | Transactions exist, valid activity period selected, valid transaction type   |
| Steps                | 1. Select account<br>2. Select activity period<br>3. Select transaction type |
| Expected Result      | Transaction history is displayed for the selected account                    |
| Priority             | High                                                                         |
| Type                 | Functional                                                                  |
| Automation Candidate | Yes                                                                          |

---

### TC-VIEW-04 – Error when transaction type not selected (Rule 2 – Rejected)

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-VIEW-02                                                                   |
| Preconditions        | User is authenticated, account selected, transactions exist, activity period selected |
| Test Data            | Transaction type not selected                                               |
| Steps                | 1. Select account<br>2. Select activity period<br>3. Do not select transaction type |
| Expected Result      | Error message prompting user to select a transaction type                    |
| Priority             | Medium                                                                       |
| Type                 | Negative                                                                    |
| Automation Candidate | Yes                                                                          |

---

### TC-VIEW-05 – Error when activity period not selected (Rule 3 – Rejected)

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-VIEW-02                                                                   |
| Preconditions        | User is authenticated, account selected, transactions exist, transaction type selected |
| Test Data            | Activity period not selected                                                |
| Steps                | 1. Select account<br>2. Do not select activity period<br>3. Select transaction type |
| Expected Result      | Error message prompting user to select an activity period                    |
| Priority             | Medium                                                                       |
| Type                 | Negative                                                                    |
| Automation Candidate | Yes                                                                          |

---

### TC-VIEW-06 – Error when no transactions exist (Rule 4 – Rejected)

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-VIEW-02                                                                   |
| Preconditions        | User is authenticated, account selected, no transactions exist             |
| Test Data            | No transactions for selected account                                        |
| Steps                | 1. Select account<br>2. Select activity period<br>3. Select transaction type |
| Expected Result      | Error message indicating no transactions exist for the selected account     |
| Priority             | Medium                                                                       |
| Type                 | Negative                                                                    |
| Automation Candidate | Yes                                                                          |
