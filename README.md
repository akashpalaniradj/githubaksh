TASK 2 -  CI/CD Pipeline with Jenkins – Small Project


Objective:

To build a CI/CD pipeline using Jenkins that deploys a Python Flask application to Kubernetes.

TOOLS USED:

Python (Flask)
Jenkins
Docker
DockerHub
Kubernetes (Minikube)
GitHub

Pipeline Stages:

Clone source code from GitHub
Build Docker image
Push image to DockerHub
Deploy application to Kubernetes

Deployment:

Application deployed as a Kubernetes Deployment
Service exposed using NodePort
Application runs successfully inside Kubernetes Pod

Outcome:

Jenkins pipeline executed successfully
Docker image built and pushed
Flask application deployed and running in Kubernetes
----------------------------------------------------

Task 3: Observability with Prometheus & Grafana
Objective: To monitor a Python Flask application using Prometheus and visualize metrics using Grafana.

Tools used:

Python (Flask)
Prometheus
Grafana
Kubernetes (Minikube)
Prometheus Python Client

Implementation:

Flask application exposes metrics at /metrics
Prometheus configured to scrape application metrics
Grafana connected to Prometheus as a data source
Custom dashboards created for visualization

Metrics Monitored:

HTTP request count
Request latency
Application errors
CPU and memory usage
Python runtime metrics

Outcome:

Prometheus successfully scraped Flask metrics
Grafana dashboards displayed real-time metrics
Application observability achieved
--------------------------------------------------

