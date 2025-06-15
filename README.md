# parc-salesforce-devops
Version-controlled Salesforce metadata and automation scripts for the PARC application DevOps pipeline.

## 📘 Project Overview
The PARC Salesforce DevOps project is designed to manage and streamline the development, testing, and deployment of the PARC application on the Salesforce platform. This repository serves as the single source of truth for all metadata, automation scripts, and configuration files used in the DevOps lifecycle.

## 🔄 DevOps Workflow Summary
We follow a source-driven development model using Gearset and Git. The workflow includes:
- Development in Salesforce sandboxes
- Metadata retrieval and commit to Git branches
- Automated validation and deployment using Gearset CI jobs
- Promotion through QA, UAT, and Production environments

## 🌿 Branching Strategy
We use a GitFlow-inspired branching model:
- `main`: Stable production-ready code
- `develop`: Integration branch for features and fixes
- `feature/*`: Feature-specific branches (e.g., `feature/incident-tracking`)
- `release/*`: Pre-release staging branches
- `hotfix/*`: Emergency fixes for production

## 🚀 Deployment Process Using Gearset
1. Developers retrieve metadata from Salesforce and commit to a `feature/*` branch.
2. Gearset CI jobs validate and deploy changes to the `develop` branch and QA org.
3. Once tested, changes are merged into `release/*` and deployed to UAT.
4. After UAT approval, changes are merged into `main` and deployed to Production via Gearset.

## 🤝 Contribution Guidelines
- Fork the repository and create a `feature/*` branch.
- Commit descriptive messages and follow naming conventions.
- Submit a pull request to `develop` for review.
- Ensure all Gearset validations and Apex tests pass before merging.
- Coordinate with the release manager for production deployments.

---

For questions or access requests, please contact the DevOps team.
