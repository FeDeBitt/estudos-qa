# Test Design Techniques: Password Validation

**Context:** This document applies fundamental test design techniques—Equivalence Partitioning and Boundary Value Analysis (BVA)—to a password validation field. The objective is to optimize test coverage by systematically identifying valid/invalid input classes and verifying the system's behavior at its strict data limits.

---

## Part I: Equivalence Classes

| ID | Validation Rule | Class Definition | Test Input Example | Expected Result |
|:---|:---|:---|:---|:---|
| **1** | Min. 4 characters | **Valid:** >= 4 characters | `#Pas` | System accepts the password and allows registration. |
| **2** | Max. 16 characters | **Valid:** <= 16 characters | `#Password1` | System accepts the password and allows registration. |
| **3** | Capital letter required | **Valid:** Contains >= 1 capital letter | `#World1` | System accepts the password and allows registration. |
| **4** | Special character required | **Valid:** Contains >= 1 special character | `#Pass123` | System accepts the password and allows registration. |
| **5** | Min. 4 characters | **Invalid:** < 4 characters | `#12` | System rejects the password and asserts a minimum character quantity message. |
| **6** | Max. 16 characters | **Invalid:** > 16 characters | `$Password12345678` | System rejects the password and asserts a maximum character quantity message. |
| **7** | Capital letter required | **Invalid:** No capital letters | `$password2` | System rejects the password and asserts a message requiring a capital letter. |
| **8** | Special character required | **Invalid:** No special characters | `Password12` | System rejects the password and asserts a message requiring a special character. |

---

## Part II: Boundary Value Analysis (BVA)

**Conditions Tested:** Minimum 4 characters, Maximum 16 characters.
**Limit Values Identified:** 3, 4, 15, 16, 17.

| ID | Boundary Target | Test Input Example | Input Length | Expected Result |
|:---|:---|:---|:---:|:---|
| **1** | Just below minimum boundary | `Ab1` | 3 | System rejects the password and asserts a minimum character quantity message. |
| **2** | Exactly on minimum boundary | `Ab1#` | 4 | System accepts the password and allows registration. |
| **3** | Exactly on maximum boundary | `#P34567891234567` | 16 | System accepts the password and allows registration. |
| **4** | Just above maximum boundary | `#P345678912345678` | 17 | System rejects the password and asserts a maximum character quantity message. |