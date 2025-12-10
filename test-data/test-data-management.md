# Test Data Management

> **Purpose**: Document test accounts, sample data, and data management strategy

---

## Test User Accounts

### Primary Test Accounts

| Email          | Password         | Role  | Purpose           | Environment |
| -------------- | ---------------- | ----- | ----------------- | ----------- |
| [To be filled] | [Secure storage] | User  | General testing   | Staging     |
| [To be filled] | [Secure storage] | Admin | Admin features    | Staging     |
| [To be filled] | [Secure storage] | User  | Edge case testing | Staging     |

**⚠️ Security Note**: Store actual credentials in a secure password manager (1Password, LastPass, etc.), not in this file.

---

## Sample League Data

### Test Leagues

| League Name          | Creator       | Purpose             | Status |
| -------------------- | ------------- | ------------------- | ------ |
| QA Test League Alpha | [Test User 1] | Happy path testing  | Active |
| QA Test League Beta  | [Test User 1] | Validation testing  | Active |
| QA Edge Case League  | [Test User 2] | Edge case scenarios | Active |

**Note**: Prefix all test data with "QA Test" for easy identification and cleanup.

---

## Test Data Guidelines

### Data Creation

-   Always use identifiable prefixes: "QA Test", "TEST", "AUTOMATED"
-   Use timestamp in names to track when created: "QA Test League 2024-12-01"
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

Invalid (for testing validation):
- plaintext
- @example.com
- test@
- test @example.com
- test..name@example.com
```

### Passwords

```
Valid (meets requirements):
- TestPassword123!
- SecurePass456$

Invalid (for testing validation):
- 123 (too short)
- password (no numbers)
- 12345678 (no letters)
```

### League Names

```
Valid:
- Professional Tennis League
- Summer 2024 Championship

Edge Cases:
- A (single character)
- [250 character string]
- League'with"special'chars
- 🏆 League with Emoji 🎾
```

---

## Environment-Specific Data

### Local Environment

-   [Document local setup data requirements]
-   [Seed data scripts location]

### Development Environment

-   URL: [dev.xeito.app]
-   Shared data: [Yes/No]
-   Cleanup policy: [Daily/Weekly]

### Staging Environment

-   URL: [staging.xeito.app]
-   Shared data: [Yes/No]
-   Cleanup policy: [Before releases]
-   **Primary testing environment**

### Production

-   ⛔ **DO NOT use production for testing**
-   Only verify critical issues that can't be reproduced elsewhere
-   Use read-only operations only
-   Get approval before any production testing

---

## Data Dependencies

### Creating a Complete Test Scenario

**For Testing Leagues:**

1. Need: Valid user account (logged in)
2. Create: League with valid data
3. Optional: Team members, matches, schedule

**For Testing Profile:**

1. Need: Valid user account (logged in)
2. Modify: Profile fields
3. Upload: Test avatar image

---

## Test Files & Assets

### Profile Pictures

Location: `test-data/images/`

-   `avatar-valid.jpg` (500KB, 800x800)
-   `avatar-large.jpg` (5MB, test size limit)
-   `avatar-small.png` (10KB, 100x100)
-   `avatar-invalid.pdf` (test format validation)

### Documents (if applicable)

Location: `test-data/documents/`

-   [List any test documents needed]

---

## Data Isolation Strategy

### Per-Tester Isolation

-   Each tester uses unique email prefix: `qa-yourname+test@example.com`
-   Create your own test leagues: "QA YourName - Test League"
-   Avoid modifying shared data

### Shared Test Data

-   Mark clearly as "SHARED - DO NOT DELETE"
-   Document in team wiki/Notion
-   Coordinate changes in team chat

---

## API Test Data

### Sample API Payloads

**Create League:**

```json
{
	"name": "QA Test League",
	"description": "Test league for QA automation",
	"startDate": "2024-12-01",
	"endDate": "2024-12-31"
}
```

**Update Profile:**

```json
{
	"displayName": "QA Tester",
	"bio": "Test user for quality assurance"
}
```

---

## Data Management Tools

### Scripts (if available)

-   `scripts/seed-data.sh` - Seed test database
-   `scripts/cleanup-test-data.sh` - Remove QA test data
-   `scripts/create-test-user.sh` - Create test account

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

## Questions for Dev Team

-   [ ] How to reset/seed test data?
-   [ ] What's the data retention policy for test environments?
-   [ ] Can we have dedicated test user accounts?
-   [ ] Is there an API or script for bulk data creation?
-   [ ] How to coordinate with other testers on shared data?
-   [ ] What data should never be deleted?

---

**Last Updated**: [Date]  
**Maintained By**: [QA Team]
