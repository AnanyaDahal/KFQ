# KFQ - Teacher

## Module - Registration
### Test ID - Reg
### Precondition

### Test Data
- XSS Script = <script> var email = "ananya.dahal+kfq1@ing.edu.np"; alert('XSS'); </script>
### Test Case


| Test ID | Description/Scenario | Precondition | Test Step | Expected Result | Actual Result | Status |
|---------|----------------------|--------------|-----------|-----------------|---------------|--------|
| KFQ_L_001 | Login with valid credientials | User is registered | Enter valid email and password, click sign in |  User should successfully log in and redirected to dashboard | User logged in successfully and is redirected to dashboard | PASS | 
| KFQ_L_002 | Login with invalid password | User is registered |Enter valid email and wrong password, click sign in | Should display error message | Shows error message "Invalid email or password" | PASS |
| KFQ_L_003 | Login with invalid/unregistered email | No account exists | Enter invalid/unregistered email and correct password, click sign in | Should display error message | Shows error message "Invalid email or password" | PASS |
|KFQ_L_004 | Login with empty password field | no condition | Enter email, leave the password field empty, click sign in | sign in should be disable/ the field should show required so that ser understands | Sign in button cannot be accessed and "Required" is shown in the field | PASS |
|KFQ_L_005 | Login with empty email field | no condition | Enter password, leave email field empty, click sign in | Sign in should be disabled and required should be shown below the password field | Shows "required" under pasword field and "sign in" button is disabled | PASS |
| KFQ_L_006 | Invalid email address | None | Enter invalid email format (e.g., abc@, put space before email address, space after email address), Click Login | Error message like "Invalid email address" should be shown | Invalid email address message is shown below the input field | PASS |
|KFQ_L_007 | Password case sensitivity | User is registered | Enter correct email and password with wrong case in password field, click login | Login fails with error message | Login fails with error message "Invalid email or password | PASS | 
|KFQ_L_008 | Password Masked | None | Password enter in password field | Password is hidden/ masked | Password is hidden/ masked | PASS |
| KFQ_L_009 | Forget Password verification code | User is registered | Click "forget password " and type email | verification code sent to email | verification code is sent to email | PASS |
| KFQ_L_010 | Forget Password | User is registered | Click forget password, type email, verify code get redirected to reset password page | Redirect to forget password | gets redirected to forget password page | PASS |
| KFQ_L_011 | Forget Password Token | User is registered | click forget password, type email, verify code, redirect to reset password page, reset password after token is expired | Token expired message should be there | Shows Token expired message | PASS |
| KFQ_L_012 | Logout and re login | User logged in | Logut, Try login again | User logs in successfully | User successfully logs in | PASS |
| KFQ_L_013 | SQL Injection Attempt | none | Enter SQL injection in fields (eg:ananya.dahal+kfq1@ing.edu.np' OR '1' = ' 1 ) | Login should fail/ no security breach | Login Failed "Invalid email address" error message shown | PASS |
 | KFQ_L_013 | XSS attack in email input field | None | Enter script in input fields (eg: XSS Script ) | Input is sanitized, no script execution | Invalid email error message shown, Input sanitized, no script executed | PASS |

