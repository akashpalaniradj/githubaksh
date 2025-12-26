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
TASK 4:  Nginx – Small Project

Overview:
This project demonstrates the use of Nginx as a reverse proxy for a Python (Flask) application. Nginx runs inside a Docker container and forwards incoming client requests to a Python application container running on port 5000.

Components Used:

Python Flask Application
Nginx (Reverse Proxy)
Docker
Docker Network

How It Works:

The Python application runs in a Docker container (python_app) on port 5000.
Nginx runs in a separate Docker container (nginx_proxy).
Nginx listens on port 8081 and forwards requests to the Python app using Docker networking.

Files Included:

nginx.conf – Nginx reverse proxy configuration
Dockerfile – Dockerfile to build the Nginx container

Outcome:

Nginx successfully acts as a reverse proxy, routing client requests to the Python application container.
--------------------------------------------------------------------------------------------------------

