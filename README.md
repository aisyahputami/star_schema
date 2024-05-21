# Build a Star Schema with dbt

## Data Ingestion from CSV to BigQuery
First, let's create a virtual environment in the project folder.
![venv](https://github.com/aisyahputami/star_schema/blob/main/bigquery/myenv.png)

Then, let's create a dataset. We'll name the dataset 'warehouse'.

![dataset](https://github.com/aisyahputami/star_schema/blob/main/bigquery/dataset.png)

Next, activate the venv and run `dbt init`. The goal is to ensure that the dependencies and Python packages needed by our dbt project are well isolated from the global Python environment, while `dbt init` sets up the basic structure of the required project. Name our project 'warehouse'.

![dbt-init](https://github.com/aisyahputami/star_schema/blob/main/bigquery/dbt-init.png)

We select BigQuery as the database to be used. Also, choose [2] service_account as the authentication method, input the GCP project ID, dataset, threads, and location. Then, enter the 'warehouse' project folder, run 'dbt debug', and make sure all checks have passed.

![dbt-debug]()

Move the CSV dataset file into the taxi\seeds folder. Then, run 'dbt seed'. The function of 'dbt seed' is to load initial data or seed data into a database table. Make sure that in the BigQuery dataset 'warehouse', the table 'taxi' already exists.

![dbt-seed](https://github.com/aisyahputami/star_schema/blob/main/bigquery/dbt-debug.png)

![taxi-table](https://github.com/aisyahputami/star_schema/blob/main/bigquery/taxi-table.png)

