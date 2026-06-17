# Lagoon Hospitals Development Repository

Welcome to the official development repository for **Lagoon Hospitals**.

This repository serves as the central location for source code management, collaboration, and deployment workflows across software projects maintained by Lagoon Hospitals.

## 📌 Repository Purpose

The objective of this repository is to:

* Maintain high-quality and secure source code.
* Facilitate collaboration among development teams.
* Ensure controlled deployment of applications and services.
* Support consistent software delivery practices across environments.

---

# 🌳 Branching Strategy

The repository follows a structured Git branching model to ensure code quality, traceability, and controlled releases.

| Branch      | Purpose                        | Deployment Environment |
| ----------- | ------------------------------ | ---------------------- |
| `master`    | Production-ready code          | Live / Production      |
| `develop`   | Integration and testing branch | Test / Staging         |
| `feature/*` | New features and enhancements  | None                   |
| `bugfix/*`  | Bug fixes                      | None                   |
| `hotfix/*`  | Emergency production fixes     | Live (after approval)  |

---

## Branch Workflow

### master

The `master` branch contains stable, tested, and approved code that is ready for production deployment.

**Rules**

* Direct commits are prohibited.
* Changes must be merged through Pull Requests.
* Requires approval from designated reviewers.
* Protected branch.

---

### develop

The `develop` branch acts as the primary integration branch where features and fixes are consolidated for testing.

**Rules**

* Receives merges from `feature/*` and `bugfix/*` branches.
* Used for QA and User Acceptance Testing (UAT).
* Protected branch.

---

### feature/*

Feature branches are used to develop new functionality.

**Naming Convention**

```bash
feature/patient-registration
feature/mobile-appointment-booking
feature/dashboard-enhancement
```

**Workflow**

```text
develop
   │
   └── feature/new-feature
            │
            └── Pull Request → develop
```

---

### bugfix/*

Bugfix branches are used to resolve defects identified during development or testing.

**Naming Convention**

```bash
bugfix/login-validation-error
bugfix/payment-processing-issue
```

**Workflow**

```text
develop
   │
   └── bugfix/fix-name
            │
            └── Pull Request → develop
```

---

### hotfix/*

Hotfix branches are created from the `master` branch to address urgent production issues.

**Naming Convention**

```bash
hotfix/security-patch
hotfix/payment-service-failure
```

**Workflow**

```text
master
   │
   └── hotfix/critical-fix
            │
            ├── Pull Request → master
            └── Pull Request → develop
```

---

# 🔄 Pull Request Process

1. Create a branch from the appropriate source branch.
2. Complete development and testing.
3. Submit a Pull Request.
4. Obtain required approvals.
5. Ensure automated checks pass.
6. Merge into the target branch.
7. Delete the source branch after merge.

---

# 🔒 Branch Protection Rules

The following protections should be enabled:

### master

* Require Pull Requests before merging
* Require at least 2 approvals
* Require status checks to pass
* Restrict direct pushes
* Restrict branch deletion

### develop

* Require Pull Requests before merging
* Require at least 1 approval
* Require status checks to pass
* Restrict direct pushes

---

# 🚀 Deployment Flow

```text
Feature Development
        │
        ▼
 feature/*
        │
        ▼
     develop
        │
   Testing/UAT
        │
        ▼
     master
        │
        ▼
   Production
```

For emergency production issues:

```text
master
   │
   ▼
hotfix/*
   │
   ├──► master
   │
   └──► develop
```

---

# 📖 README Display Structure

When visitors open this repository, GitHub will automatically display this README on the repository homepage in the following order:

1. Repository Title
2. Repository Purpose
3. Branching Strategy Table
4. Branch Workflow Details
5. Pull Request Process
6. Branch Protection Rules
7. Deployment Flow Diagram
8. Additional Contribution Guidelines (future)
9. Contact Information (future)

This ensures developers immediately understand:

* The purpose of the repository
* Which branches to use
* How code moves between environments
* Deployment and approval processes

---

# 🤝 Contribution Guidelines

All contributors must:

* Follow the defined branching strategy.
* Use descriptive branch names.
* Submit Pull Requests for all changes.
* Ensure code reviews are completed.
* Adhere to Lagoon Hospitals coding standards and security policies.

---

© Lagoon Hospitals. All rights reserved.
