# Trello API Testing – Postman

## 📌 Description

This project contains automated API tests for Trello, created using Postman.
It simulates a complete workflow for managing boards, lists, and cards, including validation of responses using test scripts.

---

## 🚀 Features

* CRUD operations for Trello Boards
* Create and manage Lists (TODO / DONE)
* Create and move Cards between lists
* Automated test scripts (status code + response validation)
* Use of collection variables for dynamic data
* Chained requests (data passed between requests)

---

## 🛠️ Tech Stack

* Postman (API testing)
* JavaScript (Postman test scripts)

---

## 📂 Collection Structure

The collection includes the following requests:

* Get all boards
* Create board
* Get single board
* Create TODO list
* Create DONE list
* Create card
* Move card to DONE list
* Delete a board
* Get deleted board

---

## ▶️ How to Run

1. Open Postman
2. Import the collection
3. Add your credentials in collection variables:

   * `key`
   * `token`
4. Run requests individually or using Collection Runner

---

## 🧪 Test Examples

The project includes automated tests such as:

* Validate status code (200, 404)
* Verify board creation
* Validate list creation
* Validate card creation and movement
* Validate deleted resources

Example:

```javascript
pm.test("Status code is 200", function () {
    pm.response.to.have.status(200);
});
```

---

## 🔐 Variables

The project uses **collection variables** to store and reuse data between requests.

### Authentication & Configuration:

* `baseURL`
* `key`
* `token`

### Dynamic Data (generated during execution):

* `boardId`
* `todoListId`
* `doneListId`
* `cardId`
* `boardNumber`

These variables allow chaining requests and reusing data across the collection.

⚠️ API keys and tokens are NOT included for security reasons.

---

## 📊 Workflow Covered

1. Get all boards
2. Create board
3. Get created board
4. Create TODO & DONE lists
5. Create card in TODO
6. Move card to DONE
7. Delete board
8. Verify deletion

---

## 💡 Notes

* The project uses **collection variables** for simplicity and data sharing between requests
* Dynamic values (like board name) are generated during execution
* Tests validate both functionality and data integrity

---

## 📎 Author

Created as part of API Testing practice using Postman.
