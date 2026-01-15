# Test Data Management

> **Purpose**: Document test accounts, sample data, and data management strategy

---

## Test User Accounts

### Primary Test Accounts

| Email          | Password         | Role  | Purpose           | Environment |
| -------------- | ---------------- | ----- | ----------------- | ----------- |
| romeroredacre@gmail.com| OTP via email | Admin | Admin features    | PROD     |

**⚠️ Security Note**: Store actual credentials in a secure password manager (1Password, LastPass, etc.), not in this file.

---

## Sample League Data

### Test Leagues

| League Name          | Creator       | Purpose             | Status |
| -------------------- | ------------- | ------------------- | ------ |
| QA-LeagueOne | romeroredacre@gmail.com | Happy path testing  | Active |
| QA-LeagueTwo | romeroredacre@gmail.com | Validation testing  | Active |
| QA-LeagueThree | romeroredacre@gmail.com | Edge case scenarios | Active |

**Note**: Prefix all test data with "QA Test" for easy identification and cleanup.

---

## Test Data Guidelines

### Data Creation

-   Always use identifiable prefixes: "QA Test", "TEST", "AUTOMATED"
-   Create separate data for different test scenarios
-   Document dependencies between test data

### Data Cleanup

-   Clean up test data after test sessions (if possible)
-   Keep a set of "permanent" test data for ongoing testing
-   Don't delete data that other testers might be using
-   Coordinate with team on shared test environments

### Data Refresh

-   [Document how to reset test data]
-   [Document how to seed fresh data]
-   [Document data retention policies]

---

## Edge Case Test Data

### Email Addresses

```
Valid:
- test+valid@example.com
- qa.tester@example.com
- test_user123@example.co.uk
- TEST+valid@example.com

Invalid (for testing validation):
- plaintext
- @example.com
- test@
- test @example.com
- test..name@example.com
- testname😊@example.com
- Bob</username><role>admin</role>@injection.com
```

### League Names

```
Valid:
- Professional Tennis League
- Summer 2024 Championship
- A (single character)
- League'with"special'chars
- 🏆 League with Emoji 🎾
```

---

### Production

-   ⛔ **DO NOT use production for testing**
-   Only verify critical issues that can't be reproduced elsewhere
-   Use read-only operations only
-   Get approval before any production testing

---

## Data Dependencies

### Creating a Complete Test Scenario

**For Testing Leagues:**

1. Need: Valid admin user account (logged in)
2. Create: League with valid data
3. Optional: Team members, matches, schedule

**For Testing Profile:**

1. Need: Valid user account (logged in)
2. Modify: Profile fields
3. Upload: Test avatar image

---

## Data Isolation Strategy

### Per-Tester Isolation

-   Each tester uses unique email prefix: `qa-yourname+test@example.com`
-   Create your own test leagues: "QA YourName - Test League"
-   Avoid modifying shared data

### Shared Test Data

-   Mark clearly as "SHARED - DO NOT DELETE"
-   Document in team Confluence/Notion
-   Coordinate changes in team chat

---

### Manual Processes

-   [Document manual data creation steps]
-   [Document manual cleanup steps]

---

## Special Test Scenarios

### Performance Testing

-   Create 100+ leagues for pagination testing
-   Use script: [location or document manual process]

### Load Testing

-   Multiple users performing same action
-   Coordinate with dev team for load test environment

### Security Testing

-   Use isolated test accounts
-   Test data includes XSS/SQL injection attempts (sanitized)
-   Never test security exploits in shared environments

---

## Notes & Best Practices

1. **Never use real user data** - Always create test accounts
2. **Coordinate with team** - Check before cleaning up shared data
3. **Document as you go** - Update this file when creating new test data
4. **Security first** - Never commit credentials to version control
5. **Think about cleanup** - Easy to create, easy to remove

---

**Last Updated**: [Date]  
**Maintained By**: [QA Team]
