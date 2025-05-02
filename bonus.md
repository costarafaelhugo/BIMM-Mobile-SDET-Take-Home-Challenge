## Bonus

### API Test: Sample Scenario

**Endpoint:** `GET https://example.com/api/tasks`

**Goal:** Validate the API returns a list of tasks and proper status code.

**Tool:** Postman (Collection exported as `api_test_collection.json`)

**Assertions:**

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});

pm.test("Response has tasks", function () {
    const jsonData = pm.response.json();
    pm.expect(jsonData.length).to.be.above(0);
});
```

**Expected Response Example:**

```json
[
  { "id": 1, "title": "Buy Milk", "completed": false },
  { "id": 2, "title": "Read Book", "completed": true }
]
```

**Instructions:** Import the Postman collection and run it manually or with `newman` in CI.

---

### Performance Test: App Launch Time

**Objective:** Measure how fast the app launches.

**Method:**

* Instrumented manually via Xcode `Instruments → Time Profiler`
* Start measuring from `application(_:didFinishLaunchingWithOptions:)` to HomeView load

**Result (Example):**

```
Launch Time: 1.43 seconds on iPhone 14 Simulator (iOS 17)
```

**Additional Notes:**

* Launch time under 2 seconds is acceptable for good UX
* If desired, repeat test on physical device for comparison
