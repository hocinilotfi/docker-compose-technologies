# Technologies essentielles pour un Data Scientist (FR/LUX)

| Technologie / Outil       | Usage principal                                  | Docker / Installation locale possible ?           | Pourquoi c’est utile                              |
|--------------------------|------------------------------------------------|---------------------------------------------------|--------------------------------------------------|
| **JupyterLab / Notebook** | Environnement interactif pour data exploration | Oui (`jupyter/datascience-notebook`)               | Exploration, prototypage rapide                   |
| **MLflow**                | Suivi d’expériences ML, gestion modèles         | Oui (officiel MLflow + PostgreSQL + MinIO)         | MLOps, traçabilité et reproductibilité            |
| **Apache Airflow**        | Orchestration workflows ETL/ML                   | Oui (Airflow + PostgreSQL + Redis)                   | Pipelines data complexes, automatisation          |
| **PostgreSQL**            | Base relationnelle robuste                       | Oui (image officielle)                              | Stockage structuré, analytics, backend            |
| **MongoDB**               | Base NoSQL document store                        | Oui                                                | Pour données semi-structurées, flexibilité        |
| **Redis**                 | Cache, broker message, data clé-valeur          | Oui                                                | Accélération, queues, session management           |
| **Kafka + Zookeeper**     | Streaming données en temps réel                  | Oui                                                | Gestion data temps réel, pipelines d’events        |
| **DVC (Data Version Control)** | Gestion version données et modèles             | Oui (CLI + Gitea/GitLab pour repo)                  | Collaboration, gestion dataset versionnés          |
| **Docker Compose**        | Orchestration multi-containers                    | Oui                                                | Déploiement local multi-service                     |
| **FastAPI / Flask**       | APIs ML & data exposées                          | Oui                                                | Production et serveurs de modèles ML                |
| **Grafana + Prometheus**  | Monitoring et alerting                           | Oui                                                | Supervision modèles, infra, pipelines               |
| **Keycloak**              | Authentification et sécurité                     | Oui                                                | Sécuriser accès API, dashboard                      |
| **ElasticSearch + Kibana**| Recherche full-text, analytics log data          | Oui                                                | Analyse de logs, recherches rapides                 |
| **Apache Spark / PySpark**| Traitement Big Data distribué                    | Oui (via Spark standalone ou k8s)                   | Big Data, ML distribué                               |
| **Kubeflow**              | MLOps et workflows Kubernetes                    | Oui (nécessite Kubernetes local type k3d/minikube) | Pipeline ML à grande échelle                         |
