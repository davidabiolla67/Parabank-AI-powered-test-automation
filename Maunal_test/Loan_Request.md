# Test Suite: Request Loan

## Feature Overview

This test suite covers functional and validation testing for the **Parabank Request Loan** feature. Test cases are derived to validate loan submission, field validation, and approval/rejection messaging.

---

## Requirements Covered

* **FR-LOAN-01**: The system shall allow users to submit a loan request.  
* **FR-LOAN-02**: The system shall validate loan request details.  
* **FR-LOAN-03**: The system shall display loan request approval or rejection status.

---

## Test Suite: Request Loan

### TC-LOAN-01 – Submit loan request successfully

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-LOAN-01                                                                  |
| Preconditions        | User is authenticated and on the Request Loan page                          |
| Test Data            | Valid loan amount, valid down payment                                       |
| Steps                | 1. Enter loan amount<br>2. Enter down payment<br>3. Click Submit            |
| Expected Result      | Loan request submitted successfully; confirmation message displayed         |
| Priority             | High                                                                         |
| Type                 | Functional                                                                  |
| Automation Candidate | Yes                                                                          |

---

### TC-LOAN-02 – Reject loan request when fields are missing

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-LOAN-01                                                                  |
| Preconditions        | User is authenticated and on the Request Loan page                          |
| Test Data            | One or more required fields left empty                                       |
| Steps                | 1. Leave one or more required fields blank<br>2. Click Submit               |
| Expected Result      | Loan request is rejected; validation error message displayed                |
| Priority             | High                                                                         |
| Type                 | Negative                                                                    |
| Automation Candidate | Yes                                                                          |

---

### TC-LOAN-03 – Reject negative or zero loan amount

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-LOAN-02                                                                  |
| Preconditions        | User is authenticated and on the Request Loan page                          |
| Test Data            | Loan amount ≤ 0, valid down payment                                         |
| Steps                | 1. Enter negative or zero loan amount<br>2. Enter valid down payment<br>3. Click Submit |
| Expected Result      | Loan request is rejected; validation error message displayed                |
| Priority             | High                                                                         |
| Type                 | Negative                                                                    |
| Automation Candidate | Yes                                                                          |

---

### TC-LOAN-04 – Reject down payment greater than loan amount

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-LOAN-02                                                                  |
| Preconditions        | User is authenticated and on the Request Loan page                          |
| Test Data            | Down payment > loan amount                                                  |
| Steps                | 1. Enter loan amount<br>2. Enter down payment greater than loan<br>3. Click Submit |
| Expected Result      | Loan request is rejected; validation error message displayed                |
| Priority             | High                                                                         |
| Type                 | Negative                                                                    |
| Automation Candidate | Yes                                                                          |

---
 