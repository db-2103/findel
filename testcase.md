To test the User Registration feature effectively, need to ensure that all form fields are validated correctly, error messages are displayed appropriately, and the registration process works as intended. Here's a comprehensive approach to building and executing test cases for this feature:
### **1. Test Scenario: Full Name**
**Objective:** Ensure the Full Name field accepts valid inputs and rejects invalid inputs.
- **Test Cases:**
  - **Valid Input:**  - Input: "Test Engineer"  - Expected Result: Field accepts the input and allows submission.
  - **Invalid Input:**  - Input: "12345"  - Expected Result: Error message "Invalid Full Name, Please enter valid Name" is displayed.
  - **No Input:**  - Input: "" - Expected Result: Error message "Full Name is required" is displayed.
### **2. Test Scenario: Email Address**
**Objective:** Ensure the Email Address field accepts unique and valid email formats.
- **Test Cases:**
  - **Valid Input:**  - Input: "test.engineer@yahoo.com"  - Expected Result: Field accepts the input, and submission proceeds.
  - **Duplicate Email:**  - Input: "test@yahoo.com" (already registered)  - Expected Result: Error message "Email Address is already in use" is displayed.
  - **Invalid Format:**  - Input: "test12@com"  - Expected Result: Error message "Invalid email format" is displayed.
  - **No Input:**   - Input: ""    -Expected Result: Error message "Email is required" is displayed.
### **3. Test Scenario: Password**
**Objective:** Ensure the Password field meets the specified criteria.
- **Test Cases:**
  - **Valid Password:**  - Input: "Passw0rd!"  - Expected Result: Field accepts the input and allows submission.
  - **Too Short Password:**  - Input: "P@ss12"  - Expected Result: Error message "Password must be at least 8 characters long" is displayed.
  - **Missing Number:**  - Input: "Password!"  - Expected Result: Error message "Password must contain at least one number" is displayed.
  - **Missing Special Character:**  - Input: "Password1"  - Expected Result: Error message "Password must contain at least one special character" is displayed.
  - **No Input:**   - Input: ""   -  Expected Result: Error message "Password is required" is displayed.
### **4. Test Scenario: Confirm Password**
**Objective:** Ensure the Confirm Password field matches the Password field.
- **Test Cases:**
  - **Matching Passwords:**  - Password: "Passw0rd!"  - Confirm Password: "Passw0rd!"  - Expected Result: Field accepts the input and allows submission.
  - **Non-Matching Passwords:**  - Password: "Passw0rd!"  - Confirm Password: "Passw0rd123"  - Expected Result: Error message "Passwords do not match" is displayed.
  - **No Input:** - Input: ""    - Expected result: Error message "confirm Password is required" is displayed.
### **5. Test Scenario: Phone Number**
**Objective:** Ensure the Phone Number field accepts valid formats.
- **Test Cases:**
  - **Valid Format:**  - Input: "+44-7432522631"  - Expected Result: Field accepts the input and allows submission.
  - **Invalid Format:**  - Input: "+1234567"  - Expected Result: Error message "Invalid phone number format" is displayed.
  - **No Input:**   -Input: ""   -Expected result : Field accepts the input as it's optional filed and allows submission.
### **6. Test Scenario: Date of Birth**
**Objective:** Ensure the Date of Birth field allows valid dates and complies with any age restrictions.
- **Test Cases:**
  - **Valid Date:**  - Input: "01/01/2000"  - Expected Result: Field accepts the input and allows submission.
  - **Invalid Date (future date):**  - Input: "01/01/2025"  - Expected Result: Error message "Date of Birth cannot be in the future" is displayed.
  - **No Input:**  - Input: "" (Do not select any date)   -Expected Result: Error message "Date of Birth is required, Please select valid date" is displayed.
### **7. Test Scenario: Accept Terms and Conditions**
**Objective:** Ensure the checkbox for accepting terms is required.
- **Test Cases:**
  - **Checked Box:**  - Expected Result: Field accepts the input and allows submission.
  - **Unchecked Box:**  - Expected Result: Error message "You must accept the Terms and Conditions" is displayed, and submission is blocked.
### **8. Test Case: Successful Registration With Mandatory and Optional fileds**
**Objective:** Ensure that the registration process completes successfully when all inputs for Mandatory and Optional fileds are valid.
- **Test Scenario:**
  - **Valid Inputs:**
  - Full Name: "Test Engineer"  
  - Email Address: "test.engineer@yahoo.com"
  - Password: "Passw0rd!"
  - Confirm Password: "Passw0rd!"
  - Phone Number: "+44-7452322851"
  - Date of Birth: "01/01/1990"
  - Accept Terms and Conditions: Checked
  - Expected Result: Registration is successful, and a confirmation email is sent.
### **9. Test Scenario: Successful Registration With only Mandatory fileds**
**Objective:** Ensure that the registration process completes successfully when all inputs for only Mandatory fileds are valid.
- **Test Cases:**
  - **Valid Inputs:**
  - Full Name: "Test Engineer"  
  - Email Address: "test.engineer@yahoo.com"
  - Password: "Passw0rd!"
  - Confirm Password: "Passw0rd!"
  - Phone Number: ""
  - Date of Birth: "01/01/1990"
  - Accept Terms and Conditions: Checked
  - Expected Result: Registration is successful, and a confirmation email is sent.
### **Approach to Testing**
1. **Create Test Data:** Generate both valid and invalid data for each field.
2. **Execute Tests:** Perform manual or automated testing using the test cases listed.
3. **Verify Responses:** Check for correct error messages and successful registration.
4. **Check Confirmation Email:** Ensure users receive the confirmation email after successful registration.
5. **Regression Testing:** After fixing any issues, re-run the tests to ensure no new issues are introduced.
This approach will help ensure that the user registration feature is robust, user-friendly, and secure.
