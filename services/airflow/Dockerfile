FROM apache/airflow:2.7.1-python3.11

USER root
# Standard Linux updates to ensure pip works smoothly
RUN apt-get update && apt-get install -y --no-install-recommends build-essential

USER airflow
