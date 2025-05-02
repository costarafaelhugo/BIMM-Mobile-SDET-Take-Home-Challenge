# Phase 1: Test Planning & Strategy

## 1. Test Scope & Coverage

| ID | Scenario                         | Purpose                                                          | Type        | Priority |
| -- | -------------------------------- | ---------------------------------------------------------------- | ----------- | -------- |
| 1  | Create a new task list           | Verifies that the user can create a task list                    | Functional  | High     |
| 2  | Delete Task Section              | Verify that a user can tap the "Add Section" button.             | Functional  | High     |
| 3  | Home Screen Title Exists         | Confirm that the "Reminders" title is present on the HomeView    | Functional  | High     |
| 4  | Delete a task                    | Ensures that a user can remove an unwanted task                  | Functional  | High     |
| 5  | Empty state message              | Ensures the UI displays a proper message when no data is present | UI/UX       | Medium   |
| 6  | Button accessibility labels      | Ensures accessibility compliance for assistive technologies      | UI/UX       | Medium   |
| 7  | App remembers data after restart | Verifies task lists are persisted across sessions                | Regression  | High     |
| 8  | Startup time < 2s                | Verifies the app launches quickly                                | Performance | Low      |
| 9  | Scroll through task list         | Ensures smooth UX when scrolling large lists                     | Performance | Medium   |
| 10 | Input validation                 | Ensures the user cannot save empty task list names               | UI/UX       | High     |

## 2. Test Data & Environment

* **Test Data**:

  * No login/account data required.
  * Will test with:

    * 0 task lists (to trigger empty state)
    * 1–2 manually created task lists
    * Task names like "Buy groceries", "Complete assignment"

* **Environment**:

  * Xcode Simulator (iPhone 14)
  * iOS 17.0+
  * Device: iPhone 14 / iOS 17 simulator

## 3. Tooling & Framework

* **Chosen Approach**: Code-first using XCTest/XCUITest (native iOS test framework).

* **Justification**:

  * The project is a native SwiftUI iOS app and already uses Xcode tools.
  * XCUITest provides seamless UI test integration with Swift.
  * Easier to maintain in small codebases; no need for external dependencies like Cucumber.

---

