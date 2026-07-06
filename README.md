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
