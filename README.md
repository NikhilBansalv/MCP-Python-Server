# 🚀 MCP Server & Database Integration using Python

A Python-based **Model Context Protocol (MCP)** server built using **FastMCP** that exposes database operations as MCP tools. The project integrates a local SQLite database and demonstrates how AI clients such as **Claude Desktop** and a custom **Python client** can interact with backend services through MCP.

---

## 📌 Project Overview

This project was developed as part of my internship to understand and implement the **Model Context Protocol (MCP)**.

The server exposes database operations through MCP tools, allowing AI applications and clients to interact with a structured SQLite database.

The project demonstrates:

- Building an MCP server using FastMCP
- Integrating a SQLite database with multiple tables
- Exposing database operations as MCP tools
- Connecting through a Python client
- Integrating with Claude Desktop
- Automated testing using pytest

---

## ✨ Features

- ✅ Python-based MCP Server using FastMCP
- ✅ SQLite Database Integration
- ✅ Users, Products and Orders Database
- ✅ CRUD Operations
- ✅ Search Functionality
- ✅ Parameterized SQL Queries
- ✅ Structured JSON Responses
- ✅ Logging
- ✅ Python MCP Client
- ✅ Claude Desktop Integration
- ✅ Automated Testing using pytest

---

## 🛠 Tech Stack

| Technology     | Purpose                 |
| -------------- | ----------------------- |
| Python 3.13    | Programming Language    |
| FastMCP        | MCP Server Framework    |
| SQLite         | Local Database          |
| pytest         | Automated Testing       |
| Claude Desktop | MCP Client              |
| MCP Inspector  | Tool Testing            |
| VS Code        | Development Environment |

---

## 🏗 System Architecture

```text
                 Claude Desktop
                       │
                       │
                (MCP Tool Calls)
                       │
                       ▼
            ┌─────────────────────┐
            │    FastMCP Server   │
            │      server.py      │
            └─────────────────────┘
                  │         │
                  ▼         ▼
             MCP Tools   Logging
                  │
                  ▼
             Database Layer
                 db.py
                  │
                  ▼
            SQLite Database
      (Users • Products • Orders)
```

---

## 📂 Project Structure

```text
mcp-python-server/
│
├── client.py              # Python MCP client
├── server.py              # FastMCP server exposing database tools
├── db.py                  # Database access layer
├── seed.py                # Creates and seeds the SQLite database
├── requirements.txt
├── pytest.ini
├── README.md
│
├── tests/
│   ├── test_db.py         # Database tests
│   └── test_tools.py      # MCP tool tests
│
└── .gitignore
```

---

## 🗄 Database Schema

The project uses a **SQLite** database consisting of three tables.

### Users

| Column | Type    |
| ------ | ------- |
| id     | INTEGER |
| name   | TEXT    |
| email  | TEXT    |

### Products

| Column   | Type    |
| -------- | ------- |
| id       | INTEGER |
| name     | TEXT    |
| category | TEXT    |
| price    | REAL    |
| stock    | INTEGER |

### Orders

| Column     | Type    |
| ---------- | ------- |
| id         | INTEGER |
| user_id    | INTEGER |
| product_id | INTEGER |
| quantity   | INTEGER |
| order_date | TEXT    |

---

## 🔧 MCP Tools

### User Tools

| Tool          | Description           |
| ------------- | --------------------- |
| get_all_users | Retrieve all users    |
| get_user      | Retrieve a user by ID |
| search_user   | Search users by name  |
| add_user      | Add a new user        |
| remove_user   | Delete a user         |

---

### Product Tools

| Tool             | Description              |
| ---------------- | ------------------------ |
| get_all_products | Retrieve all products    |
| get_product      | Retrieve a product by ID |
| search_product   | Search products          |

---

### Order Tools

| Tool           | Description         |
| -------------- | ------------------- |
| get_all_orders | Retrieve all orders |

---

## 🚀 Installation & Setup

Clone the repository

```bash
git clone https://github.com/<your-username>/mcp-python-server.git

cd mcp-python-server
```

Create a virtual environment

```bash
python -m venv venv
```

Activate the environment

```bash
venv\Scripts\activate
```

Install dependencies

```bash
pip install -r requirements.txt
```

Generate the SQLite database

```bash
python seed.py
```

---

## ▶ Running the Project

### Start the MCP Server

```bash
mcp dev server.py
```

### Run the Python Client

```bash
python client.py
```

### Execute Tests

```bash
pytest
```

Expected Output

```text
===========================
10 passed
===========================
```

---

## 🤖 Claude Desktop Integration

The MCP server can be integrated with Claude Desktop using the MCP configuration file.

Once configured, Claude Desktop can directly invoke the available MCP tools.

Example prompts:

- Show all users.
- List all products.
- Search for Laptop.
- Show all orders.
- Create a new user.

---

## 🧪 Testing

Automated testing was implemented using **pytest**.

The test suite validates:

- Database operations
- CRUD functionality
- Search operations
- Invalid user handling
- Invalid product handling
- MCP tool responses

Current Status

✅ 10 Tests Passed

---

## 📷 Screenshots
