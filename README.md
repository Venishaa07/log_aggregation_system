# 📊 Log Aggregation System using ELK Stack on Kubernetes

A centralized logging system built using **ELK Stack (Elasticsearch, Logstash, Kibana)** on **Kubernetes**, with **Docker**, **Filebeat**, and full **Ansible automation** on **AWS EC2**.

> ✅ Used by real-world DevOps teams to monitor, analyze, and visualize logs from distributed services.

## 🧱 Project Architecture

[ Flask Log App ]
⬇ (writes logs)
[ Filebeat DaemonSet ] 🌀 runs on all nodes
⬇ (ships logs)
[ Logstash Pod ]
⬇ (parses logs)
[ Elasticsearch Pod ]
⬇ (stores logs)
[ Kibana Pod ]
⬅ (visualizes logs)

## 🚀 Tech Stack

| Tool            | Role                                  |
|-----------------|----------------------------------------|
| **AWS EC2**      | Hosts Kubernetes master and workers   |
| **Docker**       | Container runtime                     |
| **Kubernetes**   | Deploys and scales ELK + log app      |
| **Ansible**      | Automates all installation and setup  |
| **Filebeat**     | Ships container logs to Logstash      |
| **Logstash**     | Parses and forwards logs              |
| **Elasticsearch**| Indexes and stores logs               |
| **Kibana**       | Visualizes logs & builds dashboards   |
| **Flask**        | Simulates real app generating logs    |

## 📦 Features

- 🔄 Full Ansible automation (Docker, Kubernetes, ELK, Filebeat, App)
- ⚙️ Multi-node Kubernetes cluster (1 master + N workers)
- 📈 Real-time log collection and dashboard visualization
- 🧪 Simulated microservice app producing logs
- 💾 Logs indexed by date using Logstash filters

## 🗂️ Folder Structure

ansible-elk/
├── install_docker.yml
├── install_k8s.yml
├── deploy_k8s_cluster.yml
├── deploy_elk_stack.yml
├── deploy_logapp.yml
├── deploy_filebeat.yml
├── site.yml
├── hosts.ini
├── files/
│ ├── elasticsearch-deployment.yaml
│ ├── elasticsearch-service.yaml
│ ├── kibana-deployment.yaml
│ ├── kibana-service.yaml
│ ├── logstash.conf
│ ├── logstash-deployment.yaml
│ ├── logstash-service.yaml
│ ├── logapp-deployment.yaml
│ ├── logapp-service.yaml
│ ├── filebeat-kubernetes.yaml
│ ├── app.py
│ └── Dockerfile

📚 Use Case
DevOps teams use this system to:

Monitor app performance

Identify errors and bottlenecks

Audit access logs

Set up alerting rules

Centralize all logs from microservices

🧠 Key Learning Outcomes
Real-world Kubernetes + Docker + DevOps stack

Full automation using Ansible

Filebeat + Logstash + Elasticsearch pipeline

Infrastructure-as-Code and container orchestration

Centralized logging design used in production

📄 License
This project is open-sourced under the MIT License.

🧑‍💻 Author
Venishaa N
