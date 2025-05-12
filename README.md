# 📺 Netflix Dataset Cleaning with pandas

This project focuses on cleaning and preprocessing the [Netflix Titles Dataset](https://www.kaggle.com/shivamb/netflix-shows) using Python and pandas. The notebook includes missing value handling, text standardization, and date formatting for better data quality and analysis readiness.

---

## 📂 Dataset

The dataset used: `netflix_titles.csv`

It contains metadata about Netflix content including title, cast, country, release date, duration, and more.

---

## ✅ Tasks Performed

### 1. **Initial Exploration**
- Loaded the dataset with `pandas.read_csv()`.
- Displayed first few records using `.head()`.
- Explored data types and summary statistics using `.info()` and `.describe()`.

---

### 2. **Handling Missing Values**

#### a. Identifying Nulls
- Used `.isnull().sum()` to count missing values per column.
- Identified which columns contain null values.

#### b. Dropping Null Values (Option 1)
- Created a cleaned version of the dataset using `df.dropna()`.

#### c. Filling Null Values (Option 2)
- For key columns with missing values like:
  - `director`, `cast`, `country`, `date_added`, `rating`, and `duration`
- Filled missing entries with `"Unknown"` using `.fillna()`.

---

### 3. **Text Cleaning and Standardization**

- Applied `.str.lower()` to standardize text in `gender` and `country` fields (if present).
- Mapped multiple variations of values (e.g., `"usa"`, `"U.S.A."`, `"us"` → `"united states"`).

---

### 4. **Date Parsing and Formatting**

- Used `pd.to_datetime()` to convert the `date_added` column from string to datetime.
- Re-formatted the dates to `dd-mm-yyyy` string format using `.dt.strftime('%d-%m-%Y')`.

---

## 🛠️ How to Run

1. Clone this repository:
   ```bash
   git clone https://github.com/your-username/netflix-data-cleaning.git
   cd netflix-data-cleaning
   ```

2. Install required packages:
   ```bash
   pip install pandas numpy jupyter
   ```

3. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

---

## 📁 Project Structure

```
netflix-data-cleaning/
├── netflix_cleaning.ipynb   # Jupyter notebook with all steps
├── README.md
├── requirements.txt         # Optional: use `pip freeze > requirements.txt`
└── .gitignore               # Recommended to avoid logs, checkpoints, etc.
```

---

## 📝 License

This project is open-source and available under the [MIT License](LICENSE).
