# Test Execution Report: PetStore Shopping Cart

**Context:** This document provides the final execution metrics and defect statistics for the PetStore Shopping Cart test cycle. Test summary reports are essential for communicating the quality status of a software module to stakeholders, translating testing efforts into measurable data.

**Related artifacts:** [Execution Checklist](../3_Casos_de_Teste/checklist_petstore_cart.md) | [Bug Reports](../4_Gestao_de_Defeitos/relatorio_bugs_petstore_cart.md)

---

## 1. Test Execution Statistics

**Run Date:** 2026-04-23

| Metric | Value |
|:---|:---:|
| **Total Tests Planned** | 37 |
| **Tests Executed** | 36 |
| **Execution Rate** | 97.30% |
| **Passed Tests** | 26 |
| **Pass Rate** | 72.22% |
| **Failed Tests** | 10 |
| **Skipped Tests** | 1 |

**Skipped test:** Item 34 (*Product name link redirects to product description*) could not be executed because it is blocked by CART-002 — the product name is not displayed in the cart, so its link cannot be tested.

---

## 2. Defect Statistics by Severity

The 10 failed checks map to **9 unique defects**, since items 3 and 21 of the checklist fail due to the same defect (CART-002).

| Severity Level | Number of Bugs | Percentage |
|:---|:---:|:---:|
| **Critical** | 0 | 0% |
| **Major** | 2 | 22.2% |
| **Moderate** | 4 | 44.4% |
| **Minor** | 3 | 33.3% |
| **Total** | **9** | **100%** |

---

## 3. Conclusion

The Shopping Cart module is **not recommended for release** in its current state. Although the core flows (adding and removing products, subtotal recalculation, and checkout redirection) work as expected, two Major defects break business rules directly tied to orders: the 5-unit limit per product is not enforced (CART-005) and out-of-stock products can be added to the cart (CART-006). These two defects should be fixed and retested before release, followed by a regression run of the cart module.
