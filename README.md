# Solving an SDG Problem with Data (Choose Your SDG)

## Overview
Select a Sustainable Development Goal (SDG) that resonates with you and develop a data-driven solution to address a specific problem within that SDG. Design a database, perform data analysis, and use Microsoft Excel as the user interface.

## Objectives
- Choose an SDG and identify a specific problem to address.
- Design and implement a relational database relevant to your chosen problem.
- Write SQL queries to retrieve and analyze data.
- Use Microsoft Excel for data visualization and analysis.

## Requirements

### Part 1: SDG Selection and Problem Definition
- **SDG Selection:** Choose an SDG (e.g., SDG 3: Good Health, SDG 7: Affordable and Clean Energy).
- **Problem Definition:** Define a specific problem within your chosen SDG that can be addressed using data.

### Part 2: Database Design
- **ERD:** Design an ERD for your project, including entities relevant to your SDG problem.
- **Schema:** Write SQL statements to create the database schema based on your ERD.
- **Sample Data:** Populate the database with relevant sample data.

### Part 3: SQL Programming
- **Data Retrieval:** Write SQL queries to retrieve relevant data based on your problem definition.
- **Data Analysis:** Write SQL queries to analyze data and generate insights related to your SDG problem.

### Part 4: Data Analysis Using Excel
- **Import Data:** Import data from your database into Excel.
- **Analysis:** Analyze the data using pivot tables, charts, and other Excel tools.
- **Dashboard:** Create an interactive Excel dashboard to visualize key insights.

### Part 5: Integration and Testing
- **Integration:** Document the process of importing data into Excel and ensuring consistency.
- **Testing:** Test the integration and functionality of your Excel dashboard.

### Part 6: Presentation
- **Pitch Deck:** Develop a 10-slide PowerPoint presentation as taught in the entrepreneurship module covering:
  - Project overview and SDG alignment.
  - Problem definition and significance.
  - Database design and schema.
  - Data analysis insights.
  - Excel dashboard demonstration.
- **Delivery:** Present your pitch deck, demonstrating how your project addresses the SDG problem.

## Deliverables (upload onto this repo)
- SDG problem definition document
- ERD
- SQL scripts
- Excel workbook with data analysis and dashboard
- Integration documentation
- Pitch deck presentation (Provide the link e.g Canva or Gamma in your documentation)

[Uploading CREATE TABLE Users (
    UserID INT PRIMARY KEY,
    Name VARCHAR(100),
    Age INT,
    Income DECIMAL(12, 2)
);

CREATE TABLE Expenses (
    ExpenseID INT PRIMARY KEY,
    UserID INT,
    Category VARCHAR(50),
    Amount DECIMAL(10, 2),
    Date DATE,
    FOREIGN KEY (UserID) REFERENCES Users(UserID)
);

CREATE TABLE Savings (
    SavingID INT PRIMARY KEY,
    UserID INT,
    Amount DECIMAL(10, 2),
    Date DATE,
    FOREIGN KEY (UserID) REFERENCES Users(UserID)
);
SELECT Users.Name, COALESCE(SUM(Expenses.Amount), 0) AS TotalExpenses, COALESCE(SUM(Savings.Amount), 0) AS TotalSavings
FROM Users
LEFT JOIN Expenses ON Users.UserID = Expenses.UserID
LEFT JOIN Savings ON Users.UserID = Savings.UserID
GROUP BY Users.Name;
SELECT Users.Name, 
       (COALESCE(SUM(Savings.Amount), 0) / COALESCE(SUM(Expenses.Amount), 1)) * 100 AS SavingsRate
FROM Users
LEFT JOIN Expenses ON Users.UserID = Expenses.UserID
LEFT JOIN Savings ON Users.UserID = Savings.UserID
GROUP BY Users.Name;


expenseee.sql…]()
[assign 8.xlsx](https://github.com/user-attachments/files/16728998/assign.8.xlsx)


