# Incubeta take home assignment - Backend developer

## Business case

This assignment will use a real-life use-case that we also needed to solve for our existing client. However, we simplified the scenario a bit to make it solvable within 3-4 hours. In this modified scenario, we ask you to write a server application that serves client requests from a database through a REST API. For the data layer, you will get two CSV's that contains flight data. The data structure is the same for both files, but the data is different.

## Before you start - preparation

- Make sure you book enough time for yourself to complete this assignment. Based on our experience maximum 3-4 hours should be enough to deliver a solution.
- Your solution should be in a private repository. Once you created one please don't forget to invite us, so we can track your progress. Our accounts: https://github.com/S4n3L, https://github.com/miguelosana, https://github.com/baspenny
- Use commits and commit messages as you would work in our team already. We intend to check your timestamps to know how much time you needed to spend with certain tasks.
- Please make sure that your application is production-ready and runs in a docker environment. We are happy to see a good enough test coverage and a readme file that describes how we can deploy and use the application.

## Step 1

Links to the CSV files: [file_1](./feed-google-qatar-api-side.csv), [file_2](./feed-google-qatar-application-side.csv)

1. Take the second CSV file, examine the data and create a normalized data structure that represents the data.
2. Create a backend application that accepts client requests regarding the flight data and serves the requests from the database you created.
    
    Request example:
    
    - Origin
    - Destination
    - Date of departure
    
    Result example
    
    - A list of routes with ticket prices included

## Step 2

Consider the first CSV file as the primary data source of your API. Ensure that your API will synchronise with this data source periodically and the data in your database is accurate. Make sure that you remove the data that is not present in the primary source and add additional data if present.

## Step 3

Present an export in ***any*** format for the following API request:

* All direct and indirect flights from Dar es Salaam to the USA with all different prices. Departure date of start flight > 2021-11-12 and < 2021-11-22

***We wish you a great time with this assignment. Trust us: you have nothing to fear and we hope we can welcome you in our team soon! See you on the other side! :)***
