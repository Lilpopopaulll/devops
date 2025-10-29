# Infrastructure As Code Lab Recap

## Main Purpose of the Lab

The main goal of this lab was to **understand Infrastructure as Code (IaC)** principles through two different approaches:
- **Imperative** (Vagrant + Shell Provisioner): manually executing configuration commands on a virtual machine.
- **Declarative** (Vagrant + Ansible): automatically defining and provisioning infrastructure through playbooks.

---

## Possible Application in a Company

In a professional environment, the concepts used in this lab can be applied to:

- **Automating infrastructure setup** for development, testing, or production environments.
- **Standardizing configurations** across multiple servers.
- **Reducing human errors** 
- **Simplifying onboarding** for new developers (a full environment can be created with a single `vagrant up`).
- **Integrating with CI/CD pipelines**, for instance, automatically provisioning test environments before running integration tests.

Example:  
A DevOps engineer could use **Vagrant + Ansible** to spin up consistent GitLab instances for testing configuration changes before deploying them to production.

---

## Step in the DevOps Cycle

This lab directly contributes to building a **perfect Agile DevOps flow**, where the process is:

> **Write code → Test → Deploy to production**

With **Infrastructure as Code (IaC)**, as implemented in this lab:
- The **infrastructure is treated like code** — it’s versioned, reviewed, and maintained in Git.
- Any developer can **recreate the entire environment automatically**, using simple commands (`vagrant up`).
- Infrastructure changes are **tracked, reproducible, and reversible**.
- It enables **faster iteration** between development, testing, and deployment phases.



---

## Problems Encountered and Solutions

### 1. **Vagrant not recognizing the VirtualBox provider**
**Error:**  The provider 'virtualbox' could not be found.
**Cause:** VirtualBox was not properly installed or not added to PATH.  
**Solution:** Reinstalled VirtualBox and rebooted the system.


## Final State of the Lab

The virtual environments were successfully created and provisioned.

GitLab was installed and accessible through http://localhost:8080.

Health checks (/health, /readiness, /liveness) returned positive responses.
