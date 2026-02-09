# Test Suite: Open New Account

## Feature Overview

This test suite covers functional and validation testing for the **Parabank Open New Account** feature. Test cases are derived using **decision table analysis** to validate authentication status, account type selection, funding account selection, and system behavior after account creation.

---

## Requirements Covered

* **FR-ACC-01**: The system shall allow authenticated users to open a new bank account.
* **FR-ACC-02**: The system shall create the account and display it in the Account Overview.

---

## Test Suite: Open New Account

### TC-ACC-01 – Open new account with all valid inputs (Rule 1 – Accepted)

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-ACC-01                                                                    |
| Preconditions        | User is authenticated and on the Open New Account page                      |
| Test Data            | Valid account type, valid existing account                                  |
| Steps                | 1. Ensure user is logged in<br>2. Select account type<br>3. Select existing account<br>4. Click Open |
| Expected Result      | New bank account is opened successfully                                      |
| Priority             | High                                                                         |
| Type                 | Functional                                                                  |
| Automation Candidate | Yes                                                                          |

---

### TC-ACC-02 – Open new account fails when user is not authenticated (Rule 2 – Rejected)

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-ACC-01                                                                    |
| Preconditions        | User is not authenticated                                                   |
| Test Data            | Valid account type and valid existing account                                |
| Steps                | 1. Attempt to access Open New Account page<br>2. Select account type<br>3. Select existing account<br>4. Click Open |
| Expected Result      | Account creation is rejected and user is redirected to Login page or shown an error |
| Priority             | High                                                                         |
| Type                 | Negative                                                                    |
| Automation Candidate | Yes                                                                          |

---

### TC-ACC-03 – Open new account fails without selecting account type (Rule 3 – Rejected)

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-ACC-01                                                                    |
| Preconditions        | User is authenticated and on the Open New Account page                      |
| Test Data            | No account type selected, valid existing account                             |
| Steps                | 1. Ensure user is logged in<br>2. Do not select account type<br>3. Select existing account<br>4. Click Open |
| Expected Result      | Account creation fails and validation error is displayed                     |
| Priority             | High                                                                         |
| Type                 | Negative                                                                    |
| Automation Candidate | Yes                                                                          |

---

### TC-ACC-04 – Open new account fails without selecting existing account (Rule 4 – Rejected)

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-ACC-01                                                                    |
| Preconditions        | User is authenticated and on the Open New Account page                      |
| Test Data            | Valid account type, no existing account selected                             |
| Steps                | 1. Ensure user is logged in<br>2. Select account type<br>3. Do not select existing account<br>4. Click Open |
| Expected Result      | Account creation fails and validation error is displayed                     |
| Priority             | Medium                                                                       |
| Type                 | Negative                                                                    |
| Automation Candidate | Yes                                                                          |

---

  

## Account Creation & Overview Validation

### TC-ACC-08 – New account appears in Account Overview

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-ACC-02                                                                    |
| Preconditions        | Account creation is successful                                              |
| Test Data            | Newly created account                                                       |
| Steps                | 1. Open a new account successfully<br>2. Navigate to Account Overview       |
| Expected Result      | Newly created account is displayed with correct account number and type     |
| Priority             | High                                                                         |
| Type                 | Functional                                                                  |
| Automation Candidate | Yes                                                                          |

---

 