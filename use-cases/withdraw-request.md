### Use Case Example: Withdraw Pending Vacation Time Request

**Goal:**

To enable an employee to withdraw a pending vacation time request.

**Preconditions:**

- The employee is authenticated and authorized to use the Vacation Time System (VTS).

- The employee has a vacation time request that is currently pending approval.

**Main Flow:**

1- **_Access VTS:_**

The employee accesses the VTS home page through the intranet portal.

2- **_Review Requests:_**

The VTS displays a summary of the employee's vacation time requests, including:

- Outstanding balance for each time category
  Status of all active requests for the past 6 months and future 18 months

3- **_Select Request for Withdrawal:_**

- The employee selects a pending vacation time request.

4- **_Confirmation of Withdrawal:_**

- The system prompts the employee to confirm the withdrawal of the selected request.

**System Processing:**

_Confirmed Withdrawal:_

- The pending request is removed from the manager's approval queue.

- An email notification is sent to the manager informing them of the withdrawal.

- The request status is updated to "Withdrawn."

**Return to Home Page:**

- The system returns the employee to the VTS home page.

- The displayed summaries are updated to reflect the changes in the employee's vacation time balance and request status.

**Alternative Flows:**

- _Unauthorized Access:_ If the employee is not authenticated or authorized, access to the VTS is denied.

- _Request Not Found:_ If the selected request is not found or invalid, an error message is displayed.

- _System Error:_ If a system error occurs during the withdrawal process, an error message is displayed, and the user is notified.

**Postconditions:**

- The selected vacation time request is withdrawn.

- The employee's manager is notified of the withdrawal via email.

---

### State Diagram

![img](https://drive.google.com/uc?id=1X14bvKYikYVdNWG2WpiyWZOWoQtfs38R)

---

### Sequence Diagram
