# 🍽️ Zomato Restaurant Data Analysis (Python EDA)

Exploratory Data Analysis (EDA) on 148 Zomato restaurant listings using Python, Pandas, Matplotlib and Seaborn. The project looks at restaurant types, customer votes, ratings, spending for two people, and how online ordering relates to ratings.

💡 Built while following the online tutorial "Zomato Data Analysis Using Python" (GeeksforGeeks).

---

## 📸 Project Preview

![Order mode by restaurant type](images/order-mode-heatmap.png)

| Restaurant types | Votes by type | Ratings distribution |
|---|---|---|
| ![Types](images/restaurant-types.png) | ![Votes](images/votes-by-type.png) | ![Ratings](images/ratings-distribution.png) |

| Cost for two | Online vs offline ratings |
|---|---|
| ![Cost](images/cost-for-two.png) | ![Boxplot](images/online-vs-offline-ratings.png) |

---

## 📌 Project Objectives

- ✅ Analyze the types of restaurants listed on Zomato
- ✅ Understand customer voting and rating patterns
- ✅ Compare online and offline ordering
- ✅ Find the most common spending level for two people
- ✅ Visualize insights with count plots, histograms, box plots and heatmaps

---

## 📁 Dataset

File: `data/Zomato_data_.csv`: 148 restaurant listings, 7 columns, no missing values.

| Column | Description |
|---|---|
| `name` | Restaurant name |
| `online_order` | Whether the restaurant accepts online orders (Yes/No) |
| `book_table` | Whether table booking is available (Yes/No) |
| `rate` | Rating out of 5 (stored as text like "4.1/5") |
| `votes` | Number of customer votes |
| `approx_cost(for two people)` | Approximate cost for two people (₹) |
| `listed_in(type)` | Restaurant type: Dining, Cafes, Buffet or other |

---

## 🔧 Analysis Workflow

### 1️⃣ Data cleaning
- Converted the `rate` column from text (for example `4.1/5`) to a float
- Checked data types with `info()` and confirmed there are no null values

```python
def handleRate(value):
    value = str(value).split('/')
    return float(value[0])

dataframe['rate'] = dataframe['rate'].apply(handleRate)
```

### 2️⃣ Exploratory analysis

| # | Question | Chart |
|---|---|---|
| 1 | Which restaurant type is listed most? | Count plot |
| 2 | Which type gets the most votes? | Group by + plot |
| 3 | Which restaurant has the most votes? | `max()` filter |
| 4 | Do more restaurants accept online orders? | Count plot |
| 5 | What ratings do most restaurants get? | Histogram |
| 6 | What cost for two is most common? | Count plot |
| 7 | Do online-order restaurants rate higher? | Box plot |
| 8 | Which types get online vs offline orders? | Pivot table + heatmap |

---

## 🔑 Key Findings

- **Restaurant types:** Dining is the most common type (110 of 148, 74%), followed by Cafes (23), other (8) and Buffet (7).
- **Votes:** Dining restaurants receive 52% of all 39,192 votes. The most voted restaurant is Empire Restaurant (4,884 votes, rated 4.4).
- **Ratings:** Ratings range from 2.6 to 4.6 with an average of 3.63. 72 restaurants (49%) are rated between 3.5 and 4.0.
- **Spending:** ₹300 is the most common cost for two (23 restaurants), and the median is ₹400.
- **Online ordering:** 58 restaurants (39%) accept online orders and 90 (61%) do not. Online-order restaurants average a 3.86 rating versus 3.49 for the rest.
- **Order mode by type:** 70% of Dining restaurants do not take online orders, while 65% of Cafes do.
- **Table booking:** Only 8 restaurants offer booking, and they average 4.19 compared with 3.60 for the rest.

> Note: the dataset has 148 restaurants, so findings show patterns in this sample and may not represent all of Zomato.

---

## 🚀 How to Run

1. Clone the repository
   ```bash
   git clone https://github.com/Anil-analytics-maker/zomato-restaurant-eda-python.git
   cd zomato-restaurant-eda-python
   ```
2. Install the libraries
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```
3. Start Jupyter and open the notebook
   ```bash
   jupyter notebook
   ```
4. Run all cells. The dataset is read from `data/Zomato_data_.csv`.

---

## 🧰 Tools Used

Python • Pandas • NumPy • Matplotlib • Seaborn • Jupyter Notebook

---

## 📚 What I Learned

- Cleaning text columns and converting data types
- Exploratory data analysis with Pandas
- Choosing the right chart: count plots, histograms, box plots and heatmaps
- Turning charts into business insights

---

## 👨‍💻 About Me

Hi, I'm **Anil**, a B.Tech Civil Engineering student at Delhi Technological University, building a career in data analytics with SQL, Python, Excel, Power BI and Tableau.

## 🚀 Let's Connect

- 💼 LinkedIn: https://www.linkedin.com/in/anildtu27
- 💻 GitHub: https://github.com/Anil-analytics-maker
- 📧 Email: anil_23bt012@dtu.ac.in
