# 🚀 Trello API Testing Portfolio
**Clarence Faith B. Saligumba**

Automated functional testing project for the **Trello REST API** using **Postman** and **JavaScript**. This project demonstrates end-to-end (E2E) testing, dynamic data handling, and negative testing scenarios.

---

### 🛠️ Tech Stack
* **Testing Tool:** Postman
* **Scripting:** JavaScript (Chai Assertion Library)
* **Environment:** Postman Global & Environment Variables
* **API Target:** Trello REST API

---

### 📋 Test Scenarios
I validated the full lifecycle of Trello resources to ensure system reliability:

* **Board Management:** Full CRUD (Create, Read, Update, Delete) operations.
* **List & Card Operations:** Automated creation, updating, and archiving of lists and cards.
* **Dynamic Data Generation:** Used **Pre-request Scripts** to generate random names (e.g., *QA-Testing-Batch-1*) for every request to avoid data duplication.
* **Negative Testing:** Verified system behavior for:
    * **404 Not Found:** Confirming resources are permanently deleted.
    * **401 Unauthorized:** Testing security with invalid API keys.
    * **400 Bad Request:** Validating error handling for invalid operations.
