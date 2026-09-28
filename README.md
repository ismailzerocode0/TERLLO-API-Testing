# Trello API E2E Testing & Automation Collection

A robust, end-to-end (E2E) Postman collection for testing the [Trello REST API](https://developer.atlassian.com/cloud/trello/). This project covers complete CRUD operations across core Trello resources: **Boards**, **Lists**, **Cards**, and **Checklists**, complete with automated test scripts and environment variable management.

---

## 🚀 Features

- **End-to-End Scenarios:** Automates the complete lifecycle from creating a Board to adding Lists, Cards, and Checklists, and cleaning them up afterward.
- **Automated ID Chaining:** Automatically captures IDs (like `boardID`, `ListID`, `cardID`, `checklistID`) from responses and stores them in collection/environment variables for subsequent requests.
- **Built-in Test Scripts:** Includes comprehensive assertions using Postman's `pm.test` to validate:
  - Status codes (e.g., `200 OK`)
  - Response payload structures and schema properties
  - Data integrity (e.g., ensuring a card belongs to the correct list)
- **Global Test Hooks:** Pre-request scripts and global test assertions to track response times, validate JSON structures, and log API errors gracefully.

---

## 📋 Collection Structure & Priority

The requests follow a strict execution priority (`Create` ➔ `Update` ➔ `Delete` ➔ `Get`):

| Section | Requests Included |
| :--- | :--- |
| **Board** | Create Board, Update Board, Get Board, Delete Board, Get Board checks |
| **List** | Create List, Update List, Get List, Archive/Unarchive List |
| **Card** | Create Card, Update Card, Get Card, Delete Card, Get Card Checks |
| **CheckList** | Create Checklist, Update Checklist, Get Checklist, Delete Checklist |

---

## ⚙️ Prerequisites & Setup

1. **Postman:** Make sure you have [Postman](https://www.postman.com/) installed on your machine.
2. **Trello Account & API Credentials:**
   - Get your **API Key** from your Trello account developer page.
   - Generate a token with **Read, Write, and Account** permissions.

---

## 📥 Installation & Usage

1. **Clone or Download:**
   Clone this repository or download the `TERLLO APIS.postman_collection.json` file.
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   ```

2. **Import into Postman:**
   - Open Postman.
   - Click the **Import** button in the top left.
   - Drag and drop the downloaded JSON file into the import window.

3. **Configure Environment Variables:**
   Set up your Postman Environment with the following variables (or use the collection variables pre-configured in the file):
   - `base_url`: `https://api.trello.com`
   - `Key`: Your Trello API Key
   - `token`: Your Trello Token (with Write privileges)

4. **Run the Collection:**
   - Open the **Collection Runner** in Postman.
   - Select the `Terllo-Apis` collection.
   - Hit **Run TERLLO APIS** to execute the entire E2E test suite automatically!

---

## 📊 Google Sheets Reference
You can view the detailed execution mapping and dependency matrix sheet here:
[Trello APIs Sheet Reference](https://docs.google.com/spreadsheets/d/1VH0P7eIIIy4qhgtCyVHc0bxUzEIzhUywshlvywm_XK0/edit?usp=sharing)

---

## 🤝 Contributing
Contributions, issues, and feature requests are welcome! Feel free to check issues page or submit a pull request.
