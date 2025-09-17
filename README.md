# 📚 My Study Tracker App


The **My Study Tracker App** is a **console-based Java application** designed to help students systematically **log, track, summarize, and export study activities**.  
It demonstrates practical usage of **Java Collections, File I/O, and Object-Oriented Design** in a real-world, utility-driven project.

---

## ✨ Key Features
- **Insert Study Log**  
  Record study sessions with:
  - 📅 Date (auto-generated using `LocalDate`)  
  - 📖 Subject  
  - ⏱ Duration  
  - 📝 Description  

- **Display Logs**  
  View all study logs stored in memory.

- **Summary by Date**  
  Calculate & display total study hours grouped by date.

- **Summary by Subject**  
  Calculate & display total study hours grouped by subject.

- **Export to CSV**  
  Export all study logs into `MarvellousStudy.csv` for offline tracking.

- **User-Friendly Console Menu**  
  Simple, menu-driven interface with **switch-case navigation**.

---

## 🛠️ Technologies Used
- **Language:** Java  
- **Packages & APIs:**  
  - `java.util.*` → Data structures (`ArrayList`, `TreeMap`) & user input (`Scanner`).  
  - `java.time.LocalDate` → Auto-capture current date.  
  - `java.io.*` → File handling & CSV export.  

---

## 🔄 Project Flow
1. Launch the application → Main Menu displayed.  
2. **Choice 1:** Insert new study log → User enters subject, duration, description → Date auto-generated.  
3. **Choice 2:** Display all study logs stored in memory.  
4. **Choice 3:** Display summary grouped by **date** (total hours per day).  
5. **Choice 4:** Display summary grouped by **subject** (total hours per subject).  
6. **Choice 5:** Export all study logs to `MarvellousStudy.csv`.  
7. **Choice 6:** Exit application.  

---

## 🏗️ Classes & Responsibilities
### `StudyLog`
- Represents a single study session.  
- **Attributes:**  
  - `LocalDate date`  
  - `String subject`  
  - `double duration`  
  - `String description`  
- **Methods:** Constructor, getters, `toString()`  

### `StudyTracker`
- Manages all logs in memory.  
- **Attributes:**  
  - `ArrayList<StudyLog> database`  
- **Methods:**  
  - `InsertLog()`  
  - `DisplayLog()`  
  - `SummaryByDate()`  
  - `SummaryBySubject()`  
  - `ExportCSV()`  

### `StudyTrackerApp` (Main Class)
- Contains `main()` method.  
- Handles **menu-driven interface & user input**.  
- Calls methods from `StudyTracker`.  

---

## 💻 Example Usage (Console Flow)

====== Marvellous Study Tracker ======

Insert Study Log

Display All Logs

Summary By Date

Summary By Subject

Export to CSV

Exit

Enter choice: 1
Enter Subject: Java Programming
Enter Duration (hours): 2.5
Enter Description: Practiced ArrayList and TreeMap
Study log added successfully for date: 2025-09-13


---

## 📂 Sample Exported CSV (`MarvellousStudy.csv`)
```csv
Date,Subject,Duration,Description
2025-09-13,Java Programming,2.5,Practiced ArrayList and TreeMap
2025-09-13,Database,1.5,Revised SQL Joins