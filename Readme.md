# Essential Technologies for a Data Scientist (FR/LUX)

| Technology / Tool         | Main Use                                         | Docker / Local Install Available?                   | Why It’s Useful                                   |
|--------------------------|-------------------------------------------------|----------------------------------------------------|--------------------------------------------------|
| **JupyterLab / Notebook** | Interactive environment for data exploration    | Yes (`jupyter/datascience-notebook`)                | Exploration, rapid prototyping                    |
| **MLflow**                | ML experiment tracking, model management         | Yes (official MLflow + PostgreSQL + MinIO)          | MLOps, traceability and reproducibility           |
| **Apache Airflow**        | ETL/ML workflow orchestration                     | Yes (Airflow + PostgreSQL + Redis)                   | Complex data pipelines, automation                 |
| **PostgreSQL**            | Robust relational database                        | Yes (official image)                                 | Structured storage, analytics, backend             |
| **MongoDB**               | NoSQL document store                              | Yes                                                 | Semi-structured data, flexibility                   |
| **Redis**                 | Cache, message broker, key-value store            | Yes                                                 | Speed up, queues, session management                 |
| **Kafka + Zookeeper**     | Real-time data streaming                           | Yes                                                 | Real-time data management, event pipelines          |
| **DVC (Data Version Control)** | Data and model version control                  | Yes (CLI + Gitea/GitLab for repo)                     | Collaboration, versioned dataset management          |
| **Docker Compose**        | Multi-container orchestration                      | Yes                                                 | Local multi-service deployment                        |
| **FastAPI / Flask**       | ML & data APIs                                    | Yes                                                 | Production and serving ML models                      |
| **Grafana + Prometheus**  | Monitoring and alerting                           | Yes                                                 | Monitoring models, infra, pipelines                   |
| **Keycloak**              | Authentication and security                       | Yes                                                 | Secure API and dashboard access                       |
| **ElasticSearch + Kibana**| Full-text search, log data analytics              | Yes                                                 | Log analysis, fast searches                            |
| **Apache Spark / PySpark**| Distributed Big Data processing                    | Yes (via standalone Spark or k8s)                    | Big Data, distributed ML                               |
| **Kubeflow**              | Kubernetes-based MLOps and workflows               | Yes (requires local Kubernetes like k3d/minikube)   | Large-scale ML pipeline                                |