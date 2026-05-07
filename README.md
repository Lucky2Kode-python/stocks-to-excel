# Stocks2Excel

Converts a plain text file containing stock ticker entries into a formatted Excel spreadsheet with three columns: **Name**, **Exchange**, and **Symbol**.

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| Python 3.8+ | Core language |
| `re` (built-in) | Regex parsing of stock text formats |
| `openpyxl` | Excel file creation and styling |

---

## Supported Input Formats

The parser handles three common ways stock tickers appear in text:

| Format | Example | Name | Exchange | Symbol |
|--------|---------|------|----------|--------|
| `Name (EXCHANGE: SYMBOL)` | `Bloom Energy (NYSE: BE)` | Bloom Energy | NYSE | BE |
| `(EXCHANGE: SYMBOL)` | `(NYSEARCA: XLE)` | *(empty)* | NYSEARCA | XLE |
| `EXCHANGE: SYMBOL` | `NASDAQ: MRVL` | *(empty)* | NASDAQ | MRVL |

---

## How It Works

1. **Read** — reads `stocks.txt` line by line
2. **Parse** — each line is matched against 3 regex patterns (most specific to least specific) to extract name, exchange, and symbol
3. **Write** — creates `stocks.xlsx` using `openpyxl` with a styled header row and auto-fitted column widths

---

## Project Structure

```
Stocks2Excel/
├── main.py        # Main script
├── stocks.txt     # Input file (edit this with your tickers)
├── stocks.xlsx    # Output file (generated on run)
└── README.md
```

---

## Local Setup & Usage

### 1. Install dependency

```bash
pip install openpyxl
```

### 2. Edit `stocks.txt`

Add your stock entries, one per line. Mix and match formats freely:

```
Bloom Energy (NYSE: BE)
Alphabet Inc. (NASDAQ: GOOGL)
(NYSEARCA: XLE)
BATS: NANC
NASDAQ: MRVL
NYSE: STZ
RTX (NYSE: RTX)
MU (NASDAQ: MU)
```

### 3. Run the script

```bash
python main.py
```

### 4. Open the output

The file `stocks.xlsx` is created in the same directory. Open it in Excel, Numbers, or Google Sheets.

---

## Example Output

| Name | Exchange | Symbol |
|------|----------|--------|
| Bloom Energy | NYSE | BE |
| Alphabet Inc. | NASDAQ | GOOGL |
| | NYSEARCA | XLE |
| | BATS | NANC |
| | NASDAQ | MRVL |
| | NYSE | STZ |
| RTX | NYSE | RTX |
| MU | NASDAQ | MU |

---

## Running in PyCharm

1. Open `main.py`
2. Right-click → **Run 'main'** or press `⌃R`
3. `stocks.xlsx` will appear in the project root
