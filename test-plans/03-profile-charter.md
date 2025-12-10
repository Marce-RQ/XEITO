# Exploratory Test Charter: Profile

> **Feature**: User Profile Management  
> **Status**: Ready for Testing  
> **Tester**: [Your Name]  
> **Date**: [Test Date]  
> **Session Duration**: [e.g., 60 minutes]

---

## Charter Mission

**Explore** the user profile viewing and editing functionality  
**With** various data inputs and user interactions  
**To discover** bugs, usability issues, and edge cases in profile management

---

## Prerequisites

-   [ ] Logged in user account
-   [ ] Understanding of what profile data is collected
-   [ ] Access to test environment

---

## Areas to Explore

### 1. Profile View

#### Display

-   [ ] Navigate to profile page
-   [ ] All profile fields display correctly
-   [ ] User's own data shown
-   [ ] Profile picture/avatar displays (if exists)
-   [ ] Empty fields handled gracefully
-   [ ] Loading states work correctly

#### Navigation

-   [ ] Can access profile from main navigation
-   [ ] Can access profile from user menu
-   [ ] Direct URL access works
-   [ ] Back navigation works

---

### 2. Profile Editing

#### Happy Path

-   [ ] Edit button/mode accessible
-   [ ] Modify profile information
-   [ ] Save changes successfully
-   [ ] Changes persist after refresh
-   [ ] Success message shown
-   [ ] Return to view mode

#### Editable Fields (document what exists)

**Name/Display Name:**

-   [ ] Empty name
-   [ ] Very short name (1 character)
-   [ ] Very long name (>100 characters)
-   [ ] Special characters
-   [ ] Unicode/emoji
-   [ ] Leading/trailing spaces

**Email:**

-   [ ] Can email be changed?
-   [ ] Invalid email format
-   [ ] Duplicate email (another user)
-   [ ] Email verification required after change?

**Phone Number** (if exists):

-   [ ] Empty phone
-   [ ] Invalid format
-   [ ] International formats
-   [ ] Too many/too few digits

**Bio/Description** (if exists):

-   [ ] Empty bio
-   [ ] Very long bio (test character limit)
-   [ ] Special characters
-   [ ] Line breaks/formatting
-   [ ] HTML/script injection attempts

**Location/Address** (if exists):

-   [ ] Free text or dropdown?
-   [ ] Validation rules
-   [ ] International addresses

**Date of Birth** (if exists):

-   [ ] Date picker works
-   [ ] Invalid dates (Feb 30, etc.)
-   [ ] Future dates
-   [ ] Very old dates
-   [ ] Age validation (minimum age?)

**[Other Fields]:**

-   [ ] [Document and test each field]

---

### 3. Profile Picture/Avatar

#### Upload

-   [ ] Upload button exists
-   [ ] Can select image file
-   [ ] Upload succeeds with valid image
-   [ ] Loading state during upload
-   [ ] Preview before save
-   [ ] Image displays after upload

#### File Validation

-   [ ] Valid formats accepted (JPG, PNG, etc.)
-   [ ] Invalid formats rejected (PDF, DOC, etc.)
-   [ ] File size limit enforced
-   [ ] Very large file (>10MB)
-   [ ] Very small file (<1KB)
-   [ ] Corrupted file
-   [ ] Non-square image (aspect ratio)

#### Image Management

-   [ ] Can change/replace image
-   [ ] Can remove/delete image
-   [ ] Default avatar shown when none uploaded
-   [ ] Image quality after upload (compression)

---

### 4. Input Validation

#### Required Fields

-   [ ] Which fields are required?
-   [ ] Can't save without required fields
-   [ ] Clear error messages

#### Optional Fields

-   [ ] Can leave optional fields empty
-   [ ] Can clear optional fields

#### Validation Messages

-   [ ] Error messages are clear and helpful
-   [ ] Errors show inline near fields
-   [ ] Multiple errors shown simultaneously
-   [ ] Errors clear when corrected

---

### 5. Save & Cancel Operations

**Save:**

-   [ ] Save button enabled only when changes made
-   [ ] Loading state during save
-   [ ] Success message after save
-   [ ] Failure handling (network error, server error)
-   [ ] Data persists after save

**Cancel:**

-   [ ] Cancel button exists
-   [ ] Canceling reverts changes
-   [ ] No confirmation needed for cancel?
-   [ ] Unsaved changes warning (if navigating away)

---

### 6. Privacy & Visibility Settings (if applicable)

-   [ ] Profile visibility options (public, private, friends-only)
-   [ ] Which fields can be made private?
-   [ ] Privacy settings persist
-   [ ] Non-logged-in users see correct visibility
-   [ ] Other users respect privacy settings

---

### 7. Account Settings Integration

**Connected to Profile?**

-   [ ] Change password option
-   [ ] Email preferences
-   [ ] Notification settings
-   [ ] Connected accounts (social auth)
-   [ ] Two-factor authentication

**Account Deletion:**

-   [ ] Delete account option exists
-   [ ] Confirmation required
-   [ ] What happens to user data?
-   [ ] Can create new account with same email after deletion?

---

### 8. Viewing Other Users' Profiles (if applicable)

-   [ ] Can view other users' profiles
-   [ ] Correct user data shown
-   [ ] Privacy settings respected
-   [ ] Can't edit other users' profiles
-   [ ] Edit button not shown for other users

---

### 9. Edge Cases & Stress Tests

-   [ ] Edit multiple fields at once
-   [ ] Save without making changes
-   [ ] Rapid saves (click save multiple times)
-   [ ] Network interruption during save
-   [ ] Browser back button during edit
-   [ ] Multiple tabs editing same profile
-   [ ] Session timeout during edit
-   [ ] Maximum length on all text fields

---

### 10. Cross-Browser Testing

Test critical flows on:

-   [ ] Chrome (latest)
-   [ ] Firefox (latest)
-   [ ] Safari (latest)
-   [ ] Edge (if relevant)

---

### 11. Responsive/Mobile Testing

-   [ ] Profile view on mobile
-   [ ] Edit mode on mobile
-   [ ] Image upload on mobile
-   [ ] Camera option for profile picture (mobile)
-   [ ] Form fields usable on small screens
-   [ ] Touch interactions work correctly

---

### 12. Integration with Other Features

-   [ ] Profile changes reflect in navigation bar
-   [ ] Profile changes reflect in leagues (if name/avatar shown)
-   [ ] Profile changes reflect in other users' views
-   [ ] Profile data used elsewhere in app

---

## Test Data

### Valid Profile Data

```
Name: Test User
Email: testuser@example.com
Phone: +1-555-0123
Bio: This is a test user profile for QA testing purposes.
Location: San Francisco, CA
```

### Edge Case Data

```
Name: A
Name: [250 character string]
Name: 🎾 Player with Emoji 🏆
Name: User'with"quotes
Email: invalid-email
Phone: 123 (too short)
Bio: [10,000 character string]
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
-   [Which fields are editable?]
-   [Profile visibility model?]
-   [Image size/format requirements?]

---

## Coverage Summary

**Areas Covered**: [e.g., 85% - covered editing and validation]  
**Areas Not Covered**: [e.g., Didn't test account deletion]  
**Confidence Level**: [High/Medium/Low]  
**Ready for Release?**: [Yes/No/With Conditions]

---

## Follow-Up Actions

-   [ ] File bugs in [tracking system]
-   [ ] Retest after bug fixes
-   [ ] Test integration with Leagues
-   [ ] Test profile visibility from other user accounts
-   [ ] Clarify editable fields with dev team

---

## Session Notes

**Start Time**: [HH:MM]  
**End Time**: [HH:MM]  
**Interruptions**: [Any blockers or interruptions]  
**Test Environment**: [staging.xeito.app]  
**Build/Version**: [if available]
