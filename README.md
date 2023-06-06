# DVDRENTAL-SQL-ANALYSIS

## INTRODUCTION
The database DvdRental has 15 tables. Below are the different tables and a brief description of them.

actor — contains actors data including first name and last name.
film — contains films data such as title, release year, length, rating, etc.
film_actor — contains the relationships between films and actors.
category — contains film’s categories data.
film_category — containing the relationships between films and categories.
store — contains the store data including manager staff and address.
inventory — stores inventory data.
rental — stores rental data.
payment — stores customer’s payments.
staff — stores staff data.
customer — stores customer’s data.
address — stores address data for staff and customers
city — stores the city names.
country — stores the country names.
Note: I analyzed this database using PostgreSQL. You can get details to install PostgreSQL here and download the DVD rental database here.

Objective & Goals
In this project, I’ll aim to answer the following questions:

What are the top and least rented (in-demand) genres and what are their total sales?
Can we know how many distinct users have rented each genre?
What is the average rental rate for each genre? (from the highest to the lowest)
How many rented films were returned late, early, and on time?
In which countries does Rent A Film have a presence and what is the customer base in each country? What are the total sales in each country? (from most to least)
Who are the top 5 customers per total sales and can we get their details just in case Rent A Film wants to reward them?
Before getting started with analyses, I first tried understanding the ERM (Entity Relationship Model) of this database also known as Schema. Here is the Schema below:

Re5gkP7yWnJhl7p84eVLeVRxixkh9Po284s0
DVD RENTAL SCHEMA
You can view my code on my GitHub profile here.

Analysis
To answer the first question “What are the top and least rented (in-demand) genres and what are what are their total sales?”, I first identified with tables I would need to Join, which are:

Category >film_Category >film>inventory>rental >customer >payment
Below is the query I used to extract to answer the question:
