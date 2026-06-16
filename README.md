# Zomato Data Analysis Project

## 📌 Project Overview
This project analyzes Zomato restaurant data to understand customer preferences, restaurant categories, ratings, votes, online ordering behavior, and approximate cost for two people. The analysis uses Python libraries to clean, explore, and visualize the dataset, helping identify useful business insights for restaurants and food delivery platforms.

## 🎯 Objective
The main objective of this project is to perform exploratory data analysis (EDA) on Zomato restaurant data and answer questions such as:

- Which restaurant type is most common?
- Which restaurant category receives the highest votes?
- What is the common rating range for restaurants?
- What approximate cost do couples usually prefer?
- Do online orders receive better ratings than offline orders?
- Which restaurant types prefer online or offline ordering?

## 🛠️ Tools and Technologies Used

- **Python**
- **Pandas**
- **NumPy**
- **Matplotlib**
- **Seaborn**
- **Jupyter Notebook**

## 📂 Dataset
The project uses a Zomato restaurant dataset containing information such as:

- Restaurant name
- Online order availability
- Ratings
- Votes
- Restaurant type
- Approximate cost for two people
- Listed category/type

> Dataset file used in the notebook: `Zomato data .csv`

## 🔍 Project Workflow

### 1. Importing Libraries
Python libraries such as Pandas, NumPy, Matplotlib, and Seaborn were imported for data handling and visualization.

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
```

### 2. Loading the Dataset
The dataset was loaded into a Pandas DataFrame.

```python
dataframe = pd.read_csv("Zomato data .csv")
```

### 3. Data Cleaning
The `rate` column was cleaned by removing the `/5` format and converting the values into float data type.

```python
def handleRate(value):
    value = str(value).split('/')
    value = value[0]
    return float(value)

dataframe['rate'] = dataframe['rate'].apply(handleRate)
```

### 4. Exploratory Data Analysis
Different visualizations were created to analyze restaurant types, votes, ratings, approximate cost, and online ordering behavior.

## 📊 Visualizations Performed

### Restaurant Type Distribution
A count plot was created to identify the most common restaurant type.

**Insight:** Most restaurants belong to the **Dining** category.

### Votes by Restaurant Type
The total votes were grouped by restaurant type and visualized using a line plot.

**Insight:** **Dining restaurants** received the maximum number of votes.

### Ratings Distribution
A histogram was used to analyze the distribution of restaurant ratings.

**Insight:** Most restaurants received ratings between **3.5 and 4.0**.

### Approximate Cost for Couples
A count plot was used to analyze the approximate cost preferred by couples.

**Insight:** Most couples prefer restaurants with an approximate cost of around **₹300 for two people**.

### Online vs Offline Order Ratings
A box plot was used to compare ratings between online and offline orders.

**Insight:** Offline orders received lower ratings compared to online orders.

### Online Order Preference by Restaurant Type
A heatmap was created to compare online and offline ordering behavior across restaurant types.

**Insight:** Dining restaurants mainly receive offline orders, while cafes receive more online orders.

## ✅ Key Business Insights

- Dining restaurants are the most common restaurant category in the dataset.
- Dining restaurants received the highest customer votes.
- Most restaurant ratings are concentrated between 3.5 and 4.0.
- Couples generally prefer restaurants costing around ₹300 for two people.
- Online orders tend to receive better ratings than offline orders.
- Cafes show stronger online ordering behavior, while dining restaurants are more offline-order focused.

## 📈 Business Impact
This analysis can help restaurant owners and food delivery platforms understand customer behavior, improve online ordering services, optimize pricing strategies, and focus on restaurant categories with higher customer engagement.

## 🚀 How to Run This Project

1. Clone this repository:

```bash
git clone https://github.com/your-username/zomato-data-analysis.git
```

2. Open the project folder:

```bash
cd zomato-data-analysis
```

3. Install the required libraries:

```bash
pip install pandas numpy matplotlib seaborn
```

4. Open the Jupyter Notebook:

```bash
jupyter notebook
```

5. Run the notebook file:

```text
Zomato_data_analysis_project.ipynb
```

## 📌 Conclusion
The Zomato Data Analysis Project provides useful insights into restaurant trends, customer ratings, voting patterns, cost preferences, and online ordering behavior. The findings show that dining restaurants dominate the dataset, online orders generally perform better in ratings, and pricing around ₹300 for two people is popular among customers.

## 👨‍💻 Author

**Mouryan Kosare**


