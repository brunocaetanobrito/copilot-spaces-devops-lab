# Copilot Spaces DevOps Lab

Supporting reference material for a product feedback submission to GitHub's Copilot Conversations forum: [Create an advanced follow-up module for Copilot Spaces on Microsoft Learn](https://github.com/orgs/community/discussions/207031).

**Repository name suggestion:** `copilot-spaces-devops-lab`

## Purpose
This repository outlines a proposed learning path and hands-on lab series that would extend the Microsoft Learn module *Introduction to Copilot Spaces* into an advanced, production-oriented track for Developer Tools and DevOps practitioners. It sketches reproducible labs, templates, and curated Copilot Chat prompts to teach CI/CD, IaC, dependency analysis, story refinement, PR review, and enterprise governance using Copilot Spaces.

## Proposed structure
None of the files below exist yet - this repository currently contains only this proposal.

- `learn-path/` — module guides and learning objectives.
- `labs/lab-01-devops-space/` — hands‑on lab with step‑by‑step exercises.
- `.github/workflows/ci.yml` — example multi‑stage pipeline.
- `scripts/check-deps.sh` — wrapper to run dependency scanners.
- `prompts/prompts.md` — curated Copilot Chat prompts.
- `analysis/dependency-report.md` — template for scan results and mitigation actions.
- `playbooks/` — remediation and rollback playbooks.
- `examples/sample-prs/` — sample PRs and diffs for review exercises.

## Learning path overview
**Module 1 — Advanced Concepts for Copilot Spaces**  
Deep dive into Space scopes, context management, and collaboration patterns.

**Module 2 — CI/CD with Copilot Spaces**  
Author and troubleshoot GitHub Actions and Azure DevOps pipelines inside a Space.

**Module 3 — Infrastructure as Code Workflows**  
Hands‑on with Terraform, Bicep, and ARM templates using Copilot assistance.

**Module 4 — Dependency Analysis and Mitigation**  
Run scanners, interpret results with Copilot Chat, and produce mitigation playbooks.

**Module 5 — Story Refinement and PR Review**  
Convert user stories into acceptance criteria and use AI‑assisted code review workflows.

**Module 6 — Enterprise Governance and Adoption**  
Policies, auditability, access control, and operational checklists for corporate use.

## Lab exercises (Lab 01: DevOps Space)
Open the repo in a Copilot Space and complete these exercises:

1. **Open the Space**  
   - Fork the repo and open it in Copilot Spaces. Ensure editor, terminal, and Copilot Chat panes are visible.

2. **CI/CD authoring and troubleshooting**  
   - Inspect `/.github/workflows/ci.yml`. Use Copilot to generate a multi‑stage workflow (build → test → deploy).  
   - Simulate a failing job and use Copilot Chat to diagnose and propose fixes. Commit a fix to a branch and create a sample PR.

3. **IaC validation and refactor**  
   - Review files in `/infrastructure/terraform/`. Ask Copilot to suggest modularization, variable usage improvements, and security hardening.

4. **Dependency analysis and mitigation**  
   - Run `scripts/check-deps.sh` to collect scanner outputs. Use Copilot Chat to summarize results, prioritize vulnerabilities, and produce a mitigation playbook. Commit `analysis/dependency-report.md`.

5. **Story refinement workshop**  
   - Convert a sample user story in `/docs/user-stories.md` into acceptance criteria, tasks, and CI checks using Copilot prompts. Create issues and link them to a PR.

6. **Governance drill**  
   - Apply the governance checklist, simulate an approval flow, and commit audit artifacts to the repo.

## Prompts collection (`prompts/prompts.md`)
**Refine story**  
```
Convert this user story into acceptance criteria, implementation tasks, and suggested tests. Highlight integration risks and required CI checks.
```

**Review PR**  
```
Analyze this diff and list bugs, security issues, performance concerns, and missing tests. Suggest concrete code changes and test cases.
```

**Dependency mitigation**  
```
Summarize the dependency scan outputs, prioritize vulnerabilities by severity and exploitability, and produce a mitigation playbook with commands, tests, and rollback steps.
```

**IaC refactor**  
```
Review these IaC files and suggest modularization, variable usage improvements, and security hardening recommendations.
```

## Governance checklist
- **Access control:** define who can open and execute Spaces and who can approve PRs.  
- **Audit trail:** commit dependency reports and playbooks to the repo for traceability.  
- **Testing gates:** require automated dependency checks and tests before merges.  
- **Approval workflow:** require human review for major dependency upgrades and infra changes.  
- **Sandboxing:** provide a disposable sandbox environment for learners to run labs safely.

## How to use this repo in Microsoft Learn
- Publish the repo as a downloadable lab or template for a Learn module.  
- Each module should include learning objectives, estimated time, prerequisites, and expected outcomes.  
- Provide step‑by‑step tasks and expected results for each exercise.  
- Link the lab from the Learn module so learners can fork the repo and open a Copilot Space to run the exercises.

## Contribution and license
**Contributing**  
Contributions are welcome. Open issues for improvements, add sample PRs, or propose new prompts and playbooks.

**License**  
Choose an appropriate open source license for your organization (for example, MIT or Apache 2.0) and add a `LICENSE` file.

## Suggested initial files to commit
```
README.md
learn-path/module-01-advanced-concepts.md
learn-path/module-02-ci-cd.md
learn-path/module-03-iac.md
learn-path/module-04-deps.md
learn-path/module-05-stories-prs.md
learn-path/module-06-governance.md
labs/lab-01-devops-space/README-lab.md
labs/lab-01-devops-space/.github/workflows/ci.yml
labs/lab-01-devops-space/scripts/check-deps.sh
labs/lab-01-devops-space/prompts/prompts.md
labs/lab-01-devops-space/examples/sample-prs/README.md
analysis/dependency-report.md
playbooks/ci-troubleshooting.md
```
