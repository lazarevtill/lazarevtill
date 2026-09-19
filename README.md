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

## Things I've built

<table>
<tr><td width="50%" valign="top">

### [ServerGlass](https://github.com/lazarevtill/ServerGlass)

Agentless SSH server monitoring for macOS, iOS, Android, Windows and Linux. One Rust core owns the parsing, scheduling, rate maths and health verdicts; each platform contributes only a view.

A full refresh costs exactly **one** network round trip however many collectors are enabled — and a test fails if that ever stops being true. Nothing is installed, written or modified on a monitored host; no sample ever reaches disk.

`Rust · SwiftUI · Kotlin · GTK4 · WinUI 3 · UniFFI`

</td><td width="50%" valign="top">

### [Morgan](https://github.com/lazarevtill/Morgan)

A project-scoped memory for AI tools, consolidated into dated facts by a local model. Tell it something from any repository; any MCP client recalls it, scoped to the repo it is working in.

Hybrid recall (sqlite-vec + FTS5, Cyrillic-aware) fused by reciprocal rank, facts with validity intervals rather than overwrites, and a labelled probe suite that scores recall@k instead of assuming it works.

`Python · SQLite · MCP · llama.cpp · RAG`

</td></tr>
<tr><td width="50%" valign="top">

### [strix-halo-llm](https://github.com/lazarevtill/strix-halo-llm)

Measured llama.cpp tuning for AMD Strix Halo — the real memory ceiling (~109 GB, not the 96 GB the BIOS implies), the flags that matter, and five "obvious" optimisations that measurement killed.

Shipped with the eval harness and a catalogue of fourteen harness bugs, each with the believable wrong number it produced. When the suites turned out to be measuring the tasks instead of the models, the numbers were withdrawn rather than published.

`PowerShell · Python · Vulkan · benchmarking`

</td><td width="50%" valign="top">

### [lazarev.cloud](https://lazarev.cloud)

My own production platform: a 9-node Proxmox cluster with NVIDIA GPU and Ryzen AI NPU passthrough for local ML workloads, fully infrastructure-as-code across 11 OpenTofu providers.

Vault internal PKI and SSO everywhere, a self-hosted CI/CD supply chain (GitLab, Harbor, Nexus, Renovate), Prometheus/Grafana observability, 3-2-1 backups.

`Proxmox · OpenTofu · Vault · GitLab CI · Harbor`

</td></tr>
</table>

Also: [fingerprint-manager](https://github.com/lazarevtill/fingerprint-manager), a Qt desktop front end for `fprintd`.

## Background

Seven years of secure, scalable platforms across bare-metal Linux and AWS. Before the founding MLOps role I was DevOps Manager at the same fintech, standardising Kubernetes across multi-region clusters for 6+ teams and cutting allocated CPU and memory by ~10%. Earlier: a 50%+ cut in company-wide AWS spend and 60% faster deployments at a Dubai real-estate group, and observability handling 150,000 metrics per second at a US e-commerce company.

## Toolbox

<div align="center">

`Kubernetes (EKS & bare-metal)` `Kubeflow` `MLflow` `KServe` `Istio` `Kyverno` `HAMi / NVIDIA H100`
`AWS` `Snowflake` `OpenTofu / Terraform` `Helm` `Argo CD` `GitLab CI` `Proxmox`
`HashiCorp Vault (PKI/OIDC)` `Keycloak` `CrowdSec` `Prometheus / VictoriaMetrics / Grafana` `OpenTelemetry`
`Python` `Go` `Rust` `Bash` `Linux` `Cisco networking`

</div>

---

<div align="center">

[lazarev.cloud](https://lazarev.cloud) · [LinkedIn](https://www.linkedin.com/in/lazarevtill) · till@lazarev.cloud

*Just a man with servers and ideas.*

</div>
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

## Things I've built

<table>
<tr><td width="50%" valign="top">

### [ServerGlass](https://github.com/lazarevtill/ServerGlass)

Agentless SSH server monitoring for macOS, iOS, Android, Windows and Linux. One Rust core owns the parsing, scheduling, rate maths and health verdicts; each platform contributes only a view.

A full refresh costs exactly **one** network round trip however many collectors are enabled — and a test fails if that ever stops being true. Nothing is installed, written or modified on a monitored host; no sample ever reaches disk.

`Rust · SwiftUI · Kotlin · GTK4 · WinUI 3 · UniFFI`

</td><td width="50%" valign="top">

### [Morgan](https://github.com/lazarevtill/Morgan)

A project-scoped memory for AI tools, consolidated into dated facts by a local model. Tell it something from any repository; any MCP client recalls it, scoped to the repo it is working in.

Hybrid recall (sqlite-vec + FTS5, Cyrillic-aware) fused by reciprocal rank, facts with validity intervals rather than overwrites, and a labelled probe suite that scores recall@k instead of assuming it works.

`Python · SQLite · MCP · llama.cpp · RAG`

</td></tr>
<tr><td width="50%" valign="top">

### [strix-halo-llm](https://github.com/lazarevtill/strix-halo-llm)

Measured llama.cpp tuning for AMD Strix Halo — the real memory ceiling (~109 GB, not the 96 GB the BIOS implies), the flags that matter, and five "obvious" optimisations that measurement killed.

Shipped with the eval harness and a catalogue of fourteen harness bugs, each with the believable wrong number it produced. When the suites turned out to be measuring the tasks instead of the models, the numbers were withdrawn rather than published.

`PowerShell · Python · Vulkan · benchmarking`

</td><td width="50%" valign="top">

### `lazarev.cloud` — self-hosted platform

A 9-node Proxmox cluster with NVIDIA GPU and Ryzen AI NPU passthrough for local ML workloads, fully infrastructure-as-code across 11 OpenTofu providers.

Vault internal PKI and SSO everywhere, a self-hosted CI/CD supply chain (GitLab, Harbor, Nexus, Renovate), Prometheus/Grafana observability, 3-2-1 backups.

`Proxmox · OpenTofu · Vault · GitLab CI · Harbor`

</td></tr>
</table>

Also: [fingerprint-manager](https://github.com/lazarevtill/fingerprint-manager), a Qt desktop front end for `fprintd`.

## Background

Seven years of secure, scalable platforms across bare-metal Linux and AWS. Before the founding MLOps role I was DevOps Manager at the same fintech, standardising Kubernetes across multi-region clusters for 6+ teams and cutting allocated CPU and memory by ~10%. Earlier: a 50%+ cut in company-wide AWS spend and 60% faster deployments at a Dubai real-estate group, and observability handling 150,000 metrics per second at a US e-commerce company.

## Toolbox

<div align="center">

`Kubernetes (EKS & bare-metal)` `Kubeflow` `MLflow` `KServe` `Istio` `Kyverno` `HAMi / NVIDIA H100`
`AWS` `Snowflake` `OpenTofu / Terraform` `Helm` `Argo CD` `GitLab CI` `Proxmox`
`HashiCorp Vault (PKI/OIDC)` `Keycloak` `CrowdSec` `Prometheus / VictoriaMetrics / Grafana` `OpenTelemetry`
`Python` `Go` `Rust` `Bash` `Linux` `Cisco networking`

</div>

---

<div align="center">

[lazarev.cloud](https://lazarev.cloud) · [LinkedIn](https://www.linkedin.com/in/lazarevtill) · till@lazarev.cloud

*Just a man with servers and ideas.*

</div>
