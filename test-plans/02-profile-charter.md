# Exploratory Test Charter: Profile

> **Feature**: User Profile Management  
> **Status**: Ready for Testing  
> **Tester**: [Your Name]  
> **Date**: [Test Date]  
> **Environment**: Production
> **Session Duration**: [e.g., 60 minutes]

---

## Charter Mission

**Explore** the user profile viewing and editing functionality  
**To discover** bugs, usability issues, and edge cases in profile management

---

## Prerequisites

-   [ ] Logged in user account

---

## Areas to Explore

### 1. Profile View

#### Display

-   [ ] Navigate to profile page (e.g., /profile)
-   [ ] All profile fields display correctly
-   [ ] User's own data shown
-   [ ] Profile picture/avatar displays (if exists)
-   [ ] Empty fields handled gracefully
-   [ ] Loading states work correctly

#### Navigation

-   [ ] Can access profile from main navigation
-   [ ] Can access profile from user menu
-   [ ] Direct URL access works
-   [ ] Back navigation from brand Logo works

---

### 2. Profile Editing

#### Happy Path

-   [ ] Edit button on allowed fields are accessible
-   [ ] Personal Details are not editable
-   [ ] Modify profile information
-   [ ] Save changes successfully
-   [ ] Changes persist after refresh
-   [ ] Return to view mode

#### Editable Fields (document what exists)

**About Me**

-   [ ] Empty bio
-   [ ] Very long bio (test character limit)
-   [ ] Special characters (e.g., emojis, accented characters, international characters)
-   [ ] Line breaks/formatting
-   [ ] HTML/script injection attempts

**Contact:Phone Number**

-   [ ] Empty phone
-   [ ] Invalid characters (letters, symbols)
-   [ ] Too many/too few digits
-   [ ] Available on WhatsApp check works

**Player Info**

-   [ ] Dominant hand dropdown is clickable
-   [ ] Started Playing date picker works
-   [ ] Experience is calculated correctly

**Timezone**

-   [ ] Your Timezone dropdown works
-   [ ] Use detected feature works

**Availability**

-   [ ] Add availability per day works
-   [ ] Remove availability per day works

---

### 3. Profile Picture/Avatar

#### Upload

-   [ ] Upload button exists and works
-   [ ] Can select image file
-   [ ] Upload succeeds with valid image
-   [ ] Loading state during upload
-   [ ] Image displays after upload
-   [ ] Avatar is displayed in profile view

#### Image Management
-   [ ] Remove button exist and works
-   [ ] Can change/replace image
-   [ ] Can remove/delete image
-   [ ] User's initial are display when no image is uploaded

---

### 4. Cross-Browser Testing

Test critical flows on:

-   [ ] Chrome (latest)
-   [ ] Firefox (latest)
-   [ ] Safari (latest)
-   [ ] Edge (if relevant)

---

### 5. Responsive/Mobile Testing

-   [ ] Profile view on mobile
-   [ ] Edit mode on mobile
-   [ ] Image upload on mobile
-   [ ] Camera option for profile picture (mobile)
-   [ ] Form fields usable on small screens
-   [ ] Touch interactions work correctly

---

### 6. Integration with Other Features

-   [ ] Profile changes reflect in navigation bar
-   [ ] Profile changes reflect in leagues (if name/avatar shown)
-   [ ] Profile changes reflect in other users' views
-   [ ] Profile data used elsewhere in app

