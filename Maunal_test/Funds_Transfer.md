# Test Suite: Transfer Funds

## Feature Overview

This test suite covers functional and validation testing for the **Parabank Transfer Funds** feature. Test cases are derived to validate fund transfers, amount validation, account selection, and balance updates.

---

## Requirements Covered

* **FR-TF-01**: The system shall allow users to transfer funds between their own accounts.
* **FR-TF-02**: The system shall validate transfer amount and account selections.
* **FR-TF-03**: The system shall update account balances after a successful transfer.

---

## Test Suite: Transfer Funds

### TC-TF-01 – Successful transfer between accounts

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-TF-01                                                                    |
| Preconditions        | User is authenticated and has multiple accounts with sufficient balance     |
| Test Data            | Positive transfer amount, valid source and destination accounts             |
| Steps                | 1. Select source account<br>2. Select destination account<br>3. Enter transfer amount<br>4. Click Send |
| Expected Result      | Transfer completes successfully; confirmation message displayed             |
| Priority             | High                                                                         |
| Type                 | Functional                                                                  |
| Automation Candidate | Yes                                                                          |

---

### TC-TF-02 – Reject transfer when amount is empty or zero (Rule 1 – Rejected)

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-TF-02                                                                    |
| Preconditions        | User is authenticated and has multiple accounts                             |
| Test Data            | Amount = 0 or empty, valid source and destination accounts                  |
| Steps                | 1. Select source account<br>2. Select destination account<br>3. Enter 0 or empty amount<br>4. Click Send |
| Expected Result      | Transfer is rejected with validation error message                           |
| Priority             | High                                                                         |
| Type                 | Negative                                                                    |
| Automation Candidate | Yes                                                                          |

---

### TC-TF-03 – Reject transfer when amount is negative (Rule 3 – Rejected)

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-TF-02                                                                    |
| Preconditions        | User is authenticated and has multiple accounts                             |
| Test Data            | Amount < 0, valid source and destination accounts                           |
| Steps                | 1. Select source account<br>2. Select destination account<br>3. Enter negative amount<br>4. Click Send |
| Expected Result      | Transfer is rejected with validation error message                           |
| Priority             | High                                                                         |
| Type                 | Negative                                                                    |
| Automation Candidate | Yes                                                                          |

---

### TC-TF-04 – Reject transfer when positive amount exceeds source balance (Rule 2 – Rejected)

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-TF-02                                                                    |
| Preconditions        | User is authenticated and has multiple accounts                             |
| Test Data            | Amount > source account balance, valid source and destination accounts      |
| Steps                | 1. Select source account<br>2. Select destination account<br>3. Enter amount greater than balance<br>4. Click Send |
| Expected Result      | Transfer is rejected with error indicating insufficient funds               |
| Priority             | High                                                                         |
| Type                 | Negative                                                                    |
| Automation Candidate | Yes                                                                          |

---

### TC-TF-05 – Accept transfer when positive amount within balance (Rule 4 – Accepted)

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-TF-02                                                                    |
| Preconditions        | User is authenticated and has multiple accounts                             |
| Test Data            | Amount > 0 and ≤ source account balance, valid source and destination accounts |
| Steps                | 1. Select source account<br>2. Select destination account<br>3. Enter valid amount<br>4. Click Send |
| Expected Result      | Transfer completes successfully                                             |
| Priority             | High                                                                         |
| Type                 | Functional                                                                  |
| Automation Candidate | Yes                                                                          |

---

## Account Balance Updates

### TC-TF-06 – Source account balance reduced correctly

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-TF-03                                                                    |
| Preconditions        | Successful transfer completed                                               |
| Test Data            | Source account before and after transfer                                     |
| Steps                | 1. Perform successful transfer<br>2. Check source account balance           |
| Expected Result      | Source account balance decreased by transfer amount                          |
| Priority             | High                                                                         |
| Type                 | Functional                                                                  |
| Automation Candidate | Yes                                                                          |

---

### TC-TF-07 – Destination account balance increased correctly

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-TF-03                                                                    |
| Preconditions        | Successful transfer completed                                               |
| Test Data            | Destination account before and after transfer                                |
| Steps                | 1. Perform successful transfer<br>2. Check destination account balance      |
| Expected Result      | Destination account balance increased by transfer amount                     |
| Priority             | High                                                                         |
| Type                 | Functional                                                                  |
| Automation Candidate | Yes                                                                          |
