# ETL - Basic

**Date: (June 29, 2016)**

ETL or *Extract - Transform - Load* is a process done in data warehousing. It is used when:
- You want to aggregate data from different sources into one collection (the warehouse)
- You want to select and arrange only the pertinent information for any kind of analytic, and provide his/her own user view of the data (Data mart)
- You want to clean the data and make meaningful sense out of it.

ETL can be broken down to three major steps:
1. Extract
    - The part where you gather data from different data sources (csv files, databases, etc...). Data can also come from different data warehouses.
    - It should be designed to avoid negative effects on source system such as its performance, response time, or any kind of data locking.
2. Transform
    - Making the extracted data usable.
    - This includes mapping the data, matching rows, enhancing data, summarizing data, etc.
    - Transformation also includes standardizing data (such as currency and time formats) and handling encoding
3. Load
    - Fetches prepared data and storing them to the data warehouse and database, or data mart.

Source: [ETL Tutorial | Extract Transform and Load](https://www.youtube.com/watch?v=WZw0OTgCBOY)
