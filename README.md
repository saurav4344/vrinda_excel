# My first excel project with interactive dashboard - Vrinda Sales 2022 Case Study

### This project is aimed at gaining valuable insights from customer behaviour and enhancing sales performance for upcoming years. To achieve this, it focuses on generating interactive dashboards and extracting meaningful insights from the data to perform strategic decision making.

### Below are the list of questiong strategically employed througout the project to extract meaningful insights:
1. Compare Sales and Order data
2. Which month got the highest sales and orders?
3. Who's sales were more - men or women?
4. What are different order status?
5. List top 10 states contributing to the sales
6. Relationship between age and gender bases on number of orders
7. Which channel is contrubuting which highest shares of sales?

### Below are the steps used to build the project:
1. Data Cleaning: Check for null and duplicate values, and if found any then fix it. Ensure consistency and uniformity in the dataset.
2. Data Processing: This involves simplifying and refining our raw data to align with specific questions or requirements of the project. In question 6, we aim to explore the relationship between age and gender. So to simplify this, we can group individuals into age categories instead of just using age. This simplification will help us drive insights more easily. I've created a new column 'Age Group' with the below formula:

```yml
=IF(E2<=19, "Teens", IF(AND(E2>19, E2<=35), "Adult", IF(AND(E2>35, E2<60), "Middle Aged", "Senior")))
```

Next for extracting 'Month' from the Date, I applied the following formula:

```yml
=TEXT(G2, "mmm")
```

3. Data Analysis: This is where the fun part beigns, I begin by summarizing the dataset with the help of pivot tables to answer the questions asked for the project. Afterwards, created pivot charts built on top of pivot tables. And finally made all the charts interactive with the use of slicers.
4. Insights:
  - March recorded both the highest sales and order count figures.
  - Women made more purchases compared to men.
  - A massive portion, around 92% of orders were delivered.
  - The top 10 states contributing to the highest sales are: Maharashta, Karnataka, Uttar Pradesh, Telangana, Tamil Nadu, Delhi, Kerla, West Bengal, Anddra Pradesh, Haryana.
  - Sales predominantly came from Middle Aged individuals (36 - 59 years), with women being the primary purchasers.
  - Amazon accounted for highest portion of sales ~35% followed by Myntra ~23% and Flipkart ~22%

5. Final Conclusion: Target women customers of age group (36 - 59 years) living in Maharashtra, Karnataka and Uttar Pradesh by showing ads/offers/coupons available on Amazon, Myntra and Flipkart.
