# Test Suite: Bill Pay

## Feature Overview

This test suite covers functional and validation testing for the **Parabank Bill Pay** feature. Test cases are derived to validate bill payment submission, amount validation, and payment confirmation display.

---

## Requirements Covered

* **FR-BP-02**: The system shall allow users to submit bill payments to selected payees.
* **FR-BP-03**: The system shall display payment confirmation after successful bill payment.

---

## Test Suite: Bill Pay

### TC-BP-03 – Successful bill payment

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-BP-02                                                                    |
| Preconditions        | User is authenticated, payee added, and sufficient funds in from account    |
| Test Data            | Valid payee selected, valid positive amount, from valid account             |
| Steps                | 1. Select payee<br>2. Select from account<br>3. Enter valid amount<br>4. Click Submit |
| Expected Result      | Bill payment is processed successfully                                      |
| Priority             | High                                                                         |
| Type                 | Functional                                                                  |
| Automation Candidate | Yes                                                                          |

---

### TC-BP-04 – Reject payment with invalid amount

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-BP-02                                                                    |
| Preconditions        | User is authenticated, payee added, and from account exists                 |
| Test Data            | Invalid amount (empty, 0, or negative), valid payee, valid from account     |
| Steps                | 1. Select payee<br>2. Select from account<br>3. Enter invalid amount<br>4. Click Submit |
| Expected Result      | Payment is rejected and error message displayed                              |
| Priority             | High                                                                         |
| Type                 | Negative                                                                    |
| Automation Candidate | Yes                                                                          |

---

### TC-BP-05 – Display payment confirmation message

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-BP-03                                                                    |
| Preconditions        | Bill payment completed successfully                                         |
| Test Data            | Valid bill payment details                                                  |
| Steps                | 1. Complete a successful bill payment<br>2. Observe system response        |
| Expected Result      | Payment confirmation message is displayed                                   |
| Priority             | High                                                                         |
| Type                 | Functional                                                                  |
| Automation Candidate | Yes                                                                          |

---
 