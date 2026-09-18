# STATEMENT.md

## 1. Problem Statement

Educational institutions and resource centers often face operational challenges managing reading materials, member transactions, and overdue items. Traditional manual ledgers are labor-intensive, error-prone, and lack reliable data backups. Conversely, modern web-based enterprise applications often introduce unnecessary complexity, requiring dedicated database servers, complex web frameworks, and continuous network connectivity for local operations.

There is a distinct need for a lightweight, zero-configuration, command-line Library Management System (LMS) written in Java 17. The application must operate independently of external database software, process catalog operations efficiently, enforce 14-day borrowing windows, calculate overdue fines automatically, and persist state across application restarts using local flat-file storage.

---

## 2. Scope of the Project

### In-Scope
* **Terminal Interface:** Interactive, menu-driven Command-Line Interface (CLI) built with Java 17.
* **Inventory Initialization:** Automated population of 1,000 academic records on the first execution.
* **Paginated Browsing:** High-performance catalog browsing displayed in 50-item pages with interactive terminal navigation.
* **Transaction Lifecycle:** Full issue and return tracking with automatic 14-day return date calculation.
* **Automated Penalty Engine:** Temporal late-fee calculations computed automatically upon book return.
* **Flat-File Persistence:** Automatic reading and writing of inventory and cumulative penalty data to `books.txt`.
* **Search & Analytics:** Keyword substring matching across catalog titles and real-time system metric summary reports.

### Out-of-Scope
* Graphical User Interface (GUI) or web browser frontend.
* External relational database servers (e.g., MySQL, PostgreSQL) or cloud hosting.
* Multi-user online network authentication or multi-node client-server protocols.

---

## 3. Target Users

* **Academic Librarians & Staff:** Primary operators who manage book issuing, process returns, handle user fine collections, and register new catalog entries using a fast terminal interface.
* **Resource Center Administrators:** Stakeholders requiring high-level inventory analytics, total borrowing metrics, and cumulative financial penalty tracking.
* **Library Members (Students & Faculty):** End-users whose loan periods, return deadlines, and book availability statuses are managed through staff console operations.

---

## 4. High-Level Features

* **Automated Catalog Bootstrapping:** Automatically creates and categorizes 1,000 reference items across core academic fields if no storage file is detected.
* **50-Item Paginated View:** Renders large catalog datasets in manageable 50-book pages with `Next`, `Prev`, and `Exit` page navigation.
* **Transactional Issue & Return Engine:** Records user loan assignments, sets 14-day due dates, and processes book returns using standard date formats (`dd/MM/yyyy`).
* **Dynamic Fine Calculation:** Tracks overdue returns using Java `LocalDate` and `ChronoUnit` APIs, automatically assessing fines for delayed returns.
* **Persistent Flat-File Storage (`books.txt`):** Ensures state persistence by auto-saving records and total accumulated penalties upon every transaction and application exit.
* **Title Search & Filtering:** Case-insensitive substring search engine to quickly look up availability across the entire catalog.
* **Real-Time System Metrics:** Summary dashboard displaying total catalog size, currently issued count, available inventory count, and total accumulated penalty fees.
