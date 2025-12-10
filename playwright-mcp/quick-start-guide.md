# Quick Start Guide: Using Playwright MCP for Testing

> **For**: Manual QA testers new to Playwright MCP  
> **Goal**: Get productive with MCP-assisted exploratory testing in 15 minutes

---

## What is Playwright MCP?

Playwright MCP (Model Context Protocol) lets you control a web browser using natural language. Instead of clicking through the same flows manually, you describe what you want to test, and MCP automates the repetitive parts.

**Think of it as**: A smart assistant that drives the browser for you while you focus on analyzing results.

---

## When to Use MCP vs Manual Testing

### ✅ Use Playwright MCP For:

-   Filling forms quickly with different test data
-   Running the same test scenario multiple times
-   Taking screenshots at different viewport sizes
-   Extracting data from pages (links, form fields, etc.)
-   Testing multiple input combinations rapidly
-   Documenting test steps automatically

### 🚫 Keep Manual Testing For:

-   Initial exploration of new features (use your eyes and intuition)
-   Subjective UX evaluation (does this feel right?)
-   Visual design review
-   Complex user interactions that are hard to describe
-   Final sign-off before release

### 🎯 Best Approach:

Combine both! Use MCP to speed up repetitive tasks, then manually verify the interesting cases.

---

## Your First MCP Test Session

### Step 1: Start with Simple Exploration

**Try this prompt:**

```
Navigate to https://www.xeito.app/ and tell me:
1. What navigation links exist
2. What the main heading says
3. If there's a login button

Take a screenshot.
```

**What happens**: MCP will open a browser, visit the site, analyze it, and give you a summary with a screenshot.

---

### Step 2: Test a Login Form

**After discovery, use:**

```
Navigate to [your staging login URL].

Test login with these credentials:
1. Email: test@example.com, Password: ValidPass123! (should succeed)
2. Email: test@example.com, Password: wrongpass (should fail)
3. Email: invalid-email, Password: anything (should show validation error)

For each attempt:
- Fill the form
- Click login button
- Tell me what happened
- Take a screenshot

Provide a summary table of results.
```

**What you get**: 3 login attempts executed automatically with screenshots and error messages documented.

---

### Step 3: Test Form Validation

```
Navigate to [signup form URL].

Try submitting the form with these email addresses:
1. (empty)
2. test@example.com (valid)
3. notanemail (invalid)
4. @example.com (invalid)
5. test@ (invalid)

For each, document:
- Was it accepted?
- What error message appeared?
- When did validation trigger?
```

**What you get**: Validation testing done in seconds, complete report of all error messages.

---

## Workflow: A Complete Test Session

### 1. Discovery Phase (15 min)

**Manual**: Explore the feature yourself first. Understand the happy path.

**MCP Assist**:

```
Navigate to [feature URL] and document:
- All form fields (names, types, required/optional)
- All buttons and their labels
- Any validation messages visible
Create a table of all elements.
```

### 2. Happy Path Testing (10 min)

**MCP**:

```
Navigate to [feature URL] and complete this user flow:
1. [Step 1]
2. [Step 2]
3. [Step 3]
Document if all steps succeeded and take screenshots.
```

**Manual**: Verify the MCP execution was correct and check for visual issues.

### 3. Edge Case Testing (30 min)

**MCP**: Run batch tests for validation, edge cases, different data sets.

**Manual**: Review MCP findings and investigate interesting failures deeper.

### 4. Bug Documentation (ongoing)

**MCP Output → Bug Report Template**: Copy MCP screenshots and findings into your bug reports.

---

## Example: Testing the Sign Up Flow

### Traditional Manual Approach (60 min):

1. Fill form with valid data → submit → check → document (5 min)
2. Fill form with invalid email → submit → check → document (5 min)
3. Fill form with short password → submit → check → document (5 min)
4. Repeat for 10 more scenarios...

### MCP-Assisted Approach (20 min):

**One prompt** (5 min):

```
Test the signup form at [URL] with these 12 scenarios:
[List all scenarios]
For each, document the result and error message.
Provide a summary table.
```

**Review results** (10 min): Analyze the table, take notes, investigate interesting cases manually.

**Document findings** (5 min): Copy MCP output into test charter.

---

## Best Practices

### 1. Start Simple, Then Expand

-   Begin with one test scenario
-   If it works, expand to multiple scenarios
-   Build complexity gradually

### 2. Be Specific in Prompts

❌ Vague: "Test the login"
✅ Specific: "Navigate to [URL], enter email '[email]' and password '[pass]', click the submit button with text 'Login', and tell me if the URL changed"

### 3. Use MCP for Repetition, Manual for Analysis

-   MCP executes the steps
-   YOU evaluate if the behavior is correct
-   MCP can't tell if a design looks wrong or UX feels clunky

### 4. Save Your Prompts

-   When you write a good prompt, save it in `playwright-mcp/prompt-library.md`
-   Reuse and adapt prompts across test sessions
-   Build your personal prompt collection

### 5. Combine with Test Charters

-   Use test charters for planning
-   Use MCP prompts to execute the plan
-   Document findings back in the charter

---

## Common Patterns

### Pattern 1: Batch Input Testing

```
Test [field name] with these inputs:
[List 10 test values]
For each, document if accepted/rejected and any error message.
```

### Pattern 2: User Journey Testing

```
Complete this user flow:
1. Login as [user]
2. Navigate to [section]
3. Perform [action]
4. Verify [expected outcome]
Take screenshots at each step.
```

### Pattern 3: Cross-Browser Screenshots

```
Take screenshots of [URL] on:
- Chrome at 1920x1080
- Firefox at 1920x1080
- Safari at 1920x1080
Compare and note any differences.
```

### Pattern 4: Data Extraction

```
Navigate to [URL] and extract:
- All links (text and href)
- All form fields (name, type, required)
- All buttons (text and action)
Create a structured table.
```

---

## Troubleshooting

### "MCP couldn't find the button"

-   Be more specific: use exact button text or describe location
-   Check if there's a loading state or delay
-   Try manually to confirm the button exists

### "The form didn't submit"

-   Verify you're targeting the right form
-   Check if there are validation errors blocking submission
-   Some forms need Enter key instead of clicking button

### "Screenshots look wrong"

-   Specify exact viewport size
-   Add wait time for page to fully load
-   Check if content loads dynamically (AJAX)

---

## Next Steps

1. **Read** the full `prompt-library.md` for more prompts
2. **Practice** with simple prompts on a test site
3. **Customize** prompts for your actual test URLs
4. **Document** your findings in test charters
5. **Iterate** - improve your prompts based on what works

---

## Example Session Checklist

Planning a test session? Follow this:

-   [ ] Review test charter for the feature
-   [ ] Open `playwright-mcp/prompt-library.md`
-   [ ] Copy relevant prompts
-   [ ] Customize with actual URLs and test data
-   [ ] Run prompts in MCP
-   [ ] Review and analyze outputs
-   [ ] Do manual spot-checks on interesting findings
-   [ ] Document bugs found
-   [ ] Update test charter with results
-   [ ] Save any new custom prompts you created

---

## Remember

Playwright MCP is a **tool to accelerate testing**, not replace your expertise. You're still the QA engineer who:

-   Decides what to test
-   Evaluates if behavior is correct
-   Finds subtle UX issues
-   Makes release decisions

MCP just makes you faster at the repetitive parts! 🚀
