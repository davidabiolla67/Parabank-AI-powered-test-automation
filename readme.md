# # Parabank – AI-Powered Test Automation & Systematic Test Design

## Project Overview

This repository demonstrates a **structured, calculated, and AI-powered approach to testing a banking application (Parabank)**.

The objective of this project is to achieve **high functional coverage with minimal redundancy** by combining:

- **Formal test design techniques** (systematic test case derivation)
- **AI-driven test automation using testRigor**
- **Automated execution via CI/CD using GitHub Actions**

The test cases in this project were **not created by intuition or exploratory clicking**.  
They were **deliberately derived using defined rules and test design techniques** to cover a wide range of functional outcomes and edge cases typical of real-world banking systems.

---

## Why AI-Powered Test Automation?

Traditional UI automation is often brittle and costly to maintain due to:
- Hard-coded locators
- Frequent UI changes
- High maintenance overhead

This project uses **testRigor**, an AI-powered automation tool, to:
- Create tests in a **structured, human-readable language**
- Leverage **self-healing locators**
- Reduce test maintenance when UI elements change
- Focus on **user behavior and business logic**, not UI implementation

AI is used to **execute and maintain tests**, while **test coverage and logic are driven by formal test design**.

---

## Systematic Test Case Derivation Approach

All test cases in this repository were derived using a **repeatable and defensible methodology**.  
The same process was applied consistently across all modules (Registration, Login, Transfers, Bill Pay, etc.).

The steps below illustrate **exactly how the Registration test cases were derived**.

---

## Example: Registration Module – Test Case Derivation

### Step 1: Identify the Input Domain (Parameters)

The first step was to identify all **input parameters that influence system behavior** for the Registration feature.

#### Personal Information Parameters
- First Name
- Last Name
- Address
- City
- State
- ZIP Code
- Phone Number
- SSN

#### Account Information Parameters
- Username
- Password
- Confirm Password

These parameters define the **complete input domain** for registration.

---

### Step 2: Define Characteristics for Each Parameter

Each parameter was analyzed to identify its **behavior-affecting characteristics**.

| Parameter | Characteristic |
|---------|---------------|
| Username | Uniqueness |
| Password | Strength & Match |
| Phone Number | Numeric & Length |

This ensures testing focuses on **meaningful behavioral variations**, not arbitrary values.

---

### Step 3: Apply Equivalence Partitioning

Each characteristic was divided into **equivalence blocks**, where each block represents a **set of input values expected to behave the same way**.

#### Username – Equivalence Partitioning

**Characteristic:** Uniqueness

| Block ID | Description |
|--------|-------------|
| UN-V | Valid username |
| UN-E | Empty |
| UN-D | Duplicate |

Each block represents a **class of values**, not a single value.

---

### Step 4: Represent Each Block with Concrete Values

Each block was represented using a **representative input**:

- **UN-V (Valid):** Provide a unique, unused username  
- **UN-E (Empty):** Leave the username field blank  
- **UN-D (Duplicate):** Reuse an existing username  

This approach reduces the total number of test cases **without losing coverage**.

---

### Step 5: Apply Decision Table to Derive Outcomes

To calculate valid and invalid scenarios, the blocks were combined using a **decision table**.

#### Username Decision Table

| Conditions | Rule 1 | Rule 2 | Rule 3 |
|----------|--------|--------|--------|
| Is Duplicate | No | Yes | No |
| Is Empty | No | No | Yes |
| **Outcome** | Accepted | Rejected | Rejected |

This table explicitly defines **how the system should behave** under each condition combination.

---

### Step 6: Derive Test Cases from the Decision Table

Each rule in the decision table maps directly to a test case:

| Rule | Input Combination | Derived Test Case |
|----|------------------|------------------|
| Rule 1 | Not duplicate + Not empty | TC-REG-01 |
| Rule 2 | Duplicate username | TC-REG-05 |
| Rule 3 | Empty username | TC-REG-05 |

---

### Derived Registration Test Cases

- **TC-REG-01** – Successful registration with valid data  
- **TC-REG-02** – Registration fails when required personal information is missing  
- **TC-REG-03** – Registration fails when account credentials are missing  
- **TC-REG-04** – Registration fails when passwords do not match  
- **TC-REG-05** – Registration fails with duplicate or empty username  

Each test case can be **traced back to a parameter, characteristic, block, and rule**.

---

## Result

Using this structured approach ensures that:

- Test cases are **calculated, not guessed**
- Coverage is **intentional and justifiable**
- Redundant tests are avoided
- Test design is **scalable and repeatable** across modules
- Automation focuses on **high-value business behavior**

This same methodology was consistently applied to all other features in this repository.

---

## Tools & Technologies

- **testRigor** – AI-powered test automation
- **GitHub Actions** – CI/CD execution
- **Markdown** – Test documentation
- **Equivalence Partitioning & Decision Tables** – Test design techniques

---

## Author

**David Abiola**  
Quality Assurance Analyst | AI-Driven Test Automation | Banking Systems
