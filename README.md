# Data Engineering Assessment 1A

[Assessment Instructions](https://docs.google.com/document/d/1ZR54AGjCqrTMnpMC5vbkkkVD5LkKhopqOstWTWHPJSU/preview)

[General Setup and Submission Instructions](https://docs.google.com/document/d/1DyX6H6mP1bM1y35C5_xQhTWyiOnJYH46SfDVKEysyJo/preview)
# AssessmentAccountETL

DE ASSESSMENT 1

OVERVIEW
Write an ETL script to extract user data from an API into a Postgres database in the provided userAccounts.ipynb file.

QUESTION 1: Extract
A GET request to the following endpoint provides you with randomly generated user information: https://randomuser.me/api/

Make 25 requests to the endpoint and add each response into a pandas DataFrame.
Your resulting DataFrame should be 25 rows and 34 columns.
Take advantage of pandas’ json_normalize() function
Each request should have at least a one second wait before the next request


QUESTION 2:  Transform
Using the DataFrame from Question 1:
Create the following columns:
na_user: boolean representing if the user is based in North America (defined as: US, Mexico, or Canada)
age_at_registration: the user’s age when they registered their account
Update the phone and cell column to remove any characters except for a leading + symbol
Your DataFrame should be 25 rows and 36 columns


QUESTION 3: Load
Load the updated DataFrame from Question 2 into a Postgres table named user_accounts
Query the new postgres table in python and display the output results
Use pd.read_sql() to query your new table and verify it’s been loaded correctly









GRADING CRITERIA:
There are 10 points possible:
Question 1 (3 points)
Correct API request made (1 point)
Correct usage of pandas to create DataFrame of JSON response (1 point)
Each request pauses for at least a one second wait before the next request (1 point)
Question 2 (4 points):
Create the na_user table (1 point)
Create the age_at_registration table (1 point)
Updated the phone column to remove extra characters (1 point)
Updated the cell column to remove extra characters (1 point)
Question 3 (2 points):
Correctly load data into postgres table (1 point)
Correct usage of python to query data in postgres table (1 point)
Overall (1 point):
Notebook and code legibility, organization, readability (1 Point)

