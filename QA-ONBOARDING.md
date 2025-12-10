# QA Onboarding Checklist

> **For**: New QA engineers joining the Xeito project  
> **Goal**: Get fully productive in your first week

---

## Day 1: Setup & Discovery

### Access & Tools

-   [ ] Access to project repository
-   [ ] Access to Xeito staging environment
-   [ ] Credentials for test user accounts
-   [ ] Access to bug tracking tool (Jira/Linear/GitHub Issues)
-   [ ] Join team communication channels (Slack/Discord)
-   [ ] Add to QA team calendar for standups/meetings

### Read Documentation

-   [ ] Read `README.md` - Project overview
-   [ ] Read `discovery/developer-interview-guide.md` - Questions to ask
-   [ ] Read `discovery/application-overview-template.md` - Fill this out after dev meeting
-   [ ] Read `discovery/risk-assessment-template.md` - Understand testing priorities

### Schedule Meetings

-   [ ] Developer interview session (60-90 min)
-   [ ] QA team intro (if team exists)
-   [ ] Product demo from PM (if available)

---

## Day 2: Environment Setup

### Test Environment

-   [ ] Access staging environment: [URL]
-   [ ] Create test user accounts (or get credentials)
-   [ ] Verify you can login
-   [ ] Explore the app manually for 1-2 hours
-   [ ] Document your first impressions

### Local Setup (if needed)

-   [ ] Clone repository
-   [ ] Follow dev setup instructions
-   [ ] Run app locally
-   [ ] Verify local environment works

### Tools

-   [ ] Install/verify browser versions (Chrome, Firefox, Safari)
-   [ ] Set up Playwright MCP (if using)
-   [ ] Set up screen recording tool (Loom, QuickTime, etc.)
-   [ ] Set up screenshot tool

---

## Day 3: Learn the App

### Manual Exploration

-   [ ] Follow test charter: `test-plans/01-signup-login-charter.md`
-   [ ] Follow test charter: `test-plans/02-leagues-charter.md`
-   [ ] Follow test charter: `test-plans/03-profile-charter.md`
-   [ ] Take notes on anything unclear or buggy

### Fill Out Templates

-   [ ] Complete `discovery/application-overview-template.md` with info learned
-   [ ] Update `discovery/risk-assessment-template.md` based on exploration
-   [ ] Document test data in `test-data/test-data-management.md`

### Ask Questions

-   [ ] Create list of questions for dev team
-   [ ] Schedule follow-up with devs if needed
-   [ ] Document answers in your notes

---

## Day 4: Start Testing

### First Test Session

-   [ ] Pick one feature (e.g., Sign Up & Login)
-   [ ] Use test charter as guide
-   [ ] Document findings
-   [ ] File your first bug (if found)

### Practice Playwright MCP (if using)

-   [ ] Read `playwright-mcp/quick-start-guide.md`
-   [ ] Try simple prompts from `playwright-mcp/prompt-library.md`
-   [ ] Run a few test scenarios with MCP
-   [ ] Compare manual vs MCP-assisted testing

---

## Day 5: Integrate with Team

### Bug Reporting

-   [ ] File at least 2-3 bugs using `bug-reports/bug-report-template.md`
-   [ ] Get feedback from team on bug reports
-   [ ] Adjust reporting style based on feedback

### Team Workflow

-   [ ] Understand release schedule
-   [ ] Understand when QA gets involved (PR? After merge?)
-   [ ] Understand sign-off process
-   [ ] Coordinate with other QA (if applicable)

### Plan Next Week

-   [ ] Review backlog of features to test
-   [ ] Prioritize based on risk assessment
-   [ ] Schedule test sessions
-   [ ] Block time for regression testing

---

## Week 2+: Ongoing Work

### Regular Activities

-   [ ] Daily/weekly exploratory testing sessions
-   [ ] Bug triage and tracking
-   [ ] Regression testing before releases
-   [ ] Update test documentation as app evolves
-   [ ] Coordinate with dev team on testing needs

### Continuous Improvement

-   [ ] Add new test charters for new features
-   [ ] Update Playwright MCP prompts library
-   [ ] Refine risk assessment
-   [ ] Share learnings with team
-   [ ] Propose process improvements

---

## Key Resources

### Essential Documents

-   `README.md` - Start here
-   `discovery/developer-interview-guide.md` - Questions for devs
-   `test-plans/*.md` - Test charters for each feature
-   `bug-reports/bug-report-template.md` - How to file bugs
-   `playwright-mcp/quick-start-guide.md` - MCP crash course

### Quick References

-   `bug-reports/quick-reference.md` - Bug severity guide
-   `discovery/risk-assessment-template.md` - Testing priorities

---

## Questions to Answer

By end of Week 1, you should know:

**About the App:**

-   [ ] What does Xeito do? Who uses it?
-   [ ] What features are ready for testing?
-   [ ] What's in active development?
-   [ ] What are the critical user flows?

**About Testing:**

-   [ ] What environments exist and how to access them?
-   [ ] Where to file bugs and how?
-   [ ] When does QA get involved in the workflow?
-   [ ] What's expected test coverage?

**About the Team:**

-   [ ] Who are the developers?
-   [ ] Who is the product manager?
-   [ ] Who else is on QA team (if anyone)?
-   [ ] What's the communication culture?

---

## Success Criteria

After 1 week, you should be able to:

-   ✅ Access all test environments independently
-   ✅ Navigate the app confidently
-   ✅ Run exploratory test sessions without guidance
-   ✅ File clear, detailed bug reports
-   ✅ Use Playwright MCP for basic testing (if applicable)
-   ✅ Know who to ask for help

After 2 weeks, you should be able to:

-   ✅ Work independently on test assignments
-   ✅ Contribute to test planning discussions
-   ✅ Provide quality sign-off for releases
-   ✅ Mentor other QA team members (if they join)

---

## Need Help?

**Stuck on something?**

-   Ask in team chat
-   Schedule time with dev lead
-   Review documentation again
-   Reach out to QA lead (if exists)

**Found documentation gaps?**

-   Add to this checklist
-   Update relevant docs
-   Share with team

---

**Welcome to the team! 🎉**
