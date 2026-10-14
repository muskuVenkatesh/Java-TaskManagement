# Task Management Application

A simple, modular Java application with a web-based browser interface and an optional console CLI. **No build tools or external dependencies required.**

---

## 📁 Directory Structure

```
JavaApplication/
├── .gitignore
├── README.md
├── bin/                                       # Compiled class files
└── src/                                       # Source code
    └── com/
        └── taskmanager/
            ├── Main.java                      # Application launcher
            ├── model/
            │   └── Task.java                  # Task data model
            ├── service/
            │   └── TaskService.java           # Business logic & thread-safe storage
            └── web/
                └── TaskWebServer.java         # Built-in HTTP server & web UI
```

---

## 🚀 How to Run in Browser

### Step 1: Compile
From the `JavaApplication` root directory:
```bash
javac -d bin $(find src -name "*.java")
```

### Step 2: Start the Web Server
```bash
java -cp bin com.taskmanager.Main
```

### Step 3: Open in Browser
Open your web browser (Chrome, Safari, Firefox, Edge) and go to:
```
http://localhost:8081
```

*(To stop the server, press `Ctrl + C` in your terminal)*

---

## 🖥️ Optional Console (CLI) Mode
If you ever want to run the terminal-based menu instead of the browser:
```bash
java -cp bin com.taskmanager.Main --cli
```

---

## 📋 Features in Browser UI
- **Dashboard Stats**: Real-time counter for Total, Completed, Pending tasks, and progress bar.
- **Add Tasks**: Form to add tasks with title and category (Work, Personal, Development, QA, Setup).
- **Interactive Checkboxes**: Toggle tasks complete/pending instantly.
- **Filter Tabs**: Filter by *All*, *Pending*, or *Completed*.
- **Search Bar**: Live search filtering by keyword.
- **Delete Tasks**: Remove tasks with one click.
