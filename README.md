<div align="center">

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="assets/header-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="assets/header-light.svg" />
  <img src="assets/header-light.svg" alt="Chandan Kumar, Senior DevOps / Site Reliability Engineer" width="100%" />
</picture>

<a href="https://www.linkedin.com/in/connectchandan"><img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white" alt="LinkedIn" /></a> <a href="mailto:chan.upen@gmail.com"><img src="https://img.shields.io/badge/chan.upen@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white" alt="chan.upen@gmail.com" /></a> <a href="https://www.credly.com/users/chanupen"><img src="https://img.shields.io/badge/Credly-FF6B00?style=flat-square&logo=credly&logoColor=white" alt="Credly" /></a>

<p>
  <img src="https://img.shields.io/badge/Experience-13%2B%20years-0f766e?style=flat-square" />
  <img src="https://img.shields.io/badge/AWS%20accounts-50%2B-FF9900?style=flat-square&logo=amazonwebservices&logoColor=white" />
  <img src="https://img.shields.io/badge/EKS%20namespaces-50%2B-326CE5?style=flat-square&logo=kubernetes&logoColor=white" />
  <img src="https://img.shields.io/badge/Engineers%20on%20my%20CI%2FCD-150%2B-2088FF?style=flat-square&logo=githubactions&logoColor=white" />
  <img src="https://img.shields.io/badge/Certificates%20automated-100%2B-2EA043?style=flat-square&logo=letsencrypt&logoColor=white" />
</p>

</div>

---

```console
$ kubectl describe engineer chandan

Name:          Chandan Kumar
Role:          Senior DevOps / Site Reliability Engineer
Location:      Noida, India (remote or anywhere in India)
Experience:    13+ years in production operations
Current:       adidas, Platform Operations (2022 – present)
Previously:    Hero Electronix / Qubo IoT · UST Global for Bharti Airtel · CSS Corp for AT&T and Juniper
Focus:         AWS · Kubernetes · Terraform · GitOps · Observability · AI for operations
Certs:         AWS Security – Specialty · AWS Solutions Architect – Associate · RHCE · RHCSA
Status:        Ready (open to Senior / Staff DevOps, SRE and Platform roles)
Events:
  Normal  Built     Qubo IoT cloud on AWS, from an empty account to production, solo
  Normal  Scaled    Platform ops across 50+ AWS accounts and 50+ EKS namespaces
  Normal  Saved     ~15% Kubernetes spend, ~20% database spend, ~30% AWS bill
  Normal  Removed   Manual certificate renewals: 100+ certs, zero missed since
```

## <img src="https://img.shields.io/badge/-%20-0f766e?style=flat-square" height="18" /> About

I started as a Linux administrator in 2013 and have worked on production systems ever since: telecom production support for Bharti Airtel, the AWS IoT cloud for Hero Group's Qubo, and platform operations at adidas. Titles changed along the way. The job didn't: keep production stable, make releases safe and quick for developers, and get rid of the manual steps that cause outages.

## <img src="https://img.shields.io/badge/-%20-0f766e?style=flat-square" height="18" /> Career

| Period | Company | What I did |
| --- | --- | --- |
| 2022 – now | **adidas**, Gurugram | Platform operations for 50+ AWS accounts and 50+ EKS namespaces. Shared CI/CD for 150+ engineers, observability, SLOs and incident RCA, cost work, AI tooling for on-call. Lead a small team of external DevOps and SRE engineers. |
| 2019 – 2022 | **Hero Electronix (Qubo)**, Noida | Designed, built and ran the complete Qubo IoT cloud on AWS on my own and took it live: MQTT at scale, data pipelines, Kubernetes, CI/CD, monitoring. |
| 2015 – 2019 | **UST Global** for Bharti Airtel, Noida | Production support for authentication, KYC, billing, SMS and SIM activation platforms on RHEL. Automation in Python and Bash. |
| 2014 – 2015 | **CSS Corp** for AT&T and Juniper, Chennai | Solaris and Linux production support, P1 incidents on outage bridges. |
| 2013 – 2014 | **KR Network Cloud**, New Delhi | First systems role: Linux servers, NFS, web and mail, Nagios, backups. |

## <img src="https://img.shields.io/badge/-%20-0f766e?style=flat-square" height="18" /> Selected work

<details open>
<summary><b>Certificate automation at adidas with cert-manager and Venafi</b></summary>
<br>

100+ TLS, Kafka, ingress and domain certificates across dev, SIT, staging and production used to be requested and renewed by hand, and ops had missed 10–20 renewals over time. Now a team declares a certificate in a file and the platform does the rest. **No missed renewals since.**

```mermaid
flowchart TB
    A["Certificate declared in Git"] --> B["cert-manager<br/>Helm, per namespace"]
    B -->|request| C["Venafi<br/>security approval"]
    C -->|signed certificate| B
    B --> D["Kubernetes Secret"]
    D --> E["Ingress · services · Kafka"]
    classDef src fill:#0f766e,stroke:#0f766e,color:#ffffff
    classDef step fill:#e0f2f1,stroke:#0f766e,color:#134e4a
    classDef gate fill:#fff4e5,stroke:#d97706,color:#7c2d12
    classDef out fill:#e0f2fe,stroke:#0369a1,color:#0c4a6e
    class A src
    class B,D step
    class C gate
    class E out
```
</details>

<details open>
<summary><b>Shared CI/CD for 150+ engineers</b></summary>
<br>

Jenkins shared libraries in Groovy and GitHub Actions workflows that developers and QA release through: builds from Bitbucket, Checkmarx SAST as a gate, images in Harbor, Flux for GitOps deploys to EKS. Cut build and test time for a Lerna monorepo **by about half**.

```mermaid
flowchart LR
    A[Bitbucket] --> B["Jenkins /<br/>GitHub Actions"]
    B --> C{Checkmarx SAST}
    C -->|pass| D[Harbor]
    D --> E[Flux]
    E --> F["EKS<br/>dev → prod"]
    classDef src fill:#0f766e,stroke:#0f766e,color:#ffffff
    classDef step fill:#e0f2f1,stroke:#0f766e,color:#134e4a
    classDef gate fill:#fff4e5,stroke:#d97706,color:#7c2d12
    classDef out fill:#e0f2fe,stroke:#0369a1,color:#0c4a6e
    class A src
    class B,D,E step
    class C gate
    class F out
```
</details>

<details>
<summary><b>Qubo IoT cloud on AWS, built solo</b></summary>
<br>

From an empty AWS account to devices in customers' homes: clustered HiveMQ (MQTT 3.1 and 5) with authentication and authorization; Kafka, Kinesis, Firehose and SQS pipelines; MongoDB, Cassandra, DynamoDB, RDS and Redis; Kubernetes built with kops and kubeadm; blue-green releases; ELK and Prometheus monitoring. Then I ran it: **AWS bill down ~30%** and **broker performance up ~40%** after fixing crypto and code-path issues.

```mermaid
flowchart LR
    D[IoT devices] -->|MQTT over TLS| H["HiveMQ cluster"]
    APP[Mobile app] --> GW["API Gateway<br/>Lambda · Cognito"]
    H --> K["Kafka · Kinesis<br/>Firehose"]
    K --> DB[("DynamoDB · MongoDB<br/>Cassandra · RDS · Redis")]
    K --> S3[(S3)] --> CF[CloudFront]
    classDef src fill:#0f766e,stroke:#0f766e,color:#ffffff
    classDef step fill:#e0f2f1,stroke:#0f766e,color:#134e4a
    classDef gate fill:#fff4e5,stroke:#d97706,color:#7c2d12
    classDef out fill:#e0f2fe,stroke:#0369a1,color:#0c4a6e
    class D,APP src
    class H,GW,K step
    class DB,S3 out
    class CF out
```
</details>

<details>
<summary><b>AI for operations</b></summary>
<br>

- Shared pipelines that take other teams' AI applications to production on **AWS Bedrock**, using IRSA instead of long-lived AWS keys.
- Internal **MCP servers** for AWS, AWS Knowledge Base, Atlassian and Instana, so on-call engineers get context in one place. MCP also keeps our Confluence docs current.
- **Bedrock RAG** over runbooks and incident history, plus a local RAG stack on **Ollama, FastMCP and ChromaDB**.
- **SmartOps** (internal AI hackathon): one search across Jira and Confluence to find related incidents faster.
</details>

<details>
<summary><b>Cost and observability</b></summary>
<br>

- **Kubernetes spend down ~15%**: right-sized workloads, cluster downscaler, non-production shut down at weekends.
- **RDS, DocumentDB and ElastiCache spend down ~20%**: right-sized instance classes, idle capacity removed.
- **~25% faster issue resolution**: one log format for frontend, backend and platform services in OpenSearch.
- Reworked dashboards and alerts to cut noisy pages; set and report SLOs and MTTR; lead incident RCA and postmortems.
</details>

## <img src="https://img.shields.io/badge/-%20-0f766e?style=flat-square" height="18" /> Tools

| Area | |
| --- | --- |
| **Cloud and infrastructure as code** | <img src="https://img.shields.io/badge/AWS-FF9900?style=flat-square&logo=amazonwebservices&logoColor=white" alt="AWS" /> <img src="https://img.shields.io/badge/Amazon%20EKS-FF9900?style=flat-square&logo=amazoneks&logoColor=white" alt="Amazon EKS" /> <img src="https://img.shields.io/badge/Terraform-7B42BC?style=flat-square&logo=terraform&logoColor=white" alt="Terraform" /> <img src="https://img.shields.io/badge/CloudFormation-E7157B?style=flat-square&logo=amazonwebservices&logoColor=white" alt="CloudFormation" /> <img src="https://img.shields.io/badge/AWS%20Service%20Catalog-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white" alt="AWS Service Catalog" /> <img src="https://img.shields.io/badge/Ansible-EE0000?style=flat-square&logo=ansible&logoColor=white" alt="Ansible" /> <img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black" alt="Linux" /> <img src="https://img.shields.io/badge/Red%20Hat-EE0000?style=flat-square&logo=redhat&logoColor=white" alt="Red Hat" /> |
| **Kubernetes and delivery** | <img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=kubernetes&logoColor=white" alt="Kubernetes" /> <img src="https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white" alt="Helm" /> <img src="https://img.shields.io/badge/Flux-5468FF?style=flat-square&logo=flux&logoColor=white" alt="Flux" /> <img src="https://img.shields.io/badge/cert--manager-326CE5?style=flat-square&logo=kubernetes&logoColor=white" alt="cert-manager" /> <img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white" alt="Docker" /> <img src="https://img.shields.io/badge/Harbor-60B932?style=flat-square&logo=harbor&logoColor=white" alt="Harbor" /> <img src="https://img.shields.io/badge/Jenkins-D24939?style=flat-square&logo=jenkins&logoColor=white" alt="Jenkins" /> <img src="https://img.shields.io/badge/GitHub%20Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white" alt="GitHub Actions" /> <img src="https://img.shields.io/badge/Bitbucket-0052CC?style=flat-square&logo=bitbucket&logoColor=white" alt="Bitbucket" /> <img src="https://img.shields.io/badge/Checkmarx-54B848?style=flat-square" alt="Checkmarx" /> |
| **Observability** | <img src="https://img.shields.io/badge/Prometheus-E6522C?style=flat-square&logo=prometheus&logoColor=white" alt="Prometheus" /> <img src="https://img.shields.io/badge/Grafana-F46800?style=flat-square&logo=grafana&logoColor=white" alt="Grafana" /> <img src="https://img.shields.io/badge/OpenSearch-005EB8?style=flat-square&logo=opensearch&logoColor=white" alt="OpenSearch" /> <img src="https://img.shields.io/badge/Elastic%20%2F%20Kibana-005571?style=flat-square&logo=elastic&logoColor=white" alt="Elastic / Kibana" /> <img src="https://img.shields.io/badge/Instana-1F70C1?style=flat-square" alt="Instana" /> <img src="https://img.shields.io/badge/Dynatrace-1496FF?style=flat-square&logo=dynatrace&logoColor=white" alt="Dynatrace" /> <img src="https://img.shields.io/badge/Splunk-000000?style=flat-square&logo=splunk&logoColor=white" alt="Splunk" /> <img src="https://img.shields.io/badge/OpsGenie-172B4D?style=flat-square&logo=opsgenie&logoColor=white" alt="OpsGenie" /> |
| **Data and messaging** | <img src="https://img.shields.io/badge/Kafka-231F20?style=flat-square&logo=apachekafka&logoColor=white" alt="Kafka" /> <img src="https://img.shields.io/badge/HiveMQ%20%2F%20MQTT-660066?style=flat-square&logo=mqtt&logoColor=white" alt="HiveMQ / MQTT" /> <img src="https://img.shields.io/badge/Kinesis-8C4FFF?style=flat-square&logo=amazonwebservices&logoColor=white" alt="Kinesis" /> <img src="https://img.shields.io/badge/RDS%20%2F%20PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white" alt="RDS / PostgreSQL" /> <img src="https://img.shields.io/badge/DynamoDB-4053D6?style=flat-square&logo=amazondynamodb&logoColor=white" alt="DynamoDB" /> <img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=white" alt="MongoDB" /> <img src="https://img.shields.io/badge/Cassandra-1287B1?style=flat-square&logo=apachecassandra&logoColor=white" alt="Cassandra" /> <img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=white" alt="Redis" /> |
| **Security and edge** | <img src="https://img.shields.io/badge/Venafi-1F2937?style=flat-square" alt="Venafi" /> <img src="https://img.shields.io/badge/TLS%20%2F%20mTLS-2EA043?style=flat-square" alt="TLS / mTLS" /> <img src="https://img.shields.io/badge/Akamai-0096D6?style=flat-square&logo=akamai&logoColor=white" alt="Akamai" /> <img src="https://img.shields.io/badge/CloudFront-8C4FFF?style=flat-square&logo=amazonwebservices&logoColor=white" alt="CloudFront" /> <img src="https://img.shields.io/badge/Kong-003459?style=flat-square&logo=kong&logoColor=white" alt="Kong" /> <img src="https://img.shields.io/badge/Apigee-4285F4?style=flat-square" alt="Apigee" /> <img src="https://img.shields.io/badge/IAM%20%2F%20IRSA-DD344C?style=flat-square&logo=amazonwebservices&logoColor=white" alt="IAM / IRSA" /> |
| **AI for operations** | <img src="https://img.shields.io/badge/AWS%20Bedrock-01A88D?style=flat-square&logo=amazonwebservices&logoColor=white" alt="AWS Bedrock" /> <img src="https://img.shields.io/badge/MCP%20servers-D97757?style=flat-square" alt="MCP servers" /> <img src="https://img.shields.io/badge/RAG-6E40C9?style=flat-square" alt="RAG" /> <img src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white" alt="Ollama" /> <img src="https://img.shields.io/badge/ChromaDB-FF6446?style=flat-square" alt="ChromaDB" /> |
| **Languages** | <img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white" alt="Python" /> <img src="https://img.shields.io/badge/Bash-4EAA25?style=flat-square&logo=gnubash&logoColor=white" alt="Bash" /> <img src="https://img.shields.io/badge/Groovy-4298B8?style=flat-square&logo=apachegroovy&logoColor=white" alt="Groovy" /> <img src="https://img.shields.io/badge/Go%20(learning)-00ADD8?style=flat-square&logo=go&logoColor=white" alt="Go (learning)" /> |

## <img src="https://img.shields.io/badge/-%20-0f766e?style=flat-square" height="18" /> Certifications

<p>
  <a href="https://www.credly.com/users/chanupen"><img src="https://img.shields.io/badge/AWS%20Certified-Security%20Specialty-FF9900?style=flat-square&logo=amazonwebservices&logoColor=white" /></a>
  <a href="https://www.credly.com/users/chanupen"><img src="https://img.shields.io/badge/AWS%20Certified-Solutions%20Architect%20Associate-FF9900?style=flat-square&logo=amazonwebservices&logoColor=white" /></a>
  <img src="https://img.shields.io/badge/Red%20Hat-RHCE%20%7C%20RHCSA-EE0000?style=flat-square&logo=redhat&logoColor=white" />
  <img src="https://img.shields.io/badge/Codefresh-GitOps%20Fundamentals-0B5FFF?style=flat-square" />
</p>

| Certification | Valid |
| --- | --- |
| [AWS Certified Security – Specialty](https://www.credly.com/users/chanupen) | 2026 – 2029 |
| [AWS Certified Solutions Architect – Associate](https://www.credly.com/users/chanupen) | 2024 – 2027 |
| Red Hat Certified Engineer (RHCE) and System Administrator (RHCSA) | 2014 |
| GitOps Fundamentals, Codefresh | 2021 |

## <img src="https://img.shields.io/badge/-%20-0f766e?style=flat-square" height="18" /> Working on now

- **Go** for infrastructure tooling and Kubernetes controllers
- **CKA** and **Terraform Associate** exams
- An AI on-call assistant built on MCP and RAG

---

<sub>Most of my production work lives in private company repositories, so public activity here shows only a small part of it. Happy to walk through any of it in detail.</sub>
