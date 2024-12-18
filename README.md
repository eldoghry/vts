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
  - [Flow Charts](#flow-charts)
  - [Use Cases Examples](#use-cases-examples)
- [Data Model](#data-model)
- [UI](#ui)
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

#### Flow Charts

You can find below high-level flowchart description for Manager and Employee journey.

![img](https://drive.google.com/uc?id=1AXeXeXMni8jBlkX37hXZgmClGsR5Uvnd)

---

#### Use Cases Examples

Each one of the following has use case details, State diagram, Sequance diagram and Pseudocode

- [Manage vacation time](./use-cases/submit-request.md)
- [Edit Pending Vacation time request](./use-cases/edit-request.md)
- [Cancel vacation request](./use-cases/cancel-request.md)
- [Withdraw pending vacation time request](./use-cases/withdraw-request.md)

---

### Data Model

![img](https://drive.google.com/uc?id=1z7x_FME9RGtWtBajkAQj8eHBypn8HNgn)

### UI

**Employee UI**

![img](https://drive.google.com/uc?id=1ShLLsNyA2blZ_GaY99PEFqzVet0FV6qq)

**Manager UI**

![img](https://drive.google.com/uc?id=1ti8JsA4_4zO3ivfYGmxbbzgWFl3NegqO)

### Links & Reference

- [Diagrams](https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&target=blank&highlight=0000ff&edit=_blank&layers=1&nav=1&title=vts.drawio#Uhttps%3A%2F%2Fdrive.google.com%2Fuc%3Fid%3D1mJUx4L7VJeDy99Ff2yqsFeGfKAYl6axi%26export%3Ddownload)
