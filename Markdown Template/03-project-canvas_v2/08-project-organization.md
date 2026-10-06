# Project Organization

This page shows who does what, and how the team relates to the people who govern and review the project. Roles use the stakeholder roles of ISO/IEC 5339 wherever possible [1]. Scrum roles can also appear [2].

"Data Scientist: develops the model" is a weak entry. It uses an informal role name and says nothing about which work, at which stage. A strong entry uses the ISO role and makes the responsibility concrete for your project: "AI developer (two named members): design, build, verify and validate the retrieval pipeline and the answer model before deployment." (illustrative only)

This page is a red cell of the Project Canvas, so it must be completed in the first version.

## 1. Project Team Structure

Use an organizational chart to show the structure of the project team and the relationships between team members. Show how the team relates to the governance structure of the project. For a small project, show the roles of the team members; for a larger one, name the groups that form the project teams.

Governance in DI 502:

- **The instructors are the Project Review Committee**.
- **Peer groups also review your documents at Sprints 2, 3 and 4**. After a sprint, an assigned group reviews your documents and fills in your Review page. For Sprint 2 the pairing is announced in the sprint instructions.
- **There is no sponsor**, and there is no single manager: every member manages the project in some capacity.

Show every member on the chart, including those in non-technical roles.

## 2. Roles and Responsibilities

Define the roles and responsibilities of each team member, and of any stakeholders and working groups that have a significant influence on the project.

### Fields

| Field | What it means | Question it answers | Source |
|---|---|---|---|
| **Project Role** | An ISO/IEC 5339 stakeholder role wherever one fits, spelled exactly as below; otherwise a Scrum role | Which standard role is this? | [1] |
| **Responsibilities** | What this role does in *your* project, and at which life cycle stages | What work does this role own? | [1] |
| **Assigned to** | Named team members, or the outside organization or person | Who holds this role? | |

### The roles

Responsibilities below are paraphrased from ISO/IEC 5339. Rewrite each one for your project.

| Role | Responsibility (paraphrased) | Life cycle stages | Source |
|---|---|---|---|
| **AI producer** | Designs, develops, tests and deploys the product or service that uses the AI system; makes the management decisions about starting and retiring it. In this course, the whole team holds this role. | All stages | [1] |
| **AI developer** | Builds the AI product for the producer: model and system design, development, implementation, verification and validation. Can be a team member, a contractor or a partner. Data scientists and data engineers act as AI developers in machine learning [3]. | Design and development; verification and validation | [1] |
| **Data provider** | Collects or prepares the data used by the AI model. Can be a partner of the producer. May also collect data after deployment for continuous validation. | Design and development; verification and validation; after deployment if data is collected for continuous validation | [1] |
| **AI application provider** | Provides the AI system's capabilities as an application, a product or service, to internal or external customers. Can be inside the producer's organization or a third party. | Deployment, operation and monitoring | [1] |
| **AI partner** | Provides services to the AI producer and the AI application provider within a business relationship, for example a cloud machine-learning service. | — | [1] |
| **AI customer** | Uses the AI product or service, or provides it to AI users, and has a business relationship with the AI application provider. Is consulted at inception for requirements and takes part in verification and validation, deployment, operation and retirement. | All stages | [1] |
| **AI user** | Uses the AI product or service. Need not be an AI customer. | Deployment, operation and monitoring | [1] |
| **Community** | People affected by the application beyond its customers and users. | Deployment, operation and monitoring | [1] |
| **Regulators and policy makers** | The authorities in the place of deployment that set and enforce the legal requirements for using AI. | Deployment, operation and monitoring | [1] |

In DI 502, the AI customer is the course instructors and the peer groups.

### Scrum roles

Please also name Scrum roles for sprint work. Use them alongside the ISO roles, not instead of them.

| Role | Responsibility (paraphrased) | Source |
|---|---|---|
| **Product Owner** | Writes most of the user stories and clarifies their Who, What and Why with the team; works with the developers to refine them. | [2] |
| **Scrum Master** | Guides the team, together with the Product Owner, towards user stories that meet the INVEST criteria. | [2] |

## Rules

1. Every Project Role uses an ISO/IEC 5339 role name wherever one fits, spelled exactly [1]. Product Owner and Scrum Master may also appear for sprint work [2]. No other informal role names are used.
2. Every team member appears at least once in Assigned to.
3. Every Responsibilities entry defines what the role does in this specific project.
4. Every role held by more than one person lists each person by name.
5. Every person named as an owner, approver or contact on another page appears here: deliverable approvers in [Deliverables](03-project-canvas_v2/05-deliverables.md), risk owners in [Risks](03-project-canvas_v2/11-risks.md), contacts in [Dependencies](03-project-canvas_v2/06-dependencies.md).
6. The Project Review Committee is the instructors, not team members.
7. The team chart shows how the team relates to governance.
8. The MVP and other customer-facing deliverables are developed for the AI customer, not for the project team.
9. The AI customer row names the course instructors and the peer groups.

## Test to apply to your draft

Collect every name and role that appears on [Milestones](03-project-canvas_v2/02-milestones.md), [Dependencies](03-project-canvas_v2/06-dependencies.md) and [Risks](03-project-canvas_v2/11-risks.md). Can you find each one on this page?

## Not this / this

The left column shows weak entries, each tagged with the rule it breaks.

| Not this | Rule broken | This (illustrative only) |
|---|---|---|
| "Project Review Committee: reviews project outcomes, ensures alignment with goals. Assigned to: two team members." | The committee is the instructors (rule 6) | Remove it from the roles table. Show the instructors as the Project Review Committee on the team chart, with the Sprint 2–4 peer groups beside them. |
| "Data Scientist: develops and fine-tunes the model." | Informal role name (rule 1) | "AI developer (named members): design and fine-tune the adapter, run and record the experiments, and verify it against the evaluation set before deployment." |
| Separate rows for "Scrum Master: manages sprint planning and team coordination" and "Project Lead: manages overall project execution", given to the same person. | "Project Lead" is neither an ISO/IEC 5339 role nor a Scrum role (rule 1) | Keep the Scrum Master row if you use Scrum roles. Overall project execution is part of the AI producer role, which the whole team holds; drop the "Project Lead" row. |
| A roles table with no team chart. | Missing chart and governance relation (rule 7) | A chart showing the team inside the AI producer box, the instructors as Project Review Committee, the peer groups, and the outside data provider and AI partner. |

## Patterns to use if you are stuck

- **One person, several roles:** one row per role, with the person's name in each.
- **Whole team as AI producer:** one row with every member's name.
- **Outside data owner:** the data provider is the organization that published or licenses the dataset; name the team member who handles it in Responsibilities [1].
- **Cloud or model API service:** an AI partner [1].
- **Hosting team or service:** an AI application provider; it can be internal, such as the team itself, or a third-party service [1].

## What doesn't belong here

- **The stakeholders who benefit from the project** go in [Project Executive Summary](03-project-canvas_v2/01-project-executive-summary.md). This page gives responsibilities, not benefits.
- **Team size and weekly hours** are constraints in [Assumptions & Constraints](03-project-canvas_v2/03-assumptions-and-constraints.md).
- **Who approves each deliverable** goes in [Deliverables](03-project-canvas_v2/05-deliverables.md).
- **Who owns each risk** goes in [Risks](03-project-canvas_v2/11-risks.md).

## Roles and Responsibilities table

| Project Role | Responsibilities | Assigned to |
|---|---|---|
| AI producer | | |
| AI developer | | |
| Data provider | | |
| AI application provider | | |
| AI partner | | |
| AI customer | | |
| AI user | | |
| Community | | |
| Regulators and policy makers | | |
| Product Owner | | |
| Scrum Master | | |

## Example (illustrative only)

Scenario: a legal research assistant. Member names are placeholders.

Team chart (as a list):

- Project Review Committee: course instructors. Peer review group at Sprints 2–4.
- AI producer: the whole team (Members 1–4).
  - AI developers: Members 1 and 2 (retrieval and answer model); Member 3 (data pipeline and PII masking).
  - AI application provider: Member 4 (staging deployment and user guide).
- Outside: data provider (document publisher); AI partner (cloud service under the university credit).

| Project Role | Responsibilities | Assigned to |
|---|---|---|
| AI producer | Decide scope changes with the AI customer; approve go/no-go at each milestone. All stages. | Members 1–4 |
| AI developer | Build and verify the retrieval pipeline and answer model; run and record experiments; build PII masking (C-03). Design, development, verification and validation. | Members 1, 2, 3 |
| Data provider | Publish the document set under its licence. Member 3 handles requests and delivery checks ([Dependencies](03-project-canvas_v2/06-dependencies.md) row 2). | Document publisher; Member 3 |
| AI application provider | Deploy to staging, write the user guide, monitor logs in Sprint 4. Deployment, operation and monitoring. | Member 4 |
| AI partner | Provide GPU compute and hosting under the university credit. | Cloud service |
| AI customer | Agree on the target metric and accept the MVP ([Milestones](03-project-canvas_v2/02-milestones.md)). | Course instructors and peer groups |
| Scrum Master | Run sprint planning and retrospectives. | Member 4 |
| AI user | Ask research questions and rate answers during the pilot. | Associates in the pilot group (scenario) |
| Community | Members of the public affected by the advice associates give. | — |
| Regulators and policy makers | The bar association and data-protection authority where the assistant is used. | — |

## Checklist before submitting

- [ ] Every Project Role uses an ISO/IEC 5339 role name where one fits, and otherwise only Product Owner or Scrum Master (rule 1)
- [ ] Every team member appears at least once (rule 2)
- [ ] Every Responsibilities cell is specific to this project (rule 3)
- [ ] Every shared role lists each person by name (rule 4)
- [ ] Every owner, approver and contact on [Milestones](03-project-canvas_v2/02-milestones.md), [Dependencies](03-project-canvas_v2/06-dependencies.md) and [Risks](03-project-canvas_v2/11-risks.md) appears here (rule 5)
- [ ] The Project Review Committee is shown as the instructors (rule 6)
- [ ] The team chart shows the relation to governance (rule 7)
- [ ] Customer-facing deliverables are for the AI customer (rule 8)
- [ ] The AI customer row names the course instructors and peer groups (rule 9)

---

## References

[1] ISO/IEC JTC 1/SC 42, *ISO/IEC 5339:2024 Information technology — Artificial intelligence — Guidance for AI applications*, 1st ed. Geneva, Switzerland: International Organization for Standardization and International Electrotechnical Commission, Jan. 2024. UK implementation: BS ISO/IEC 5339:2024, London, UK: BSI Standards Limited, 2024.

[2] A. Ben Salem, "Creating the Perfect User Story with INVEST Criteria," Scrum-Master·Org, Dec. 5, 2023 (updated Jun. 20, 2024). [Online]. Available: https://scrum-master.org/en/creating-the-perfect-user-story-with-invest-criteria/ (accessed Oct. 5, 2026).

[3] ISO/IEC JTC 1/SC 42, *ISO/IEC 5338:2023 Information technology — Artificial intelligence — AI system life cycle processes*, 1st ed. Geneva, Switzerland: International Organization for Standardization and International Electrotechnical Commission, Dec. 2023. UK implementation: BS ISO/IEC 5338:2023, London, UK: BSI Standards Limited, 2024.
