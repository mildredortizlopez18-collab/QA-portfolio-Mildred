## Login Test Cases - SauceDemo - https://www.saucedemo.com/

## Test Execution Summary
Total test cases: 8
Passed: 5
Fail: 3

# Test Cases

## TC01_Valid_login
Title: Login with valid credentials.

Preconditions: User is on login page.

Steps:
1. Enter valid username.
2. Enter valid password.
3. Click on login button.

Test Data:

*User: standard_user

*Password: secret_sauce

Expected Result: User is redirected to the products page.

Test Type: Positive.

Status: Pass.

Actual Results: User logged in successfully and inventory page displayed.


## TC02_Empty_fields_login
Title: Login with empty username and password.

Preconditions: User is on login page.

Steps:
1. Field username empty.
2. Field password empty.
3. Click login button.

Test Data: N/A

Expected Results:Error message displayed = "Epic sadface: Username and Password is required."

Test Type: Negative.

Status: Fail.

Actual Results: Error message displayed = "Epic sadface: Username is required."

## TC03_Empty_password_login
Title:Login with valid Username and empty password
Preconditions:User is on login page 
Steps:
1. Enter valid username
2. Field password empty
3. Click on login button
Test Data:
*User: standard_user
Expected Results: Error message displayed = "Epic sadface: Password is required"
Test Type: Negative
Status: Pass
Actual Results: Error message displayed = "Epic sadface: Password is required"

## TC04_Empty_username_login
Title:Login with empty username and valid password
Preconditions: User is on login page
Steps:
1. Field username empty
2. Enter valid password
3. Click on login button 
Test Data:
*Password: secret_sauce
Expected Results: Error message displayed = "Epic sadface: Username is required"
Test Type:Negative
Status: Pass
Actual Results:Error message displayed = "Epic sadface: Username is required"

## TC05_Locked_user_login
Title:Login with locked user
Preconditions: User is on login page
Steps:
1. Enter with locked user
2. Enter valid password
3. Click on login button
Test Data:
*Username: locked_out_user
*Password: secret_sauce
Expected Results: Error message displayed: "Epic sadface: Sorry, this user has been locked out."
Test Type: Negative
Status: Pass
Actual Results: Error message displayed: "Epic sadface: Sorry, this user has been locked out."

## TC06_Wrong_password
Title:Login with valid username and invalid password
Preconditions: User is on login page
Steps:
1. Enter valid username
2. Enter incorrect password
3. Click on login button 
Test Data:
*Username: standard_user
*Password: secretsauce
Expected Results: Error message displayed: "Epic sadface: Invalid password."
Test Type: Negative
Status: Fail
Actual Results: Error Message displayed: "Epic sadface: Username and password do not match any user in this service."

## TC07_Case_sensitivity
Title:Login with uppercase username and valid password
Preconditions: User is on login page
Steps:
1. Enter uppercase username
2. Enter valid password
3. Click on login button  
Test Data:
*Username: STANDARD_USER
*Password: secret_sauce
Expected Results: Error message displayed: "Epic sadface: Invalid username."
Test Type: Negative
Status: Fail
Actual Results: Error message displayed: "Epic sadface: Username and password do not match any user in this service."

## TC08_SQL_Injection
Title:Login with SQL injection input 
Preconditions: User is on login page
Steps:
1. Enter ' OR '1'='1 in username
2. Enter valid password
3. Click on login button  
Test Data:
*Password: secret_sauce
Expected Results: Login should fail
Test Type: Security
Status: Pass 
Actual Results: System rejected the input and displayed an error message.
