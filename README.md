# microsoft-az-800-az-801-study-guide-notes
Complete community study guide, revision notes, hands-on lab scenarios, and study resources for Microsoft AZ-800 &amp; AZ-801 exams (Windows Server Hybrid Administrator Associate)
# Microsoft Windows Server Hybrid Administrator Associate (AZ-800 & AZ-801) Study Guide

Welcome to the ultimate community-driven study guide for earning the **Microsoft Certified: Windows Server Hybrid Administrator Associate** credential by passing both **Exam AZ-800** and **Exam AZ-801**.

Whether you are an enterprise system administrator, cloud engineer, IT infrastructure manager, or hybrid systems architect, this repository provides a detailed, practical, and structured roadmap to master core and advanced Windows Server hybrid capabilities across on-premises and Microsoft Azure environments.

---

## 📌 Certification Overview

To earn the **Windows Server Hybrid Administrator Associate** badge, candidates must successfully pass two exams:

1. **Exam AZ-800:** Administering Windows Server Hybrid Core Infrastructure
2. **Exam AZ-801:** Configuring Windows Server Hybrid Advanced Services

* **Exam Provider:** Microsoft / Pearson VUE
* **Question Count:** ~40–60 questions per exam (Multiple Choice, Drag-and-Drop, Active Screen, Case Studies)
* **Passing Score:** 700 / 1000 per exam
* **Duration:** 100 minutes exam duration per test (~120 minutes seating time)
* **Retirement Notice:** Per Microsoft Learn, AZ-800 and AZ-801 exams are scheduled to retire on September 30, 2026.

---

## 🎯 Who Should Take These Exams?

- **Windows Server Administrators:** Systems engineers seeking to extend on-premises Active Directory, File Services, and Hyper-V workloads into Microsoft Azure.
- **Hybrid Cloud Engineers:** IT professionals managing Azure Arc-enabled servers, hybrid networking (VPN/ExpressRoute), and Azure File Sync.
- **Infrastructure & Security Operations Specialists:** Engineers tasked with managing disaster recovery (Azure Site Recovery), failover clusters, and cross-realm security baselines.

---

## 📊 Exam Objectives & Domain Breakdown

### Exam AZ-800: Core Infrastructure (Domain Weights)
| Domain | Weightage |
| :--- | :--- |
| **Deploy and manage Active Directory Domain Services (AD DS) in on-premises and cloud environments** | 30–35% |
| **Manage Windows Servers and workloads in a hybrid environment** | 10–15% |
| **Manage virtual machines and containers** | 15–20% |
| **Implement and manage an on-premises and hybrid networking infrastructure** | 15–20% |
| **Manage storage and file services** | 15–20% |

### Exam AZ-801: Advanced Services (Domain Weights)
| Domain | Weightage |
| :--- | :--- |
| **Secure Windows Server on-premises and hybrid infrastructures** | 25–30% |
| **Implement and manage Windows Server high availability** | 10–15% |
| **Implement disaster recovery** | 10–15% |
| **Migrate servers and workloads** | 20–25% |
| **Monitor and troubleshoot Windows Server environments** | 20–25% |

---

## 🧠 Detailed Study Notes & Important Concepts

### Part 1: AZ-800 (Core Infrastructure)

#### Active Directory & Identity
* **Hybrid Identity:** Connecting on-premises Active Directory Domain Services (AD DS) to Microsoft Entra ID using **Microsoft Entra Connect Sync** or **Microsoft Entra Cloud Sync**.
* **FSMO Roles:** Managing Schema Master, Domain Naming Master, RID Master, PDC Emulator, and Infrastructure Master placement and seize/transfer procedures.
* **Microsoft Entra Domain Services:** Managed domain services (domain join, group policy, LDAP, Kerberos/NTLM) running in Azure without deploying infrastructure domain controllers.

#### Hybrid Server Management
* **Azure Arc-Enabled Servers:** Onboarding physical/virtual Windows Servers outside Azure into the Azure Resource Manager (ARM) plane to enforce Azure Policy, Azure Extension deployment, and Defender for Cloud management.
* **Windows Admin Center (WAC):** Browser-based management console for managing servers, clusters, hyper-converged infrastructure, and cloud integration points.

#### Virtualization & Networking
* **Hyper-V & Azure VMs:** Managing Hyper-V hosts, VM generation differences, nested virtualization, Azure VM resizing, and Availability Zones.
* **Hybrid Networking:** Configuring DNS resolution between on-premises DNS and Azure Private DNS Zones, Azure VPN Gateways (Site-to-Site), and Azure Route Server.

#### Storage & File Services
* **Storage Spaces Direct (S2D):** Software-defined storage for hyper-converged clusters using local storage drives over SMB3 / SMB Direct (RDMA).
* **Azure File Sync:** Replicating on-premises file server shares to Azure Files shares while providing cloud tiering to retain local disk space.

---

### Part 2: AZ-801 (Advanced Services)

#### Security & Hardening
* **Local Administrator Password Solution (LAPS):** Managing Windows LAPS (integrated into Active Directory and Microsoft Entra ID) for dynamic local admin password rotation.
* **Credential Guard & Credential Isolation:** Utilizing virtualization-based security (VBS) to prevent credential theft tools (e.g., Mimikatz) from extracting NTLM/Kerberos tickets from memory.
* **SMB over QUIC:** Provides secure, encrypted file share connectivity for remote workers without requiring a traditional VPN network client.

#### High Availability & Disaster Recovery
* **Failover Clustering:** Managing multi-site clusters, quorum configurations (Cloud Witness in Azure Storage), and Cluster-Aware Updating (CAU).
* **Azure Site Recovery (ASR):** Orchestrating VM replication, failover testing, and automated disaster recovery from on-premises Hyper-V/VMware into Azure IaaS.

#### Migration & Monitoring
* **Azure Migrate:** Discovering, assessing, and migrating on-premises physical and virtual Windows Servers into Azure virtual machines.
* **Monitoring & Insights:** Collecting log events via Azure Monitor Agent (AMA), Data Collection Rules (DCRs), and Kusto Query Language (KQL) queries.

---

## 🛠️ Practical Hands-on Exercises (Labs)

To gain required practical operational proficiency, execute these four hands-on scenario labs:

1. **Deploy Azure File Sync with Cloud Tiering:**
   * Provision an Azure Storage Account and File Share.
   * Install the Azure File Sync agent on an on-premises Windows Server node.
   * Register the server, set up a Sync Group, configure a server endpoint, and enable **Cloud Tiering** to automatically offload infrequently accessed files.
2. **Onboard Servers to Azure Arc:**
   * Generate an onboarding script from the Azure Portal using an interactive authentication mode or Service Principal.
   * Run the script on a local Windows Server instance.
   * Apply an Azure Policy definition to evaluate guest OS compliance metrics directly from the Azure portal.
3. **Configure a Cloud Witness for Failover Clustering:**
   * Set up a 2-node Windows Server Failover Cluster using Windows Admin Center.
   * Provision a general-purpose Azure Storage Account.
   * Configure the cluster quorum to use a **Cloud Witness** backended by the Azure storage account key.
4. **Build an Azure Site Recovery (ASR) Vault:**
   * Deploy a Recovery Services Vault in an Azure region.
   * Prepare the source environment (Hyper-V host or VM) and establish replication policies.
   * Perform a **Test Failover** into an isolated Azure Virtual Network without disrupting production traffic.

---

## 📅 30-Day Dual-Exam Study Plan
