# 🛒 Smart Store Management and Sales Analysis

A menu-driven Python application that helps a retail store manager manage products, process customer purchases, keep sales records, and analyse sales performance, all from the console.

Built with plain Python (no external libraries), in a Jupyter Notebook.

---

## ✨ Features

| # | Option | What it does |
|---|--------|--------------|
| 1 | **View All Products** | Lists every product with ID, name, category, price and stock. Items at or below the low-stock limit are flagged `(Low)`. |
| 2 | **Search Product** | Search by product ID, name (partial match) or category. |
| 3 | **Purchase Product** | Validates the product, quantity and stock, deducts stock, records the sale and warns if stock becomes low. |
| 4 | **View Sales History** | Shows all sales with sale ID, product, quantity, total, customer and order number, plus total transactions and revenue. |
| 5 | **Sales Analysis** | Total revenue, units sold, transactions, average sale value, best-selling products, revenue by category and top customers by spend. |
| 6 | **Low Stock Products** | Lists products at or below the threshold (default `10`), sorted by lowest stock first. |
| 7 | **Exit** | Closes the program. |

---

## 📦 Sample Data

The store starts with 7 products across 5 categories:

| ID | Name | Category | Price | Stock |
|----|------|----------|-------|-------|
| P001 | Wireless Mouse | Electronics | Rs. 599.00 | 45 |
| P002 | Bluetooth Headphones | Electronics | Rs. 1,499.00 | 8 |
| P003 | Notebook A5 | Stationery | Rs. 60.00 | 120 |
| P004 | Ballpoint Pen Pack | Stationery | Rs. 45.00 | 5 |
| P005 | Ceramic Mug | Kitchen | Rs. 249.00 | 30 |
| P006 | LED Desk Lamp | Home | Rs. 899.00 | 15 |
| P007 | Yoga Mat | Fitness | Rs. 799.00 | 4 |

---

## 🚀 Getting Started

### Prerequisites
- Python 3.8 or newer
- Jupyter Notebook or JupyterLab

### Run it

```bash
# 1. Clone the repository
git clone https://github.com/<your-username>/<your-repo-name>.git
cd <your-repo-name>

# 2. Launch Jupyter
jupyter notebook "smart store management and sales analysis.ipynb"
```

Run all cells from top to bottom (**Kernel → Restart & Run All**). The last cell starts the interactive menu and asks for your choice (1-7).

---

## 🧠 How It Works

- **Products** are stored as a list of dictionaries (`product_id`, `name`, `category`, `price`, `stock`).
- **Sales** are stored as a list of dictionaries, one per purchase, with an auto-generated sale ID (`S0001`, `S0002`, ...) and order number.
- **Helper functions** (`find_product`, `format_money`, `print_table`) keep the display and lookup logic reusable.
- **Sales analysis** uses dictionaries to aggregate units and revenue per product, per category and per customer.
- **Input validation** covers unknown product IDs, non-numeric or zero quantities, and quantities above available stock. A blank customer name becomes `Walk-in Customer`.

### Project structure

```
.
├── smart store management and sales analysis.ipynb   # all code and the main menu
└── README.md
```

---

## 📸 Example Menu

```
=================================================
     SMART STORE MANAGEMENT & SALES ANALYSIS
=================================================
1. View All Products
2. Search Product
3. Purchase Product
4. View Sales History
5. Sales Analysis
6. Low Stock Products
7. Exit
=================================================
Enter your choice (1-7):
```

---

## 🔧 Possible Improvements

- Save products and sales to a CSV/JSON file or database so data persists between runs
- Add, edit and delete products from the menu
- Multi-item shopping carts and discounts/tax
- Real timestamps for sales instead of an order counter
- Charts for sales trends (matplotlib / pandas)

---

## 🛠 Built With

- Python 3
- Jupyter Notebook

---

## 📄 License

This project is open source. Add a license of your choice (e.g. MIT) before publishing.
