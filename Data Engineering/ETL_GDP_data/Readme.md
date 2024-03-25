# ETL GDP Data

## Introduction

This project encompasses the development of an Extract, Transform, and Load (ETL) pipeline for GDP data retrieval. The aim is to extract data from a specified URL, transform it into a desired format, and load it into both a CSV file and a database. Additionally, the process involves running a query on the database table and logging the execution progress.

## Project Scenario

The project revolves around the creation of an automated script capable of extracting GDP data of various countries, sorting it based on their GDP in billion USDs, and processing it for accessibility. The International Monetary Fund (IMF) releases this data semi-annually, necessitating a script that can fetch and process updated information.

**URL:** 
'https://web.archive.org/web/20230902185326/https://en.wikipedia.org/wiki/List_of_countries_by_GDP_%28nominal%29'

The data is required to be available in two formats:

1. **CSV File:** `Countries_by_GDP.csv`
2. **Database Table:** `Countries_by_GDP` in `World_Economies.db`, with attributes `Country` and `GDP_USD_billion`.

To validate the success of the script, a query on the database table is required to display entries with a GDP exceeding 100 billion USD. Furthermore, the execution process needs to be logged in a file named `etl_project_log.txt`.

## Objectives

The primary objectives of this project are as follows:

1. Write a data extraction function to retrieve relevant information from the provided URL.
2. Transform the extracted GDP information into billion USD format.
3. Load the transformed information into the required CSV file and database.
4. Execute a query on the database table.
5. Log the code execution progress with appropriate timestamps.

## Initial Setup

Before commencing with the project, ensure the installation of necessary libraries:

- **requests**: For accessing information from the URL.
- **bs4**: Contains the BeautifulSoup function for web scraping.
- **pandas**: For data processing and storage.
- **sqlite3**: Required for creating a database server connection.
- **numpy**: Needed for mathematical rounding operations.
- **datetime**: Contains the datetime function for logging purposes.

Use the following commands in the terminal to install the libraries:

```bash
python3.11 -m pip install pandas
python3.11 -m pip install numpy
python3.11 -m pip install bs4
```

## Task Breakdown

The project tasks are segmented as follows:

1. **Task 1: Extracting information**
2. **Task 2: Transforming information**
3. **Task 3: Loading information**
4. **Task 4: Querying the database table**
5. **Task 5: Logging progress**

## Function Calls

Set up the sequence of function calls for the assigned tasks as per the following table:

| Task                       | Log Message on Completion             |
|----------------------------|---------------------------------------|
| Declaring known values    | Preliminaries complete. Initiating ETL process. |
| Call extract() function   | Data extraction complete. Initiating Transformation process. |
| Call transform() function | Data transformation complete. Initiating loading process. |
| Call load_to_csv()        | Data saved to CSV file. |
| Initiate SQLite3 connection | SQL Connection initiated. |
| Call load_to_db()         | Data loaded to Database as table. Running the query. |
| Call run_query()          | Process Complete. |
| Close SQLite3 connection | |

## Important Note

Due to potential delays or connection errors with the archive server, it's recommended to retry the code execution if encountering issues. Alternatively, you can switch to the live version of the URL provided in the scenario.

## Conclusion

Congratulations on completing this project! By successfully executing complex ETL operations on real-world data, you've gained valuable experience in:

- Extracting data from websites using web scraping and requests API.
- Transforming data into desired formats.
- Loading processed data into local files or database tables.
- Querying database tables using Python.
- Creating comprehensive logs of all conducted operations.