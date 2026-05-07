# Running Stocks2Excel as a Standalone Executable

This guide explains how to package the script into a single executable file — no Python, no pip, no source code needed on the target machine. Similar to running a `.jar` in Java.

---

## Build the Executable (Do this once on your machine)

### 1. Install PyInstaller

```bash
pip install pyinstaller
```

### 2. Build the executable

```bash
pyinstaller --onefile main.py
```

This creates:

```
Stocks2Excel/
├── dist/
│   └── main          # <-- your standalone executable (main.exe on Windows)
├── build/            # temporary build files (safe to delete)
└── main.spec         # build config (safe to delete)
```

---

## Send to Another Machine

Copy these two files to the target machine:

```
main          (or main.exe on Windows)
stocks.txt    (input file with stock entries)
```

Place both files in the **same folder**.

---

## Run on the Target Machine

No installation required — just run the executable.

**Mac / Linux:**
```bash
./main
```

**Windows:**
```
main.exe
```

`stocks.xlsx` will be generated in the same folder.

---

## Platform Compatibility

The executable is OS-specific. Build it on the same OS as the target machine.

| Build machine | Runs on |
|---------------|---------|
| Mac | Mac only |
| Windows | Windows only |
| Linux | Linux only |

---

## Example

Folder on the target machine before running:
```
my-folder/
├── main
└── stocks.txt
```

After running:
```
my-folder/
├── main
├── stocks.txt
└── stocks.xlsx    ✓ generated
```

---

## Updating the Input

Just edit `stocks.txt` and re-run the executable — no rebuild needed.
