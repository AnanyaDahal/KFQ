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

## Module - Discover
### Test Case 
| Test ID | Description/Scenario | Precondition | Test Step | Expected Result | Actual Result | Status |
|---------|----------------------|--------------|-----------|-----------------|---------------|--------|
| KFQ_D_001 | Verify Discover page loads successfully | User is logged in | Navigate to discover page | Page should loads without error and all sections should be visible | Page loads without error and all the sections are properly visible | PASS |
| KFQ_D_002 | Verify search bar functionality | User is on discover page | Enter keyword in search bar and press Enter | Relivant changes should be visible according to the query searched | Relivant changes are visible according to the keyword searched | PASS |
| KFQ_D_003 | Verify Filter functionality | User is on discover page | Select the subject and the grade from the filter section | Relivant changes according to the filter should be visible | Relivant changes are visible based on filter | PASS |
| KFQ_D_004 | Verify Reset functionality | User is on discovery page in filter section | Click the reset button once the filter is applied | The filter should be reset once reset button clicked | The filter is reset and the sifu arena is changed to default | PASS |
| KFQ_D_005 | Verify "Create Video Challenge" button | User is logged in | click the "Create Video challenge" button | The pop up for video challenge creation should be shown or the User should be redirected to video challenge creation page | The pop up for cideo challenge creation is shown | PASS |
| KFQ_D_006 | Verify "Create Quiz-only Challenge" button | User is logged in | click the "Create Quiz-only Challenge" button | The pop up for Create Quiz-only Challenge should be shown or the User should be redirected to Create Quiz-only Challenge page | The pop up for Create Quiz-only Challenge is shown | PASS |
| KFQ_D_007 | Verify "Create Flashcard" button | User is logged in | click the "Create Flashcard" button | The pop up for Create Flashcard should be shown or the user should be redirected to Create Flashcard page | The pop up for Create Flashcard is shown | PASS |
| KFQ_D_008 | Verify "Verify View Sifu Guide" button | User is logged in | click the "View Sifu Guide" button | The guide in the form of list or video should be shown |The video guide of the difu arena is shown in detail | PASS |
| KFQ_D_009 | Verify "Become The Defender of Education" button | User is logged in | click the "Become The Defender of Education" button | The pop up for "Become The Defender of Education" should be shown or the user should be redirected to Become The Defender of Education page | The user gets redirected to Become The Defender of Education page | PASS |
| KFQ_D_010 | Verify Top Sifu leaderboard display | User is on discovery page | Check who is the top sifu | The top sifu should be displayed also when clicked on sifu name redirect to sifu contents | The top sifu are displayed and when the sifu names are clicked user gets redirected to sifu contents | PASS |

