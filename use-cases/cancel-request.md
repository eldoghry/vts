### Use Case Example: Cancel Request

**Goal:**

To enable an employee to cancel an approved vacation time request.

**Preconditions:**

- The employee is authenticated and authorized to use the Vacation Time System (VTS).
- The employee has a vacation time request that has been approved.
- The approved request is either scheduled for a future date or within the past 5 business days.

**Main Flow:**

1- _Access VTS:_

The employee accesses the VTS home page through the intranet portal.

2- _Review Requests:_

The VTS displays a summary of the employee's vacation time requests, including:

- Outstanding balance for each time category

- Status of all active requests for the past 6 months and future 18 months

3- _Select Request for Cancellation:_

The employee selects an approved request that is either future-dated or within the past 5 business days.

4- _Confirmation and Explanation:_

- **_Future-Dated Request:_**

  - The system prompts the employee to confirm the cancellation.

- **_Past-Dated Request:_** The system prompts the employee to:
  - Confirm the cancellation.
  - Provide a brief explanation for the cancellation.

**System Processing:**

**_Confirmed Cancellation:_**

- An email notification is sent to the employee's manager.
  The request status is updated to "Canceled."

- The time allowances used for the request are returned to the employee's balance.

**Canceled Cancellation:**

- The system returns to the previous screen without making any changes to the request.

**Return to Home Page:**

- The system returns the employee to the VTS home page.
- The displayed summaries are updated to reflect the changes in the employee's vacation time balance and request status.

**Alternative Flows:**

- _Unauthorized Access:_ If the employee is not authenticated or authorized, access to the VTS is denied.

- _Request Not Found:_ If the selected request is not found or invalid, an error message is displayed.

- _System Error:_ If a system error occurs during the cancellation process, an error message is displayed, and the user is notified.

**Postconditions:**

- The selected vacation time request is canceled.

- The employee's vacation time balance is updated to reflect the cancellation.

- The employee's manager is notified of the cancellation via email.

---

### State Diagram

![img](https://drive.google.com/uc?id=16dvbpRnRbgb8c080ChUZkHEWO0PmBH3S)

---

### Sequence Diagram

---

submit
https://drive.google.com/file/d/1sBTc6v7n3V_qbyZ3dUd1nHE2tv5HeSTb/view?usp=sharing
