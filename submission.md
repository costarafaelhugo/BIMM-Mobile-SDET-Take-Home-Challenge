# BIMM Mobile SDET Take-Home Challenge Submission

## Candidate Information
- **Name:** Hugo Rafael Costa

## Time Spent
- **Phase 1 - Test Planning:** ~2 hours
- **Phase 2 - Automation:** ~3 hours
- **CI Integration & Setup:** ~1 hour
- **Total:** ~6 hours

## Assumptions
- The app does not require login or backend validation, so all data manipulation is local.
- The 'Add Section' button is used to create a new task list.
- The field labeled "Name" refers to the title of the task list.
- The app UI is assumed to remain stable (accessibility labels and identifiers won't change).

## Notes
- Tests were written using `XCTest/XCUITest`, Apple's native UI testing framework.
- CI was implemented using GitHub Actions with a workflow that installs dependencies and runs tests on a simulator.
- All tests are designed to run headlessly in a simulator environment (iPhone 14 / iOS 17).
- Test coverage includes functional scenarios, UI checks, and persistence assumptions.

## Deliverables Included
- `Phase1_TestPlan.md`
- `Phase2_Automation/` (with test cases, framework helpers, CI config)
- `SUBMISSION.md` (this file)
