# Developer Interview Guide

## Purpose

Gather essential information about the application, tech stack, and development process to establish effective QA processes.

---

## Pre-Meeting Setup

-   [ ] Schedule 60-90 minute session with dev lead + 1-2 developers
-   [ ] Frame as collaborative: "Understanding what you've built to protect it properly"
-   [ ] Prepare recording/note-taking method

---

## Questions Checklist

### Application Architecture

**Tech Stack**

-   [ ] What frontend framework/library? (React, Vue, Angular, etc.)
-   [ ] What backend technology? (Node.js, Python, Ruby, etc.)
-   [ ] Database type and version? (PostgreSQL, MySQL, MongoDB, etc.)
-   [ ] Hosting/deployment platform? (AWS, Vercel, Heroku, etc.)
-   [ ] Any external services integrated? (Auth0, Stripe, SendGrid, etc.)

**Architecture**

-   [ ] Monolith or microservices?
-   [ ] Separate frontend/backend or full-stack framework?
-   [ ] API type? (REST, GraphQL, tRPC, etc.)
-   [ ] State management approach?

---

### User Roles & Permissions

-   [ ] What user roles exist? (Admin, User, Coach, Player, etc.)
-   [ ] How do permissions differ between roles?
-   [ ] Are there subscription tiers or feature flags?
-   [ ] Can users belong to multiple organizations/teams?

---

### Ready Features Deep Dive

#### Sign Up & Login

-   [ ] Walk through the happy path user flow
-   [ ] Email validation rules?
-   [ ] Password requirements? (length, complexity, etc.)
-   [ ] Social authentication available? (Google, Facebook, etc.)
-   [ ] Email verification required?
-   [ ] What happens with duplicate email signup?
-   [ ] Password reset flow available?
-   [ ] Session timeout duration?
-   [ ] Remember me functionality?

#### Leagues

-   [ ] What is a "league" in this context?
-   [ ] Who can create leagues? (any user, admin only, etc.)
-   [ ] What fields/data define a league?
-   [ ] Validation rules for league creation?
-   [ ] Can leagues be edited? By whom?
-   [ ] Can leagues be deleted? What happens to related data?
-   [ ] Are there visibility settings? (public/private)
-   [ ] User limits per league?
-   [ ] What related features exist? (teams, matches, schedules, etc.)

#### Profile

-   [ ] What fields are on the profile?
-   [ ] Which fields are editable vs. read-only?
-   [ ] Avatar/image upload supported? (size limits, formats)
-   [ ] Privacy settings available?
-   [ ] Can users delete their account?
-   [ ] Profile visibility options? (public, private, friends-only)
-   [ ] What data is public vs. private by default?

---

### Stability & Change Management

-   [ ] Which features are stable (won't change next 2-3 sprints)?
-   [ ] What's on the roadmap that affects current sections?
-   [ ] Any experimental features or A/B tests running?
-   [ ] Known bugs/limitations in ready sections?
-   [ ] Features intentionally disabled or in beta?

---

### Testing Environments

**Environment Access**

-   [ ] What environments exist? (local, dev, staging, production)
-   [ ] URLs for each environment?
-   [ ] How to access? (VPN, IP whitelist, public)
-   [ ] Credentials needed?
-   [ ] How to request access?

**Test Data Management**

-   [ ] Separate databases per environment?
-   [ ] Can I create test accounts freely?
-   [ ] Specific test credentials provided?
-   [ ] Data seeding available?
-   [ ] How to reset/clean test data?
-   [ ] Any data that should NOT be modified?

**API Testing**

-   [ ] API documentation available? (Swagger, Postman collection)
-   [ ] Direct API access for testing?
-   [ ] Authentication mechanism for API? (JWT, API keys, etc.)
-   [ ] Rate limits or quotas to be aware of?

---

### Development Process

**Release Cycle**

-   [ ] How often do you release? (continuous, weekly, bi-weekly)
-   [ ] Deployment process? (manual, automated CI/CD)
-   [ ] When should QA be involved? (PR stage, after merge, before deploy)
-   [ ] Code freeze windows?

**Current Testing Practices**

-   [ ] Unit test coverage?
-   [ ] Integration tests?
-   [ ] Manual testing process?
-   [ ] Code review requirements?

**Bug Tracking**

-   [ ] What tool for bug reports? (Jira, GitHub Issues, Linear, etc.)
-   [ ] Bug severity definitions?
-   [ ] Expected turnaround time for bug fixes?
-   [ ] How to mark bugs as blocking vs. non-blocking?

**Communication**

-   [ ] Primary communication channel? (Slack, Teams, Discord)
-   [ ] Daily standups or async updates?
-   [ ] Where to ask quick questions?

**Definitions of Done**

-   [ ] What makes a feature "ready for testing"?
-   [ ] What makes a feature "ready for production"?
-   [ ] Sign-off requirements before release?

---

### Critical Paths & Priorities

-   [ ] What are the critical user flows that CANNOT break?
-   [ ] What features have the highest usage?
-   [ ] What areas have had the most bugs historically?
-   [ ] Security-sensitive areas to prioritize?
-   [ ] Performance requirements or SLAs?

---

### QA Expectations

-   [ ] Desired level of test automation? (none, smoke tests, comprehensive)
-   [ ] Browser/device coverage needed?
-   [ ] Accessibility requirements? (WCAG compliance level)
-   [ ] Performance testing needed? (load, stress, etc.)
-   [ ] Security testing expectations?
-   [ ] Mobile app testing? (native, PWA, responsive web)

---

### Integration & Dependencies

-   [ ] Third-party services the app depends on?
-   [ ] How are service failures handled?
-   [ ] Any background jobs or cron tasks?
-   [ ] Email/notification systems?
-   [ ] Payment processing (if applicable)?
-   [ ] Analytics/tracking tools integrated?

---

## Post-Interview Actions

-   [ ] Document all findings in `application-overview.md`
-   [ ] Create feature-specific docs in `test-plans/`
-   [ ] Update risk assessment based on critical paths
-   [ ] Set up environment access
-   [ ] Create test user accounts
-   [ ] Schedule follow-up if needed
