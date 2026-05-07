# Stocks2Excel — IDE Setup Guide

Step-by-step instructions to import and run this project in IntelliJ IDEA, Eclipse, and VS Code.

---

## 1. VS Code

### Prerequisites
- Download and install [VS Code](https://code.visualstudio.com)
- Download and install [Python 3.8+](https://www.python.org/downloads)

### Steps

**Step 1 — Install the Python extension**
- Open VS Code
- Click the Extensions icon in the left sidebar (or press `⌘⇧X` on Mac / `Ctrl+Shift+X` on Windows)
- Search for **Python** (by Microsoft) and click **Install**

**Step 2 — Open the project**
- `File → Open Folder`
- Select the `Stocks2Excel` folder
- Click **Open**

**Step 3 — Select Python interpreter**
- Press `⌘⇧P` (Mac) / `Ctrl+Shift+P` (Windows) to open Command Palette
- Type `Python: Select Interpreter` and press Enter
- Choose the interpreter from `.venv` inside the project folder, or your system Python

**Step 4 — Install dependency**
- Open the terminal: `` Ctrl+` `` or `Terminal → New Terminal`
- Run:
```bash
pip install openpyxl
```

**Step 5 — Run the script**
- Open `main.py`
- Click the **Run** button (▶) at the top right
- Or in the terminal:
```bash
python main.py
```

**Output:** `stocks.xlsx` is generated in the project folder.

---

## 2. IntelliJ IDEA

### Prerequisites
- Download and install [IntelliJ IDEA](https://www.jetbrains.com/idea/download) (Community edition is free)
- Install the **Python plugin** inside IntelliJ
- Download and install [Python 3.8+](https://www.python.org/downloads)

### Steps

**Step 1 — Install the Python plugin**
- Open IntelliJ IDEA
- Go to `IntelliJ IDEA → Settings` (Mac) / `File → Settings` (Windows)
- Navigate to `Plugins → Marketplace`
- Search for **Python** and click **Install**
- Restart IntelliJ when prompted

**Step 2 — Open the project**
- Click `File → Open`
- Select the `Stocks2Excel` folder
- Click **OK** → select **Open as Project** if prompted

**Step 3 — Configure Python SDK**
- Go to `File → Project Structure`
- Under **Project**, click `SDK → Add SDK → Python SDK`
- Select **New virtual environment** or point to your existing Python installation
- Click **OK**

**Step 4 — Install dependency**
- Open the terminal: `View → Tool Windows → Terminal`
- Run:
```bash
pip install openpyxl
```

**Step 5 — Run the script**
- Open `main.py`
- Right-click anywhere in the editor → **Run 'main'**
- Or click the green **Run** button (▶) in the top toolbar

**Output:** `stocks.xlsx` is generated in the project folder.

---

## 3. Eclipse

### Prerequisites
- Download and install [Eclipse IDE](https://www.eclipse.org/downloads) (Eclipse IDE for Java Developers is fine)
- Install the **PyDev** plugin for Python support
- Download and install [Python 3.8+](https://www.python.org/downloads)

### Steps

**Step 1 — Install the PyDev plugin**
- Open Eclipse
- Go to `Help → Eclipse Marketplace`
- Search for **PyDev** and click **Install**
- Accept the license and restart Eclipse when prompted

**Step 2 — Configure Python interpreter**
- Go to `Eclipse → Preferences` (Mac) / `Window → Preferences` (Windows)
- Navigate to `PyDev → Interpreters → Python Interpreter`
- Click **New** → **Browse** → locate your Python executable (e.g. `/usr/bin/python3` on Mac)
- Click **OK** to apply

**Step 3 — Import the project**
- Go to `File → New → Project`
- Expand **PyDev** → select **PyDev Project** → click **Next**
- Set **Project name** to `Stocks2Excel`
- Uncheck **Create default src folder**
- Click **Finish**
- Right-click the project in the Project Explorer → `Import → File System`
- Browse to the `Stocks2Excel` folder → select `main.py` and `stocks.txt` → click **Finish**

**Step 4 — Install dependency**
- Open the terminal (outside Eclipse) or use `Window → Show View → Terminal`
- Run:
```bash
pip install openpyxl
```

**Step 5 — Run the script**
- Right-click `main.py` in the Project Explorer
- Select `Run As → Python Run`

**Output:** `stocks.xlsx` is generated in the project folder.

---

## Quick Reference

| IDE | Plugin Needed | Run Shortcut |
|-----|--------------|--------------|
| VS Code | Python (Microsoft) | `▶` button or `python main.py` in terminal |
| IntelliJ IDEA | Python plugin | Right-click → Run 'main' |
| Eclipse | PyDev | Right-click → Run As → Python Run |
