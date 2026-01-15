# Exploratory Test Charter: Sign Up & Login

> **Feature**: User Authentication  
> **Status**: Ready for Testing  
> **Tester**: Marcelo
> **Date**: 16 Dec 2025
> **Session Start**: 13:50
> **Session End**: [e.g., 90 minutes]
> **Session Duration**: [e.g., 90 minutes]

---

## Charter Mission

**Explore** the sign up and login functionality  
**With** various user inputs and scenarios  
**To discover** bugs, usability issues, and edge cases in the authentication flow

---

## Areas to Explore

### 1. Sign Up Flow (NOT AVAILABLE ATM)

#### Happy Path

-   [ ] Navigate to sign up page
-   [ ] Enter valid email and password
-   [ ] Submit form successfully
-   [ ] Verify account created
-   [ ] Check email verification (if applicable)
-   [ ] Confirm redirect after signup

#### Input Validation

**Email Field:**

-   [ ] Empty email
-   [ ] Invalid email format (missing @, missing domain, etc.)
-   [ ] Email with special characters
-   [ ] Very long email (>100 characters)
-   [ ] Email with spaces
-   [ ] Duplicate email (already registered)
-   [ ] Case sensitivity (test@example.com vs TEST@example.com)

**Password Field:**

-   [ ] Empty password
-   [ ] Password too short (if minimum length exists)
-   [ ] Password too long (test limit)
-   [ ] Special characters in password
-   [ ] Unicode/emoji in password
-   [ ] Spaces in password
-   [ ] Password visibility toggle works

**Password Confirmation (if exists):**

-   [ ] Passwords don't match
-   [ ] Confirm password empty

#### UI/UX Checks

-   [ ] Error messages are clear and helpful
-   [ ] Required fields are marked
-   [ ] Tab order is logical
-   [ ] Enter key submits form
-   [ ] Loading states during submission
-   [ ] Form doesn't clear on error
-   [ ] Success message after signup
-   [ ] Links to login page work

#### Security Checks

-   [ ] Password is masked/hidden by default
-   [ ] Password strength indicator (if exists)
-   [ ] HTTPS connection (check URL)
-   [ ] No sensitive data in URL parameters
-   [ ] Session created securely

---

### 2. Login Flow

#### Happy Path

-   [ ] Navigate to login page
-   [ ] Enter valid email
-   [ ] Enter valid OTP
-   [ ] Redirect to Dashboard
-   [ ] User session persists after refresh

#### Input Validation

**Email/Username:**

-   [ ] Empty field 
-   [ ] Invalid format 
-   [ ] Non-existent email 
-   [ ] Case sensitivity

**OTP Code:**

-   [ ] Empty fiel
-   [ ] Wrong Code 
-   [ ] Partial Code (Enter a 6 digit code)
-   [ ] Login with already used code (The requested action could only be executed once.)


#### Authentication Scenarios

-   [ ] Login with newly created account
-   [ ] Login after logout
-   [ ] Login after session timeout
-   [ ] Multiple failed OTP code attempts (account locked)
-   [ ] Login after password reset (if exists)

#### UI/UX Checks

-   [ ] Error messages for wrong credentials
-   [ ] Generic error (don't reveal "email not found")
-   [ ] Loading state during authentication
-   [ ] Disable submit button during processing
-   [ ] Tab order is logical
-   [ ] Enter key submits form
-   [ ] Link to sign up page works
-   [ ] Link to password reset works (if exists)

---

### 3. Social Authentication (if applicable)

-   [ ] Google sign in button exists
-   [ ] Facebook sign in button exists
-   [ ] Apple sign in button exists
-   [ ] Social auth flow works correctly
-   [ ] Account linking for existing email
-   [ ] New account creation via social auth

---

### 4. Password Reset (if available)

-   [ ] Password reset link accessible
-   [ ] Enter email for reset
-   [ ] Email sent confirmation
-   [ ] Reset link works
-   [ ] Can set new password
-   [ ] Login with new password works
-   [ ] Old password no longer works

---

### 5. Session Management

-   [ ] User stays logged in after page refresh
-   [ ] User stays logged in after browser close (if "Remember Me")
-   [ ] User logged out after timeout (test duration)
-   [ ] Logout button/link works
-   [ ] After logout, can't access protected pages
-   [ ] Redirect to login when accessing protected route while logged out

---

### 6. Cross-Browser Testing

Test critical flows on:

-   [ ] Chrome (latest)
-   [ ] Firefox (latest)
-   [ ] Safari (latest)
-   [ ] Edge (if relevant)

---

### 7. Responsive/Mobile Testing

-   [ ] Sign up form usable on mobile (375px width)
-   [ ] Login form usable on mobile
-   [ ] Touch interactions work correctly
-   [ ] Keyboard appears appropriately
-   [ ] Form doesn't zoom on input focus (iOS)
-   [ ] Buttons are tap-friendly (min 44px)

---

## Test Data

### Valid Test Accounts

```
Email: [test+1@example.com]
Password: [TestPass123!]

Email: [test+2@example.com]
Password: [TestPass123!]
```

### Invalid Test Data

```
Invalid emails:
- plaintext
- @example.com
- user@
- user @example.com
- user..name@example.com

Invalid passwords:
- 123 (too short)
- [test minimum length]
```

---

## Bugs & Issues Found

### Bug #1: [Title]

**Severity**: [Critical/High/Medium/Low]  
**Steps to Reproduce**:

1. [Step 1]
2. [Step 2]
3. [Step 3]

**Expected**: [What should happen]  
**Actual**: [What actually happened]  
**Screenshot/Video**: [Link if available]  
**Browser**: [Chrome 120, etc.]  
**Device**: [Desktop/Mobile]

---

### Bug #2: [Title]

[Same format as above]

---

## Observations & Notes

### Positive Findings

-   [Things that work well]
-   [Good UX decisions]

### Areas for Improvement

-   [Non-critical issues]
-   [UX suggestions]

### Questions for Dev Team

-   [Unclear behavior]
-   [Intended vs. actual functionality]

---

## Coverage Summary

**Areas Covered**: [e.g., 85% - covered most scenarios]  
**Areas Not Covered**: [e.g., Didn't test social auth, no accounts available]  
**Confidence Level**: [High/Medium/Low]  
**Ready for Release?**: [Yes/No/With Conditions]

---

## Follow-Up Actions

-   [ ] File bugs in [tracking system]
-   [ ] Retest after bug fixes
-   [ ] Test integration with Leagues/Profile
-   [ ] Performance testing for login speed
-   [ ] Security review (if required)

---

## Session Notes

**Start Time**: [HH:MM]  
**End Time**: [HH:MM]  
**Interruptions**: [Any blockers or interruptions]  
**Test Environment**: [staging.xeito.app]  
**Build/Version**: [if available]
