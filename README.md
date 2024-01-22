# project-2

# Crowdfunding_ETL

# Overview
The purpose of this ETL mini project is to build an ETL pipeline that processes crowdfunding campaign data. We uses Python, Pandas and data transformation techniques to extract data from Excel files, perform necessary transformations, create CSV files, design a relational database schema, and load the data into a Postgres database.
Crowdfunding dataset contains information on backers who made pledges to live projects. Perform the ETL (extract, transform and load) process on the dataset.

# Resources :
PgAdmin 4
Visual Studio Code
Jupyter Notebook
QuickDBD

# Steps performed: 

# Category and Subcategory DataFrames :
We extracted data from the "crowdfunding.xlsx" file to create a category DataFrame.
The category DataFrame contained category_IDs and category.
We performed similar extraction to create a subcategory DataFrame.
The subcategory DataFrame contained subcategory_IDs and subcategory.
Both DataFrames were exported to "category.csv" and "subcategory.csv" respectively.
We uses list comprehension it creates a new list cat_ids by iterating over each category_id in the existing list category_ids and appending a new string to the cat_ids list for each category_id. The new string is created using an f-string, which allows for the embedding of expressions inside curly braces. In this case, the expression "cat{category_id}" is embedded inside the f-string to create the new string for each category_id.

# Campaign DataFrame :
We extracted campaign data from the "crowdfunding.xlsx" file.
The campaign DataFrame underwent various transformations, including data type conversions and renaming of columns.
UTC times were converted to datetime format for "launch_date" and "end_date".
Category and subcategory IDs were added to link with the respective DataFrames.
The transformed campaign DataFrame was exported to "campaign.csv".