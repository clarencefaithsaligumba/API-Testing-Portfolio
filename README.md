# 📡 Trello API Functional Testing with Postman

This repository contains my API Testing project for the **Trello REST API**. The goal of this project is to validate the core functionalities of Trello's Board and Card management using **Postman** and **JavaScript**.

---

## 🛠️ Tools & Technologies
* **Postman:** Request development and test execution.
* **JavaScript (Chai Library):** For writing automated test assertions within Postman.
* **Trello REST API:** The target application for testing.

---

## 📋 Scenarios Tested (Board Lifecycle)
1. **Create Board (POST):** Validates board creation with custom names and background colors.
2. **Get Board Details (GET):** Verifies that the retrieved board data matches the created parameters.
3. **Update Board (PUT):** Tests the ability to change board visibility or name.
4. **Error Handling:** Validates system response when using an invalid API Key (Expected: 401 Unauthorized).
5. **Delete Board (DELETE):** Ensures proper cleanup of resources after testing.

---

## 🧪 Automated Test Samples
I implemented JavaScript assertions in the **Tests** tab to automate verification:

```javascript
// Example: Validating Status Code and Response Time
pm.test("Status code is 200 OK", function () {
    pm.response.to.have.status(200);
});

pm.test("Response time is less than 500ms", function () {
    pm.expect(pm.response.responseTime).to.be.below(500);
});

// Example: Validating Response Body Content
pm.test("Board Name is Correct", function () {
    var jsonData = pm.response.json();
    pm.expect(jsonData.name).to.eql("My Portfolio Board");
});
