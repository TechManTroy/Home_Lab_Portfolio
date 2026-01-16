# Project A: Infrastructure Migration (Docker & Linux)

**Objective:** Transition containerized workloads from a Type-2 hypervisor (VirtualBox) to a dedicated bare-metal server to improve resource efficiency and network segmentation.

## 1. Hardware & Network Architecture
* **Primary Host:** Dell OptiPlex Desktop (Bare Metal)
* **OS:** Linux (Ubuntu Server)
* **Network:** Implemented VLANs for traffic isolation.
* **Orchestration:** Docker Engine managed via **Portainer**.

## 2. Implementation Log
### Step 1: Host Provisioning
* Installed Linux OS directly on hardware, removing the virtualization overhead.
* Configured static networking and SSH access.

### Step 2: Network Hardening
* Configured firewall rules (UFW) to allow only essential traffic:
    * Port `22` (SSH)
    * Port `9443` (Portainer HTTPS)

### Step 3: Service Migration
* Migrated persistent data volumes.
* Re-deployed container stacks (Bitcoin Node, Monitoring Tools).
* **Outcome:** Achieved persistent, always-on availability for lab services.
