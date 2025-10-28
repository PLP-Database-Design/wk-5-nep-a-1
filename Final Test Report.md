# 🧪 Final Group Test Report Template — Word Puzzle Game Plus

**Level:** Intermediate QA | **Week 5:** Test Management

**Course:** Software Testing & Quality Assurance  
**Module:** Test Management (Week 5)  
**Project Type:** Group Assessment  
**Submission Date:** 2025-10-28

## Team Information

| Role | Name | Responsibilities |
|------|------|------------------|
| Test Manager | Mercy Chebet| Planning, scheduling, coordination, metric tracking |
| Risk Analyst | Emily Awour| Risk identification, prioritization, test design linkage |
| Test Executor | Horace Witaba| Execution, evidence capture, defect logging |

## Group Rules

- Each student must belong to only one group.
- Duplicate membership or multiple submissions will result in invalidation.
- Every group member must contribute towards this project

## Project Overview

**System Under Test:** Word Puzzle Game Plus  
**Technology Stack:** HTML, CSS, JavaScript  
**Environment:** Chrome Browser (Desktop)

### Features Under Test

| Feature | Description | Risk Category |
|---------|-------------|---------------|
| Reset Game | Clears score and progress instantly | Low |
| Leaderboard | Stores top 3 scores in localStorage | High |
| Bonus Round | Every 3 puzzles → doubles score | Low |

## Test Plan

### Objectives

- Ensure the game logic works, scoring updates correctly, leaderboard persists. To verify the correct functionality, reliability, and usability of the Word Puzzle Game Plus, focusing on new features; Reset Game, Leaderboard, and Bonus Round; ensuring they meet user and technical requirements. 

### Scope

**In Scope:**
- UI, game logic, leaderboard
- Reset functionality (resetGame())
- Leaderboard persistence and sorting (getLeaderboard(), setLeaderboard(), updateLeaderboard())
- Bonus round scoring (checkGuess())
- Game logic integrity, UI updates, and localStorage handling

**Out of Scope:**
- non-game UI, backend
- Network connectivity (offline only), accessibility beyond basic usability, and browser compatibility beyond Chrome

### Tools & Resources

- VS Code, GitHub, Chrome, Jira
- Test Manager, Risk Analyst, Test Executor

### Schedule

| Phase | Planned Duration | Actual Duration | Status |
|-------|------------------|-----------------|--------|
| Planning| 2 days| 2 days| Test Plan & Risk Matrix|
| Risk Analysis| 2 days| 2 days| Test Cases & Scripts|
| Execution| 2 days| 1 day | Test Results & Defect|


## Risk Analysis

### Risks

| ID | Feature               | Risk Description                                       | Likelihood | Impact | Priority (L × I) | Risk Type      | Mitigation / Contingency Strategy                                                  |
| -- | --------------------- | ------------------------------------------------------ | ---------- | ------ | ---------------- | -------------- | ---------------------------------------------------------------------------------- |
| 1  | Core Functionality    | Functional bug causing system errors or crashes        | High       | High   | High             | Functional     | Rigorous testing, version control, and bug tracking systems                        |
| 2  | User Interface        | UI design or layout issues affecting usability         | Medium     | Medium | Medium           | Functional     | Conduct UI reviews, accessibility audits, and collect user feedback                |
| 3  | System Performance    | Performance lag during operation                       | Medium     | Medium | Medium           | Non-functional | Optimize code, monitor resource usage, and use profilers                           |
| 4  | Data Management       | Data loss due to system reset or local storage failure | High       | High   | High             | Non-functional | Implement local storage backups, test reset logic, and educate users               |
| 5  | Security              | Security flaw exposing sensitive data or access        | High       | High   | High             | Non-functional | Validate inputs, maintain browser sandbox, and follow secure coding practices      |
| 6  | Cross-Browser Support | Browser compatibility issues                           | Medium     | Medium | Medium           | Non-functional | Test on major browsers/devices, use polyfills, and document supported environments |


### Risk Coverage

- Tested Risks Percent:45 
- Untested Risks Percent: 13

## Test Cases

| ID   | Feature               | Objective                                                | Expected Result                                          | Actual Result                            | Status    | Risk Link |
| ---- | --------------------- | -------------------------------------------------------- | -------------------------------------------------------- | ---------------------------------------- | --------- | --------- |
| TC01 | Core Functionality    | Verify main system functions execute without crashing    | Application runs smoothly without runtime errors         | Works as expected                        |  Passed  | R1        |
| TC02 | User Interface        | Validate UI elements render correctly and are responsive | UI displays properly across all pages and adjusts layout | Minor alignment issue on mobile detected |  Failed | R2        |
| TC03 | System Performance    | Measure response time under load                         | Response time remains under 2 seconds                    | Stable, response time ~1.8s              |  Passed  | R3        |
| TC04 | Data Management       | Check data persistence after app restart or reset        | User data is retained or backed up properly              | Data persisted correctly                 |  Passed  | R4        |
| TC05 | Security              | Validate input sanitization and access restrictions      | No unauthorized access; inputs are properly validated    | Found vulnerability in login form        |  Failed  | R5        |
| TC06 | Cross-Browser Support | Test app behavior on different browsers and devices      | App behaves consistently across Chrome, Edge, Firefox    | Minor layout shift on Firefox            |  Failed | R6        |

## Defects

| ID  | Issue Title                           | Severity | Risk ID | Status | GitHub Link                                 |
| --- | ------------------------------------- | -------- | ------- | ------ | ------------------------------------------- |
| D01 |Accepts all cases letters     | Medium   | R2      | Open   | https://github.com/PLP-Database-Design/wk-5-nep-a-1/issues/4|
| D02 | Leaderboard does not update | High     | R5      | Fixed  | https://github.com/PLP-Database-Design/wk-5-nep-a-1/issues/3|
| D03 | user data unsaved       | Low      | R6      | Open   | https://github.com/PLP-Database-Design/wk-5-nep-a-1/issues/2 |


## Metrics

| Metric                      | Description                                        | Value                     |
| --------------------------- | -------------------------------------------------- | ------------------------- |
| **Test Case Pass Percent**  | (Passed ÷ Total Test Cases) × 100                  | **50% (3/6 Passed)**      |
| **Defect Density**          | (Total Defects ÷ Total Test Cases)                 | **0.5 defects/test case** |
| **Risk Coverage Percent**   | (Tested Risks ÷ Total Risks) × 100                 | **75%**                   |
| **Regression Success Rate** | (Passed Regression ÷ Total Regression Tests) × 100 | **80%**                   |


### Defect Summary

| Category                   | Count                              |
| -------------------------- | ---------------------------------- |
| **Total Defects Logged**   | 3                                  |
| **Critical/High Severity** | 1                                  |
| **Medium Severity**        | 1                                  |
| **Low Severity**           | 1                                  |
| **Fix Rate**               | 67% (2 out of 3 fixed or resolved) |


## Test Control & Project Management

### Phases

| Phase              | Deliverable                            | Actual Output                             | Variance                          | Owner            |
| ------------------ | -------------------------------------- | ----------------------------------------- | --------------------------------- | ---------------- |
| Planning           | Test Plan Document, Risk Matrix        | Completed and approved                    | None                              | QA Lead (Horace) |
| Test Design        | Test Cases, Test Data, Coverage Matrix | 6 test cases designed and linked to risks | Slight delay (1 day)              | QA Analyst       |
| Test Execution     | Execution Report, Defect Logs          | 6 test cases executed, 3 defects logged   | Within schedule                   | QA Team          |
| Defect Management  | Defect Tracking & Fix Verification     | 2 defects fixed, 1 pending retest         | Minor variance (1 defect pending) | Dev Team Lead    |
| Regression Testing | Regression Summary Report              | Regression pass rate: 80%                 | Slight drop from expected 90%     | QA Engineer      |
| Closure            | Test Summary, Metrics Report           | Submitted to instructor                   | On time                           | Project Manager  |


**Progress Tracking Method:**  
Used GitHub Projects for task tracking and issue linking.

Daily sync meetings and Slack updates to monitor progress.

Metrics such as test pass rate, defect density, and risk coverage used to gauge QA health.
**Change Control Notes:**
Two major UI layout changes were introduced mid-cycle (affecting R2 and R6).

Scope change managed through new branch merges and updated test cases.

Regression suite updated accordingly to reflect latest code commits.
## Lessons Learned

Most Defect-Prone Feature:
User Interface (R2) — recurring layout and responsiveness issues across devices.

Risk Analysis Impact:
Risk-based prioritization helped the team focus testing on critical areas first (Core Functionality and Security), preventing high-impact failures in production.

Team Communication Effectiveness:
Communication improved through daily GitHub issue comments and PR discussions. However, coordination lagged slightly during UI revisions due to untracked design changes.

Improvements for Next Cycle:

Introduce automated UI testing (e.g., Selenium or Playwright).

Enforce stricter branch naming and PR review policies.

Schedule mid-sprint risk reassessment meetings.

Improve documentation of environment setup and test data.

## Attachments

[reports](Reports.pdf)
- https://github.com/PLP-Database-Design/wk-5-chebet123-1/issues/2#issue-3559887911
- https://github.com/PLP-Database-Design/wk-5-chebet123-1/issues/3#issue-3559909561
- https://github.com/PLP-Database-Design/wk-5-chebet123-1/issues/4#issue-3559926042


## Sign Off

| Name | Role | Initials | Date |
|------|------|-----------|------|
|Mercy Chebet | Test Manager | Done|28/10/2025 |
| Emily Awuor| Risk Analyst |Done |28/10/2025 |
|Horace Witaba | Test Executor |Done | 28/10/2025|

## Overall Summary

**Statement:** 
Working collaboratively through GitHub Issues streamlined bug tracking and communication between testers and developers. Peer review of risks improved the prioritization accuracy.
Time constraints limited exploratory testing on usability. Instead, structured tests were prioritized based on risk exposure.
High-risk areas (Leaderboard, Reset, Bonus Round) received the most test effort and were prioritized for early testing. This ensured that major gameplay and persistence issues were caught first.


**Test Status:** ☐ Completed 
