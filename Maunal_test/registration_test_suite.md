# Test Suite: Registration

## Feature Overview

This test suite covers functional and validation testing for the **Parabank User Registration** feature. Test cases are derived using **domain analysis, equivalence partitioning, and decision table techniques** to ensure full requirement coverage.

---

## Requirements Covered

* **FR-REG-01**: The system shall allow a new user to register by providing required personal and account information.
* **FR-REG-02**: The system shall validate mandatory registration fields and display appropriate error messages for missing or invalid data.
* **FR-REG-03**: The system shall display a confirmation message after successful registration.

---

## Test Suite: Registration

### TC-REG-01 – Successful registration with valid data

| Field                | Description                                                                                                                                                         |
| -------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Requirement ID       | FR-REG-01                                                                                                                                                           |
| Preconditions        | User is on the Registration page                                                                                                                                    |
| Test Data            | All personal and account fields filled with valid data                                                                                                              |
| Steps                | 1. Enter valid First Name, Last Name, Address, City, State, ZIP Code, Phone Number, SSN<br>2. Enter valid Username, Password, Confirm Password<br>3. Click Register |
| Expected Result      | User is registered successfully                                                                                                                                     |
| Priority             | High                                                                                                                                                                |
| Type                 | Functional                                                                                                                                                          |
| Automation Candidate | Yes                                                                                                                                                                 |

---

### TC-REG-02 – Registration fails when required personal info is missing

| Field                | Description                                                                                             |
| -------------------- | ------------------------------------------------------------------------------------------------------- |
| Requirement ID       | FR-REG-01, FR-REG-02                                                                                    |
| Preconditions        | User is on the Registration page                                                                        |
| Test Data            | One or more personal information fields left empty                                                      |
| Steps                | 1. Leave at least one personal information field empty<br>2. Fill remaining fields<br>3. Click Register |
| Expected Result      | Validation message displayed and registration is rejected                                               |
| Priority             | High                                                                                                    |
| Type                 | Validation                                                                                              |
| Automation Candidate | Yes                                                                                                     |

---

### TC-REG-03 – Registration fails when account credentials are missing

| Field                | Description                                                                                     |
| -------------------- | ----------------------------------------------------------------------------------------------- |
| Requirement ID       | FR-REG-01, FR-REG-02                                                                            |
| Preconditions        | User is on the Registration page                                                                |
| Test Data            | Username and/or Password fields empty                                                           |
| Steps                | 1. Fill personal information fields<br>2. Leave Username or Password empty<br>3. Click Register |
| Expected Result      | Validation message displayed and registration is rejected                                       |
| Priority             | High                                                                                            |
| Type                 | Validation                                                                                      |
| Automation Candidate | Yes                                                                                             |

---

### TC-REG-04 – Registration fails when passwords do not match

| Field                | Description                                                                                                  |
| -------------------- | ------------------------------------------------------------------------------------------------------------ |
| Requirement ID       | FR-REG-01, FR-REG-02                                                                                         |
| Preconditions        | User is on the Registration page                                                                             |
| Test Data            | Password and Confirm Password do not match                                                                   |
| Steps                | 1. Fill all fields with valid data<br>2. Enter mismatched Password and Confirm Password<br>3. Click Register |
| Expected Result      | Validation message displayed and registration is rejected                                                    |
| Priority             | High                                                                                                         |
| Type                 | Validation                                                                                                   |
| Automation Candidate | Yes                                                                                                          |

---

### TC-REG-05 – Registration fails with duplicate or empty username

| Field                | Description                                                                                           |
| -------------------- | ----------------------------------------------------------------------------------------------------- |
| Requirement ID       | FR-REG-01, FR-REG-02                                                                                  |
| Preconditions        | User is on the Registration page                                                                      |
| Test Data            | Username is empty or already exists                                                                   |
| Steps                | 1. Enter duplicate or empty Username<br>2. Fill remaining fields with valid data<br>3. Click Register |
| Expected Result      | Validation message displayed and registration is rejected                                             |
| Priority             | High                                                                                                  |
| Type                 | Validation                                                                                            |
| Automation Candidate | Yes                                                                                                   |

---

