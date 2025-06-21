# SQL-Interview-Questions

𝗕𝗲𝘀𝘁 𝗽𝗹𝗮𝘁𝗳𝗼𝗿𝗺𝘀 𝘁𝗼 𝗽𝗿𝗮𝗰𝘁𝗶𝗰𝗲 𝗦𝗤𝗟 𝗽𝗿𝗼𝗯𝗹𝗲𝗺𝘀 𝗱𝗮𝗶𝗹𝘆

- Dataford - https://lnkd.in/gtqdw864
- LeetCode - https://lnkd.in/gkCpv7NA
- HackerRank - https://lnkd.in/gnFS4frz
- SQLZoo - https://sqlzoo.net/
__________________________________________________________________________________________________________________________

1- Find out nth Order/Salary from the tables.

2- Find the no of output records in each join from given Table 1 & Table 2

3- YOY,MOM Growth related questions.

4- Find out Employee ,Manager Hierarchy (Self join related question) or Employees who are earning more than managers.

5- RANK,DENSERANK related questions

6- Some row level scanning medium to complex questions using CTE or recursive CTE, like (Missing no /Missing Item from the list etc.)

7- No of matches played by every team or Source to Destination flight combination using CROSS JOIN.

8-Use window functions to perform advanced analytical tasks, such as calculating moving averages or detecting outliers.

9- Implement logic to handle hierarchical data, such as finding all descendants of a given node in a tree structure.

10-Identify and remove duplicate records from a table.
_________________________________________________________________________________________________

➤ 𝗪𝗶𝗻𝗱𝗼𝘄 𝗙𝘂𝗻𝗰𝘁𝗶𝗼𝗻𝘀

1. Calculate the moving average of sales for the past 3 months.
2. Assign a dense rank to employees based on their salary.
3. Retrieve the first and last order date for each customer.
4. Find the Nth highest salary for each department using window functions.
5. Determine the percentage of total sales contributed by each employee.

➤ 𝗖𝗼𝗺𝗺𝗼𝗻 𝗧𝗮𝗯𝗹𝗲 𝗘𝘅𝗽𝗿𝗲𝘀𝘀𝗶𝗼𝗻𝘀 (𝗖𝗧𝗘)

1. Use a CTE to split a full name into first and last names.
2. Write a CTE to find the longest consecutive streak of sales for an employee.
3. Generate Fibonacci numbers up to a given limit using a recursive CTE.
4. Use a CTE to identify duplicate records in a table.
5. Find the total sales for each category and filter categories with sales greater than a threshold using a CTE.

➤ 𝗝𝗼𝗶𝗻𝘀 (𝗜𝗻𝗻𝗲𝗿, 𝗢𝘂𝘁𝗲𝗿, 𝗖𝗿𝗼𝘀𝘀, 𝗦𝗲𝗹𝗳)

1. Retrieve a list of customers who have placed orders and those who have not placed orders (Full Outer Join).
2. Find employees working on multiple projects using a self join.
3. Match orders with customers and also display unmatched orders (Left Join).
4. Generate a product pair list but exclude pairs with identical products (Cross Join with condition).
5. Retrieve employees and their managers using a self join.

➤ 𝗦𝘂𝗯𝗾𝘂𝗲𝗿𝗶𝗲𝘀

1. Find customers whose total order amount is greater than the average order amount.
2. Retrieve employees who earn the lowest salary in their department.
3. Identify products that have been ordered more than 10 times using a subquery.
4. Find regions where the maximum sales are below a given threshold.

➤ 𝗔𝗴𝗴𝗿𝗲𝗴𝗮𝘁𝗲 𝗙𝘂𝗻𝗰𝘁𝗶𝗼𝗻𝘀

1. Calculate the median salary for each department.
2. Find the total sales for each month and rank them in descending order.
3. Count the number of distinct customers for each product.
4. Retrieve the top 5 regions by total sales.
5. Calculate the average order value for each customer.

➤ 𝗜𝗻𝗱𝗲𝘅𝗶𝗻𝗴 𝗮𝗻𝗱 𝗣𝗲𝗿𝗳𝗼𝗿𝗺𝗮𝗻𝗰𝗲

1. Write a query to find duplicate values in an indexed column.
2. Analyze the impact of adding a composite index on query performance.
3. Identify columns with high cardinality that could benefit from indexing
4. Compare query execution times before and after adding a clustered index.
5. Write a query that avoids the use of an index to test performance differences.

________________________________________________________________________________________________________________________

**SQL Question 1: Identify VIP Users for Netflix**

Question: To better cater to its most dedicated users, Netflix would like to identify its “VIP users” - those who are most active in terms of the number of hours of content they watch. Write a SQL query that will retrieve the top 10 users with the most watched hours in the last month.

Tables:
• users table: user_id (integer), sign_up_date (date), subscription_type (text)
• watching_activity table: activity_id (integer), user_id (integer), date_time (timestamp), show_id (integer), hours_watched (float)

**SQL Question 2: Analyzing Ratings For Netflix Shows**

Question: Given a table of user ratings for Netflix shows, calculate the average rating for each show within a given month. Assume that there is a column for user_id, show_id, rating (out of 5 stars), and date of review. Order the results by month and then by average rating (descending order).

Tables:
• show_reviews table: review_id (integer), user_id (integer), review_date (timestamp), show_id (integer), stars (integer)

**SQL Question 3: What does EXCEPT / MINUS SQL commands do?**

Question: Explain the purpose and usage of the EXCEPT (or MINUS in some SQL dialects) SQL commands.

**SQL Question 4: Filter Netflix Users Based on Viewing History and Subscription Status**

Question: You are given a database of Netflix’s user viewing history and their current subscription status. Write a SQL query to find all active customers who watched more than 10 episodes of a show called “Stranger Things” in the last 30 days.

Tables:
• users table: user_id (integer), active (boolean)
• viewing_history table: user_id (integer), show_id (integer), episode_id (integer), watch_date (date)
• shows table: show_id (integer), show_name (text)

**SQL Question 5: What does it mean to denormalize a database?**
Question: Explain the concept and implications of denormalizing a database.

**SQL Question 6: Filter and Match Customer’s Viewing Records**

Question: As a data analyst at Netflix, you are asked to analyze the customer’s viewing records. You confirmed that Netflix is especially interested in customers who have been continuously watching a particular genre - ‘Documentary’ over the last month. The task is to find the name and email of those customers who have viewed more than five ‘Documentary’ movies within the last month. ‘Documentary’ could be a part of a broader genre category in the genre field (for example, ‘Documentary, History’). Therefore, the matching pattern could occur anywhere within the string.

Tables:
• movies table: movie_id (integer), title (text), genre (text), release_year (integer)
• customer table: user_id (integer), name (text), email (text), last_movie_watched (integer), date_watched (date)


