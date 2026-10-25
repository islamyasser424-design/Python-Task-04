# 🐍 Python Programming Lab: Functions & Practical Data Processing (Task 04)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/islamyasser424-design/Python-Task-04/blob/main/Python_Task_04.ipynb)
![Python Version](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Focus](https://img.shields.io/badge/Focus-Functions%20%26%20Data%20Processing-blue?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen?style=for-the-badge)

A collection of beginner-friendly Python function exercises, moving from basic calculations and text handling to practical examples involving sales, employee records, shopping carts, student grades, and bank accounts.

---

## 📌 Table of Contents
- [📖 Overview](#-overview)
- [🎯 Learning Objectives](#-learning-objectives)
- [🧩 Exercises & Solutions](#-exercises--solutions)
- [📊 Data Analytics Applications](#-data-analytics-applications)
- [💻 Getting Started & Execution](#-getting-started--execution)
- [👤 Author & Connect](#-author--connect)

---

## 📖 Overview

This task focuses on writing reusable Python functions with `def`, passing parameters, and returning results with `return`. The exercises use basic programming tools such as conditional statements, loops, lists, strings, and dictionaries.

The notebook starts with small problems and gradually introduces practical data-processing scenarios. The solutions use core Python concepts without requiring external data-analysis libraries.

**Notebook:** [Python_Task_04.ipynb](Python_Task_04.ipynb)

---

## 🎯 Learning Objectives

- Define and call Python functions using parameters and return values.
- Use `if`, `elif`, and `else` to handle different conditions.
- Process lists and dictionaries using `for` loops.
- Perform basic calculations, text cleaning, counting, and data aggregation.
- Reuse functions across related tasks instead of repeating code.
- Handle common cases such as empty collections and invalid inputs.

---

## 🧩 Exercises & Solutions

| Question | Topic | Main Function(s) | What It Does |
| :---: | :--- | :--- | :--- |
| Q1 | Number Classification | `check_number()` | Identifies positive, negative, and zero values. |
| Q2 | Average Calculation | `calculate_average()` | Calculates a list average using a loop. |
| Q3 | String Processing | `count_vowels()` | Counts vowels without case sensitivity. |
| Q4 | Finding Maximum | `find_largest()` | Finds the largest number without `max()` or `sort()`. |
| Q5 | Duplicate Removal | `remove_duplicates()` | Keeps unique values in their original order. |
| Q6 | Student Grade Analysis | `analyze_grades()` | Calculates averages, top scores, and counts. |
| Q7 | Password Validation | `validate_password()` | Checks password rules using basic string methods. |
| Q8 | Sales Data Merging | `merge_sales()` | Combines product sales from two dictionaries. |
| Q10 | Order & Revenue Analysis | `calculate_order_total()`, `calculate_total_revenue()`, `calculate_product_revenue()`, `find_best_selling_product()` | Summarizes order values and revenue by product. |
| Q11 | Word Frequency Analysis | `clean_text()`, `count_words()`, `find_most_common_word()`, `get_unique_words()` | Cleans text and counts repeated words. |
| Q12 | Employee Records | `add_employee()`, `update_salary()`, `get_department_employees()`, `calculate_average_salary()`, `find_highest_paid_employee()` | Manages employees and analyzes salaries. |
| Q13 | Shopping Cart | `calculate_cart_total()`, `apply_discount()`, `count_cart_items()`, `get_expensive_products()`, `checkout()` | Calculates checkout totals and discounts. |
| Q14 | Student Performance Report | `calculate_student_average()`, `assign_grade()`, `generate_report()`, `get_top_students()`, `rank_students()`, `calculate_class_statistics()` | Builds student grade reports and class statistics. |
| Q15 | Banking Operations | `check_balance()`, `deposit()`, `withdraw()`, `transfer()`, `get_richest_customer()`, `bank_report()`, `main()` | Implements basic account operations and a menu-driven program. |

> **Notebook numbering note:** Q9 is not included in the source notebook, and the Q14 section appears twice. This README follows the notebook's existing numbering.

### Example 1: Average Calculation

Calculate the average of a list using a loop, without calling `sum()`:

```python
def calculate_average(numbers):
    if len(numbers) == 0:
        return 0

    total = 0
    for number in numbers:
        total += number

    return total / len(numbers)

print(calculate_average([10, 20, 30, 40]))
# 25.0
```

### Example 2: Merging Sales Records

Combine two dictionaries by adding the sales values of matching products:

```python
def merge_sales(sales1, sales2):
    result = sales1.copy()

    for product in sales2:
        if product in result:
            result[product] += sales2[product]
        else:
            result[product] = sales2[product]

    return result

sales1 = {"Laptop": 1000, "Phone": 500}
sales2 = {"Phone": 300, "Tablet": 700}
print(merge_sales(sales1, sales2))
# {'Laptop': 1000, 'Phone': 800, 'Tablet': 700}
```

### Example 3: Total Revenue by Order

Each order includes a quantity and a price. A small function calculates the revenue of one order and can be reused when processing a collection:

```python
def calculate_order_total(order):
    return order["quantity"] * order["price"]

def calculate_total_revenue(orders):
    total = 0
    for order in orders:
        total += calculate_order_total(order)
    return total
```

---

## 📊 Data Analytics Applications

| Skill | Example from the Notebook | Data Analysis Relevance |
| :--- | :--- | :--- |
| Aggregation | Order totals and product revenue | Summarizing business transactions |
| Data Cleaning | Removing duplicates and cleaning text | Preparing raw data |
| Descriptive Statistics | Average grades, salaries, balances | Understanding numerical distributions |
| Grouping | Revenue by product and employees by department | Comparing categories |
| Validation | Password, transaction, and checkout rules | Checking input quality |
| Reporting | Student and bank reports | Turning records into summaries |

These exercises build foundational Python skills useful before moving on to larger datasets and tools such as Pandas.

---

## 💻 Getting Started & Execution

### Option 1: Google Colab (No Installation)

Open the notebook directly in your browser:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/islamyasser424-design/Python-Task-04/blob/main/Python_Task_04.ipynb)

### Option 2: Jupyter Notebook

1. Clone this repository:

   ```bash
   git clone https://github.com/islamyasser424-design/Python-Task-04.git
   cd Python-Task-04
   ```

2. Open the notebook:

   ```bash
   jupyter notebook Python_Task_04.ipynb
   ```

Run the cells in order to view and test each solution. Python and Jupyter Notebook are required for local execution; the exercises themselves rely on Python's standard features.

---

## 👤 Author & Connect

**Islam Yasser**  
*Data Analyst & Business Intelligence Specialist*

- 🌐 **Portfolio Website:** [islamyasser424-design.github.io/portfolio-](https://islamyasser424-design.github.io/portfolio-/)
- 💼 **LinkedIn Profile:** [linkedin.com/in/islam-yasser-55048b378](https://www.linkedin.com/in/islam-yasser-55048b378/)
- 🐙 **GitHub Profile:** [@islamyasser424-design](https://github.com/islamyasser424-design)
- ✉️ **Email:** [islamyasser424@gmail.com](mailto:islamyasser424@gmail.com)

---

<p align="center">
  <sub>Part of the Python Programming & Data Analytics Portfolio series. Practicing Python fundamentals through reusable functions and real-world examples.</sub>
</p>
