# System Concept

Based on the [original task description](../resources/README.md) the following technical requirements extracted: 

- Due to the size of the CSV, the data should be loaded into a database and apply/tune the filtering there.
- Backend application public interface should be REST over HTTP, due to its wide support in many client devices.
- To increase a robustness and scalability, the app components should be containerised and also the database requires an HA setup
- From the functional perspective the following modules considered to be implemented:
    - Backend Sync Service (Python app with Pandas, Dask and SQLAlchemy)
    - Client Backend Application (Python app with FastAPI and SQLAlchemy)
    - Database (MySQL innoDB cluster)
  
![System Concept](system-concept.png)

# Processing the input CSV

## Data Modelling
Based on a detailed investigation on the data CSV I choose to simply keep the data in a single table reusing the original column names in the csv
- route
- org_country_code
- org_country_name
- org_station_code
- org_station_code2
- org_city_name
- dst_country_code
- dst_country_name
- dst_station_code
- dst_station_code2
- dst_city_name
- currency_code
- lowest_fare_economy_oneway
- lowest_fare_premium_oneway
- lowest_fare_economy_return
- lowest_fare_premium_return
- destination_url_economy_oneway
- destination_url_premium_oneway
- destination_url_economy_return
- destination_url_premium_return
- destination_city_image_url




# Space for improvement

## Data model fine tuning
As possible performance improvement the complete storage table can be loaded into a star schema. The possible dimensions can be: 
- Addresses
    - country_code
    - country_name
    - country_code
    - country_code2
    - city_name
    - city_image_url
- Currencies
  - currency_name 
  - currency_code
- Links
  - url_economy_oneway
  - url_premium_oneway
  - url_economy_return
  - url_premium_return

In our case only one FACT table applicable:
- Fare_Prices
  - dim_org_address
  - dim_dest_address
  - dim_currency
  - dim_link
  - fare_economy_oneway
  - fare_premium_oneway
  - fare_economy_return
  - fare_premium_return