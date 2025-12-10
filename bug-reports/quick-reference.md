# Bug Report Quick Reference

> **Quick guide** for filing effective bug reports

---

## Bug Severity Guide

### 🔴 Critical

-   App crashes or completely unusable
-   Data loss or corruption
-   Security vulnerability
-   Core feature completely broken (can't login, can't save data)
-   Affects all users
-   **Action**: Report immediately, blocks release

### 🟠 High

-   Major feature broken or significantly degraded
-   Workaround exists but is difficult
-   Affects many users
-   Poor user experience in important flow
-   **Action**: Fix before next release

### 🟡 Medium

-   Feature partially works
-   Easy workaround exists
-   Affects some users in specific scenarios
-   Minor functionality issue
-   **Action**: Fix in upcoming release

### 🟢 Low

-   Cosmetic issue (alignment, colors, spacing)
-   Typo or text issue
-   Edge case scenario
-   Affects very few users
-   **Action**: Fix when time permits, can be batched

---

## The 4 Essential Elements

Every bug report MUST have:

1. **Steps to Reproduce** - Exact actions to trigger the bug
2. **Expected Behavior** - What should happen
3. **Actual Behavior** - What actually happens
4. **Environment** - Browser, device, URL

Without these, developers can't fix the bug!

---

## Quick Tips

### ✅ DO:

-   Be specific and detailed
-   Include screenshots/videos
-   Test on multiple browsers if possible
-   Provide exact error messages
-   Include test data used
-   Check if it's already reported

### ❌ DON'T:

-   Report multiple bugs in one ticket
-   Use vague language ("doesn't work", "broken")
-   Skip reproduction steps
-   Assume developers know context
-   Report bugs without verifying first

---

## Bug Report Checklist

Before submitting:

-   [ ] Bug is reproducible (tested at least twice)
-   [ ] Steps to reproduce are clear and complete
-   [ ] Screenshot or video attached
-   [ ] Severity and priority assessed
-   [ ] Environment information included
-   [ ] Expected vs actual behavior documented
-   [ ] Checked for duplicates
-   [ ] Console errors copied (if applicable)

---

## Common Mistakes

**❌ Bad Bug Report:**

> "Login doesn't work"

**✅ Good Bug Report:**

> **Title**: Login button remains disabled after correcting invalid email
>
> **Steps**:
>
> 1. Go to staging.xeito.app/login
> 2. Enter "invalid" in email field
> 3. Enter "Pass123!" in password
> 4. Click Login - see error "Invalid email format"
> 5. Change email to "test@example.com"
> 6. Submit button stays disabled
>
> **Expected**: Button enables after valid email
> **Actual**: Button stays disabled, must refresh page
> **Environment**: Chrome 120, macOS, Desktop
> **Screenshot**: [attached]

---

## Filing Workflow

1. **Discover** bug during testing
2. **Verify** it's reproducible
3. **Document** using template
4. **Attach** evidence (screenshots/video)
5. **File** in bug tracker
6. **Tag** appropriately
7. **Notify** team if critical
8. **Track** until resolved
9. **Retest** after fix
10. **Close** when verified

---

## Templates Location

-   **Full Template**: `bug-reports/bug-report-template.md`
-   **Quick Template**: Below

---

## Quick Template (Copy/Paste)

```markdown
## [Bug Title]

**Severity**: Critical/High/Medium/Low
**Environment**: [Browser, Device, URL]

**Steps to Reproduce**:

1.
2.
3.

**Expected**:
**Actual**:

**Screenshot**: [attach]
**Console Errors**: [if any]
```

---

## Questions to Ask Yourself

Before filing a bug, ask:

1. Can I reproduce this reliably?
2. Have I documented exact steps?
3. Is this actually a bug or expected behavior?
4. Have I tested on multiple browsers?
5. Is there enough information for a developer to fix it?
6. Have I included visual evidence?
7. Is the severity assessment accurate?

If you can't answer these confidently, investigate more before filing.
