# DI 502 — Weekly Expectations and Deliverables

This document tells you what to do each week, what to deliver at the end of each sprint, and where everything lives in your repository. It is a living document: changes are announced in class and made through pull requests.

---

## Working principles

- **Everything lives in Git as Markdown.** Charter, design notes, decisions, spike notes, evaluation results and sprint reports are `.md` files in your team repository.
- **Keep documents short.** No document should be longer than one or two pages. Specifications are not separate documents: parameters live in `config/rag.yaml`, and results live in Weights & Biases.
- **Jira is the single place for planning.** GitHub is the place for code and pull requests. GitHub Issues are disabled in team repositories.
- **Every branch, commit and pull request contains a Jira key**, for example `DI3-14-vector-store-adr`. This links your work to Jira automatically.
- **Decisions are recorded when they are made**, as Architecture Decision Records (ADRs), not written up front.
- **Everything that affects an answer is versioned**: code, dependencies, models, documents, prompts, configuration and the evaluation set. The AI Bill of Materials (`ai-bom.yaml`) lists them.

---

## Repository structure

```
<team-repo>/
├── README.md               # How to install and run the system
├── ai-bom.yaml             # AI Bill of Materials (from Sprint 2)
├── requirements.txt        # Pinned dependencies (exact versions)
├── config/
│   └── rag.yaml            # All parameters: chunking, models, top-k, prompt variant
├── prompts/                # Prompt templates, one file per template
├── data/
│   └── manifest.csv        # Source URL, licence, version date and hash of each document
├── src/                    # Code
└── docs/
    ├── charter.md          # Sprint 1; later updated only through pull requests
    ├── design.md           # Starts in Sprint 2 as a one-page overview
    ├── adr/                # One file per decision, e.g. 0002-vector-store.md
    ├── spikes/             # Learning and hypothesis notes
    ├── eval/
    │   ├── eval-set-v1.csv # Question, type, gold answer, gold source
    │   └── results.md      # Metrics per sprint, compared with the baseline
    └── sprints/
        └── sprint-N.md     # One-page report per sprint
```

---

## Sprint 1 fundamentals

Most of you are new to at least some of these topics. By the **end of Sprint 1 (28/10)**, every team member should be able to do the following. Use the timeboxed learning spikes in Sprint 1 to close your gaps, and pair with a teammate who already knows the topic.

| Topic | You should be able to… | Suggested resource |
| --- | --- | --- |
| **Git & GitHub** | Clone a repository, create a branch, commit, push, open a pull request, review a teammate's pull request and resolve a merge conflict. | *Pro Git* (free online book), chapters 1–3 |
| **Markdown** | Write headings, lists, tables, code blocks, links and GitHub note boxes (`> [!NOTE]`). | GitHub Docs: "Basic writing and formatting syntax" |
| **Scrum basics** | Explain the Scrum roles, events and artefacts, and the difference between a user story, a task and a spike. | Scrum.org "What is Scrum?" video series and the Scrum Guide |
| **Jira** | Create stories, spikes and sub-tasks, plan a sprint, move issues on the board and link issues to GitHub through Jira keys. | Coursera: *Agile with Atlassian Jira* (Scrum module and lab) |
| **LLM basics** | Explain what a token, a context window, a prompt and temperature are, and why LLMs hallucinate. Run a small open-source model in Colab. | Workshop material (14/10) |
| **Embeddings & vector search** | Explain what an embedding is and how similarity search finds relevant passages. | Workshop material (14/10) |
| **RAG** | Explain the indexing and query phases of a RAG pipeline and why RAG reduces hallucination. | Lewis et al. (2020) and the lecture slides |
| **Prompt engineering** | Write a prompt that tells the model to answer only from the given passages and to say when it does not know. | Workshop material |
| **Evaluation basics** | Explain what an evaluation set is, why it must be fixed before experiments, and what "the gold article is in the top 5 results" measures. | Lecture slides: "Requirements, scope and acceptance criteria" |
| **Python environment** | Create a virtual environment, install packages and pin exact versions in `requirements.txt`. | Python documentation: "venv" |
| **Chat interface** | Build a "hello world" chat app with Gradio's `ChatInterface`. | Gradio documentation: ChatInterface guide |

---

### Sprint 1 · Discovery (14/10 – 28/10)

### Week 2 — 07/10

## Deliverables
* Project Executive Summary
* Mini presentations of project topics (10 min per team)

## Milestones
* Open a Github repository and invite your peers. Clone this git repository inside. Please note that only the Project Executive summary has been manually checked and updated. Other pages will be updated by October 8th.

If you are not familiar with Git and GitHub, such as using issues, pull requests, reviewing changes etc. please follow Datacamp guides on Intermediate Git and Advanced Git.


### Week 3 — 14/10 · Start of Sprint 1
> [!IMPORTANT]
> **Sprint goal:** Know *what* you will build and *why*, and prepare everything needed to measure it. No production code is expected in this sprint.

**Deliverables:**

- [ ] [Project Charter](Markdown Template/README.md) : Scope, Milestones, Assumptions & Constraints, Deliverables and Project Organization
- [ ] User stories in Jira (you may plan them in Miro first, but this is optional)
- [ ] Spike notes in `docs/spikes/`

**Your tasks:**

- [ ] Create your team repository from the course template ("Use this template") and your Jira project.
- [ ] Assign the Scrum roles, including the Product Owner for Sprint 1.
- [ ] Revise your topic and scope based on the feedback from Week 2.
- [ ] Choose your document sources and check their terms of use and licences.
- [ ] Check the *Sprint 1 fundamentals* table above individually and plan how to close your gaps.

**Presentation (15 minutes):** After completing this week's tasks, each team presents its repository and Jira setup, the Scrum roles, the revised topic and scope, the document sources and the charter draft.

---
