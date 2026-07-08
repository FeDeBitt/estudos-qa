# Bug Reports: JPetStore Web Application

**Context:** This document presents the identification and registration of 5 functional defects found during exploratory testing on the JPetStore web application. The objective of this task was to map behavioral flaws in the system and document them, ensuring traceability and clarity for the engineering team.

---

## 1. Mismatched Image on Search Results
* **ID:** PS-0001
* **Severity:** Medium
* **Module:** Search / Catalog

**Description:**
The system returns an incorrect image associated with a different breed when a specific search query is executed, despite displaying the correct text description.

**Steps to Reproduce:**
1. Access the JPetStore application.
2. Navigate to the search bar.
3. Enter the query 'Bulldog' and submit.
4. Observe the search results displayed.

**Expected Result:**
The search results should display images corresponding to the 'Bulldog' breed.

**Actual Result:**
A Chihuahua image appears in the search results instead of a Bulldog. The text description remains correct.

**Evidence:**
[Screenshot Attachment](https://ibb.co/MDx4pN5f)

---

## 2. Purchase Allowed for Out-of-Stock Products
* **ID:** PS-0002
* **Severity:** High
* **Module:** Shopping Cart / Checkout

**Description:**
The system lacks inventory validation during the checkout process, allowing users to proceed with purchasing items that are not currently available in stock.

**Steps to Reproduce:**
1. Access the JPetStore application.
2. Navigate to the catalog and select an item that is out of stock.
3. Add the item to the shopping cart.
4. Proceed to checkout and finish the purchase.

**Expected Result:**
The system should prevent the purchase and display an error or warning message indicating the item is out of stock.

**Actual Result:**
The product is not in stock, yet the system allows the user to finish the purchase successfully.

**Evidence:**
[Screenshot Attachment](https://ibb.co/3y6sLGC6)

---

## 3. Password Field Retains Data After Sign Out
* **ID:** PS-0003
* **Severity:** High
* **Module:** Authentication

**Description:**
The authentication system fails to clear sensitive user data from the sign-in form after the user has terminated their session.

**Steps to Reproduce:**
1. Access the JPetStore application.
2. Sign in with valid credentials.
3. Click the 'Sign Out' button.
4. Navigate back to the sign-in page.

**Expected Result:**
The username and password fields should be completely cleared upon signing out for security purposes.

**Actual Result:**
The password field remains filled with the user's credentials after signing out and returning to the sign-in page.

**Evidence:**
[Screenshot Attachment](https://ibb.co/gFT9STqZ)

---

## 4. Missing Validation for Maximum Purchase Quantity
* **ID:** PS-0004
* **Severity:** Medium
* **Module:** Shopping Cart

**Description:**
The application does not impose logical limits on the quantity of a single item that can be purchased, allowing unrealistic inventory requests.

**Steps to Reproduce:**
1. Access the JPetStore application.
2. Add a product (e.g., female chihuahua) to the shopping cart.
3. Change the quantity input to 1000 units.
4. Proceed to checkout and complete the purchase.

**Expected Result:**
The system should restrict the maximum quantity to a reasonable limit or validate the request against the actual available inventory.

**Actual Result:**
The application allows the user to successfully purchase 1000 units of the product without triggering any validation errors.

**Evidence:**
[Screenshot Attachment](https://ibb.co/sv2ymvz8)

---

## 5. Search Functionality Fails with Punctuation
* **ID:** PS-0005
* **Severity:** Low
* **Module:** Search

**Description:**
The search engine does not correctly parse or sanitize inputs containing punctuation marks, resulting in a failure to return relevant catalog items.

**Steps to Reproduce:**
1. Access the JPetStore application.
2. Navigate to the search bar.
3. Enter the query 'poodle.' (including the period at the end).
4. Submit the search query.

**Expected Result:**
The system should sanitize the input (ignoring the period) and return search results for 'poodle'.

**Actual Result:**
The search does not return any results due to the included punctuation.

**Evidence:**
[Screenshot Attachment](https://ibb.co/svr9P12b)