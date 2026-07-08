# Extended Bug Reports: JPetStore Web Application

**Context:** This document contains a detailed bug report for the JPetStore web application. This documentation includes extended parameters such as preconditions, priority levels, and environment specifics to fully comply with standard QA reporting metrics.

---

## 1. Out-of-Stock Product Purchase Allowed
* **ID:** PS-001
* **Severity:** Critical
* **Priority:** High
* **Environment:** macOS 14 (Sonoma) | Chrome (latest) | App Version: Demo

**Description:**
The system permits users to complete a checkout process for items that are currently out of stock.

**Preconditions:**
* An out-of-stock product is added to the shopping cart.

**Steps to Reproduce:**
1. Access the JPetStore application.
2. Add an out-of-stock product to the shopping cart.
3. Observe the stock availability status.
4. Proceed to checkout and complete the transaction.

**Expected Result:**
The system should block the transaction and display an error message stating the inability to finish the purchase due to item unavailability.

**Actual Result:**
The purchase is successfully finished despite the lack of inventory.

**Evidence:**
* [Video Attachment](https://drive.google.com/file/d/1FNEswKcjFIv8rRo4ljJVNY5DU83gGtF4/view?usp=sharing)

---

## 2. Mismatched Breed Image on Search Results
* **ID:** PS-002
* **Severity:** Minor
* **Priority:** Medium
* **Environment:** macOS 14 (Sonoma) | Chrome (latest) | App Version: Demo

**Description:**
When searching for a specific breed, the search results display a correct text description but an incorrect corresponding image.

**Preconditions:**
* Access to the JPetStore application search functionality.

**Steps to Reproduce:**
1. Access the application.
2. Enter 'Bulldog' into the search tab and submit.
3. Observe the returned search results.

**Expected Result:**
A Bulldog image should appear alongside the Bulldog's description.

**Actual Result:**
A Chihuahua image appears above the Bulldog's description.

**Evidence:**
* [Screenshot Attachment](https://ibb.co/QFJyMv50)

---

## 3. Search Failure with Punctuation Marks
* **ID:** PS-003
* **Severity:** Minor
* **Priority:** Low
* **Environment:** macOS 14 (Sonoma) | Chrome (latest) | App Version: Demo

**Description:**
The search functionality fails to return results when punctuation marks are included in the search query.

**Preconditions:**
* Access to the JPetStore application search functionality.

**Steps to Reproduce:**
1. Access the application.
2. Enter 'poodle.' (with a period) into the search tab and submit.
3. Observe the returned search results.

**Expected Result:**
The search engine should sanitize the input and return catalog results for 'poodle'.

**Actual Result:**
The search query returns no results.

**Evidence:**
* [Screenshot Attachment](https://ibb.co/7J3gyqvF)