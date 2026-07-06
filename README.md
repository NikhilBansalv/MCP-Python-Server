# MCP Python Server & Database Integration Project

## Overview

This project demonstrates a Python-based MCP (Model Context Protocol) server integrated with a local SQLite database. The server exposes database operations as MCP tools, and a Python client communicates with the server to access these tools.

---

## Technologies Used

- Python
- FastMCP
- SQLite
- MCP Python SDK
- VS Code

---

## Project Structure

mcp-intern-project/
│
├── server.py
├── client.py
├── db.py
├── seed.py
├── database.db
├── requirements.txt
├── README.md
├── test_db.py
└── test_cases.txt

---

## Features

- MCP server implementation
- SQLite database integration
- Database-backed MCP tools
- Python MCP client
- Error handling
- Logging
- Tool testing using MCP Inspector

---

## Database Tools

### 1. get_all_users()

Returns all users from the database.

### 2. get_user(user_id)

Returns a single user using ID.

### 3. search_user(name)

Searches users by name.

---

## Setup Instructions

### 1. Create Virtual Environment

```bash
python -m venv venv
```
