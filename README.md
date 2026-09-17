# Library Management System

A lightweight, high-performance command-line Library Management System built with Java 17. The application manages inventory cataloging, member transactions, fine calculations, and persistent file storage without requiring external database server dependencies.

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

├── Main.java          # Application entry point, CLI loops, and file persistence handlers
└── books.txt          # Persistent data file (Auto-generated on first run)
