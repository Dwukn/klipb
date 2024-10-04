# klipb

A simple command-line clipboard manager implemented in C++. This tool allows you to store, list, and delete clipboard items using an SQLite database.

## Features

- Store clipboard items from standard input.
- List all stored clipboard items.
- Decode clipboard items.
- Delete clipboard items by ID or by search query.
- Wipe all stored items.
- Persistent storage using SQLite.

## Requirements

- C++ compiler (e.g., g++, clang++)
- SQLite development libraries
- `wl-clipboard` for clipboard operations
- (Optional) `rofi` for a graphical interface

## Installation

### Step 1: Install SQLite and Dependencies

- **On Fedora:**
  ```bash
  sudo dnf install sqlite3 libsqlite3-dev
  ```

- **On Ubuntu/Debian:**
  ```bash
  sudo apt install sqlite3 libsqlite3-dev
  ```

- **Ensure you have `wl-clipboard` installed:**
  ```bash
  sudo apt install wl-clipboard
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

### Step 4: (Optional) Install `rofi`

If you want to use `rofi` for a graphical interface:

```bash
sudo dnf install rofi
```

## Usage

Klipb provides several commands:

- **Store an item**:
  ```bash
  wl-paste | ./klipb store
  ```

- **List items**:
  ```bash
  ./klipb list
  ```

- **Decode an item**:
  ```bash
  ./klipb decode "1"  # Replace "1" with the ID of the item
  ```

- **Delete an item by ID**:
  ```bash
  echo "1" | ./klipb delete  # Replace "1" with the ID of the item
  ```

- **Delete items by query**:
  ```bash
  ./klipb delete-query "search_term"
  ```

- **Wipe all items**:
  ```bash
  ./klipb wipe
  ```

- **Check version**:
  ```bash
  ./klipb version
  ```

## Configuration

You can configure Klipb via environment variables or by specifying a configuration file. For available options, see the usage message:

```bash
./klipb -h
```

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

## Contributions

Contributions are welcome! Please open an issue or submit a pull request for any enhancements or bug fixes.
