# Extended Test Suite: JPetStore Application

**Context:** This document outlines a comprehensive test case suite designed to validate the functional integrity of the JPetStore web application. The suite covers user registration, authentication, search capabilities, and shopping cart operations.

**Test Environment:**
* **Environment:** Production
* **Operating System:** macOS (Sierra or higher)
* **Browser:** Chrome (latest)

---

### PS-TC-001: User ID field should not accept an already registered User ID
* **Priority:** High | **Status:** Passed
* **Additional Info:** The tester needs to have an existing User ID in the system.
* **Steps to Perform:**
  1. Open the User registration form.
  2. Enter an existing User ID into the User ID field.
  3. Enter valid data into the rest of the fields.
  4. Click the [Save Account Information] button.
* **Expected Result:** Assert an error message indicating that the User ID field must be unique is shown.

### PS-TC-002: User ID field should not accept special characters
* **Priority:** High | **Status:** Failed
* **Steps to Perform:**
  1. Open the User registration form.
  2. Enter a value containing one special symbol into the User ID field.
  3. Enter valid data into the rest of the fields.
  4. Click the [Save Account Information] button.
* **Expected Result:** Assert an error message indicating that the User ID field accepts only alphanumeric characters is shown.

### PS-TC-003: User ID field should accept alphabetic characters and numbers
* **Priority:** Critical | **Status:** Passed
* **Steps to Perform:**
  1. Open the User registration form.
  2. Enter a value containing alphabetic characters and numbers into the User ID field.
  3. Click the [Save Account Information] button.
* **Expected Result:** Assert a successful registration message is shown and the user is redirected to the main page.

### PS-TC-004: The New Password field should not accept a value without a number
* **Priority:** Critical | **Status:** Passed
* **Steps to Perform:**
  1. Open the User registration form.
  2. Enter a value not containing numbers into the password field.
  3. Enter valid data into the rest of the fields.
  4. Click the [Save Account Information] button.
* **Expected Result:** Assert an error message indicating that the password field must contain a number is shown.

### PS-TC-005: The New Password field should not accept a value without a special symbol
* **Priority:** Critical | **Status:** Failed
* **Steps to Perform:**
  1. Open the User registration form.
  2. Enter a value not containing a special symbol into the password field.
  3. Enter valid data into the rest of the fields.
  4. Click the [Save Account Information] button.
* **Expected Result:** Assert an error message indicating that the password field must contain a special symbol is shown.

### PS-TC-006: The Repeat Password field should not accept values different from the New Password field
* **Priority:** Critical | **Status:** Failed
* **Steps to Perform:**
  1. Open the User registration form.
  2. Enter a value into the New Password field.
  3. Enter a different value into the Repeat Password field.
  4. Enter valid data into the rest of the fields.
  5. Click the [Save Account Information] button.
* **Expected Result:** Assert an error message indicating that the New Password and the Repeat Password must have the same characters is shown.

### PS-TC-007: Email field should not accept an already registered Email
* **Priority:** Critical | **Status:** Failed
* **Steps to Perform:**
  1. Open the User registration form.
  2. Enter an already registered Email.
  3. Enter valid data into the rest of the fields.
  4. Click the [Save Account Information] button.
* **Expected Result:** Assert an error message indicating that the user's email must be exclusive is shown.

### PS-TC-008: The Email field should not accept an invalid email format
* **Priority:** Critical | **Status:** Failed
* **Steps to Perform:**
  1. Open the User registration form.
  2. Enter an invalid format email.
  3. Enter valid data into the rest of the fields.
  4. Click the [Save Account Information] button.
* **Expected Result:** Assert an error message indicating that the email must not be in an invalid format is shown.

### PS-TC-009: User should be able to register with only required fields
* **Priority:** Critical | **Status:** Failed
* **Additional Info:** Test data used -> User ID: `userQA` | Email: `test@qa.team` | Password: `12345Qwert!`
* **Steps to Perform:**
  1. Open the main page.
  2. Click on "Sign In".
  3. Click on "Register Now!".
  4. Fill only the required fields: User ID, Email, New Password, Repeat Password.
  5. Click the [Save Account Information] button.
* **Expected Result:** Assert that the user is successfully registered, redirected to the main page, and the user's name is shown at the top left corner.

### PS-TC-010: Log in form should not accept blank Username and Password fields
* **Priority:** Critical | **Status:** Passed
* **Steps to Perform:**
  1. Open the sign-in page.
  2. Leave the Username and Password fields blank.
  3. Click the [Login] button.
* **Expected Result:** Assert an error message indicating that the username and password fields must not be blank is shown.

### PS-TC-011: Username field must accept User ID values given during registration
* **Priority:** Critical | **Status:** Passed
* **Steps to Perform:**
  1. Open the sign-in page.
  2. Enter an unregistered Username in the username field.
  3. Click the [Login] button.
* **Expected Result:** Assert an error message indicating that the username used during login must be previously registered is shown.

### PS-TC-012: The search field should allow users to search products by category
* **Priority:** High | **Status:** Passed
* **Steps to Perform:**
  1. Enter a product category in the search field.
  2. Click the [Search] button.
  3. Observe the results.
* **Expected Result:** The searched category products should appear in the search results.

### PS-TC-013: Search field must allow users to make searches by name
* **Priority:** High | **Status:** Passed
* **Steps to Perform:**
  1. Enter a product name in the search field.
  2. Click the [Search] button.
  3. Observe the results.
* **Expected Result:** The searched products should appear in the search results.

### PS-TC-014: The search field should allow users to search products by product ID
* **Priority:** High | **Status:** Failed
* **Steps to Perform:**
  1. Enter a product ID in the search field.
  2. Click the [Search] button.
  3. Observe the results.
* **Expected Result:** The products matching the searched product ID should appear in the search results.

### PS-TC-015: The system should allow products to be added to the cart directly from the product detail page
* **Priority:** High | **Status:** Passed
* **Steps to Perform:**
  1. Click a product category (e.g., bird, fish).
  2. Click on the product ID link.
  3. Click on the item ID link.
  4. Click the [Add to cart] button.
* **Expected Result:** The product should be successfully added to the cart.

### PS-TC-016: The system should allow products to be added to the cart from the product list
* **Priority:** High | **Status:** Passed
* **Steps to Perform:**
  1. Click on a product category (e.g., bird, fish).
  2. Click on the product ID link.
  3. Click the [Add to cart] button.
* **Expected Result:** The product should be successfully added to the cart.