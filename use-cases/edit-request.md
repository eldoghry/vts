### Use Case Example: Edit Pending Vacation Time Request

**Goal:**

To enable an employee to edit a pending vacation time request.

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
  Select Request for Editing:

- The employee selects a pending vacation time request.

3- **Edit Request Details:**

The VTS displays an editable view of the selected request, allowing the employee to modify:

- Request title
- Request description
- Start and end dates
- Time off type
- Submit Changes or Withdraw Request:

  - **_Submit Changes:_**
    - The employee makes the desired changes and submits them.
    - The system validates the changes and updates the pending request.
  - **_Withdraw Request:_**
    - The employee selects the "Withdraw Request" option.
    - The system prompts the employee to confirm the withdrawal.
    - If confirmed, the request is withdrawn and removed from the manager's approval queue.

**Return to Home Page:**

- The system returns the employee to the VTS home page.

- The displayed summaries are updated to reflect the changes in the employee's vacation time balance and request status.

**Alternative Flows:**

_Unauthorized Access:_

- If the employee is not authenticated or authorized, access to the VTS is denied.

_Request Not Found:_

- If the selected request is not found or invalid, an error message is displayed.

_Invalid Changes:_

- If the employee enters invalid information, the system displays error messages and highlights the invalid fields.

_System Error:_

- If a system error occurs during the editing process, an error message is displayed, and the user is notified.

**Postconditions:**

- The selected vacation time request is updated with the new information (if applicable).

- The request is either updated, withdrawn, or remains unchanged, depending on the employee's action.

- The employee's manager is notified of any changes to the request (if applicable).

---

### State Diagram

![img](https://drive.google.com/uc?id=1FNDZvzpyhVU-JfwZtah8fHce0oFDl7Ou)

---

### Sequence Diagram

![img](https://drive.google.com/uc?id=1V74FC55wIdYEOMDeifNWPDEo4tCKLqlV)

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

3. **SELECT REQUEST FOR EDITING:**
   Employee selects a request:
       IF request is not found OR invalid:
           Display "Request Not Found" error
           RETURN to previous screen
       ELSE:
           IF request status is "Pending":
               Proceed to editable view
           ELSE:
               Display error for invalid selection
               RETURN to previous screen

4. **EDIT REQUEST DETAILS:**
   Display editable fields for the selected request:
       - Request title
       - Request description
       - Start and end dates
       - Time off type

   Employee chooses one of the following actions:
       a. **Submit Changes:**
           - Employee modifies fields and submits changes
           - Validate changes:
               IF all fields are valid:
                   Update the request with new details
                   Notify employee's manager of changes
                   RETURN to home page with updated summaries
               ELSE:
                   Display error messages and highlight invalid fields
                   RETURN to edit screen

       b. **Withdraw Request:**
           - Employee selects "Withdraw Request" option
           - System prompts for confirmation
               IF employee confirms withdrawal:
                   Remove request from manager's approval queue
                   Notify employee's manager of withdrawal
                   RETURN to home page with updated summaries
               ELSE:
                   RETURN to edit screen without changes

5. **RETURN TO HOME PAGE:**
   Display updated summaries reflecting changes in:
       - Employee's vacation time balance
       - Request status
```
