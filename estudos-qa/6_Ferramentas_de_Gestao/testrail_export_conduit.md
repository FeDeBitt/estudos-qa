# TestRail Export: Conduit Authentication Module

**Context:** This document contains a raw export of the test cases designed and managed within TestRail for the Conduit web application. It highlights the scenarios mapped for the Authentication module (Sign In and Sign Up) and their respective priority levels, demonstrating practical experience with Test Case Management Systems (TCMS).

---

## Module: Sign In Page

* **[C48]** The email field should only accept valid email addresses (Priority: Critical).
* **[C49]** The password field should be required (Priority: Critical).
* **[C50]** Users should be able to paste data into the password field (Priority: High).
* **[C72]** Users should be able to open the Sign In page after clicking on the "Sign in" link in the Conduit navigation bar (Priority: High).
* **[C73]** The page should contain a form with two text fields - one for entering an email or username, and one for entering a password, and the [Sign in] button (Priority: Critical).
* **[C74]** The Sign In page should have the "Need an account?" link which redirects to the "Sign up" page (Priority: High).
* **[C75]** The Sign In page should have the "Forgot the password?" link which redirects to the "Forgot password" page (Priority: High).
* **[C76]** The email or username field should be required and should not be case-sensitive (Priority: Medium).
* **[C77]** The password field should be required and asterisks should cover the characters of the password (Priority: Medium).
* **[C78]** Users shouldn't be able to copy or cut values from the password field (Priority: Medium).
* **[C82]** Sign in page should contain a password field (Priority: Critical).

---

## Module: Register Page (Sign Up Form)

* **[C51]** The user should be able to register with valid data on the sign-up field (Priority: Critical).
* **[C52]** The username should be unique (Priority: Critical).
* **[C53]** After successful registration the user is redirected to "Finish Registration" page (Priority: High).
* **[C54]** Users should be able to go to the "Sign In" page by clicking on the "Have an account?" link below the "Sign Up" form (Priority: Medium).
* **[C55]** The username field is required for registration (Priority: Critical).
* **[C56]** The username should have at least 3 symbols (Priority: High).
* **[C57]** The username is limited to a maximum of 40 symbols (Priority: High).
* **[C58]** The username should accept Latin letters and digits (Priority: High).
* **[C59]** The username should start with a letter (Priority: High).
* **[C60]** The username should not contain special characters (Priority: High).
* **[C62]** The username should not be case-sensitive (Priority: High).
* **[C63]** The email format should be [name]@[domain].[top-domain] (Priority: High).
* **[C64]** The name part of the email should accept Latin letters, digits and special character such as plus (+), hyphen (-), underline (_), dot (.) (Priority: High).
* **[C65]** The email should be unique and required for registration (Priority: Critical).
* **[C66]** The password should be required for registration (Priority: Critical).
* **[C67]** The password should have at least 8 symbols (Priority: High).
* **[C68]** The password must be limited to 30 symbols (Priority: High).
* **[C69]** The password should not contain non-printing symbols (Priority: High).
* **[C70]** The password field should contain at least one special character and one capital letter (Priority: High).
* **[C71]** The confirm password field should be required and must match the password (Priority: Critical).