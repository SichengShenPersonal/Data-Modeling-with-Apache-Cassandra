## Project Overview
In this project, I applied data modeling concepts with Apache Cassandra to complete an ETL pipeline using Python. The goal was to model the data by creating tables in Apache Cassandra and run specific queries based on business needs. Part of the ETL pipeline was provided, which transfers data from multiple CSV files in a directory into a single streamlined CSV file. This processed data was then modeled and inserted into tables within Apache Cassandra for efficient querying.

## Datasets
The project uses a single dataset: `event_data`. This dataset contains CSV files partitioned by date, such as:
- `event_data/2018-11-08-events.csv`
- `event_data/2018-11-09-events.csv`

Each file contains records of events that needed to be processed and stored in a denormalized format in Apache Cassandra tables.

## Project Template
The project workspace includes a Jupyter notebook template. This notebook guides through the project’s main tasks, including:
- Processing the `event_datafile_new.csv` dataset to create a denormalized dataset.
- Designing data tables aligned with the queries to be run.
- Writing queries to create data tables in Apache Cassandra.
- Loading data into the tables and executing the queries.

## Project Steps
The following steps outline the key tasks required to complete the project:

### 1. Modeling the NoSQL Database
- **Design Tables**: Based on the required queries, I designed tables in Apache Cassandra.
- **Create Keyspace**: Wrote `CREATE KEYSPACE` and `SET KEYSPACE` statements.
- **Define Tables**: Developed `CREATE TABLE` statements for each table to answer specific questions, ensuring data is organized for optimal query performance.
- **Insert Data**: Loaded data into the tables using `INSERT` statements.
- **Create and Drop Tables**: Added `IF NOT EXISTS` clauses in `CREATE` statements to avoid duplicating tables. Included `DROP TABLE` statements to easily reset tables during testing and troubleshooting.
- **Query Testing**: Verified table designs and data by running appropriate `SELECT` statements with `WHERE` clauses.

### 2. Building the ETL Pipeline
- **Process Event Files**: In Part I of the notebook, implemented logic to iterate through each CSV file in `event_data`, creating a new consolidated CSV file.
- **Load Data into Apache Cassandra**: In Part II, added `CREATE` and `INSERT` statements in the notebook to load processed records into tables aligned with the data model.
- **Query Testing**: After loading data, verified accuracy by running `SELECT` statements to ensure the data model met the requirements.
