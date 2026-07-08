# Master Test Plan: Conduit Web Application

**Context:** The "Conduit" application is designed as an open-source platform to train software development and testing skills. The main functionality includes registration, authentication, publishing articles, reading, liking, commenting, and following users. This Test Plan prescribes the scope, approach, resources, and schedule for all testing activities of the Conduit website.

---

## 1. Test Strategy

### 1.1 Testing Scope

#### 1.1.1 Features to be Tested

| Module Name | Login State | Description |
|:---|:---|:---|
| **Conduit Logo** | Logged In / Logged Out | Situated on all pages. Clicking on it redirects to the home page. |
| **Home** | Logged In / Logged Out | The home link is situated on all pages. Clicking redirects to the home page. |
| **Sign In** | Logged Out | Situated on all pages. Clicking opens the sign-in page. |
| **Sign Up** | Logged Out | Situated on all pages. Clicking opens the sign-up page. |

#### 1.1.2 Out of Test Scope
The following areas are excluded from this specific testing cycle:
* Website Security Testing
* Website Performance/Load Testing
* Website API Testing
* Test Automation

### 1.2 Test Types
The Conduit website will be evaluated using the following testing types:
* **System Testing:** Conducted on a complete, integrated system to evaluate compliance with requirements.
* **Exploratory Testing:** Simultaneous learning, test design, and execution.
* **Smoke Testing:** Executed for each new build to verify critical core functionalities.
* **Functional Testing:** Validation of all mapped features.
* **GUI Testing:** Verification of the graphical user interface components.
* **Compatibility Testing:** Validation restricted to Windows and macOS browsers.

### 1.3 Risks and Mitigation

| Risk | Mitigation Strategy |
|:---|:---|
| Team members lack the required skills for website testing. | Ensure attendance in technical lectures and completion of preparatory assignments. |
| Insufficient time to test all browsers and Operating Systems. | Prioritize the most utilized browsers (Chrome/Safari) and OS versions based on market share. |
| Insufficient time to execute all mapped test scenarios. | Prioritize test execution based on severity and risk (P0/P1 first). |
| Resource unavailability (e.g., team member illness). | Reallocate tasks among available members utilizing agile methodologies. |

### 1.4 Test Logistics

#### 1.4.1 Roles and Responsibilities
* **QA Lead:** Felipe de Bittencourt Buss
* **Reviewers:** Mentorship Team

#### 1.4.2 Entry Criteria
Testing activities will commence only after:
1. The Decomposition Tree and Decision Tables are approved.
2. All Test Cases are finalized and have passed peer review.
3. The Test Environment URL is verified as stable and accessible.
4. Test Data (user accounts and sample articles) is prepared and seeded.

---

## 2. Test Objective
The primary objective is to verify the frontend functionality of the Conduit app. Testing focuses on the flow of publishing articles and user interaction. Main features include authorization, posting articles, following members, favoriting articles, liking, and commenting. Testing will be conducted on preselected browser versions as defined in the Resource Planning section.

---

## 3. Test Criteria

### 3.1 Suspension Criteria
Testing will be suspended and returned to the development team if:
* 10% or more of P0/P1 (Critical/High) tests fail.
* 30% or more of P2/P3 (Medium/Low) tests fail.

### 3.2 Exit Criteria
Test execution will conclude no later than the last day of the sprint, provided the following criteria are met:
* Mandatory test execution rate reaches 95%.
* Mandatory pass rate is 100% for P0/P1 tests.
* Mandatory pass rate is >= 80% for P2/P3 tests.
* All necessary artifacts are collected and documented (Test Cases, Bug Reports).
* The product has zero known Open bugs with Critical or Major severity.
* Any deferred bugs are formally agreed upon by developers and management.

---

## 4. Resource Planning

### 4.1 System Resources

| Resource | Description |
|:---|:---|
| **Browser** | Google Chrome and Safari (latest stable versions) to ensure cross-browser compatibility. |
| **Network** | Stable high-speed internet connection to validate real-time data persistence. |
| **Hardware** | PC or Laptop with at least 8GB RAM running Windows 11 or macOS (latest versions). |

### 4.2 Human Resources

| Resource | Description of Tasks |
|:---|:---|
| **QA Members** | Develop test documentation (decision tables, cases). Execute testing, track defects, and prepare final execution reports. |
| **Mentors** | Review and approve test plans/cases. Provide guidance on edge cases and assist in bug prioritization meetings. |

---

## 5. Test Environment
Testing will be conducted simulating a production-like environment. Local application execution for database validation will be managed utilizing Docker containers.

---

## 6. Schedule & Estimation

### 6.1 Task Estimation

| Task | Assignee | Estimated Effort |
|:---|:---|:---|
| Create Test Plan | QA Members | 3 person-hours |
| Create Decomposition & Decision Tables | Felipe Buss | 8 person-hours |
| Create Test Cases | Felipe Buss | 10 person-hours |
| Review Test Cases | Mentors | 3 person-hours |
| Test Case Execution | Felipe Buss | 10 person-hours |
| Create Bug Reports | Felipe Buss | 5 person-hours |
| Write Test Summary Report | Felipe Buss | 2 person-hours |

### 6.2 Sprint Schedule Matrix

| Task | Sprint 1 | Sprint 2 | Sprint 3 |
|:---|:---:|:---:|:---:|
| Create Test Plan | **[ X ]** | | |
| Create decomposition & decision tables | **[ X ]** | | |
| Create Test Cases | | **[ X ]** | |
| Review Test Cases | | **[ X ]** | |
| Test Case Execution | | | **[ X ]** |
| Create Bug Reports | | | **[ X ]** |
| Writing and preparing test results | | | **[ X ]** |

---

## 7. Test Deliverables

### 7.1 Before the Testing Phase
* Finalized Master Test Plan document.
* Decomposition Tree and Decision Tables.
* Approved Test Cases and seeded Test Data.

### 7.2 During the Testing Phase
* Bug Reports (including screenshots, environment logs, and reproduction steps).
* Test Execution Logs (Pass/Fail status updates).
* Updated/Refactored Test Documentation.

### 7.3 After the Testing Phase
* **Test Summary Report:** Final document containing execution metrics.
* **Final Defect List:** Traceability matrix of all identified bugs and their closing status.
* **Lessons Learned:** Process improvement analysis for future testing cycles.