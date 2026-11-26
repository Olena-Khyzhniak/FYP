# AI-Driven Workload Analysis and Intelligent Resource Recommendation: An Explainable AI Architecture for Classical, IBM Z, and Quantum-Hybrid Computing

**Student:** Olena Khyzhniak 
**Supervisor:** John Rellis
**Programme:** BSc (Honours) in Applied Computing (Cloud and Networks Stream)
**Institution:** South East Technological University, Waterford, Ireland

---

## Introduction

This document presents the project proposal and initial research, submitted in partial fulfilment of the requirements for a Bachelor of Science (Honours) in Applied Computing (Cloud and Networks Stream) at South East Technological University.

The aim of this project is to design and develop an intelligent architecture that runs multiple workloads on a Kubernetes cluster, collects real-time performance metrics using Prometheus and Grafana, and employs an Explainable AI component to analyse workload behaviour and recommend the most appropriate computing resources and platforms. Based on metrics such as CPU and memory utilisation, I/O activity, transaction throughput, and computational intensity, the AI component will identify potential bottlenecks and provide reasoned recommendations. These may include optimising existing classical infrastructure, considering IBM Z for transaction-intensive and I/O-heavy workloads, or exploring hybrid quantum-classical computing for suitable computationally complex problems. The system will also explain the reasoning behind each recommendation, helping users understand not only what resources may be required, but why a particular computing platform may be more suitable.

Given that this area spans topics typically explored at postgraduate level, the project scope will be refined in close consultation with the supervising lecturer, John Rellis, to ensure it remains achievable within the constraints of a BSc (Honours) final year project.

This document is a living record, intended to be updated and extended incrementally throughout the project lifecycle. All technical terms are defined in the Glossary section of the full project document.

---

## Practical Implementation

### Target User

A DevOps engineer or Cloud architect at a company that already runs Kubernetes workloads and wants to understand which of them are suitable for migration to IBM Z or hybrid quantum-classical infrastructure in the future.

### How It Works in Practice

- The company already has a Kubernetes cluster with running workloads
- They install the framework inside their own infrastructure (`helm install q-migrate`)
- The framework connects to their existing Prometheus instance (present in 90% of enterprise clusters)
- It analyses their real workloads based on collected metrics
- It produces a report: what is worth migrating, where, and why

This is not a public website where a user enters a URL. It is a tool installed inside a company's own infrastructure, similar to how Grafana or Prometheus are deployed and used internally.

### Real-World Analogues

- Turbonomic (IBM) analyses workloads and recommends where to run them (IBM, n.d.)
- AWS Compute Optimizer recommends the right compute size for a given workload (Amazon Web Services, n.d.)
- Google Active Assist provides optimisation recommendations for GCP resources (Google Cloud, n.d.)

AI Q-Migrate Z follows the same pattern but adds a quantum dimension: it identifies which workloads are candidates for quantum or hybrid quantum-classical execution.

### Practical Value

- **Now (2026):** helps companies identify which workloads are worth exploring for quantum computing, saving time on manual analysis and consultancy
- **Future (2030+):** when fault-tolerant quantum hardware matures, companies will already know what to migrate first

### Project Scope

The project will cover the following areas:

- Deploy and run three representative workloads on a MicroK8s Kubernetes cluster, with real-time performance monitoring using Prometheus and Grafana.
- Integrate an LLM (IBM Granite via watsonx.ai) to analyse collected metrics and workload behaviour independently for each workload.
- Evaluate workload characteristics, including CPU and memory utilisation, I/O activity, transaction throughput, and computational intensity, to identify resource requirements and potential performance bottlenecks.
- Generate AI-driven recommendations on the most suitable computing environment for each workload, considering classical infrastructure, IBM Z, and hybrid quantum-classical computing where appropriate.
- Provide explainable recommendations, describing the metrics and workload characteristics behind each decision rather than simply assigning a workload to a computing platform.
- Present monitoring data, AI-generated analysis, and resource recommendations through a Grafana dashboard or a lightweight web interface accessible at olenaonline.eu/q-migrate.

---

## References

17. IBM (n.d.) *IBM Turbonomic: Application resource management*. Available at: https://www.ibm.com/products/turbonomic (Accessed: 13 November 2026).

18. Amazon Web Services (n.d.) *AWS Compute Optimizer*. Available at: https://aws.amazon.com/compute-optimizer/ (Accessed: 13 November 2026).

19. Google Cloud (n.d.) *Active Assist: Intelligent recommendations for Google Cloud*. Available at: https://cloud.google.com/solutions/active-assist (Accessed: 13 November 2026).
