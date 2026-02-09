# Test Suite: Logout

## Feature Overview

This test suite covers functional and security testing for the **Parabank Logout** feature. Test cases are derived to validate secure logout, session termination, and prevention of unauthorized access after logout.

---

## Requirements Covered

* **FR-LOG-01**: Allow secure logout.  
* **FR-LOG-02**: Terminate user session after logout.

---

## Test Suite: Logout

### TC-LOG-01 – Logout successfully ends session

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-LOG-01                                                                    |
| Preconditions        | User is authenticated and on any page of the application                     |
| Test Data            | N/A                                                                         |
| Steps                | 1. Click Logout button                                                      |
| Expected Result      | User is logged out; session ends; redirected to Login page                  |
| Priority             | High                                                                         |
| Type                 | Functional                                                                  |
| Automation Candidate | Yes                                                                          |

---

### TC-LOG-02 – User cannot access secured pages after logout

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-LOG-02                                                                    |
| Preconditions        | User has logged out                                                          |
| Test Data            | Attempt to access secured URLs or pages                                      |
| Steps                | 1. Log out<br>2. Attempt to navigate to a secured page                     |
| Expected Result      | Access is denied; user redirected to Login page or shown error               |
| Priority             | High                                                                         |
| Type                 | Security / Negative                                                         |
| Automation Candidate | Yes                                                                          |

---

### TC-LOG-03 – Browser back button does not restore session

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-LOG-02                                                                    |
| Preconditions        | User has logged out                                                          |
| Test Data            | N/A                                                                         |
| Steps                | 1. Log out<br>2. Click browser back button                                  |
| Expected Result      | Secured pages are not restored; user stays on Login page or shown error     |
| Priority             | Medium                                                                       |
| Type                 | Security / Negative                                                         |
| Automation Candidate | Yes                                                                          |
