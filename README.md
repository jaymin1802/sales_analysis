# 📊 Sales Data Analysis — EDA with Python

A complete **Exploratory Data Analysis (EDA)** project on a real-world US electronics sales dataset using Python, Pandas, NumPy, and Matplotlib. The analysis covers data cleaning, feature engineering, and multiple business insights through visualizations.

---

## 📁 Project Structure

```
sales-data-analysis/
│
├── Sales_Data/               # Raw monthly CSV files (input)
├── final_data.csv            # Merged & cleaned dataset (output)
└── sales_analysis.ipynb      # Main Jupyter Notebook (EDA)
```

---

## 📌 Dataset Overview

| Column             | Description                          |
|--------------------|--------------------------------------|
| `order_id`         | Unique identifier for each order     |
| `product`          | Product name                         |
| `quantity_ordered` | Number of units ordered              |
| `price_each`       | Price per unit (USD)                 |
| `order_date`       | Date and time of order               |
| `purchase_address` | Full delivery address of customer    |

- **Total Records:** ~1,86,850 rows
- **Time Period:** January 2019 – December 2019
- **Products:** Electronics (phones, monitors, cables, batteries, etc.)

---

## 🔧 Steps Performed

### 1. Data Merging
- Read all monthly CSV files from `Sales_Data/` folder
- Merged them into a single `final_data.csv` using `pd.concat()`

### 2. Data Cleaning
- Dropped null/NaN rows
- Removed duplicate records
- Removed corrupted rows (where column headers appeared as data)
- Fixed data types: `quantity_ordered` → `int`, `price_each` → `float`
- Parsed `order_date` to `datetime` format

### 3. Feature Engineering
- `revenue` = `quantity_ordered × price_each`
- `order_month` — extracted from `order_date`
- `order_hour` — extracted from `order_date`
- `order_city` — extracted from `purchase_address`

---

## 📈 Analysis & Visualizations

### 🗓️ Month-wise Revenue
> Which month had the highest sales?

Bar chart showing total revenue per month — December had the peak sales.

---

### 🕐 Hour-wise Trade Activity
> What time of day do customers buy the most?

Line chart showing revenue by hour — peak activity around **11 AM** and **7 PM**.

---

### 🏙️ Top 5 Cities by Revenue
> Which cities generate the most revenue?

Pie chart of the top 5 cities — San Francisco leads in sales.

---

### 📦 Product-wise Sales Revenue
> Which products earn the most?

Horizontal bar chart of all products sorted by total revenue.

---

### 📊 Product Quantity vs. Price
> Do cheaper products sell more units?

Dual-axis chart comparing quantity ordered (bar) vs. average price (line) for each product — confirms that lower-priced products like batteries and cables sell in higher volumes.

---

## 🛠️ Technologies Used

| Tool         | Purpose                        |
|--------------|--------------------------------|
| Python 3.x   | Core programming language      |
| Pandas       | Data manipulation & cleaning   |
| NumPy        | Numerical operations           |
| Matplotlib   | Data visualization             |
| Jupyter      | Interactive notebook           |

---

## 🚀 How to Run

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/sales-data-analysis.git
   cd sales-data-analysis
   ```

2. **Install dependencies**
   ```bash
   pip install pandas numpy matplotlib jupyter
   ```

3. **Launch the notebook**
   ```bash
   jupyter notebook sales_analysis.ipynb
   ```

> ⚠️ Make sure the `Sales_Data/` folder with monthly CSV files is present in the same directory before running the merging cell.

---

## 💡 Key Insights

- 📅 **December** is the highest revenue month (holiday season effect)
- 🕙 Peak buying hours are **11 AM** and **7 PM**
- 🏙️ **San Francisco** is the top city by revenue
- 🔋 **Batteries and cables** sell in the highest quantities (low price = high volume)
- 💻 **Macbook Pro** and **iPhone** contribute most to revenue despite lower quantity

---

## 👨‍💻 Author

**Jaymin** — Data Analytics Enthusiast  
B.E. Information Technology | GTU  


---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).
