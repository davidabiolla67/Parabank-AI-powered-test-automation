# Test Suite: Login & Authentication

## Feature Overview

This test suite covers functional and validation testing for the **Parabank Login & Authentication** feature. Test cases are derived using **equivalence partitioning and decision table analysis** to validate credential handling and post-login system behavior.

---

## Requirements Covered

* **FR-AUTH-01**: The system shall allow a registered user to log in using valid username and password.
* **FR-AUTH-02**: The system shall redirect authenticated users to the Account Overview page after successful login.

---

## Test Suite: Login & Authentication

### TC-AUTH-01 – Successful login with valid credentials

| Field                | Description                                                           |
| -------------------- | --------------------------------------------------------------------- |
| Requirement ID       | FR-AUTH-01                                                            |
| Preconditions        | User is registered and on the Login page                              |
| Test Data            | Valid username and valid password                                     |
| Steps                | 1. Enter valid username<br>2. Enter valid password<br>3. Click Submit |
| Expected Result      | User is authenticated successfully                                    |
| Priority             | High                                                                  |
| Type                 | Functional                                                            |
| Automation Candidate | Yes                                                                   |

---

### TC-AUTH-02 – Login fails with valid username and invalid password

| Field                | Description                                                             |
| -------------------- | ----------------------------------------------------------------------- |
| Requirement ID       | FR-AUTH-01                                                              |
| Preconditions        | User is registered and on the Login page                                |
| Test Data            | Valid username and invalid password                                     |
| Steps                | 1. Enter valid username<br>2. Enter invalid password<br>3. Click Submit |
| Expected Result      | Authentication fails and error message is displayed                     |
| Priority             | High                                                                    |
| Type                 | Negative                                                                |
| Automation Candidate | Yes                                                                     |

---

### TC-AUTH-03 – Login fails with invalid username and valid password

| Field                | Description                                                             |
| -------------------- | ----------------------------------------------------------------------- |
| Requirement ID       | FR-AUTH-01                                                              |
| Preconditions        | User is on the Login page                                               |
| Test Data            | Invalid username and valid password                                     |
| Steps                | 1. Enter invalid username<br>2. Enter valid password<br>3. Click Submit |
| Expected Result      | Authentication fails and error message is displayed                     |
| Priority             | High                                                                    |
| Type                 | Negative                                                                |
| Automation Candidate | Yes                                                                     |

---

 

 

### TC-AUTH-06 – No redirection without form submission

| Field                | Description                                          |
| -------------------- | ---------------------------------------------------- |
| Requirement ID       | FR-AUTH-02                                           |
| Preconditions        | User is on the Login page                            |
| Test Data            | Valid username and valid password                    |
| Steps                | 1. Enter valid credentials<br>2. Do not click Submit |
| Expected Result      | No authentication attempt and no redirection occurs  |
| Priority             | Low                                                  |
| Type                 | Negative                                             |
| Automation Candidate | No                                                   |
