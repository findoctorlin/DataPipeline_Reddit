# Reddit Data Pipeline Engineering | AWS End to End Data Engineering

# Tools & Services

- Apache Airflow (—version 2.8.1)
- AWS Redshift data Warehouse
- AWS Glue
- Amazon S3 bucket
- Amazon Athena
- PostgreSQL

# **Prerequisites**

- Python 3.9 or higher
- AWS Account with permissions for S3, Glue, Athena, and Redshift
- Reddit API credentials
- Docker Installed

# Set-Up

```markdown
# change VScode python interpreter to the virtual environment python (3.9.6 under venv)
```

![Untitled](YT_Reddit%20Data%20Pipeline%20Engineering%20AWS%20End%20to%20End%207d38f419a92f442c8d68ca0561fe0c3e/Untitled.png)

```bash
pip freeze > requirements.txt # make sure the requirements in this virtual environment is same as mentioned
docker compose up -d --build # create containers defined in docker-compose.yml file; Build images before starting containers.
```

![Untitled](YT_Reddit%20Data%20Pipeline%20Engineering%20AWS%20End%20to%20End%207d38f419a92f442c8d68ca0561fe0c3e/Untitled%201.png)

```markdown
# Airflow deployed in Docker
```

# Project Introduction

1. ***Connect*** Airflow to Reddit instance on the cloud
2. ***Push*** the data from Airflow → S3 bucket → ***Connect*** AWS Glue
3. ***Perform*** manipulation on these data
4. ***Querying*** & ***Visualization***

# reddit_dag.py

- If you run Airflow instance in Docker, by the time you start the dag,
