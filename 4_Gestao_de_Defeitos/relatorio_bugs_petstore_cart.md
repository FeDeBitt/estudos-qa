# Bug Reports: PetStore Shopping Cart

**Context:** This document contains detailed bug reports identified during the execution of the PetStore Shopping Cart test checklist. Each report includes reproducibility steps, environment constraints, severity and priority levels (priority inherited from the corresponding checklist item), and visual evidence to assist the development team in tracking and resolving the defects.

---

## 1. Cart Icon Tooltip Missing
* **ID:** CART-001
* **Severity:** Minor
* **Priority:** Low
* **Environment:** macOS 14 (Sonoma) | Chrome (latest) | App Version: Demo

**Description:**
The shopping cart icon fails to display a descriptive tooltip when the user interacts with it.

**Preconditions:**
* Access to the application site.

**Steps to Reproduce:**
1. Hover the mouse cursor over the cart icon.
2. Observe if the tooltip pops up.

**Expected Result:**
A tooltip containing the text 'Cart' should pop up when hovering the cursor over the cart icon.

**Actual Result:**
No tooltip pops up.

**Evidence:**
* [Screenshot Attachment](https://ibb.co/B2zYYZWb)

---

## 2. Product Name Missing in Shopping Cart
* **ID:** CART-002
* **Severity:** Moderate
* **Priority:** High
* **Environment:** macOS 14 (Sonoma) | Chrome (latest) | App Version: Demo

**Description:**
The system fails to display the name of the product once it has been added to the shopping cart.

**Preconditions:**
* A product is added to the shopping cart.

**Steps to Reproduce:**
1. Access the site.
2. Add a product to the shopping cart.
3. Observe the product information in the shopping cart interface.

**Expected Result:**
The product name should be clearly displayed alongside other product details.

**Actual Result:**
The product name is missing from the product information in the shopping cart.

**Evidence:**
* [Screenshot Attachment](https://ibb.co/p6tf4wP6)

---

## 3. Missing Product Quantity Badge on Cart Icon
* **ID:** CART-003
* **Severity:** Minor
* **Priority:** Medium
* **Environment:** macOS 14 (Sonoma) | Chrome (latest) | App Version: Demo

**Description:**
The cart icon does not render a visual badge to indicate the total quantity of items currently in the cart.

**Preconditions:**
* At least one product is added to the shopping cart.

**Steps to Reproduce:**
1. Access the site.
2. Add at least one product to the shopping cart.
3. Observe the cart icon in the navigation menu.

**Expected Result:**
A numeric badge indicating the current product quantity should be displayed above or next to the cart icon.

**Actual Result:**
There is no badge informing the product quantity.

**Evidence:**
* [Screenshot Attachment](https://ibb.co/p6tf4wP6)

---

## 4. Missing Clickable Links for Product ID and Name
* **ID:** CART-004
* **Severity:** Moderate
* **Priority:** Medium
* **Environment:** macOS 14 (Sonoma) | Chrome (latest) | App Version: Demo

**Description:**
The shopping cart does not provide hyperlinks on the Product ID and Name to redirect users back to the Product Detail Page.

**Preconditions:**
* A product is added to the shopping cart.

**Steps to Reproduce:**
1. Access the site.
2. Add a product to the shopping cart.
3. Observe the product information displayed.

**Expected Result:**
There should be active, clickable links on both the "Product ID" and the "Product Name".

**Actual Result:**
The product name is missing entirely, and there is no clickable link on the "Product ID".

**Evidence:**
* [Screenshot Attachment](https://ibb.co/p6tf4wP6)

---

## 5. System Allows Adding More Than 5 Units of the Same Product
* **ID:** CART-005
* **Severity:** Major
* **Priority:** High
* **Environment:** macOS 14 (Sonoma) | Chrome (latest) | App Version: Demo

**Description:**
The application fails to enforce the business rule that limits the purchase of a single item to a maximum of 5 units per order.

**Preconditions:**
* A product is added to the shopping cart.

**Steps to Reproduce:**
1. Access the site.
2. Add a product to the shopping cart.
3. Change the product quantity to a value greater than 5.
4. Observe the system's response.

**Expected Result:**
The system should block the action and display a validation message informing the user that it is not possible to add more than 5 units of the same item.

**Actual Result:**
It is possible to successfully add more than 5 units of the same product to the shopping cart.

**Evidence:**
* [Screenshot Attachment](https://ibb.co/4wQ0VdLm)

---

## 6. Out-of-Stock Products Can Be Added to Cart
* **ID:** CART-006
* **Severity:** Major
* **Priority:** High
* **Environment:** macOS 14 (Sonoma) | Chrome (latest) | App Version: Demo

**Description:**
The system lacks inventory validation, allowing users to add items that are currently out of stock to their shopping cart.

**Preconditions:**
* An out-of-stock product is identified in the catalog.

**Steps to Reproduce:**
1. Access the site.
2. Attempt to add an out-of-stock product to the shopping cart.
3. Observe the "In stock" state and system behavior.

**Expected Result:**
An error message should pop up informing the user that the product is not available for purchase.

**Actual Result:**
The system allows the out-of-stock product to be added to the cart without any warnings.

**Evidence:**
* [Screenshot Attachment](https://ibb.co/4wQ0VdLm)

---

## 7. Missing Validation Message for Maximum Quantity Exceeded
* **ID:** CART-007
* **Severity:** Moderate
* **Priority:** High
* **Environment:** macOS 14 (Sonoma) | Chrome (latest) | App Version: Demo

**Description:**
When a user bypasses the 5-item limit, the system does not trigger any front-end validation messages to warn the user of the policy violation.

**Preconditions:**
* Attempting to add more than 5 units of a product to the shopping cart.

**Steps to Reproduce:**
1. Access the site.
2. Add more than 5 products to the shopping cart.
3. Observe the interface results.

**Expected Result:**
An error validation message should be displayed explicitly stating that it is not possible to add more than 5 products to the shopping cart.

**Actual Result:**
No message is displayed, and it is possible to add the items without restriction.

**Evidence:**
* [Screenshot Attachment](https://ibb.co/ycSJjG0P)

---

## 8. Available Product Quantity Not Displayed
* **ID:** CART-008
* **Severity:** Minor
* **Priority:** Medium
* **Environment:** macOS 14 (Sonoma) | Chrome (latest) | App Version: Demo

**Description:**
The system does not inform the user about the actual available stock quantity for items in the catalog or cart.

**Preconditions:**
* A product is added to the shopping cart.

**Steps to Reproduce:**
1. Access the site.
2. Add a product to the shopping cart.
3. Observe the "In stock" state indicators.

**Expected Result:**
The exact available product quantity should be displayed to guide the user's purchase limits.

**Actual Result:**
The available product quantity is completely hidden from the user interface.

**Evidence:**
* [Screenshot Attachment](https://ibb.co/99w4fQcH)

---

## 9. Missing Stock Exceedance Warning Message
* **ID:** CART-009
* **Severity:** Moderate
* **Priority:** Medium
* **Environment:** macOS 14 (Sonoma) | Chrome (latest) | App Version: Demo

**Description:**
If a user requests a quantity higher than the available physical stock, the system fails to warn them that their request cannot be fulfilled.

**Preconditions:**
* A product is added to the shopping cart.

**Steps to Reproduce:**
1. Access the site.
2. Add a product to the shopping cart.
3. Increase the product quantity beyond the known available stock.
4. Observe the results.

**Expected Result:**
An error message should pop up informing the user: "Requested quantity exceeds available stock".

**Actual Result:**
The validation message is not displayed, and the system allows any arbitrary product quantity to be added.

**Evidence:**
* [Screenshot Attachment](https://ibb.co/Pzv3D6LT)