# An Explainable AI Framework for Classifying Kubernetes Workloads for Quantum, Hybrid, and Classical Execution

**Student:** Olena Khyzhniak 
**Supervisor:** John Rellis
**Programme:** BSc (Honours) in Applied Computing (Cloud and Networks Stream)
**Institution:** South East Technological University, Waterford, Ireland

---

## 2. Introduction

This document presents the project proposal and initial research for AI Q-Migrate Z, submitted in partial fulfilment of the requirements for a Bachelor of Science (Honours) in Applied Computing (Cloud and Networks Stream) at South East Technological University.

The project explores the intersection of three emerging technology domains: Explainable Artificial Intelligence (XAI), hybrid quantum-classical computing, and enterprise cloud infrastructure on IBM Z. The aim is to design and develop a software framework capable of analysing existing Kubernetes-based applications and producing an explainable, reasoned assessment of each component's suitability for migration to a hybrid quantum-classical environment hosted on IBM Z.

Given that this area spans topics typically explored at postgraduate level, the project scope will be refined in close consultation with the supervising lecturer, John Rellis, to ensure it remains achievable within the constraints of a BSc (Honours) final year project.

This document is a living record, intended to be updated and extended incrementally throughout the project lifecycle. All technical terms are defined in the Glossary section of the full project document.

---

## 3.3 Practical Implementation

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

The framework will be deployed and demonstrates the following:

- Displays three real workloads running on the cluster
- Classifies each workload: classical, IBM Z classical, or hybrid quantum
- Explains the classification reasoning using XAI (feature importance)
- For hybrid quantum workloads, executes a real Qiskit circuit and displays the result

---

## References

17. IBM (n.d.) *IBM Turbonomic: Application resource management*. Available at: https://www.ibm.com/products/turbonomic (Accessed: 13 November 2026).

18. Amazon Web Services (n.d.) *AWS Compute Optimizer*. Available at: https://aws.amazon.com/compute-optimizer/ (Accessed: 13 November 2026).

19. Google Cloud (n.d.) *Active Assist: Intelligent recommendations for Google Cloud*. Available at: https://cloud.google.com/solutions/active-assist (Accessed: 13 November 2026).
