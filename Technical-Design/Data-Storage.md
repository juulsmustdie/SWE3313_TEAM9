# Data Storage Plan

This document outlines the data storage strategy for our cafe menu application.  
We will store all essential data in JSON files to make sure our data persists between sessions and behaves like a real-world application.  

The goal is to use a lightweight, readable format that integrates smoothly with Python and doesn't require a full database system—ideal.


## Storage Format Choice: JSON
- We chose **JSON** because it is readable, easy to work with in Python (thanks to the JSON module), and suitable for small-scale applications like ours.  
- JSON will be used to store data persistently between sessions (users, orders, menus, etc.).

---

## Technologies & Libraries 
- **Python Standard Library:**
  - JSON module – Reading and writing JSON files.
  - OS module – Checking for file existence and handle file paths.
- **Flask Framework:**
  - Routing and handling HTTP requests.
  - No ORM or database layer is needed since JSON will act as the database.

---

## Data Storage Workflow

1. **Check for Existing Data on Startup**
   - On app start, check if the JSON data file exists.
   - If it exists, load the data into Python structures (dictionaries/lists).
   - If it does not exist, create an empty structure and write it to a new JSON file.

2. **Read Data**
   - Use _with open()_ and _json.load()_ to read data from the JSON file.
   - Parse the data into Python dictionaries/lists for in-app use.

3. **Write Data**
   - After adding, editing, and/or deleting data (such as new order or updated user info), use _json.dump()_ to save the updated Python structure back to the JSON file.
   - This allows our application to persist change across sessions.

4. **File Organization**
   - Store data files in a dedicated _data/_ or _storage/_ folder (such as data/users.json, data/orders.json, etc.).
   - Use separate files for different data types to maintain both clarity and modularity (no one likes disorganization).

---

## Example Files

| Data Type      | File Name          | Description                            |
|----------------|--------------------|----------------------------------------|
| Users          | users.json         | Stores registered user info            |
| Orders         | orders.json        | Stores all orders made by users        |
| Menu Items     | menu.json          | Stores available menu items            |
| Admin Settings | admin.json         | Stores admin-related configuration     |

---

## Handling Errors
- Use _try_ or _except_ blocks when reading or writing files to handle issues involving file not found, corruption, etc.
- Implement backups or temporary files during write operations if/when needed.
