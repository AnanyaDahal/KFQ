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
| KFQ_D_011 | Verify leaderboard refresh timestamp | User is on discovery page | Referesh the discovery page, Check "Updated X minutes ago" text | Timestamp is visible and updates periodically | Time stamp is visible and updates periodically after refresh | PASS |
| KFQ_D_012 | Verify challenge cards display | User is on discovery page | Scroll to "From Kung Fu Quiz Team" section, select the video check if the video is working properly or not | Challenge cards should be displayed with title, duration and metadata, when click on the card it should redirect to either the video section, quiz section of the respective challenge | Challenge cards are displayed with title, duration, and metadata, when click on the card it redirects to the video section or the quiz section of the respective challenge | PASS |
| KFQ_D_013 | Verify view all button | User is on discovery page in From Kung Fu Quiz Team section | Click on the view all button | All the challenges should be shown in a scroll view or user should be redirected to the different page | When user clicks user is redirected to different page where all the challenges are shown | PASS |
| KFQ_D_014 | Verify Top challenges section | User is in discovery page | Scroll to the top challenges section | The top challenges should be there and when clicked on the challenges it should navigate to respective challenge page | Top challenges across all challenges are shown and when clicked on the challenge it navigates to respective challenge page | PASS |
| KFQ_D_015 | Verefy Around the Kung Fu Arena section | User is in discovery page | Scroll to the Around the Kung Fu Arena section | The Around the Kung Fu Arena should be there and when clicked on the challenges it should navigate to respective challenge page | The Around the Kung Fu Arena across all challenges are shown and when clicked on the challenge it navigates to respective challenge page | PASS |
| KFQ_D_016 | Verify Around the Kung Fu Arena, video challenge button | User is on discovery page in Around the Kung Fu Arena section | Scroll to the Around the Kung Fu Arena section, video challenge button | When click on video challenge button only video challenges should be filtered | When user clicks on video challenge button, all the video challenges are filtered and shown | PASS |
| KFQ_D_017 | Verify Around the Kung Fu Arena, quiz challenge button | User is on discovery page in Around the Kung Fu Arena section | Scroll to the Around the Kung Fu Arena section, quiz challenge button | When click on quiz challenge button only quiz challenges should be filtered | When user clicks on quiz challenge button, all the quiz challenges are filtered and shown | PASS | 
| KFQ_D_018 | Verify Around the Kung Fu Arena, flashcard button | User is on discovery page in Around the Kung Fu Arena section | Scroll to the Around the Kung Fu Arena section, flashcard button | When click on flashcard button only flashcard should be filtered | When user clicks on flashcard button, all the flashcard are filtered and shown | PASS |



## Module - Challenges


### Test Case 


| Test ID | Description/Scenario | Precondition | Test Step | Expected Result | Actual Result | Status |
|---------|----------------------|--------------|-----------|-----------------|---------------|--------|
| KFQ_C_001 | Verify Challenges page loads | User is logged in | Navigate to challenges page | Page should load with header and how many challenges are there | Page loads with header "challenges" and the number of challenges there | PASS |
| KFQ_C_002 | Verify Create New Challenge card | User is in challenge page | click create new challenge button | The Create New challenge card should pop up from where user should be able to add more challenges | When user clicks create new challenge, card pops up from where user can add more challenges of their choice (video, quiz, flashcard) | PASS |
| KFQ_C_003 |  Verefy challenge mode dropdown | Create challenge popup is open | click challenge mode dropdown | should display options (quiz-only, dlashcard) | All the challenge types are visible in dropdown | PASS |
| KFQ_C_004 | Verify challenge creation with required field in video challenges | Pop up is open | Enter title, URL and click  "Create Challenge" | Challenge should be created successfully and notification should be shown | Challenge is crreated successfully and notification saying challenge successfully created is shown | PASS |
| KFQ_C_005 | Verify challenge creation with empty fields | Pop up is open | Without filling the fields click create challenge | Error message should pop up or the fields that needs to be filled should show required option | Required message is shown below the input field | PASS |
| KFQ_C_006 | Verify urls format | Pop up is open | Enter other urls except the youtube video url | Error message or invalid url pop up should be shown | Error message saying invalid url format is shown | PASS |
| KFQ_C_007 | Verify cancle button in pop up | Pop up is open | Click "Cancle" | popup should close without saving | popup closes and no challenge is created | PASS |
| KFQ_C_008 | Verify clicking on existing challenge | challenge exists | click on a challenge card | user should be redirected to challenge detail page | user gets redirected properly | PASS |
| KFQ_C_009 | Verify challenge details page | user is on challenge detail page | observe details | should show subject, grade, date, status | all details are displayed correctly | PASS |
| KFQ_C_010 | verify challenge status (Draft/ Published) | Challenge exists | open challenge | status should be visible | Status (Draft/ Publish) is shown correctly | PASS |
| KFQ_C_011 | Verify preview quiz option | Challenge detail page | Click preview quiz | Quiz preview should open | Quiz preview loads successfully | PASS |
| KFQ_C_012 | Verify edit challenge | Challenge detail page | Click edit | Should allow editing | User can edit and save changes | PASS |
| KFQ_C_013 | Verify customize quiz | Challenge detail page | Click customize quiz | Customization options should appear | Customization works correctly | PASS |
| KFQ_C_014 | Verify present challenge | challenge detail page | click present mode | should redirect to presentation mode | Redirects correctly to presentation mode | PASS |
| KFQ_C_015 | Verify Video Challenges filter | User is on challenges page | Click "Video Challenges" | Only video challenges should be displayed | Only video challenges are shown | PASS |
| KFQ_C_016 | Verify Quiz Challenges filter | User is on challenges page | Click "Quiz Challenges" | Only quiz challenges should be displayed | Only quiz challenges are shown | PASS |
| KFQ_C_017 | Verify Flashcards filter | User is on challenges page | Click "Flashcards" |Only flashcard challenges should be displayed | Only flashcards are shown | PASS |
| KFQ_C_018 | Verify Add Video Challenge | Video filter is active | Click "Add Video Challenge" | Popup should open | Popup opens for video challenge | PASS |
| KFQ_C_019 | Verify Add Quiz Challenge | Quiz filter is active | Click "Add Quiz Challenge" | Popup should open | Popup opens for quiz challenge | PASS |
| KFQ_C_020 | Verify Add Flashcard Challenge | Flashcard filter is active | Click "Add Flashcard Challenge" | Popup should open | Popup opens for flashcard challenge | PASS |
| KFQ_C_021 | Verify challenge count update | User creates/deletes challenge | Perform create/delete action | Challenge count should update correctly | Count updates correctly | PASS |
| KFQ_C_022 | Verify empty state | No challenges exist | Navigate to challenges page | Should show empty state or prompt to create | Empty state displayed correctly | PASS |







## Module - Dojos



### Test Case 
 

| Test ID | Description/Scenario | Precondition | Test Step | Expected Result | Actual Result | Status |
|---------|----------------------|--------------|-----------|-----------------|---------------|--------|
| KFQ_DJ_001 | Verify Dojos page loads | User is logged in | Navigate to Dojo page | Page loads with total number of dojos created by user | Page loads successfully with correct dojo count in header | PASS |
| KFQ_DJ_002 | Verify Create New Dojo button popup | On Dojo Page | Click "Create New Dojo" button | Create Dojo popup should be displayed | Popup opens successfully | PASS |
| KFQ_DJ_003 | Verify dojo list display | Dojos exist | View left panel | All dojos listed with name & category | All dojo list items are displayed | PASS |
| KFQ_DJ_004 | Verify dojo selection | Dojos exist | Click a dojo | Selected dojo highlighted and details shown on right panel | User is redirected to dojo details view | PASS |
| KFQ_DJ_005 | Verify dojo details panel | Dojo selected | View right panel | Title, date, status, ID, and stats are displayed correctly | The title, date, status, ID are displayed properly and correctly in details page | PASS |
| KFQ_DJ_006 | Verify search functionality (valid input) | Dojos exist | Enter valid keyword in search | Matching dojos should be displayed | When the valid keyword is given dojos related to that keyword are present | PASS |
| KFQ_DJ_007 | Verify default dojo selection | Multiple dojos exist | Open Dojos page | First or last selected dojo is displayed by default | The previous dojo that was selected is displayed | PASS |
| KFQ_DJ_008 | Verify dojo list according to filter (Active/Inactive, game dojo/assesment dojo/feedback dojo) | Dojos exist with Active & Inactive status | Select "Active" or "Inactive" filter | Dojo list count should update based on selected status filter | Dojo list count does not update according to Active/Inactive filter | FAIL |
| KFQ_DJ_009 | Verify dojo list count according to challenge type filters | Dojos exist with different challenge types (Video, Quiz) | Select "Video Challenges" or "Quiz Challenges" filter | Dojo list count updates based on selected challenge type | Dojo list count updates correctly according to Video/Quiz filters | PASS |
| KFQ_DJ_010 | Verify create dojo functionality | User is logged in | Create a new dojo with valid details | New dojo is added to list and displayed | After new dojo created it is added on the list and is displayed | PASS |
| KFQ_DJ_011 | Verify newly created dojo | New dojo created | Create a dojo | redirect to particular dojo section where all the dojos related to that challenge are displayed | User gets redirected to particular challenge section where all the dojos related to that challenge are there | PASS |
| KFQ_DJ_012 | Verify Active filter functionality | Dojos with mixed status exist | Select "Active" filter | Only active dojos should be displayed | Active and inactive dojos are displayed (BUG) | FAIL |
| KFQ_DJ_013 | Verify Inactive filter functionality | Dojos with mixed status exist | Select "Inactive" filter | Only inactive dojos should be displayed | Dojos that are inactive are displayed | PASS |
| KFQ_DJ_014 | Verify All Status filter | Dojos with mixed status exist | Select "All Status" | All dojos are displayed | All dojos regardless of status are displayed | PASS |
| KFQ_DJ_015 | Verify search functionality (no result) | Dojos exist | Enter invalid keyword | No results / empty state shown | No dojo exists error message is displayed | PASS |
| KFQ_DJ_016 | Verify empty dojo state | No dojos exist | Navigate to Dojos page | Empty state message is displayed | No dojo exits create new dojo message is displayed in case of the empty dojo | PASS |



## Module - Profile



### Test Case 


| Test ID | Description/Scenario | Precondition | Test Step | Expected Result | Actual Result | Status |
|---------|----------------------|--------------|-----------|-----------------|---------------|--------|
| KFQ_PR_001 | Verify Profile page loads successfully | User is logged in | Navigate to Profile page | Profile page should load with all tabs visible | Profile page loads successfully with all sections visible | PASS |
| KFQ_PR_002 | Verify Account Information tab | User is on Profile page | Click "Account Information" tab | User account details should be displayed | Account details displayed correctly | PASS |
| KFQ_PR_003 | Verify user profile information display | User account exists | View Full Name and Email fields | Correct user information should be displayed | Correct user information displayed | PASS |
| KFQ_PR_004 | Verify Update Avatar button functionality | User is on Account Information tab | Click "Update Avatar" and upload image | Avatar should update successfully | Avatar updated successfully | PASS |
| KFQ_PR_005 | Verify Remove Avatar functionality | User has uploaded avatar | Click "Remove Avatar" | Avatar should be removed and default avatar shown | Avatar removed successfully | PASS |
| KFQ_PR_006 | Verify Save Changes button | User updates profile details | Modify profile information and click "Save Changes" | Updated profile information should be saved | Profile changes saved successfully | PASS |
| KFQ_PR_007 | Verify Change Password tab navigation | User is on Profile page | Click "Change Password" tab | Change Password section should open | Change Password section opens successfully | PASS |
| KFQ_PR_008 | Verify password change with valid credentials | User knows current password | Enter valid old password, new password, confirm password and submit | Password should update successfully | Password updated successfully | PASS |
| KFQ_PR_009 | Verify password validation requirements | User is on Change Password tab | Enter weak password | Validation message should appear according to password rules | The change password button doesnt enable unless the user keeps strong password | PASS |
| KFQ_PR_010 | Verify confirm password mismatch validation | User is changing password | Enter different New Password and Confirm Password | User should receive mismatch validation error | The change password button doesnt enable unless password match | PASS |
| KFQ_PR_011 | Verify Preferences tab loads | User is on Profile page | Click "Preferences" tab | Preferences section should load successfully | Preferences section loaded correctly | PASS |
| KFQ_PR_012 | Verify subject preference selection | User is on Preferences tab | Select or deselect subjects | Selected preferences should be highlighted and saved | Subject preferences updated correctly | PASS |
| KFQ_PR_013 | Verify grade preference selection | User is on Preferences tab | Select or deselect grades | Selected grade preferences should be updated | Grade preferences updated correctly | PASS |
| KFQ_PR_014 | Verify Update Preferences button | Preferences modified | Click "Update Preferences" | Preferences should save successfully | Preferences updated successfully | PASS |
| KFQ_PR_015 | Verify Discover page recommendations update based on preferences | User has updated preferences | Update subjects/grades, Navigate to Discover page | Recommended videos around Kung Fu Arena should change according to preferences | Recommended videos updated according to selected preferences | PASS |
| KFQ_PR_016 | Verify search functionality in Preferences | User is on Preferences tab | Search for subject or grade | Matching subjects/grades should be displayed | Search functionality works correctly | PASS |
| KFQ_PR_017 | Verify Subscription tab loads | User is on Profile page | Click "Subscription" tab | Subscription plans and features should be displayed | Subscription section loads correctly | PASS |
| KFQ_PR_018 | Verify Unlock All Features popup | User is on Subscription tab | Click "Unlock All Features" | Payment popup/modal should appear | Payment popup displayed successfully | PASS |
| KFQ_PR_019 | Verify payment method selection | Payment popup is open | Select PayPal or Stripe | Selected payment method should be highlighted and redirect to the selected payment method | Payment method selection works correctly and upon clicking continue user is redirected to the payment page | PASS |
| KFQ_PR_020 | Verify Continue button activation after payment selection | Payment popup is open | Select payment method | Continue button should become enabled | Continue button enabled correctly | PASS |
| KFQ_PR_021 | Verify Cancel button in payment popup | Payment popup is open | Click "Cancel" | Popup should close without payment process | Popup closed successfully | PASS |
| KFQ_PR_022 | Verify popup close icon functionality | Payment popup is open | Click close (X) icon | Popup should close successfully | Popup closed successfully | PASS |
| KFQ_PR_023 | Verify current subscription plan display | User has active/current plan | Open Subscription tab | Current plan should be correctly highlighted | Current plan displayed correctly | PASS |
| KFQ_PR_024 | Verify Google account linking button | User is on Account Information tab | Click "Link with Google" button | User should be redirected to Google account linking flow | No action occurs when clicking the button | FAIL |




## Module - Navigation Sidebar


### Test Case 

| Test ID | Description/Scenario | Precondition | Test Step | Expected Result | Actual Result | Status |
|---------|----------------------|--------------|-----------|-----------------|---------------|--------|
| KFQ_NAV_001 | Verify sidebar visibility | User is logged in | Open application dashboard | Sidebar navigation should be visible on the left side | Sidebar displayed correctly | PASS |
| KFQ_NAV_002 | Verify Discover navigation | User is logged in | Click "Discover" icon/tab | User should be redirected to Discover page | Discover page opens successfully | PASS |
| KFQ_NAV_003 | Verify Challenges navigation | User is logged in | Click "Challenges" icon/tab | User should be redirected to Challenges page | Challenges page opens successfully | PASS |
| KFQ_NAV_004 | Verify Dojos navigation | User is logged in | Click "Dojos" icon/tab | User should be redirected to Dojos page | Dojos page opens successfully | PASS |
| KFQ_NAV_005 | Verify Profile navigation | User is logged in | Click "Profile" icon/tab | User should be redirected to Profile page | Profile page opens successfully | PASS |
| KFQ_NAV_006 | Verify Host Live navigation | User is logged in | Click "Host Live" option | User should be redirected to Host Live section or the challenge page of those that can be hosted live | user gets redirected to the challenge section that can be hosted live successfully | PASS |
| KFQ_NAV_007 | Verify Upgrade Now navigation | User is logged in | Click "Upgrade Now" option | User should be redirected to Subscription/Upgrade section or a pop up should be there so that they can redirect to subscription section in profile | A pop up opens so that they can redirect to subscription section in profile | PASS |
| KFQ_NAV_008 | Verify active page highlight in sidebar | User navigates between pages | Open different sections from sidebar | Current active page should be highlighted | Active section highlighted correctly | PASS |
| KFQ_NAV_009 | Verify sidebar icons visibility | User is logged in | View sidebar | All sidebar icons should load correctly | All icons displayed correctly | PASS |
| KFQ_NAV_010 | Verify sidebar labels visibility | User is logged in | View sidebar | All navigation labels should be readable and aligned | Labels displayed correctly | PASS |
| KFQ_NAV_011 | Verify navigation state persistence | User navigates to another page | Refresh browser on selected page | Active navigation state should remain selected | Navigation state preserved correctly | PASS |
| KFQ_NAV_012 | Verify tooltip or hover effect on sidebar items | User hovers over sidebar items | Hover over navigation options | Hover effect/tooltip should appear correctly | Hover effects displayed properly | PASS |



