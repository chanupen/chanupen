<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=600&size=26&duration=3200&pause=900&color=2EA043&center=true&vCenter=true&width=760&lines=Chandan+Kumar;Senior+DevOps+%2F+Site+Reliability+Engineer;AWS+%C2%B7+Kubernetes+%C2%B7+Terraform+%C2%B7+GitOps;Keeping+production+boring+since+2013" alt="Chandan Kumar" />

<p>
  <a href="https://www.linkedin.com/in/connectchandan"><img src="https://img.shields.io/badge/LinkedIn-connectchandan-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" /></a>
  <a href="mailto:chan.upen@gmail.com"><img src="https://img.shields.io/badge/Email-chan.upen%40gmail.com-D14836?style=for-the-badge&logo=gmail&logoColor=white" /></a>
  <a href="https://www.credly.com/users/chanupen"><img src="https://img.shields.io/badge/Credly-Certifications-FF6B00?style=for-the-badge&logo=credly&logoColor=white" /></a>
</p>

<p>
  <img src="https://img.shields.io/badge/Experience-13%2B%20years-2EA043?style=flat-square" />
  <img src="https://img.shields.io/badge/AWS%20accounts-50%2B-FF9900?style=flat-square&logo=amazonwebservices&logoColor=white" />
  <img src="https://img.shields.io/badge/K8s%20namespaces-50%2B-326CE5?style=flat-square&logo=kubernetes&logoColor=white" />
  <img src="https://img.shields.io/badge/Engineers%20on%20my%20CI%2FCD-150%2B-2088FF?style=flat-square&logo=githubactions&logoColor=white" />
  <img src="https://img.shields.io/badge/Open%20to-Senior%20%2F%20Staff%20roles-8957E5?style=flat-square" />
  <img src="https://komarev.com/ghpvc/?username=chanupen&style=flat-square&color=555555&label=Profile+views" />
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

## About me

I started as a Linux administrator in 2013 and have worked on production systems ever since: telecom production support for Bharti Airtel, the AWS IoT cloud for Hero Group's Qubo, and platform operations at adidas. Titles changed along the way. The job didn't: keep production stable, make releases safe and quick for developers, and get rid of the manual steps that cause outages.

## Career

| Period | Company | What I did |
| --- | --- | --- |
| 2022 – now | **adidas**, Gurugram | Platform operations for 50+ AWS accounts and 50+ EKS namespaces. Shared CI/CD for 150+ engineers, observability, SLOs and incident RCA, cost work, AI tooling for on-call. Lead a small team of external DevOps and SRE engineers. |
| 2019 – 2022 | **Hero Electronix (Qubo)**, Noida | Designed, built and ran the complete Qubo IoT cloud on AWS on my own and took it live. MQTT at scale, data pipelines, Kubernetes, CI/CD, monitoring. |
| 2015 – 2019 | **UST Global** for Bharti Airtel, Noida | Production support for authentication, KYC, billing, SMS and SIM activation platforms on RHEL. Automation in Python and Bash. |
| 2014 – 2015 | **CSS Corp** for AT&T and Juniper, Chennai | Solaris and Linux production support, P1 incidents on outage bridges. |
| 2013 – 2014 | **KR Network Cloud**, New Delhi | First systems role: Linux servers, NFS, web and mail, Nagios, backups. |

## Things I've built

<details open>
<summary><b>🔐 Certificate automation at adidas: cert-manager + Venafi</b></summary>
<br>

100+ TLS, Kafka, ingress and domain certificates across dev, SIT, staging and production used to be requested and renewed by hand. Ops had missed 10–20 renewals over time. Now a team declares a certificate in a file and the platform does the rest. **No missed renewals since.**

```mermaid
flowchart LR
    A["Team declares a<br/>Certificate in Git"] --> B["cert-manager<br/>(Helm, per namespace)"]
    B -->|request| C["Venafi<br/>(security approval)"]
    C -->|signed cert| B
    B --> D["Kubernetes Secret"]
    D --> E["Ingress / service / Kafka client"]
    B -.->|auto-renews before expiry| C
```
</details>

<details open>
<summary><b>🚀 Shared CI/CD for 150+ engineers</b></summary>
<br>

Jenkins shared libraries in Groovy and GitHub Actions workflows that developers and QA release through. Builds from Bitbucket, images in Harbor, Checkmarx SAST as a gate, Flux for GitOps deploys to EKS. Cut build and test time for a Lerna monorepo **by about half**.

```mermaid
flowchart LR
    A[Bitbucket] --> B["Jenkins shared libs /<br/>GitHub Actions"]
    B --> C[Build and test]
    C --> D{Checkmarx SAST}
    D -->|pass| E[Harbor registry]
    E --> F["Flux GitOps"]
    F --> G["EKS namespaces<br/>dev → SIT → staging → prod"]
```
</details>

<details>
<summary><b>📡 Qubo IoT cloud on AWS, built solo</b></summary>
<br>

From an empty AWS account to devices in customers' homes. Clustered HiveMQ (MQTT 3.1 and 5) with authentication and authorization, Kafka, Kinesis, Firehose and SQS pipelines, MongoDB, Cassandra, DynamoDB, RDS and Redis, Kubernetes built with kops and kubeadm, blue-green releases, ELK and Prometheus monitoring. Then I ran it: **AWS bill down ~30%**, **broker performance up ~40%** after fixing crypto and code-path issues.

```mermaid
flowchart LR
    D[IoT devices] -->|MQTT / TLS| H["HiveMQ cluster<br/>(EC2)"]
    APP[Mobile app] --> GW[API Gateway / Lambda]
    GW --> COG[Cognito]
    H --> K[Kafka / Kinesis / Firehose]
    K --> DB[("DynamoDB · MongoDB<br/>Cassandra · RDS · Redis")]
    K --> S3[(S3)]
    S3 --> CF[CloudFront]
```
</details>

<details>
<summary><b>🤖 AI for operations</b></summary>
<br>

- Shared pipelines that take other teams' AI applications to production on **AWS Bedrock**, with IRSA instead of long-lived AWS keys.
- Internal **MCP servers** for AWS, AWS Knowledge Base, Atlassian and Instana, so on-call engineers get context in one place. MCP also keeps our Confluence docs up to date.
- **Bedrock RAG** over runbooks and incident history, plus a local RAG stack on **Ollama, FastMCP and ChromaDB**.
- **SmartOps** (internal AI hackathon): one search across Jira and Confluence to find related incidents faster.
</details>

<details>
<summary><b>📉 Cost and observability</b></summary>
<br>

- **Kubernetes spend down ~15%**: right-sized workloads, cluster downscaler, non-production shut down at weekends.
- **RDS, DocumentDB and ElastiCache spend down ~20%**: right-sized instance classes, idle capacity removed.
- **~25% faster issue resolution**: one log format for frontend, backend and platform services in OpenSearch.
- Reworked dashboards and alerts to cut noisy pages; set and report SLOs and MTTR; lead incident RCA and postmortems.
</details>

## Tech stack

**Cloud, containers and infrastructure as code**

<p>
  <img src="https://skillicons.dev/icons?i=aws,kubernetes,docker,terraform,ansible,linux,redhat,debian,nginx&perline=9" />
</p>

**CI/CD, languages and tooling**

<p>
  <img src="https://skillicons.dev/icons?i=jenkins,githubactions,git,bitbucket,maven,npm,py,bash&perline=8" />
</p>

**Observability and data**

<p>
  <img src="https://skillicons.dev/icons?i=prometheus,grafana,elasticsearch,kafka,mongodb,cassandra,postgres,mysql,redis,dynamodb&perline=10" />
</p>

**Platform, security and AI**

<p>
  <img src="https://img.shields.io/badge/Amazon%20EKS-FF9900?style=flat-square&logo=amazoneks&logoColor=white" />
  <img src="https://img.shields.io/badge/Helm-0F1689?style=flat-square&logo=helm&logoColor=white" />
  <img src="https://img.shields.io/badge/Flux-5468FF?style=flat-square&logo=flux&logoColor=white" />
  <img src="https://img.shields.io/badge/cert--manager-326CE5?style=flat-square&logo=kubernetes&logoColor=white" />
  <img src="https://img.shields.io/badge/Venafi-1F2937?style=flat-square" />
  <img src="https://img.shields.io/badge/Harbor-60B932?style=flat-square&logo=harbor&logoColor=white" />
  <img src="https://img.shields.io/badge/Checkmarx-54B848?style=flat-square" />
  <img src="https://img.shields.io/badge/CloudFormation-FF4F8B?style=flat-square&logo=amazonwebservices&logoColor=white" />
  <img src="https://img.shields.io/badge/Service%20Catalog-232F3E?style=flat-square&logo=amazonwebservices&logoColor=white" />
  <img src="https://img.shields.io/badge/OpenSearch-005EB8?style=flat-square&logo=opensearch&logoColor=white" />
  <img src="https://img.shields.io/badge/Instana-1F70C1?style=flat-square" />
  <img src="https://img.shields.io/badge/Dynatrace-1496FF?style=flat-square&logo=dynatrace&logoColor=white" />
  <img src="https://img.shields.io/badge/Splunk-000000?style=flat-square&logo=splunk&logoColor=white" />
  <img src="https://img.shields.io/badge/OpsGenie-172B4D?style=flat-square&logo=opsgenie&logoColor=white" />
  <img src="https://img.shields.io/badge/Akamai-0096D6?style=flat-square&logo=akamai&logoColor=white" />
  <img src="https://img.shields.io/badge/CloudFront-8C4FFF?style=flat-square&logo=amazonwebservices&logoColor=white" />
  <img src="https://img.shields.io/badge/Kong-003459?style=flat-square&logo=kong&logoColor=white" />
  <img src="https://img.shields.io/badge/Apigee-4285F4?style=flat-square" />
  <img src="https://img.shields.io/badge/HiveMQ%20%2F%20MQTT-660066?style=flat-square&logo=mqtt&logoColor=white" />
  <img src="https://img.shields.io/badge/Kinesis-8C4FFF?style=flat-square&logo=amazonwebservices&logoColor=white" />
  <img src="https://img.shields.io/badge/AWS%20Bedrock-01A88D?style=flat-square&logo=amazonwebservices&logoColor=white" />
  <img src="https://img.shields.io/badge/MCP%20servers-000000?style=flat-square" />
  <img src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white" />
  <img src="https://img.shields.io/badge/ChromaDB-FF6446?style=flat-square" />
  <img src="https://img.shields.io/badge/Groovy-4298B8?style=flat-square&logo=apachegroovy&logoColor=white" />
  <img src="https://img.shields.io/badge/Jira-0052CC?style=flat-square&logo=jira&logoColor=white" />
  <img src="https://img.shields.io/badge/Confluence-172B4D?style=flat-square&logo=confluence&logoColor=white" />
</p>

## Certifications

<p>
  <a href="https://www.credly.com/users/chanupen"><img src="https://img.shields.io/badge/AWS%20Certified-Security%20Specialty%20(2026–2029)-FF9900?style=for-the-badge&logo=amazonwebservices&logoColor=white" /></a>
  <a href="https://www.credly.com/users/chanupen"><img src="https://img.shields.io/badge/AWS%20Certified-Solutions%20Architect%20Associate%20(2024–2027)-FF9900?style=for-the-badge&logo=amazonwebservices&logoColor=white" /></a>
</p>
<p>
  <img src="https://img.shields.io/badge/Red%20Hat-RHCE%20%26%20RHCSA-EE0000?style=for-the-badge&logo=redhat&logoColor=white" />
  <img src="https://img.shields.io/badge/Codefresh-GitOps%20Fundamentals-0B5FFF?style=for-the-badge" />
</p>

## Working on now

- 🐹 **Go** for infrastructure tooling and Kubernetes controllers
- ☸️ **CKA** and **Terraform Associate** exams
- 🤖 An AI on-call assistant built on MCP and RAG

## GitHub activity

<div align="center">

<img height="165" src="https://github-readme-stats.vercel.app/api?username=chanupen&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true" />
<img height="165" src="https://github-readme-streak-stats.herokuapp.com/?user=chanupen&theme=tokyonight&hide_border=true" />

<img width="95%" src="https://github-readme-activity-graph.vercel.app/graph?username=chanupen&theme=tokyo-night&hide_border=true&area=true" />

<img src="https://github-profile-trophy.vercel.app/?username=chanupen&theme=tokyonight&no-frame=true&no-bg=true&margin-w=6&row=1&column=7" />

</div>

> Most of my production work lives in private company repositories, so the public numbers here show only a small part of it. Happy to walk through any of it in detail.

<div align="center">

<sub>Noida, India · <a href="https://www.linkedin.com/in/connectchandan">LinkedIn</a> · <a href="mailto:chan.upen@gmail.com">chan.upen@gmail.com</a></sub>

</div>
