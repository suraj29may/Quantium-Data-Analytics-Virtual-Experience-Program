# [Quantium Data Analytics Virtual Experience Program](https://www.theforage.com/virtual-internships/prototype/NkaC7knWtjSbi6aYv/Data-Analytics)
- This program consists of 3 tasks.
- All files are my personal submission for this program. Not Quantium's model work files.

---

### Task 1 - Data preparation and customer analytics
Conduct analysis on client's transaction dataset and identify customer purchasing behaviours to generate insights and provide commercial recommendations.

---

#### Insights:
- Top 3 total sales contributor segment are
  - Older families (Budget) $156,864
  - Young Singles/Couples (Mainstream) $147,582
  - Retirees (Mainstream) $145,169
- Young Singles/Couples (Mainstream) has the highest population, followed by Retirees (Mainstream). Which explains their high total sales.
- Despite Older Families not having the highest population, they have the highest frequency of purchase, which contributes to their high total sales.
- Older Families followed by Young Families has the highest average quantity of chips bought per purchase.
- The Mainstream category of the "Young and Midage Singles/Couples" have the highest spending of chips per purchase. And the difference to the non-Mainstream "Young and Midage Singles/Couples" are statistically significant.
- Chips brand Kettle is dominating every segment as the most purchased brand.
- Observing the 2nd most purchased brand, "Young and Midage Singles/Couples" is the only segment with a different preference (Doritos) as compared to others' (Smiths).
- Most frequent chip size purchased is 175gr followed by the 150gr chip size for all segments.

---

### Task 2 - Experimentation and uplift testing
Extend analysis from Task 1 to help identify benchmark stores to test the impact of the trial store layouts on customer sales.
- Client selected store number 77, 86 and 88 as trial stores. The goal of this task is to select 1 control store for each trial store.
- Control store will be chosen based on combined similarity magnitude of "Monthly overall sales revenue" and "Monthly number of customers" of the store with the trial stores.
- Groupby each store into monthly groups and remove stores that had less than 12 months of transaction data.
- Each groupby store has columns consisting total sales, number of customers, transactions per customer, chips per customer and the average price per unit.
- Made 2 functions that calculates trial store's correlation of chosen metric to other stores (using pandas DataFrame.corrwith method) and another that calculates normalized distance magnitude of chosen metric to other store 1 - ( (value - min_value) / (max_value - min_value) )
- The above 2 funcitons are used and averaged to compute the magnitude of similartiy for the trial stores based on Total_Sales and Number_of_Customers.
- Highest average score (average of Total_Sales and Number_of_Customers magnitude of similarity) for each trial store is chosen as the control store.
- Next phase is to assess trial store's performance compared to control store's scaled performance (scaled control store's performance to match trial store's). Used t-value to check if each trial and control store's percentage difference is statistically significant during the trial phase compared to the percentage difference during pre-trial phase.

---

#### Conclusion
- Trial store 77 and 86 had significant increase in total sales and number of customers during trial compared to control store. Trial store 88 had increases as well but insignificant.

---

### Task 3 - Analytics and commercial application
- Use analytics and insights from Task 1 and 2 to prepare a report for the client, the Category Manager.
- Used Pyramid Principle method to deliver insigths and recommendation to client in Powerpoint.

---

## Completion Certificate

![completion certificate](https://user-images.githubusercontent.com/23745118/118409665-3b90b680-b6a9-11eb-88a5-ff1c5661399b.png)
