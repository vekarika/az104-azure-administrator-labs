# AZ-104 Azure Administrator Labs

![AZ-104 Complete Learning Environment cover showing Azure administration services](docs/visuals/az104-complete-learning-environment-cover.png)

> A hands-on Azure Administrator learning and implementation portfolio aligned with the Microsoft AZ-104 certification objectives.

## About This Repository

This repository documents my hands-on journey through Azure administration using practical labs, automation, validation, troubleshooting, and operational exercises.

My objective is not only to prepare for the Microsoft AZ-104 certification, but also to build practical, job-relevant experience administering Azure environments.

The labs provide structured hands-on experience across:

- Azure identity and governance
- Azure storage
- Azure compute
- Azure networking
- Monitoring and maintenance
- Azure CLI
- PowerShell automation
- Bicep and Infrastructure as Code
- Troubleshooting and validation
- Security and governance considerations

## About Me

**Victor Ekarika**
Network Engineer | Cloud & IT Operations Engineer

My professional interests include cloud infrastructure, networking, Microsoft Azure, Microsoft 365, automation, cybersecurity, and IT operations.

Through this project, I am building and documenting practical Azure administration experience while strengthening my understanding of:

- Microsoft Entra ID and Azure RBAC
- Azure networking and infrastructure
- Azure compute and storage
- Azure governance and Azure Policy
- PowerShell automation
- Azure CLI
- Bicep and Infrastructure as Code
- Azure Monitor and KQL
- Security-aware cloud operations

My long-term career objective is to progress toward a **Cloud Security Architect** role, and this repository forms part of the practical foundation supporting that journey.

## My Learning Approach

Each lab is treated as an operational exercise rather than simply a certification task.

My approach is:

```text
Plan
  ↓
Preflight Validation
  ↓
Deploy
  ↓
Validate
  ↓
Test Failure Conditions
  ↓
Troubleshoot
  ↓
Repair
  ↓
Document Lessons Learned
  ↓
Cleanup
```

---

A command-first path from Azure fundamentals to job-ready administration, aligned with Microsoft AZ-104.

All learner Azure operations use Azure CLI (`az` and `az rest`), Bicep, AzCopy, or KQL from PowerShell 7. There are no browser-based lab steps, screenshots, or screenshot-evidence requirements. Architecture diagrams are the only instructional visuals.

> [!IMPORTANT]
> This independent project is not an official Microsoft course. Azure resources can incur charges. Use an approved disposable subscription, review each lab's cost and permission gates, and complete its residual-resource audit.

## Choose a Pathway

| Pathway | Best for | Route |
|---|---|---|
| Quick Start | New learners who want a safe first deployment | Readiness → Lab 00 → Labs 01, 06, 10, 17, and 22 |
| Full AZ-104 Preparation | Learners covering every official objective | Labs 00–25 in order → all 1,250 questions → Capstones 26–27 |
| Job Ready | Learners practising operational ownership | Labs 00–25 → every break/fix and job-style challenge → both capstones |

The searchable documentation site adds generated domain navigation, a glossary, cost guidance, and private browser-local progress.

## Local Documentation Development

From PowerShell, install the required dependencies:

```powershell
python -m pip install -r requirements-dev.txt -r requirements-docs.txt
```

Build the documentation site:

```powershell
python tools/build_docs_site.py
```

Run the local MkDocs server:

```powershell
python -m mkdocs serve --strict
```

The Pages workflow builds on pull requests and deploys only from `main`.

Before the first deployment, the repository owner must enable GitHub Pages with **GitHub Actions** as its publishing source.

## Start Safely

1. Install or open PowerShell 7.4 or later.
2. Run `./tools/Initialize-LabEnvironment.ps1` for the blocking readiness report.
3. Review [prerequisites](docs/prerequisites.md) and [cost and cleanup safety](docs/cost-and-cleanup.md).
4. Complete [Lab 00: Safe Bootstrap](labs/00-safe-bootstrap/README.md).
5. Choose a pathway above or continue through the [lab catalog](labs/README.md).

The initializer checks:

- Azure CLI
- `az bicep`
- AzCopy
- Python
- Node.js
- Required extensions
- Local configuration
- Lab-specific prerequisites

It does not authenticate, install dependencies silently, register providers, or deploy Azure resources.

## What Every Lab Provides

Each of the 28 standalone lab folders includes:

- A real-world scenario and learner role
- Expected outcome and completion criteria
- Objective-to-checkpoint mapping
- Architecture diagrams and service-topology walkthroughs
- Explicit inputs, permissions, and cost gates
- Read-only preflight checks
- Azure CLI commands in PowerShell blocks
- Expected output
- Positive and negative validation checks
- Safe retry guidance
- Troubleshooting and break/fix scenarios
- Service-specific validation
- Optional job-style challenges
- Dependency-aware cleanup
- Ownership and residual-resource checks
- `Preflight.ps1`
- `Setup.ps1`
- `Validate.ps1`
- `Cleanup.ps1`

Labs 01–25 also include assessment questions mapped to tasks and AZ-104 objectives.

`Setup.ps1` and `Cleanup.ps1` preview by default.

Mutations require:

```text
-Execute
```

Moderate or elevated cost operations require:

```text
-AcknowledgeCost
```

Tenant-wide changes require:

```text
-AcknowledgeTenantChange
```

Lab 00 and Capstones 26–27 are hands-on only.

## AZ-104 Coverage

| Official AZ-104 Domain | Labs | Questions |
|---|---|---:|
| Manage Azure identities and governance | 01–05 | 250 |
| Implement and manage storage | 06–09 | 200 |
| Deploy and manage Azure compute resources | 10–16 | 350 |
| Implement and manage virtual networking | 17–21 | 250 |
| Monitor and maintain Azure resources | 22–25 | 200 |
| Foundation and capstones | 00, 26–27 | Hands-on only |

All 82 official objective bullets are covered.

Every assessment-enabled lab contains exactly 50 questions with a:

- 15 foundational
- 25 applied
- 10 advanced

distribution, for a total of **1,250 questions**.

## Learning and Safety Model

Use a different run ID for the guided and automated lanes.

A successful lab run follows this process:

1. Confirm tools, context, region, quota, SKU, permissions, and inputs without changing Azure.
2. Preview the setup and review the exact ownership boundary.
3. Build each checkpoint using Azure CLI hosted in PowerShell.
4. Prove both the expected state and a denied, absent, or misconfigured state.
5. Diagnose and repair the deterministic break/fix condition.
6. Save redacted command evidence and machine-readable validation results.
7. Preview cleanup, execute it only when ready, and prove no active managed resource remains.
8. Use assessment remediation links to repeat weak tasks.

A deployment is considered successful only when every required checkpoint passes.

Skipped optional gates produce a partial result.

Cleanup passes only when no active managed resources remain. Deliberately retained or soft-deleted items must be listed in `cleanup.json`.

## Repository Interfaces

- [Lab Catalog](labs/README.md)
- [Objective Map](docs/objective-map.md)
- [Permissions Matrix](docs/permissions-matrix.md)
- [Study Plan](docs/study-plan.md)
- [Troubleshooting](docs/troubleshooting.md)
- [Command Cheat Sheet](docs/command-cheatsheet.md)
- [Evidence Handling](docs/evidence-handling.md)
- [Assessment Guide](docs/assessment-guide.md)
- [Assessment Dashboard](docs/question-bank-index.md)
- [Generated Lab Dashboard](docs/implementation-status.md)

## My Portfolio Objective

This repository is intended to demonstrate practical Azure administration capabilities beyond certification knowledge.

As I complete the labs, I will focus on developing and documenting experience in:

- Azure infrastructure administration
- Cloud networking
- Identity and access management
- Azure governance
- Infrastructure automation
- Azure troubleshooting
- Monitoring and operational validation
- Resource lifecycle management
- Security-aware cloud operations

My long-term objective is to build a strong technical foundation for advanced cloud engineering and Cloud Security Architecture roles.

## Repository Validation

Repository authoring and automated validation are performed offline.

No lab is labeled live-verified until a separately approved disposable-environment run completes:

1. The inline implementation path
2. Break/fix testing
3. Validation
4. Cleanup
5. Residual-resource auditing

## License

Code and documentation are available under the [MIT License](LICENSE).