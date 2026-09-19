<div align="center">

`// platform & MLOps engineer`

# Anatoly (Till) Lazarev

**I build the platforms other engineers ship on** — ML infrastructure, Kubernetes, GPU, and the security underneath.

[![Website](https://img.shields.io/badge/lazarev.cloud-0b0b0b?style=flat-square&logo=icloud&logoColor=white)](https://lazarev.cloud)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0b0b0b?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/lazarevtill)
[![Email](https://img.shields.io/badge/till@lazarev.cloud-0b0b0b?style=flat-square&logo=maildotru&logoColor=white)](mailto:till@lazarev.cloud)
[![Location](https://img.shields.io/badge/Novi%20Sad,%20Serbia-0b0b0b?style=flat-square&logo=googlemaps&logoColor=white)](#)

</div>

---

Platform and MLOps engineer, 7+ years. Founding MLOps hire at a fintech serving millions of users, where I designed and built the company's ML platform and still run it as its sole engineer — from the EKS clusters and H100s up to the SDK its users write code against.

The systems on this profile are mine: designed, built and operated end to end, not by a company. Most of my day-to-day code lives on a self-hosted GitLab behind [lazarev.cloud](https://lazarev.cloud); this is the public slice.

## What I work on

**ML platform, at work.** Built from zero: Snowflake and S3 data through notebooks, training, benchmarking and versioning to a served model — Kubeflow, MLflow, KServe, Langfuse and Label Studio on EKS, behind Keycloak SSO and delivered by Argo CD. Five team workspaces run on it.

Two parts I'd point at:

- **Serving with provenance, no tenant credentials.** A custom KServe storage container resolves an `mlflow://` reference through the tracking server using the team's own token, so no object-storage keys exist in tenant namespaces — with a Kyverno admission policy requiring every InferenceService to reference a registered model version.
- **An SDK, CLI and MCP server.** One authenticated entry point for notebooks, training, the registry, serving and status — usable from a laptop over OIDC with no kubeconfig. State-changing operations sit behind an explicit opt-in, because an agent that can redeploy production by accident is a design mistake, not a feature.

GPU capacity runs on HAMi sharing over 8×H100, with selectable VRAM slices and admission-time quota checks that refuse with the actual numbers instead of hanging.

## Systems I build & run

<table>
<tr><td width="50%" valign="top">

**`lazarev.cloud` — self-hosted platform**

A 9-node Proxmox cluster with NVIDIA GPU and Ryzen AI NPU passthrough for local ML workloads, fully infrastructure-as-code across 11 OpenTofu providers. Vault internal PKI and SSO everywhere, a self-hosted CI/CD supply chain (GitLab, Harbor, Nexus, Renovate), Prometheus/Grafana observability, 3-2-1 backups.

`Proxmox · OpenTofu · Vault · GitLab CI · Harbor`

</td><td width="50%" valign="top">

**Local LLM agent memory stack**

External memory for LLM agents — vector storage and retrieval with reranking, persistent agent memory and a fast cache layer. Benchmarked against current research, running entirely on local hardware.

`Qdrant · Mem0 · Valkey · Qwen3 embeddings + reranker`

</td></tr>
<tr><td colspan="2" valign="top">

**Local AI media pipeline**

A ComfyUI image and video generation pipeline tuned for AMD Ryzen AI hardware on ROCm, with a fully autonomous build and setup flow — large generative models on my own silicon, without a cloud bill.

`ComfyUI · ROCm · Ryzen AI MAX+ 395`

</td></tr>
</table>

## Background

Seven years of secure, scalable platforms across bare-metal Linux and AWS. Before the founding MLOps role I was DevOps Manager at the same fintech, standardising Kubernetes across multi-region clusters for 6+ teams and cutting allocated CPU and memory by ~10%. Earlier: a 50%+ cut in company-wide AWS spend and 60% faster deployments at a Dubai real-estate group, and observability handling 150,000 metrics per second at a US e-commerce company.

## Toolbox

<div align="center">

`Kubernetes (EKS & bare-metal)` `Kubeflow` `MLflow` `KServe` `Istio` `Kyverno` `HAMi / NVIDIA H100`
`AWS` `Snowflake` `OpenTofu / Terraform` `Helm` `Argo CD` `GitLab CI` `Proxmox`
`HashiCorp Vault (PKI/OIDC)` `Keycloak` `CrowdSec` `Prometheus / VictoriaMetrics / Grafana` `OpenTelemetry`
`Python` `Go` `Bash` `Linux` `Cisco networking`

</div>

---

<div align="center">

[lazarev.cloud](https://lazarev.cloud) · [LinkedIn](https://www.linkedin.com/in/lazarevtill) · till@lazarev.cloud

*Just a man with servers and ideas.*

</div>
