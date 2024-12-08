### Vacation Tracking System (VTS)

### Index

- [Vacation Tracking System (VTS)](#vacation-tracking-system-vts)
- [Index](#index)
- [Overview](#overview)
  - [Domain](#domain)
  - [Vision](#vision)
  - [Goals](#goals)
  - [Functional Requirements](#functional-requirements)
  - [Non-Functional Requirements](#non-functional-requirements)
  - [Constraints](#constraints)
  - [Assumptions](#assumptions)
  - [Actors](#actors)
  - [Use Cases](#use-cases)
- [Use Case Example: Manage Time](#use-case-example-manage-time)
- [Links \& Reference](#links--reference)

---

### Overview

The Vacation Tracking System (VTS) is a web-based application designed to streamline the management of vacation time, sick leave, and personal time off for employees and managers. It aims to improve internal business operations by automating leave management processes and providing intuitive tools for all actors involved.

#### Domain

Managers struggle to effectively manage and stay aware of their employees' vacation schedules.

---

#### Vision

The organization aims to develop a Vacation Tracking System (VTS) to streamline vacation and leave management. This web-based system will provide:

- Employees the ability to manage vacation time, sick leave, and personal time off without needing expertise in company or local policies.

- Managers the tools to efficiently approve and track employee leave requests.

- HR and admin staff with comprehensive control and override capabilities for exceptional cases.

---

#### Goals

1- Automate leave management processes to reduce inefficiencies.

2- Improve internal business operations by integrating leave management into a centralized intranet portal.

3- Ensure simplicity, flexibility, and policy adherence in managing vacation and leave.

---

#### Functional Requirements

- Employees can:

  - Request vacation, sick, and personal time off.
  - View their leave balances and past requests (up to 18 months in the future and 6 months in the past).
  - Edit or withdraw pending requests and cancel approved ones.

- Managers can:

  - Approve or deny leave requests.
  - Award additional personal leave time within system-set limits.

- HR clerks can:

  - Manage employee records, location-based rules, and leave categories.
  - Override leave decisions with logging of overrides.

- System Administrators can:

  - Maintain system logs and ensure smooth technical operations.

- Notifications:

  - Notify managers of pending approvals via email.
  - Notify employees of status changes in real-time.

- Integration:

  - Uses a single sign-on mechanism via the intranet portal.
  - Integrates with HR legacy systems for employee data synchronization.
  - Offers a web service interface for querying employee vacation summaries.

- Logging:
  - Tracks all system transactions, including overrides and rule violations.

---

#### Non-Functional Requirements

- **User Experience:**
  The interface should be intuitive, easy to use, and unified for employees and managers.

- **Rules Compliance:**
  Enforce HR-defined vacation rules based on employee work location and company policies.

- **Consistency:**
  All employees work 8-hour days; time is tracked accordingly.

- **Scalability:**
  Designed to handle current and future employee growth.

---

#### Constraints

- The system uses existing intranet hardware and middleware.
- All actions must adhere to HR-defined rules and policies.
- Managers and employees share a unified home screen for consistency.

---

#### Assumptions

- The HR department owns and maintains all leave policies and validation rules.

- Employee credentials in the portal are reliable for authentication and role identification.

- Employees and managers understand basic navigation of the portal.

---

#### Actors

**_Employee:_**

- Manages their own leave.
- Submits, withdraws, or edits vacation requests.

**_Manager:_**

- Approves or denies leave requests.
- Awards additional leave (comp time).

**_HR Clerk:_**

- Manages employee records, rules, and overrides.
- Ensures the system reflects updated policies.

**_System Administrator:_**

- Manages technical resources, backups, and logs.

---

#### Use Cases

![img](https://drive.google.com/uc?id=10mRuk9pdAwl_Fp9POcwoVCTC7zfQH4jI)

The following use case diagram show that there are 8 use cases

1- **Manage Time (Primary Use Case):**
Employees request or view vacation time and leave.

2- **Approve Request:**
Managers review and respond to leave requests.

3- **Award Time:**
Managers grant additional leave time within limits.

4-**Edit Employee Record:**
HR clerks modify employee details, allowances, or leave rules.

5- **Manage Locations:**
HR clerks handle location-specific policies and restrictions.

6- **Manage Leave Categories:**
HR clerks manage leave types and associated rules.

7- **Override Leave Records:**
HR clerks override automated decisions while maintaining logs.

8- **Back Up System Logs:**
Administrators archive system transaction logs.

---

### Use Case Example: Manage Time

**Actor:** Employee

**Goal:** Submit a new vacation request.

**Preconditions:**

- Employee is authenticated through the intranet portal.
- Employee has the privileges to manage leave.

**Main Flow:**

1- Employee accesses the VTS through the intranet portal.

2- The system retrieves and displays their leave balances and previous requests.

3- Employee selects a leave category with a positive balance.

4- The system provides a visual calendar for selecting dates and hours.

5- Employee enters details, including a title and description, and submits the request.

6- The system validates the request:

- If valid, the request is saved, and an email is sent to the manager for approval.

- If invalid, errors are displayed, allowing the employee to correct them.

**Alternate Flows:**

- **_Withdraw Request:_**

  Employee cancels a pending request, and the manager is notified.

- **_Cancel Approved Request:_**

  Employee cancels a previously approved request with notification to the manager.

- **_Edit Pending Request:_**

  Employee modifies the details of a pending request.

Below is sequence diagram for mange time use case

![img](https://drive.google.com/uc?id=1rEhvxkAycneZ-iCrOzEZmT3b9V1N6W83)

---

### Links & Reference

- [Diagrams](https://app.diagrams.net/#G1mJUx4L7VJeDy99Ff2yqsFeGfKAYl6axi#%7B%22pageId%22%3A%22_BaTuaqoY-boYIiUupAF%22%7D)
