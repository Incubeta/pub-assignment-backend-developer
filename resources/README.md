# Incubeta take home assignment - Backend developer
Welcome to the Incubeta take home assignment. We hope you have fun in doing this assignment and feel free to ask questions when 
you come accross anything you need clarifying.

## Business case
Incubeta is a leading digital media company and one of the things we do is providing tecnical expertise and solutions to make advertisements 
more specific and based on realtime, or near-realtime data.
This assignment is based on real-life use-case that we also needed to solve for an existing client. The client is an airline company
that wants more dynamic data to be presented in their advertisements. The API that you will design/built wil provide the advertisements with this data 
about flights and prices.

We simplified the scenario a bit to make it solvable within 3-4 hours. 
In this modified scenario, we ask you to write a server application that serves client requests from a datastore 
through a REST API written in Python. For the data layer, you will get two CSV's that contains flight data. The data structure is 
the same for both files, but the data is different.

## Before you start - preparation

> Please note that the assignment consists of three steps. We do not expect you to implement all three steps, but at least the first step is required.
> What needs to be included in the solution is an overall conceptual plan for how you would approach all the steps. How you present that is up to you.
> Of course, if you want to implement the complete solution, feel free!

- Make sure you book enough time for yourself to complete this assignment. Based on our experience maximum 3-4 hours should be enough to deliver a solution.
- Your solution should be in a private repository. Once you created one please don't forget to invite us, so we can track your progress. 
Our accounts: 
  - https://github.com/S4n3L
  - https://github.com/miguelosana
  - https://github.com/baspenny
- Use commits and commit messages as you would work in our team already. We intend to check your timestamps to know how much time you needed to spend with certain tasks.
- Please make sure that your application runs in a Docker environment. We are happy to see a good enough test coverage and a `README` file that describes how we can deploy and use the application.

## Step 1

Links to the CSV files: [file_1](file_1.csv), [file_2](file_2.csv)

1. Take the second CSV file, examine the data and create a normalized data structure that represents the data.
2. Create a backend application that accepts client requests regarding the flight data and serves the requests from the database you created.
```
Reqiurements:  
-------------
- Origin
- Destination
- Date of departure

Result example:
---------------
- A list of routes with ticket prices included
```   

## Step 2

Consider the first CSV file as the primary data source of your API. Ensure that your API will synchronise with this data source periodically 
and the data in your database is accurate (the second file is the fresh delta). Make sure that you remove the data that is not present in the primary source and add additional data if present.
```
Requirements:  
-------------
- The API cannot have any downtime when the database is updated
- The flights that are NOT in the update file, must not exist in the datastore after the update
- Updating cannot take longer that 5 minutes
```

## Step 3

Create an endpoint `trips` that can solve the following query

* All direct and indirect flights from Dar es Salaam to the USA with all different prices. Departure date of start flight > 2021-11-12 and < 2021-11-22 (for a one way, no return) 

***We wish you a great time with this assignment. Trust us: you have nothing to fear and we hope we can welcome you in our team soon! See you on the other side! :)***
