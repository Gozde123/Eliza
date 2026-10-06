# Major Activities

Expand on the scope definition by outlining the major activities required to complete the project. Structure these around the five stages of the Team Data Science Process (TDSP): business understanding, data acquisition & understanding, modeling, deployment, and customer acceptance.

Include activities such as project management, feature engineering, model training, performance evaluation and analysis.

Mark each activity as In Scope or Out of Scope to reduce ambiguity.

Add rows as required. The table should give a summary view; add narrative explanation below it where more detail is needed. Activities can be linked to Jira from this page.

## In Scope and Out of Scope

| Status | What it means | Question it answers |
|---|---|---|
| **In Scope** | Work the team will do | What will we build or carry out? |
| **Out of Scope** | Work the team will not do at all | What are we deliberately not building? |

An out-of-scope activity is not the same as a constraint. A constraint is a rule that limits how the in-scope work is done; it goes in `03-assumptions-and-constraints.md`. If you want to show that the project's scope is narrow (for example, you plan no information-elicitation phase), list that here as Out of Scope. Limits on the system's inputs, such as a user-input boundary or English-only text, are constraints.

## Activities that come from a constraint

Many constraints create work and remove work at the same time. Write the decision as three statements, one per place, each pointing to the others:

| Where | What it says | Example wording |
|---|---|---|
| Constraint (`03`) | The rule the system must obey | "The system shall not persist personally identifiable information (e.g., names, email addresses, national ID numbers) in any database, log, or vector index." |
| In Scope (this page) | The work you do because of the constraint | "Implement PII detection and masking on user inputs before logging." "Configure logs to retain only anonymised interaction data." |
| Out of Scope (this page) | The features you give up because of it | "User accounts, personal profiles, and saved conversation history linked to an identity." |

**Do not skip the In Scope row.** Users will type names, emails or account numbers into a chatbot whether you invite them to or not. A rule such as "no PII stored" is not true just because you did not build a profile feature; enforcing it takes work. That work belongs here, in the backlog and in the estimates. Count its effort in `07-cost-and-funding.md`.

The uncertain part becomes a risk in `11-risks.md`, and the in-scope activity is its mitigation. For the example above, the risk is "Users submit PII in free-text queries, and it ends up in logs or the retrieval index".

## Knock-on effect on user stories

Once a constraint is in the charter, a user story that contradicts it is an inconsistency between documents. The review error types call this an External Inconsistency. For example, "As a returning analyst, I want to see my previous questions" contradicts a no-PII rule. Either drop such a story, or rewrite it so the history lives only in the session and is not stored.

## Rules

1. Every activity has a TDSP stage.
2. Every activity is marked In Scope or Out of Scope.
3. Every Out of Scope row says why in its Description, as row 2 below does.
4. Every constraint in `03` that creates work has at least one In Scope row here, and every constraint that removes features has at least one Out of Scope row here.
5. Rows created by a constraint name the constraint ID in their Description (for example "Because of C-03").
6. User authentication and PII storage, if you do not plan them, are listed as Out of Scope.
7. Activities do not increase the scope of the project beyond the first proposal.
8. No user story contradicts a constraint (see the knock-on effect above).

## What doesn't belong here

- **Rules the system must obey** go in `03-assumptions-and-constraints.md` as constraints.
- **What could go wrong** with an activity goes in `11-risks.md`.
- **The order in which activities must happen**, when one blocks another, goes in `06-dependencies.md`.
- **Effort in person-hours** goes in `07-cost-and-funding.md`.

## Activities

| # | Stage | Activity | Description | Status | Jira Task |
|---|---|---|---|---|---|
| 1 | Business Understanding | Define chatbot purpose, users, and success criteria | Completed as part of project chartering. (See Project Executive Summary above) | In Scope | |
| 2 | Business Understanding | Market/competitive analysis of existing chatbot products | Not needed for an academic proof-of-concept | Out of Scope | |
| 3 | | | | | |

## Example (illustrative only)

An excerpt from a longer table for a legal research assistant (a RAG chatbot over legal documents). It shows the rows created by constraints C-03 and C-04 in the example on `03-assumptions-and-constraints.md`.

| # | Stage | Activity | Description | Status | Jira Task |
|---|---|---|---|---|---|
| 7 | Data Acquisition & Understanding | Mask PII in user inputs before logging | Because of C-03. Detect names, emails and ID numbers in queries and mask them before any log write. Mitigation for R-03. | In Scope | (link) |
| 8 | Deployment | Configure logs to keep only anonymized interaction data | Because of C-03. | In Scope | (link) |
| 12 | Deployment | User accounts, personal profiles and saved conversation history | Because of C-03: these would require storing PII. | Out of Scope | |
| 13 | Modeling | Multi-turn dialogue memory | Because of C-04: the system handles single-turn questions only. | Out of Scope | |

## Checklist before submitting

- [ ] Every activity has a TDSP stage (rule 1)
- [ ] Every activity is marked In Scope or Out of Scope (rule 2)
- [ ] Every Out of Scope row says why (rule 3)
- [ ] Every work-creating constraint in `03` has an In Scope row, and every feature-removing constraint has an Out of Scope row (rule 4)
- [ ] Rows created by a constraint name its ID (rule 5)
- [ ] User authentication and PII storage are listed as Out of Scope if you do not plan them (rule 6)
- [ ] No activity goes beyond the first proposal's scope (rule 7)
- [ ] No user story contradicts a constraint (rule 8)
