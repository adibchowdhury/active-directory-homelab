# Active Directory Enterprise Home Lab

![Status](https://img.shields.io/badge/status-planned-lightgrey) ![Environment](https://img.shields.io/badge/environment-virtual_lab-blue) ![Users](https://img.shields.io/badge/target_users-150-informational)

## Project Overview

Design, deploy, secure, and validate a simulated corporate Windows domain environment supporting **150 employee accounts across five departments**. This hands-on project demonstrates Windows Server administration, Active Directory Domain Services (AD DS), networking, PowerShell automation, identity and access management, and security-control validation.

> **Project status:** Planning. Objectives below are targets, not completed work. Screenshots, configurations, results, and diagrams will be added as the lab is built.

### Business Scenario

A fictional organization needs centralized identity management, domain-joined workstations, departmental access controls, repeatable user onboarding/offboarding, and auditable security policies. The lab will implement these requirements in a small virtual environment; **150 users are directory accounts, not 150 virtual machines**.

## Project Objectives

### 1. Infrastructure & Networking
- [ ] Deploy Windows Server evaluation as a virtual machine.
- [ ] Configure static IP addressing, DNS, and isolated virtual networking.
- [ ] Install and configure Active Directory Domain Services (AD DS).
- [ ] Promote Windows Server to a domain controller.
- [ ] Configure Remote Access and NAT in an appropriate lab topology (if supported by available resources).
- [ ] Verify DNS resolution and internal/external network connectivity.

### 2. Active Directory Administration
- [ ] Create five Organizational Units (OUs) representing departments.
- [ ] Bulk-create 150 fictional domain users using PowerShell automation.
- [ ] Create security groups and assign role-based permissions.
- [ ] Implement departmental file shares and NTFS permissions.
- [ ] Configure password policies and account lockout thresholds.
- [ ] Implement user provisioning, disabling, and offboarding workflows.

### 3. Workstation & Domain Integration
- [ ] Deploy a Windows client evaluation virtual machine.
- [ ] Join the Windows client to the Active Directory domain.
- [ ] Authenticate domain users using their assigned credentials.
- [ ] Verify domain connectivity using ping, nslookup, and PowerShell.
- [ ] Configure centralized workstation management using Group Policy.

### 4. Security Hardening & Compliance
- [ ] Implement Group Policy Objects (GPOs) for domain security.
- [ ] Configure Windows Defender Firewall and endpoint security settings.
- [ ] Apply least-privilege access controls for standard users.
- [ ] Configure account auditing and security event logging.
- [ ] Harden Windows Server using applicable DISA STIG recommendations.
- [ ] Map implemented security controls to NIST SP 800-53.

### 5. Automation & Validation
- [ ] Develop PowerShell scripts for automated user and group provisioning.
- [ ] Automate user account creation from CSV files.
- [ ] Validate access permissions across different departments.
- [ ] Test account lockout, password, and authentication policies.
- [ ] Document troubleshooting procedures and security test results.
- [ ] Publish architecture diagrams, scripts, screenshots, and findings to GitHub.

## Technology Stack

| Component | Planned technology | Purpose |
| --- | --- | --- |
| Hypervisor | Oracle VirtualBox | Local virtual machines and networks |
| Server OS | Windows Server Evaluation | Domain controller and server roles |
| Client OS | Windows Enterprise Evaluation | Domain-joined workstation |
| Identity | Active Directory Domain Services | Centralized users, groups, and authentication |
| Networking | DNS, virtual adapters, NAT/routing | Name resolution and controlled connectivity |
| Administration | PowerShell, Group Policy | Automation and configuration management |
| Security | Windows Firewall, auditing, DISA STIG guidance | Hardening and validation |
| Framework | NIST SP 800-53 | Control mapping |

*Evaluation operating systems have time-limited licensing; verify terms before installation. The final topology will be sized for a laptop with 16 GB RAM.*

## Architecture

**Planned topology:** One Windows Server domain controller and one domain-joined Windows client on an isolated lab network, with controlled outbound connectivity as needed. NAT/routing will be designed to avoid exposing the domain controller to the public internet.

**TODO — add:**
- [ ] Architecture diagram (`diagrams/architecture.png`)
- [ ] VirtualBox network mode and adapter configuration
- [ ] Domain name, private IP plan, hostnames, and VM resource allocation
- [ ] Explanation of traffic flow and isolation boundaries

## Implementation Walkthrough

> Add the actual commands, settings, screenshots, and reasoning after completing each stage. Do not publish passwords, secrets, private information, or sensitive configuration values.

### Phase 1 — Virtual Infrastructure
**Status:** Not started  
**TODO:** Record VM creation steps, resource allocations, network adapters, and connectivity tests.  
**Evidence:** `screenshots/phase-1/` (to be added)

### Phase 2 — Domain Services
**Status:** Not started  
**TODO:** Record AD DS installation, domain controller promotion, DNS configuration, and verification commands.  
**Evidence:** `screenshots/phase-2/` (to be added)

### Phase 3 — Identity and Access Management
**Status:** Not started  
**TODO:** Document OU structure, synthetic user data, group design, provisioning scripts, and file permissions.  
**Evidence:** `scripts/`, `configurations/`, `screenshots/phase-3/` (to be added)

### Phase 4 — Domain-Joined Client
**Status:** Not started  
**TODO:** Document client configuration, domain join, user sign-in, and DNS/network tests.  
**Evidence:** `screenshots/phase-4/` (to be added)

### Phase 5 — Security Controls
**Status:** Not started  
**TODO:** Document GPO settings, firewall rules, audit policies, applicable STIG findings, and NIST mappings.  
**Evidence:** `documentation/security-controls.md` (to be added)

### Phase 6 — Validation and Troubleshooting
**Status:** Not started  
**TODO:** Record expected vs. observed results for authentication, access boundaries, lockout behavior, and network connectivity.  
**Evidence:** `documentation/test-results.md`, `documentation/troubleshooting.md` (to be added)

## Security Control Matrix

| Control area | Planned implementation | Validation evidence | Status |
| --- | --- | --- | --- |
| Account management | OU structure, account lifecycle, group membership | TODO | Planned |
| Least privilege | Role-based groups and NTFS permissions | TODO | Planned |
| Authentication | Password and lockout policies | TODO | Planned |
| Audit logging | Security event collection and review | TODO | Planned |
| Endpoint hardening | Firewall and selected STIG-aligned settings | TODO | Planned |
| NIST SP 800-53 mapping | Document applicable controls with rationale | TODO | Planned |

*Control mappings will identify specific control IDs only after implementation and validation. This lab does not claim formal NIST or DISA compliance.*

## Testing & Results

**TODO — replace with observed results:**

| Test | Expected outcome | Actual outcome | Status |
| --- | --- | --- | --- |
| Domain DNS lookup | Client resolves domain services | Not tested | Pending |
| Domain join | Client joins domain successfully | Not tested | Pending |
| User authentication | Authorized account signs in | Not tested | Pending |
| Departmental access | Authorized users access designated shares | Not tested | Pending |
| Access denial | Unauthorized users cannot access restricted shares | Not tested | Pending |
| Account lockout | Configured lockout behavior is enforced | Not tested | Pending |
| Audit events | Relevant actions generate reviewable events | Not tested | Pending |

## Challenges & Lessons Learned

**TODO:** Describe real issues encountered, root causes, troubleshooting steps, and improvements. Include at least one substantive technical lesson per major phase.

## Repository Structure

```text
active-directory-homelab/
├── README.md
├── diagrams/                 # Architecture diagrams (planned)
├── screenshots/              # Redacted implementation evidence (planned)
├── scripts/                  # PowerShell scripts (planned)
├── configurations/           # Sanitized configuration examples (planned)
└── documentation/            # Guides, test results, control mapping (planned)
```

## Key Takeaways

**TODO:** Summarize what was built, what was verified, and how the work applies to systems administration and security engineering roles after the project is completed.

## References

- [Microsoft Learn — Active Directory Domain Services](https://learn.microsoft.com/en-us/windows-server/identity/ad-ds/active-directory-domain-services)
- [Microsoft Evaluation Center](https://www.microsoft.com/en-us/evalcenter/)
- [Oracle VirtualBox](https://www.virtualbox.org/)
- [NIST SP 800-53](https://csrc.nist.gov/pubs/sp/800/53/r5/upd1/final)
- [DISA STIG resources](https://public.cyber.mil/stigs/)

---

**Scope note:** This is an educational, isolated home lab using fictional identities and non-production systems. Screenshots and exported configurations will be reviewed for secrets before publication.
