# klipb

A simple command-line clipboard manager implemented in C++. This tool allows you to store, list, and delete clipboard items using an SQLite database.

## Features

- Store clipboard items from standard input.
- List all stored clipboard items.
- Delete clipboard items by ID.
- Persistent storage using SQLite.

## Requirements

- C++ compiler (e.g., g++, clang++)
- SQLite development libraries

## Installation

### Step 1: Install SQLite

- **On Fedora:**
  ```bash
  sudo dnf install sqlite3 libsqlite3-dev
  ```
### Step 2: Clone the Repository

```bash
git clone https://github.com/dwukn/klipb.git
cd klipb
```

### Step 3: Compile the Code

Use the following command to compile the code:

```bash
g++ -o klipb klipb.cpp -lsqlite3
```





## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contributions

Contributions are welcome! Please open an issue or submit a pull request for any enhancements or bug fixes.
