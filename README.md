# Data_Engineer_Challenge
Data Engineer Project 
# Building a Data Warehousing Pipeline using Python Docker, Airflow, PostgreSQL and Dbt

## Software Requirements
* Python
* VS Code
* Docker
* PostgreSQL GUI (dBeaver or pgAdmin)
* Web Browser (Chrome, Firefox, Edge)

## How to Run
* Clone this repository
```
git clone https://github.com/rwurdig/Data_Engineer_Challenge.git
```
* Open the project folder using VS Code
* Open or run Docker Desktop
* Open command line or terminal, and write
```
docker network create etl_network
```
and then
```
docker-compose build
```
and then
```
docker-compose up airflow-init
```
and then
```
docker-compose up -d
```
* Open browser and type localhost:8080 on the address bar
* Login to Airflow using user: airflow and password: airflow
* Open or click on ETL Pipeline DAG, and click Trigger DAG or play button
* ETL Pipeline will running on the background

After all tasks finished, we can clean up the environment using below command
```
docker-compose -f docker-compose.yaml down --volumes --rmi all
docker-compose -f docker-compose.yaml down --volumes --remove-orphans
docker network rm etl_network
```
