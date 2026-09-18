# Library Management System

**Author Information**
* **Name:** Lakshya Bhardwaj
* **Registration No.:** 24BEC10118
* **Course:** Programming in Java

---

## Overview

The **Library Management System** is a lightweight, zero-configuration command-line application engineered in Java 17. Designed for educational resource centers and academic libraries, the system automates core library administrative workflows—including catalog tracking, member loan transactions, overdue fine calculations, and persistent flat-file storage—without requiring external database management systems or complex server setups.

---

## Key Features

* **Automated Catalog Initialization:** Pre-populates a catalog of 1,000 domain-specific books across multiple academic categories.
* **Paginated Browsing:** Displays catalog listings in manageable 50-book pages with interactive terminal controls (`Next`, `Prev`, `Exit`).
* **Issue & Return Mechanics:** Manages user assignments, automated 14-day due date calculations, and late return validation.
* **Penalty System:** Tracks overdue returns and calculates penalties at a rate of ₹10 per delayed day, accumulating total fines collected across sessions.
* **Keyword Search:** Supports real-time sub-string search across book titles.
* **File Persistence:** Automatically saves and loads library state and collected fines using `books.txt`.

---

## Tech Stack

* **Language:** Java 17 (OpenJDK)
* **API Libraries:** `java.util`, `java.io`, `java.time`
* **Data Storage:** Flat-file persistence (`books.txt`) via `BufferedReader` / `BufferedWriter`

## Project Structure

```text

.
├── Library-management-system/
│   ├── Main.java          # Core application source code
│   └── books.txt          # Persistent data storage file
├── README.md              # Project documentation
└── statement.md           # Problem statement and project scope
