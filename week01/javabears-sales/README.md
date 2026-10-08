# Assignment: Creating a DataFrame in Pandas

## Tasks
### Part 1 – Construct the DataFrame
Using a Python dictionary or a NumPy array format, construct a Pandas DataFrame named coffee_sales.

Your DataFrame must map out the row records and product columns to match the following raw business data exactly:
```py
Year (Index)	Americano	Latte	Espresso	Cappuccino
2021 Sales	5628	12426	852	8522
2022 Sales	6239	25384	756	7561
```

Hint: Ensure your column headers and index rows match the naming conventions above.

### Part 2 – Data Manipulation
Write the Pandas code necessary to perform the following operations on your matrix:

Calculate Total Product Volume: Find the cumulative sales for each distinct beverage type across the entire two-year timespan. Append or display this total safely.

Year-over-Year (YoY) Growth: Calculate the percentage growth rate for each beverage type from 2021 to 2022.

### Part 3 – Business Insights & Strategy
Using Pandas operations (such as row/column sorting or maximum/minimum index locators), answer the following queries within your notebook using clear Markdown cells:

Identify the absolute best-selling and least-selling beverage for both 2021 and 2022.

## Write a brief 1–2 paragraph strategic analysis explaining what these sales figures suggest for JavaBeans' leadership. Which products deserve higher marketing spend? Are there any drinks that might need to be phased out or redesigned based on their YoY trajectory?

### Submission Guidelines
Submit your completed project workspace containing:

pyproject.toml (your tracking manifest).

uv.lock (your generated lockfile).

dataframe_creation.ipynb (fully executed with markdown headers, code comments, visible outputs, and your written strategy analysis).