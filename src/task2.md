# Scenario
You are testing the login functionality of a web application. The login page contains:
- Username field
- Password field  
- Login button
- An error message displayed for invalid login attempts
- A "Remember Me" checkbox
- A "Forgot Password" link

# Task
Write 5-10 test cases for the login functionality, covering both positive and negative scenarios.

Use the following template for each test case:

## Test Case Template
- **Test Case ID:** A unique identifier for the test case
- **Title:** A brief description of the test case
- **Pre-conditions:** Any setup required before running the test
- **Test Steps:** Step-by-step instructions to execute the test
- **Expected Result:** The expected outcome for the test
- **Actual Result:** Leave this blank (to be filled during actual execution)
- **Priority:** Assign a priority (High/Medium/Low)
- **Remarks:** Any additional comments

# Solution
TODO: Your solution goes below
<!-- <Write your solution here> -->

<!-- 
### Test Case 1 

- **Test Case ID:** test-case-1
- **Title:** Verify that the login page is displayed correctly
- **Pre-conditions:** The user is on the login page
- **Test Steps:** 
  - 1. Open the login page
  - 2. Verify that the username field is displayed
  - 3. Verify that the password field is displayed
  - 4. Verify that the login button is displayed
  - 5. Verify that the "Remember Me" checkbox is displayed
  - 6. Verify that the "Forgot Password" link is displayed
- **Expected Result:** All elements are displayed correctly
- **Actual Result:** All elements are displayed as expected
- **Priority:** High
- **Remarks:** This is a critical test case that verifies the basic UI functionality of the login page
-->


Test Case 1 -->

- **Test Case ID:** test-case-1
- **Title:** Verify that the login page has all the fields required
- **Pre-conditions:** The user is on the login page
- **Test Steps:** 
  - 1. Open the login page
  - 2. Verify that the username field is displayed
  - 3. Verify that the password field is displayed
  - 4. Verify that the login button is displayed
  - 5. Verify that the "Remember Me" checkbox is displayed
  - 6. Verify that the "Forgot Password" link is displayed
- **Expected Result:** All elements are displayed correctly
- **Actual Result:** All elements are displayed as expected
- **Priority:** High
- **Remarks:** This is a critical test case that verifies the basic UI functionality of the login page

Test Case 2-->

- **Test Case ID:** test-case-2
- **Title:** Enter valid detais in login page and validate if logged in
- **Pre-conditions:** The user is on the login page
- **Test Steps:** 
  - 1. Open the login page
  - 2. Enter valid user name
  - 3. Enter valid password
  - 4. Click login button
  - 5. Verify user is navigated to home page
- **Expected Result:** User should be navigated to home page
- **Actual Result:** User is navigated to home page
- **Priority:** High
- **Remarks:** This is important test case to validate the login is working fine or not.

  Test Case 3-->

- **Test Case ID:** test-case-3
- **Title:** Validate working of "Remember Me" checkbox
- **Pre-conditions:** The user is on the login page
- **Test Steps:** 
  - 1. Open the login page
    2. Enter valid user name and password
    3. Click "Remember Me" checkbox
    4. Click login
    5. Logout
    6. Close the browser and reopen the login page
    7. Click on user name
    8. Verify if the auto suggestion comes for username and password
- **Expected Result:** Auto suggestion should come for the username and password
- **Actual Result:** Auto suggestions comes when we click on username and password
- **Priority:** Medium
- **Remarks:** This test case is of medium priority as it verifies if "Remember Me" checkbox works as expected.


Test Case 4-->

- **Test Case ID:** test-case-4
- **Title:** Validate working of "Forgot Password" link
- **Pre-conditions:** The user is on the login page
- **Test Steps:** 
  - 1. Open the login page
    2. Click "Forgot Password" link
    3. Verify if user is navigated to the page where it ask for username or email
- **Expected Result:** User should be navigated to "Forgot Password" page
- **Actual Result:** User is navigated to "Forgot Password" page
- **Priority:** High
- **Remarks:** This test case is important because it helps user recover password if they dont remember.

- Test Case 5-->

- **Test Case ID:** test-case-5
- **Title:** Invalid user name and valid password
- **Pre-conditions:** The user is on the login page
- **Test Steps:** 
  - 1. Open the login page
    2. Enter invalid user name
    3. Enter valid password
    4. Click login button
    5.Verify if validation message is thrown for invalid username
- **Expected Result:** Validation message should be thrown for invalid username
- **Actual Result:** Validation message is thrown for invalid username
- **Priority:** High
- **Remarks:** This test case is important because it ensures no unauthorised access to system.

  - Test Case 6-->

- **Test Case ID:** test-case-6
- **Title:** Valid user name and invalid password
- **Pre-conditions:** The user is on the login page
- **Test Steps:** 
  - 1. Open the login page
    2. Enter valid user name
    3. Enter invalid password
    4. Click login button
    5.Verify if validation message is thrown for invalid password
- **Expected Result:** Validation message should be thrown for invalid password
- **Actual Result:** Validation message is thrown for invalid password
- **Priority:** High
- **Remarks:** This test case is important because it ensures no unauthorised access to system.

-   - Test Case 7-->

- **Test Case ID:** test-case-7
- **Title:** Invalid user name and invalid password
- **Pre-conditions:** The user is on the login page
- **Test Steps:** 
  - 1. Open the login page
    2. Enter invalid user name
    3. Enter invalid password
    4. Click login button
    5.Verify if validation message is thrown for invalid username and invalid password
- **Expected Result:** Validation message should be thrown for invalid username and invalid password
- **Actual Result:** Validation message is thrown for invalid username and invalid password
- **Priority:** High
- **Remarks:** This test case is important because it ensures no unauthorised access to system.

- - Test Case 8-->

- **Test Case ID:** test-case-8
- **Title:** Blank user name and valid password
- **Pre-conditions:** The user is on the login page
- **Test Steps:** 
  - 1. Open the login page
    2. Do not enter user name
    3. Enter valid password
    4. Click login button
    5.Verify if validation message is thrown for blank username
- **Expected Result:** Validation message should be thrown for blank username
- **Actual Result:** Validation message is thrown for blank username
- **Priority:** Medium
- **Remarks:** This test case is of medium importance because someone would enter something if they see text field.

- - Test Case 9-->

- **Test Case ID:** test-case-9
- **Title:** Valid user name and blank password
- **Pre-conditions:** The user is on the login page
- **Test Steps:** 
  - 1. Open the login page
    2. Enter valid user name
    3. Do not enter password
    4. Click login button
    5.Verify if validation message is thrown for blank password
- **Expected Result:** Validation message should be thrown for blank password
- **Actual Result:** Validation message is thrown for blank password
- **Priority:** Medium
- **Remarks:** This test case is of medium importance because someone would enter something if they see text field.

- - - Test Case 10-->

- **Test Case ID:** test-case-10
- **Title:** Blank user name and blank password
- **Pre-conditions:** The user is on the login page
- **Test Steps:** 
  - 1. Open the login page
    2. Do not enter user name
    3. Do not enter password
    4. Click login button
    5.Verify if validation message is thrown for blank username and blank password
- **Expected Result:** Validation message should be thrown for blank username and blank password
- **Actual Result:** Validation message is thrown for blank username and blank password
- **Priority:** Medium
- **Remarks:** This test case is of medium importance because someone would enter something if they see text field.


