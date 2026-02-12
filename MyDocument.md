### Deployment Proposal


## Option 1 — Databricks
- Store data in S3
- Use Delta tables
- Schedule via Jobs API

## Option 2 — Airflow (But we have all tasks in one file so one task in DAG)
- DAG:
    - Ingest
    - Clean
    - Feature Engineering
    - Analytics
    - Store output

## Option 3 — Dockerized Spark Job

- Dockerfile
    - ENTRYPOINT python main.py

- Deploy on:
    - Kubernetes
    - EMR
    - Databricks
    - GCP Dataproc

## Trigger Strategy

- Best practice:
    - Orchestrator (Airflow / Prefect)
    - Event-based (new CSV arrival)
    - Cron scheduled daily

### Learnings
- Salary frequency normalization was critical
- Text parsing complexity

### Improvements
- NLP model for skill extraction
- Delta Lake for CDC
- ML salary prediction model