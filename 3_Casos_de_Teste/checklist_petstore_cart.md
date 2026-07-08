# Test Execution Checklist: PetStore Shopping Cart

**Context:** This document serves as the execution checklist for the PetStore Shopping Cart module. It validates functional requirements, UI elements, and business rules constraints, establishing direct traceability between failed items and their corresponding Bug IDs.

**Execution Details:**
* **Module:** Shopping Cart
* **Run Date:** 10/04/2026
* **Preconditions:** None

---

## Execution Results

| ID | Checklist Item | Priority | Result | Bug ID | Comments |
|:---|:---|:---|:---:|:---:|:---|
| **1** | User should be able to access the cart from any page. | Medium | Passed | - | - |
| **2** | The cart icon should have a tooltip 'Cart'. | Low | Failed | PS-001 | No tooltip displayed. |
| **3** | In the cart, there should be info about added products. | High | Failed | PS-002 | Product name is missing. |
| **4** | The Cart by default should not contain products. Empty Cart should contain "Your cart is empty." text. | Medium | Passed | - | - |
| **5** | The button "Proceed to Checkout" should be present under the table if at least one product was added to the Cart. | High | Passed | - | - |
| **6** | The "Proceed to Checkout" button should redirect logged-in users to the Checkout page. Not logged-in users should be redirected to the Login page. | High | Passed | - | - |
| **7** | Users should be able to leave the Cart page by clicking on the "Return to Main Menu" link. | High | Passed | - | - |
| **8** | When a user adds a new product to a Cart, it should be displayed as a badge with a quantity of products added on the Cart’s icon. | Medium | Failed | PS-003 | - |
| **9** | The product in the cart should contain clickable links for the product "Item ID" and "Name". | Medium | Failed | PS-004 | Product name is missing. |
| **10** | The "Quantity" field in the Cart should accept only numbers. | High | Passed | - | Letters can be typed, but field only retains numbers. |
| **11** | Users shouldn’t be able to add more than 5 items of the same products per order. | High | Failed | PS-005 | - |
| **12** | Validation of the quantity should happen immediately after a user enters a new quantity and presses Enter or clicks on the "Update Cart" button. | High | Passed | - | - |
| **13** | Users should be able to remove products from the Cart by clicking on the "Remove" button near the product price. | High | Passed | - | - |
| **14** | If a user enters the quantity of the product as 0 (zero) and updates the cart by the "Update Cart" button, it should be removed from the Cart. | High | Passed | - | - |
| **15** | The user should not be able to add the product to the Cart if it is not in stock. | Critical | Failed | PS-006 | - |
| **16** | If a logged-in user adds a product to the Cart, it should be displayed on all other sessions. | High | Passed | - | - |
| **17** | Can add product to shopping cart from Product Detail Page (PDP). | Medium | Passed | - | - |
| **18** | Can add product to shopping cart from the product list. | Medium | Passed | - | - |
| **19** | Item ID is present on the shopping cart. | High | Passed | - | - |
| **20** | Product ID is present on the shopping cart. | High | Passed | - | - |
| **21** | Product Name is present on the shopping cart. | High | Failed | PS-007 | - |
| **22** | Product description is present on the shopping cart. | High | Passed | - | - |
| **23** | Product availability (In stock) is present on the shopping cart. | High | Passed | - | - |
| **24** | Product quantity is present on the shopping cart. | High | Passed | - | - |
| **25** | List price is present on the shopping cart. | High | Passed | - | - |
| **26** | Total cost is present on the shopping cart. | High | Passed | - | - |
| **27** | Subtotal is displayed on the last row. | High | Passed | - | - |
| **28** | Update cart button is displayed on the last row. | High | Passed | - | - |
| **29** | Validation message is displayed when adding more than 5 products. | High | Failed | PS-008 | - |
| **30** | Show available quantity of products. | Medium | Failed | PS-009 | - |
| **31** | Display message "Requested quantity exceeds available stock". | Medium | Failed | PS-010 | - |
| **32** | Removing a product in one session removes it in others too. | Medium | Passed | - | - |
| **33** | Item ID link redirects to product description. | Low | Passed | - | - |
| **34** | Product name link redirects to product description. | High | Skipped | - | - |
| **35** | Subtotal is recalculated after quantity update. | Medium | Passed | - | - |
| **36** | Subtotal is recalculated after removing product. | Medium | Passed | - | - |
| **37** | Subtotal is recalculated after quantity is set to 0. | Medium | Passed | - | - |