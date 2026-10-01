# Software Requirements Specification: Registration Module

**Context:** This document outlines the functional requirements and business rules for the User Registration module. These atomic and testable requirements serve as the baseline for test case design and system validation.

---

## 1. General Registration Flow
* The "Registration" page allows users to create a new account.
* A registered account provides access to product ordering.
* The registered user should not be automatically logged in after a successful registration.
* Upon successful registration, the user should be redirected to the main page.
* The "Sign In" page should contain a "Register Now!" button.
* Clicking the "Register Now!" button should redirect the user to the "Registration" page.
* The "Registration" form should contain three blocks: "User Information", "Account Information", and "Profile Information".
* Users should be able to submit the form to create an account by clicking the [Save Account Information] button.
* Users should be able to submit the form by pressing the Enter key.

---

## 2. User Information Block
* This section should contain 3 required fields: Username, New Password, and Confirm Password.
* All required fields should be visually marked by asterisks.

### 2.1 Username
* This is a required field.
* The value should be unique across the entire system.
* The uniqueness validation should not be case-sensitive.
* The field itself should accept and store case-insensitive values.
* The value should contain between 3 and 40 symbols.
* The field should accept only Latin letters and digits.
* Special characters and non-printing symbols are not allowed.

### 2.2 New Password
* This is a required field.
* The user shouldn't be able to copy, cut, or paste text in this field.
* The input text should be covered by a password mask.
* The value should contain a minimum of 8 symbols and a maximum of 30 symbols.
* Non-printing symbols are not allowed.
* The value should contain at least one special character.
* The value should contain at least one digit.
* The value should contain at least one capital letter.

### 2.3 Confirm Password
* This is a required field.
* The user shouldn't be able to copy, cut, or paste text in this field.
* The value should contain a minimum of 8 symbols and a maximum of 30 symbols.
* The value should strictly match the input from the New Password field.
* The validation of matching passwords should occur upon form submission.

---

## 3. Account Information Block
* This section contains user contact details and must be filled during the registration process.

### 3.1 Email
* This is a required field.
* The format of the email should follow the pattern `[name]@[domain].[tld]`.
* The total length of the email address should be between 14 and 72 symbols.
* The `[name]` part accepts Latin letters, digits, and specific special characters: plus (+), hyphen (-), underline (_), and dot (.).
* The email address should be unique across the system.

### 3.2 Phone
* This is an optional field.
* The field should display a placeholder: `+38 098 765 43 21`.
* The entered number should start with a plus (+) symbol.
* Besides the starting plus (+) symbol, letters, special characters, and non-printing symbols are not allowed.

---

## 4. Profile Information Block
* This section contains optional additional preferences for the user account.

### 4.1 Language
* The available options are EN, ES, UK, and JA.

### 4.2 Favorite Category
* The user is able to select multiple favorite categories on the site.
* This selection is used to receive promotional emails with discounts.

### 4.3 Enable MyBanner
* The checkbox should always be present on the form.
* The checkbox should be checked by default.
* If the checkbox is checked, the additional useful info banner in the footer should be shown.
* If the checkbox is unchecked, the banner should be hidden.

---

## 5. System Validations & Error Handling
* For registration attempts with an already registered Username, the following message should be shown: *"This username is already taken. Please choose another one."*
* If validation fails, any empty required fields should be highlighted in red.
* For validations failing due to empty or invalid data, a single global message should be shown at the top of the form: *"Validation failed! Check that all required fields are filled with valid data."*