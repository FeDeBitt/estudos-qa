# Test Checklist: JShop Registration Form

**Context:** This document contains a formalized test checklist executed to validate the registration module of the JShop web application. Checklists act as a streamlined alternative to full test cases, ensuring that all critical functionalities and business rules are verified efficiently during the testing cycle.

**Test Execution Details:**
* **Target URL:** `https://jshop.mate.academy/#/register`
* **Run Date:** 09/04/2026
* **Preconditions:** None

---

## Execution Results

| ID | Checklist Item | Priority | Status | Comments |
|:---|:---|:---|:---:|:---|
| **1** | User is able to register after filling in all required fields with valid data upon clicking the [Register] button. | Critical | Passed | - |
| **2** | User is not able to register with an invalid email address format. | Critical | Passed | Passed, cannot sign up. |
| **3** | User is not able to register with an already registered email. | Critical | Passed | - |
| **4** | Password field must require at least 8 characters. | Critical | Failed | Able to register with 5 characters. |
| **5** | Password field must require at least one uppercase letter, one lowercase letter, one number, and one special character. | High | Failed | Able to register with "#1234" as a password. |
| **6** | "Repeat password" field must only be valid if it strictly matches the "password" field value. | High | Passed | - |
| **7** | Password advice indicator must be disabled by design when not triggered. | Medium | Passed | - |
| **8** | Password advice must explicitly display every password complexity requirement. | Medium | Passed | - |
| **9** | The fields "email", "password", "repeat password", "security question", and "answer" must be mandatory for registration. | Critical | Passed | - |
| **10** | The "Already a customer" link must redirect the user to the login page. | Medium | Passed | - |