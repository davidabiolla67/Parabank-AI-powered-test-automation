# Test Suite: Update Customer Profile

## Feature Overview

This test suite covers functional testing for the **Parabank Update Customer Profile** feature. Test cases are derived to validate profile editing, saving, and canceling changes.

---

## Requirements Covered

* **FR-UP-01**: The system shall allow users to update their personal profile information.

---

## Test Suite: Update Customer Profile

### TC-UP-01 – Update profile successfully

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-UP-01                                                                    |
| Preconditions        | User is authenticated and on the Update Profile page                        |
| Test Data            | Editable profile fields with valid values                                   |
| Steps                | 1. Edit one or more profile fields<br>2. Click Save                         |
| Expected Result      | Profile updates are saved successfully; confirmation message displayed      |
| Priority             | High                                                                         |
| Type                 | Functional                                                                  |
| Automation Candidate | Yes                                                                          |

---

### TC-UP-02 – Cancel update does not save changes

| Field                | Description                                                                 |
| -------------------- | --------------------------------------------------------------------------- |
| Requirement ID       | FR-UP-01                                                                    |
| Preconditions        | User is authenticated and on the Update Profile page                        |
| Test Data            | Editable profile fields with changes                                        |
| Steps                | 1. Edit one or more profile fields<br>2. Click Cancel                        |
| Expected Result      | Changes are discarded; profile remains unchanged                             |
| Priority             | Medium                                                                       |
| Type                 | Negative                                                                    |
| Automation Candidate | Yes                                                                          |
