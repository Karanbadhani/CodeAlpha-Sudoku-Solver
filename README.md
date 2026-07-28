# 🧩 Professional Sudoku Solver System

> **CodeAlpha C++ Programming Internship - Task 3**
<p align='center'>
  <img src='screenshots/banner.png' alt='Sudoku Solver Banner' width='900'/>
</p>

<p align='center'>
  <img src='https://img.shields.io/badge/C%2B%2B-17-blue?style=for-the-badge&logo=c%2B%2B' alt='C++17'/>
  <img src='https://img.shields.io/badge/OOP-Enabled-success?style=for-the-badge' alt='OOP'/>
  <img src='https://img.shields.io/badge/STL-Used-orange?style=for-the-badge' alt='STL'/>
  <img src='https://img.shields.io/badge/Backtracking-Optimized-purple?style=for-the-badge' alt='Backtracking'/>
  <img src='https://img.shields.io/badge/License-MIT-green?style=for-the-badge' alt='License'/>
  <img src='https://img.shields.io/badge/Platform-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey?style=for-the-badge' alt='Platform'/>
</p>

<p align='center'>
  <b>A production-style Sudoku Solver built with modern C++17, showcasing OOP, STL, recursion, backtracking, file handling, and clean software architecture.</b>
</p>

---

## 🚀 Why This Project?

This is not just a basic Sudoku solver. It is a **feature-rich, portfolio-quality application** designed to demonstrate:

* **Object-Oriented Design**
* **STL Usage**
* **Recursive Backtracking**
* **File Handling**
* **Input Validation**
* **Modular Architecture**
* **Console UI Design**
* **Performance Tracking**
* **Optional GUI Integration (SFML)**

Perfect for:

* 💼 **Internship applications**
* 📄 **Resume projects**
* 🎯 **Technical interviews**
* 🎓 **College submissions**
* 🌟 **GitHub portfolio**

---

## ✨ Features

### 🔹 Core Features

* ✅ Solve any valid **9×9 Sudoku**
* ✅ Optimized **recursive backtracking**
* ✅ **Row / Column / 3×3 validation**
* ✅ Manual puzzle entry
* ✅ Load puzzle from file
* ✅ Save solved puzzle
* ✅ Reset to original puzzle
* ✅ Clean formatted board display

### 🔹 Advanced Features

* 🎯 **Hint System**
* 🎲 **Random Puzzle Generator**
* 📊 **Difficulty Detection** (Easy / Medium / Hard / Expert)
* 📈 **Statistics Dashboard**
* 🔄 **Step-by-Step Solving**
* 🎨 **Dark & Light Theme**
* ⌨️ **Keyboard Shortcuts**
* 📝 **Solve History**
* 📋 **Application Logging**
* 👤 **User Profiles**
* 🏆 **Leaderboard**

### 🔹 Technical Highlights

* 🧪 **C++17**
* 🏗️ **OOP Architecture**
* 📦 **STL Containers**
* 🔒 **Const Correctness**
* ⚡ **Exception Handling**
* 🧹 **Warning-Free Compilation**
* 📄 **File I/O**

---

## 🛠️ Tech Stack

| Technology            | Purpose                   |
| --------------------- | ------------------------- |
| **C++17**             | Core language             |
| **OOP**               | Software architecture     |
| **STL**               | Efficient data structures |
| **Recursion**         | Backtracking solver       |
| **File I/O**          | Puzzle persistence        |
| **ANSI Escape Codes** | Console UI                |
| **SFML (Optional)**   | GUI support               |

---

## 📁 Project Structure

```text
SudokuSolver/
├── main.cpp
├── Sudoku.h
├── Sudoku.cpp
├── FileManager.h
├── FileManager.cpp
├── README.md
├── LICENSE
├── sample_input.txt
├── solved_output.txt
├── history.txt
├── logs.txt
├── config.txt
├── screenshots/
├── docs/
└── assets/
```

---

## ⚡ Quick Start

### Compile

```bash
g++ -std=c++17 *.cpp -o SudokuSolver
```

### Run

```bash
./SudokuSolver
```

### GUI Mode (Optional)

```bash
g++ -std=c++17 *.cpp -o SudokuSolver -lsfml-graphics -lsfml-window -lsfml-system
./SudokuSolver --gui
```

---

## 🎮 Usage

### Main Menu

| Option | Action                |
| ------ | --------------------- |
| 1      | Enter Sudoku Manually |
| 2      | Load Sudoku From File |
| 3      | Display Sudoku        |
| 4      | Validate Puzzle       |
| 5      | Solve Puzzle          |
| 6      | Hint                  |
| 7      | Generate Puzzle       |
| 8      | Save Solution         |
| 9      | View Statistics       |
| 10     | Reset Puzzle          |
| 11     | Settings              |
| 12     | Exit                  |

### Keyboard Shortcuts

| Key   | Action   |
| ----- | -------- |
| **S** | Solve    |
| **R** | Reset    |
| **H** | Hint     |
| **L** | Load     |
| **V** | Validate |
| **G** | Generate |
| **Q** | Quit     |

---

## 🧠 Algorithm

### Backtracking Strategy

1. Find an empty cell.
2. Try numbers **1–9**.
3. Check whether the number is valid.
4. Place the number.
5. Recursively solve the remaining puzzle.
6. If no solution exists, **backtrack**.

```text
solve(board):
    cell = findEmpty()
    if no cell:
        return true

    for num in 1..9:
        if isSafe(cell, num):
            place num
            if solve(board):
                return true
            remove num

    return false
```

---

## 📈 Complexity Analysis

| Metric            | Complexity   |
| ----------------- | ------------ |
| Time Complexity   | **O(9^n)**   |
| Space Complexity  | **O(n)**     |
| Validation        | **O(1)**     |
| Puzzle Generation | **Variable** |

Where **n** is the number of empty cells.

---

## 📊 Sample Performance

| Difficulty | Avg Time | Recursive Calls | Backtracks |
| ---------- | -------- | --------------- | ---------- |
| Easy       | < 0.01s  | ~500            | ~100       |
| Medium     | < 0.05s  | ~5,000          | ~1,000     |
| Hard       | < 0.1s   | ~50,000         | ~10,000    |
| Expert     | < 0.5s   | ~500,000        | ~100,000   |

---

## 🖼️ Screenshots

<p align='center'>
  <img src='screenshots/menu.png' width='700' alt='Main Menu'/>
</p>

<p align='center'>
  <img src='screenshots/solving.png' width='700' alt='Solving Process'/>
</p>

<p align='center'>
  <img src='screenshots/statistics.png' width='700' alt='Statistics'/>
</p>

---

## 🌟 What Makes This Project Stand Out?

* ✔️ **Professional folder structure**
* ✔️ **Modular source code**
* ✔️ **Real-world software design**
* ✔️ **Comprehensive documentation**
* ✔️ **GitHub-ready presentation**
* ✔️ **Interview-friendly implementation**
* ✔️ **Cross-platform support**
* ✔️ **Optional graphical interface**

---

## 🔮 Future Improvements

* [ ] WebAssembly browser version
* [ ] Android / iOS app
* [ ] Multiplayer Sudoku
* [ ] Cloud synchronization
* [ ] AI-based solving strategies
* [ ] Support for 4×4, 6×6, 16×16 boards
* [ ] Speedrun mode
* [ ] Database integration
* [ ] Automated unit tests

---

## 🤝 Contributing

Contributions are welcome! Please fork the repository and submit a pull request.

---

## 📄 License

This project is licensed under the **MIT License**.

---

## 👨‍💻 Author

**Karan Badhani**

- B.Tech Computer Science Engineering Student
- CodeAlpha C++ Programming Intern
- Passionate about C++, Data Structures, Algorithms, and Software Development

---

## ⭐ Support

If you found this project useful, please consider **starring the repository**. It helps the project reach more developers and motivates further improvements.

---
---

## 📌 Internship Information

- **Internship:** CodeAlpha C++ Programming Internship
- **Task:** Task 3 – Sudoku Solver
- **Language:** C++17
