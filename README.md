# Home Sales Analysis with PySpark

This project involves analyzing home sales data using PySpark. The tasks include creating temporary tables, running SQL queries, caching tables, partitioning data, and comparing runtimes.

## Installation

To run this project, you need to have PySpark and Java installed. Follow the instructions below to set up your environment.

### Setting Up the Environment

1. Install Java:
    ```bash
    apt-get update
    apt-get install openjdk-11-jdk-headless -qq > /dev/null
    ```

2. Install PySpark:
    ```bash
    wget -q http://www.apache.org/dist/spark/spark-3.4.0/spark-3.4.0-bin-hadoop3.tgz
    tar xf spark-3.4.0-bin-hadoop3.tgz
    pip install -q findspark
    ```

3. Set Environment Variables:
    ```bash
    export JAVA_HOME="/usr/lib/jvm/java-11-openjdk-amd64"
    export SPARK_HOME="/content/spark-3.4.0-bin-hadoop3"
    ```

4. Initialize PySpark:
    ```python
    import findspark
    findspark.init()
    ```

## Usage

To run the notebook, follow these steps:

1. Clone the repository
  

2. Open the `Home_Sales.ipynb` notebook in jupyter lab or as a colab file and run the cells to perform the analysis.

## Project Structure
## Tasks

1. **Read the Data:**
    - Read the home sales data from the provided URL into a Spark DataFrame.

2. **Create Temporary Table:**
    - Create a temporary table from the DataFrame.

3. **SQL Queries:**
    - Calculate average prices for different criteria:
        - Average price for a four-bedroom house sold per year.
        - Average price for homes built in each year with 3 bedrooms and 3 bathrooms.
        - Average price for homes built in each year with 3 bedrooms, 3 bathrooms, 2 floors, and at least 2,000 square feet.
        - Average price of homes per "view" rating with an average home price of at least $350,000.

4. **Caching and Uncaching:**
    - Cache the temporary table and run queries to compare runtimes.

5. **Partitioning:**
    - Partition the data by the "date_built" field and run queries on the partitioned data.


