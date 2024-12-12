### Use Case Example: Manage Vacation Time

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

---

### State Diagram

![img](https://drive.google.com/uc?id=1sBTc6v7n3V_qbyZ3dUd1nHE2tv5HeSTb)

---

### Sequence Diagram

Below is sequence diagram for mange time use case

![img](https://drive.google.com/uc?id=1rEhvxkAycneZ-iCrOzEZmT3b9V1N6W83)

---
