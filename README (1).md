
# **Working with Different File Formats Using Pandas**

This project demonstrates how to work with various file formats, including CSV, TSV, JSON, and SQL, using the Pandas library in Python. It provides examples for reading from and writing to these file types, along with sample data for testing.

---

## **Prerequisites**
Before you begin, ensure you have the following installed:
- Python 3.8 or higher
- Pandas library (`pip install pandas`)

Additional libraries may be required for specific tasks:
- SQLite3 (bundled with Python)
- NumPy (optional, for numerical operations)

---

## **Installation**
Clone this repository to your local machine:
```bash
git clone <repository-url>
cd pandas-file-formats
```

Install dependencies:
```bash
pip install pandas numpy
```

---

## **Usage**
### **1. CSV Files**
#### Read a CSV File:
```python
import pandas as pd

# Load the CSV file
df = pd.read_csv('data.csv')

# View the first 5 rows
print(df.head())
```

#### Write to a CSV File:
```python
df.to_csv('output.csv', index=False)
```

---

### **2. TSV Files**
#### Read a TSV File:
```python
df = pd.read_csv('data.tsv', sep='\t')
print(df.head())
```

#### Write to a TSV File:
```python
df.to_csv('output.tsv', sep='\t', index=False)
```

---

### **3. JSON Files**
#### Read a JSON File:
```python
df = pd.read_json('data.json')
print(df.head())
```

#### Write to a JSON File:
```python
df.to_json('output.json', orient='records', lines=True)
```

---

### **4. SQL Databases**
#### Read from an SQL Database:
```python
import sqlite3

# Connect to the database
conn = sqlite3.connect('database.db')

# Query the database
query = "SELECT * FROM table_name"
df = pd.read_sql_query(query, conn)
print(df.head())
```

#### Write to an SQL Database:
```python
df.to_sql('table_name', conn, if_exists='replace', index=False)
```

---

## **Sample Dataset**
Sample data files (`data.csv`, `data.tsv`, `data.json`, `database.db`) are provided in the `/data` directory to help you test the scripts.

---

## **Project Structure**
```
pandas-file-formats/
│
├── data/                # Sample data files
│   ├── data.csv
│   ├── data.tsv
│   ├── data.json
│   └── database.db
│
├── examples/            # Example scripts
│   ├── read_csv.py
│   ├── read_tsv.py
│   ├── read_json.py
│   └── read_sql.py
│
└── README.md            # Documentation
```

---

## **Contributing**
Contributions are welcome! Feel free to open an issue or submit a pull request for improvements or additional file format support.

---

## **License**
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---

## **Author**
**Kishor**

Feel free to reach out for any questions or suggestions! 😊
