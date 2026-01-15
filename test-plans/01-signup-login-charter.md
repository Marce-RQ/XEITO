# Exploratory Test Charter: Sign Up & Login

> **Feature**: User Authentication  
> **Status**: Ready for Testing  
> **Tester**: Marcelo Romero
> **Date**: 16 Dec 2025
> **Environment**: Production
> **Session Start**: 13:50
> **Session End**: 15:15
> **Session Duration**: 1 hour 25 minutes

---

## Charter Mission

**Explore** the sign up and login functionality  
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
-   [ ] Enter valid credentials 
-   [ ] Submit form successfully
-   [ ] Redirect to appropriate page (dashboard, home, etc.)
-   [ ] User session persists after refresh

#### Input Validation

**Email/Username:**

-   [ ] Empty field (Error: Please fill in this field)
-   [ ] Invalid format (Error: …missing @)
-   [ ] Non-existent email (Error: No account found with this email)
-   [ ] Case sensitivity

**OTP Code:**

-   [ ] Empty Field (Error: Please fill in this field)
-   [ ] Wrong Code (Error: Please enter a valid confirmation code)
-   [ ] Partial Code (typo) (Error: Enter a 6 digit code)
-   [ ] Old (not used) Code
-   [ ] Old (used) Code
-   [ ] Resend Code


#### Authentication Scenarios

-   [ ] Login with newly created account
-   [ ] Login after logout
-   [ ] Login with locked account

#### UI/UX Checks

-   [ ] Error messages for wrong email
-   [ ] Error messages for wrong OTP
-   [ ] Loading state during authentication
-   [ ] Disable submit button during processing
-   [ ] Tab order is logical
-   [ ] Enter key submits form

---

### 3. Session Management

-   [ ] User stays logged in after page refresh
-   [ ] User stays logged in after browser close
-   [ ] User logged out after timeout (test duration)
-   [ ] Logout button/link works
-   [ ] After logout, can't access protected pages0

---

### 4. Cross-Browser Testing

Test critical flows on:

-   [ ] Chrome (latest)
-   [ ] Firefox (latest)
-   [ ] Safari (latest)
-   [ ] Edge (latest)

---

### 5. Responsive/Mobile Testing

-   [ ] Sign up form usable on mobile 
-   [ ] Login form usable on mobile
-   [ ] Touch interactions work correctly
-   [ ] Keyboard appears appropriately
-   [ ] Form doesn't zoom on input focus (iOS)
-   [ ] Buttons are tap-friendly

---