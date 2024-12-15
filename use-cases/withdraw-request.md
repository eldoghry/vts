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

**_Confirmed Withdrawal:_**

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

![img](https://drive.google.com/uc?id=1s7jeMQJTbGTHdbVSLH6VuGuG5dK7tSvz)

---

### Pseudocode

```
1. **ACCESS VTS:**
   IF employee accesses VTS through intranet portal:
       IF employee is authenticated and authorized:
           Display VTS home page
       ELSE:
           Deny access with "Unauthorized Access" error
           EXIT

2. **REVIEW REQUESTS:**
   Display summary of:
       - Outstanding balance for each vacation time category
       - Status of all active requests for the past 6 months and future 18 months

3. **SELECT REQUEST FOR WITHDRAWAL:**
   Employee selects a request:
       IF request is not found OR invalid:
           Display "Request Not Found" error
           RETURN to previous screen
       ELSE:
           IF request status is "Pending":
               Proceed to withdrawal confirmation
           ELSE:
               Display error for invalid selection
               RETURN to previous screen

4. **CONFIRMATION OF WITHDRAWAL:**
   System prompts employee to confirm withdrawal:
       IF employee confirms withdrawal:
           - Remove request from manager's approval queue
           - Update request status to "Withdrawn"
           - Send email notification to employee's manager
           RETURN to VTS home page with updated summaries
       ELSE:
           RETURN to previous screen without changes

5. **RETURN TO HOME PAGE:**
   Display updated summaries reflecting changes in:
       - Employee's vacation time balance
       - Request status
```
