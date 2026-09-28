<div align="center">

# Chandan Kumar

**Senior DevOps / SRE · Platform Engineering**

Noida / Delhi NCR, India

[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/connectchandan)
[![Email](https://img.shields.io/badge/Email-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:chan.upen@gmail.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/chanupen)
[![Open to roles](https://img.shields.io/badge/Open_to_roles-Staff%20%2F%20Senior-2ea44f?style=flat-square)](https://www.linkedin.com/in/connectchandan)

</div>

---

## What I actually run

13+ years in infrastructure. Recent production scope:

- **50+ AWS accounts**
- **50+ Kubernetes namespaces**
- **Kong** at the edge
- **cert-manager + Venafi** for certificate issue and inventory
- **Terraform + GitHub Actions + AWS Service Catalog** for provisioning
- **AI apps on Amazon Bedrock** with **IRSA** (no long-lived AWS keys in pods)

Enterprise production work lives in private orgs. It is not mirrored in public repositories.

## Stack

```text
AWS            EKS / Kubernetes    Terraform         Argo CD         GitHub Actions
Kong           cert-manager        Venafi            IRSA            Bedrock
Docker         Helm                Service Catalog   Checkmarx

TCP  UDP  HTTP  TLS  HTTPS  MQTT  RTSP  RTSPS  mTLS  gRPC
```

## How I work

- **Multi-account AWS** — 50+ accounts as the unit of isolation. Terraform and Service Catalog for the paved path; least privilege by default.
- **GitOps** — Argo CD owns cluster desired state. GitHub Actions is the pipeline that feeds it. Git is the change record.
- **Certificate inventory** — cert-manager + Venafi so TLS is issued, rotated, and accounted for — not a spreadsheet of expiry dates.
- **IRSA** — pods get AWS API access (including Bedrock) via service-account identity. No static keys in the cluster.
- **Kong / mTLS** — API gateway as a control plane. mTLS where the protocol requires service identity, not a pile of ingress annotations.
- **Namespaces as a product** — 50+ Kubernetes namespaces with tenancy, quotas, certs, and a paved path. Not a shared-cluster dumping ground.

## Certifications

| Certification | Validity |
| --- | --- |
| AWS Certified Security – Specialty | 2026–2029 |
| AWS Certified Solutions Architect – Associate | 2024–2027 |
| GitOps Argo CD | — |
| Harness Chaos | — |
| RHCE / RHCSA | — |

## Looking for

**Staff / Senior DevOps, SRE, or Platform Engineer.**

Priority: **Delhi NCR (Noida / Gurugram)** — WFO, hybrid, or remote.

## Contact

- Email: [chan.upen@gmail.com](mailto:chan.upen@gmail.com)
- LinkedIn: [linkedin.com/in/connectchandan](https://www.linkedin.com/in/connectchandan)
- GitHub: [github.com/chanupen](https://github.com/chanupen)
- WhatsApp: [+91 70657-75607](https://wa.me/917065775607)

---

Public GitHub stats below are a thin slice of real work. Production systems sit in private enterprise orgs.

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=chanupen&show_icons=true&theme=tokyonight&hide_title=false&hide_rank=true&hide_border=true" alt="GitHub stats for chanupen" />
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=chanupen&layout=compact&theme=tokyonight&hide_border=true" alt="Top languages for chanupen" />
</div>
