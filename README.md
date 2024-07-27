# Budget / Expense Tracker Application

**Description of app**: We are building a personal budgeting application that assists people in managing personal finances. Some of the app's features include an expense overview page where users can select a daily or monthly view, groups where users can enroll to track shared expenses together, recommendations on optimizing their spending, and recurring payment tracking to help users plan their monthly expenditures. The main users of the app are individuals and groups of individuals (families, students,  adults, etc.) who want to track their personal/group expenses. The dataset will be created by us, catering to the unique features provided in the application. The administrators of the database are the developers of the application.

**Description of Platform**: Our application will run on a local machine, enabling users to interact with a locally hosted web application. The app is designed to be primarily desktop-based, rather than mobile-based, providing a more comprehensive user experience. Our technology stack includes React, Flask, HTML, CSS, and JavaScript, with MySQL for our database. The live app will be hosted on a webpage instead of a command-line interface. 

**Feature Ideas for the Application**:
1. Expense Overview: A summary page where users can view their expenditures and savings over various time frames (weekly, monthly, bi-annually, yearly, etc.).
2. Expense Trends: A tool that analyzes spending and saving patterns, displaying insights on when users tend to overspend or underspend, helping them understand their financial habits.
3. Creating Tags: A feature that presents users with the ability to create categories or tags for different things they tend to spend on.
4. Financial Goals: A feature that allows users to set personal financial goals for themselves. For example, they can set how much they want to spend on a specific category each month and the app will show them if they overspend/underspend.
5. Expense Management (Smart Recommendations): A feature that offers suggestions for reallocating funds from underspent categories to other areas, optimizing users' budgets.
6. Expense Aggregation: A graphical tool that displays spending data, using pie charts and line charts to compare actual spending against set goals, helping users visualize their financial activity.
7. Recurring Payment Detection: A tool that identifies patterns in recurring payments, helping users track and manage regular expenditures.
8. Group Enrollment: A feature that allows users to join group accounts to create and manage a collective budget.
9. Group Management and Overview: A tool for group accounts where each member's expenses can be individually tracked, aggregated, and visualized, providing a comprehensive view of the group’s financial status.


**Database Info**
<br />
Our database is created with SQLite3 as written in `milestone1_db_generation.py`. To create the database, run:
`python3 milestone1_db_generation.py`
This will create a .db file in the local directory containing our sample dataset.

Once created, we can load the .db file using SQLite3 in Python:
```
# connect to the database
import sqlite3
conn = sqlite3.connect("your_db.db")

# fetch rows from a table
c = conn.cursor()
c.execute("""SELECT * FROM expenses""")
result = c.fetchall()
print(result)
```

Sample queries for the application features can be found in `sample_queries.py`, and the query outputs in `sample_outputs.txt`

Production queries can be found in `production_queries.py`, with their corresponding outputs in `production_outputs.txt`. The production DB can be found in `flask_server/production.db`.