# Playwright MCP Prompts Library

> **Purpose**: Ready-to-use prompts for Playwright MCP to accelerate exploratory testing  
> **How to Use**: Copy these prompts and customize with actual test data/URLs

---

## Getting Started

### Initial Exploration

**Prompt: Discover App Structure**

```
Navigate to https://www.xeito.app/ and provide me with:
1. All navigation menu items and their links
2. All buttons visible on the homepage
3. The main sections/features advertised
4. Links to login and signup pages
Take screenshots of the homepage at desktop size (1920x1080).
```

**Prompt: Check Responsive Design**

```
Navigate to https://www.xeito.app/ and take screenshots at these viewport sizes:
- Mobile: 375x667 (iPhone SE)
- Tablet: 768x1024 (iPad)
- Desktop: 1920x1080

Tell me if any layout issues are visible.
```

---

## Sign Up & Login Testing

### Basic Login Testing

**Prompt: Test Valid Login**

```
Navigate to [LOGIN_URL].
Fill in the login form with:
- Email: [test@example.com]
- Password: [TestPassword123!]

Click the login button and tell me:
1. Did login succeed?
2. What page did it redirect to?
3. Is the user's name/email visible anywhere?
Take a screenshot of the result.
```

**Prompt: Test Invalid Login Scenarios**

```
Navigate to [LOGIN_URL] and test these login scenarios:

1. Empty email and password - click submit
2. Valid email, wrong password
3. Invalid email format (test@invalid), any password
4. Non-existent email, any password
5. Valid email, empty password

For each scenario:
- Fill the form
- Click submit
- Document the error message shown
- Take a screenshot

Provide a summary table of all error messages.
```

### Sign Up Testing

**Prompt: Test Valid Sign Up**

```
Navigate to [SIGNUP_URL].
Fill in the signup form with:
- Email: test+[random_number]@example.com (generate random number)
- Password: TestPassword123!
- [Other fields as needed]

Submit the form and tell me:
1. Did signup succeed?
2. What confirmation message appeared?
3. Where did it redirect?
4. Was an email verification required?
Take screenshots of each step.
```

**Prompt: Test Email Validation**

```
Navigate to [SIGNUP_URL] and test email field validation by submitting with these emails:
1. (empty)
2. plaintext
3. @example.com
4. user@
5. user @example.com
6. user..name@example.com
7. user@example (no TLD)

For each, document:
- Whether it was accepted or rejected
- The exact error message
- When the validation triggered (on blur, on submit, etc.)

Create a table summarizing the results.
```

**Prompt: Test Password Validation**

```
Navigate to [SIGNUP_URL] and test password validation with these passwords:
1. (empty)
2. 123 (too short)
3. abcdefgh (no numbers)
4. 12345678 (no letters)
5. TestPassword123! (should be valid)
6. [500 character string]

For each password:
- Enter it in the password field
- Try to submit the form
- Document if accepted/rejected and error message
- Note if there's a password strength indicator

Provide a summary of password requirements based on the results.
```

### Form Interaction Testing

**Prompt: Test Login Form UX**

```
Navigate to [LOGIN_URL] and analyze the form UX:

1. Click on each input field and tell me the placeholder text
2. Press Tab key through all fields - document the tab order
3. Check if Enter key submits the form
4. Check if there's a "show password" toggle
5. Look for links to "forgot password" and "sign up"
6. Try to submit with empty fields - does the browser show validation?

Take screenshots showing all interactive elements.
```

---

## Leagues Testing

### League Creation

**Prompt: Create a League**

```
Assume I'm logged in at [BASE_URL].
Navigate to the league creation page/section.

Create a new league with:
- Name: QA Test League [timestamp]
- [Other fields as needed - fill in based on discovery]

Document:
1. All fields in the creation form (names, types, required/optional)
2. Success message after creation
3. Where you are redirected
4. Take screenshots of the form and success state
```

**Prompt: Test League Name Validation**

```
Navigate to league creation page.

Test these league names:
1. (empty)
2. A (1 character)
3. [Generate 200 character string]
4. 🏆 League with Emoji 🎾
5. League'with"quotes
6. <script>alert('test')</script>

For each:
- Enter the name
- Try to save/create
- Document if accepted/rejected
- Note any error messages

Summarize validation rules discovered.
```

### League Management

**Prompt: List All Leagues**

```
Navigate to the leagues list/page.

Tell me:
1. How many leagues are displayed?
2. What information is shown for each league? (name, date, members, etc.)
3. Are there pagination controls?
4. Are there search or filter options?
5. What happens when you click on a league?

Take a screenshot of the league list.
```

**Prompt: View League Details**

```
Navigate to the leagues page and click on the first league.

Document:
1. All information displayed about the league
2. What actions are available? (edit, delete, invite, etc.)
3. Is there related data? (teams, matches, participants)
4. How do you navigate back to the list?

Take screenshots of the league detail view.
```

**Prompt: Edit a League**

```
Navigate to a league and access the edit functionality.

1. Change the league name to "Updated League [timestamp]"
2. Modify any other editable fields
3. Save the changes

Document:
1. What fields are editable?
2. Did changes save successfully?
3. Do changes reflect immediately in the UI?
4. What happens if you cancel instead of save?

Take screenshots before and after editing.
```

**Prompt: Delete a League**

```
Navigate to a test league and attempt to delete it.

Document:
1. Where is the delete button/option?
2. Is there a confirmation dialog?
3. What does the confirmation message say?
4. After deletion, where are you redirected?
5. Can you access the league by direct URL after deletion?

Take screenshots of the delete flow.
```

---

## Profile Testing

### Profile Viewing

**Prompt: View Profile**

```
Assuming I'm logged in, navigate to my profile page.

Document:
1. All fields/information displayed
2. Which fields appear to be editable?
3. Is there a profile picture/avatar?
4. What actions are available? (edit, change password, etc.)
5. How did you access the profile? (navigation menu, user dropdown, etc.)

Take a screenshot of the profile page.
```

### Profile Editing

**Prompt: Edit Profile**

```
Navigate to my profile and enter edit mode.

1. Change the display name to "QA Tester [timestamp]"
2. Update any other editable fields
3. Save the changes

Document:
1. What fields are editable?
2. Are there any validation messages?
3. Did changes save successfully?
4. Do changes reflect in the navigation bar or other parts of the app?

Take screenshots before and after editing.
```

**Prompt: Test Profile Field Validation**

```
Navigate to profile edit mode and test validation on each field:

For text fields (name, bio, etc.):
- Try leaving empty
- Try very long text (500+ characters)
- Try special characters

For email (if editable):
- Try invalid format
- Try duplicate email (if possible)

Document all validation rules discovered and error messages shown.
```

**Prompt: Upload Profile Picture**

```
Navigate to profile edit mode and test profile picture upload.

1. Look for an upload/change picture button
2. Document what file types are accepted
3. Try uploading a valid JPG image (if possible, use a test image URL)
4. Document what happens after upload

Note: This might require manual file selection. Document the UI and flow.
```

---

## Cross-Feature Integration

**Prompt: Test Profile in Leagues**

```
1. View your profile and note your display name and avatar
2. Navigate to leagues section
3. Check if your profile name/avatar appears in:
   - League creator information
   - League member lists
   - Any user references

Document where and how profile data is displayed throughout the app.
```

**Prompt: Test Authentication Session**

```
1. Login to the app at [LOGIN_URL]
2. Navigate through: homepage → leagues → profile → back to homepage
3. Refresh the page at each step
4. Check if you remain logged in

Then:
5. Logout
6. Try to access [PROTECTED_URL] directly
7. Document what happens (redirect to login?)

Take screenshots at key points.
```

---

## Error & Edge Case Testing

**Prompt: Test Network Error Handling**

```
Note: This might need browser DevTools simulation.

Navigate to [LOGIN_URL] and describe:
1. What happens if the page loads slowly (simulated slow 3G)?
2. Are there loading states/spinners?
3. Is there a timeout message?
4. Can the user retry?

Document the user experience during network issues.
```

**Prompt: Test Empty States**

```
Using a fresh test account (if possible):

1. Login
2. Navigate to leagues section (before creating any leagues)
3. Document the empty state:
   - What message is shown?
   - Is there a CTA to create the first league?
   - How does the UI look with no data?

Take a screenshot of the empty state.
```

**Prompt: Find All Links**

```
Navigate to [URL] and list all clickable links on the page:
1. Navigation links
2. Footer links
3. Buttons
4. Text links in content

For each link, tell me:
- Link text
- Where it points (href)
- Does it open in new tab or same tab?

Flag any broken links (404 errors).
```

---

## Accessibility Quick Checks

**Prompt: Check Basic Accessibility**

```
Navigate to [URL] and check:

1. Tab through all interactive elements - is the tab order logical?
2. Are there visible focus indicators?
3. List all images and tell me if they have alt text
4. List all form inputs and tell me if they have labels
5. Are buttons clearly labeled?
6. Is the color contrast sufficient (text vs background)?

Provide a summary of any accessibility concerns found.
```

---

## Data Extraction

**Prompt: Extract All Form Fields**

```
Navigate to [FORM_URL] and extract:
1. All input fields (name, type, required status, placeholder)
2. All dropdown/select fields and their options
3. All buttons and their text
4. Any validation messages visible by default

Create a table documenting all form elements.
```

**Prompt: Extract Navigation Structure**

```
Navigate to [BASE_URL] and document the entire navigation structure:
1. Main navigation menu items
2. User dropdown menu items (if logged in)
3. Footer links
4. Any secondary navigation

Create a hierarchical list of the site structure.
```

---

## Performance Checks

**Prompt: Measure Page Load Times**

```
Navigate to [URL] and measure:
1. Time to first contentful paint
2. Time to interactive
3. Total page load time
4. Number of network requests
5. Total page size

Run this 3 times and provide average results.
```

---

## Security Spot Checks

**Prompt: Check for XSS Vulnerabilities**

```
In form fields (profile name, league name, etc.), try entering:
1. <script>alert('XSS')</script>
2. <img src=x onerror=alert('XSS')>
3. javascript:alert('XSS')

Document:
- Is the input sanitized/escaped?
- Does it execute or is it displayed as plain text?
- How does the app handle these inputs?

IMPORTANT: This is for testing only. Document findings but don't exploit.
```

**Prompt: Check HTTPS Usage**

```
Navigate to [BASE_URL] and verify:
1. Is the connection HTTPS?
2. Is there a valid SSL certificate?
3. Do all resources load over HTTPS? (images, scripts, stylesheets)
4. Are there any mixed content warnings?

Document any security concerns.
```

---

## Tips for Using These Prompts

1. **Customize URLs**: Replace `[LOGIN_URL]`, `[SIGNUP_URL]`, etc. with actual URLs after discovery
2. **Add Test Data**: Fill in actual test credentials and data from your test accounts
3. **Iterate**: Start with basic prompts, then drill deeper based on findings
4. **Document**: Save Playwright MCP outputs as test evidence
5. **Combine**: Chain multiple prompts for complete user journey testing

---

## Next Steps

After using these prompts:

-   Document findings in test charters
-   File bugs discovered
-   Update prompts based on what you learn about the app
-   Create custom prompts for new features as they're developed
