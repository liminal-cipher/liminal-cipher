<p align="center">
<img src="avatar.png" width="150" />
</p>

# Hey, I'm liminal-cipher. 👋

I'm interested in **AI/ML engineering**, both in machine learning itself and in the systems that make models useful in practice.

I studied **Technological Systems Management** with a minor in **Computer Science**, then completed the **Microsoft AI School, 9th cohort, from December 2025 to June 2026**.

That mix shaped how I approach technical problems. I enjoy model and data experiments, but I also care about where AI should make a decision, what should stay deterministic, and how a pipeline behaves once it is deployed.

I'm currently looking for opportunities in **AI/ML Engineering**, especially work involving machine learning, RAG, backend systems, and LLMOps.

## 💻 Featured Projects

Six months. Three team projects. An unhealthy number of Azure deployments.

### [E-Nudge](https://github.com/liminal-cipher/e-nudge) 🥇

A content moderation service that evaluates text and images when a comment is submitted, then chooses **normal publishing, a nudge, or a block** based on risk.

I served as **Team Lead and Dev Lead**. My main implementation was the **Decision Engine**, which combines text and image risk signals into the final service decision. I also worked jointly on the FastAPI backend and pseudo labeling pipeline, helped design the TF-IDF and classical ML approach, and interpreted the results of the KcELECTRA controlled experiments.

Those experiments became one of the most useful parts of the project. With the same human test set, KcELECTRA trained on 6,316 examples labeled by humans reached **0.739 hate F1**. Adding all 371,459 pseudo labeled examples reduced it to **0.589**, while a 1:1 condition with 6,316 pseudo labeled examples reached **0.701**.

The results pointed to the quality of our pseudo labels as a major bottleneck rather than showing that simply adding more data would help.

For the actual service, we deployed **TF-IDF + ComplementNB**. KcELECTRA performed better offline, but the service had to run on Azure App Service without a GPU and within a short project schedule. The final choice balanced accuracy, latency, infrastructure, and implementation time.

`Python` `FastAPI` `scikit-learn` `TF-IDF` `Azure`

### [이사이상무](https://github.com/liminal-cipher/isa-isangmu)

An AI moving assistant that provides **personalized guidance** for Korean moving procedures using statutes and public sector information.

I led the team and designed the system architecture and RAG pipeline. I designed and built **three separate Azure AI Search indexes** for laws, administrative guides, and structured mappings, then implemented the parallel hybrid search layer that queried them.

A principle that came out of this project was simple:

> **Use LLMs where flexibility helps. Keep deterministic logic where correctness matters.**

Structured user conditions were converted into search queries with Python rules. Legal deadlines were calculated in Python, and regional contact information came from static mappings. LLMs were reserved for inputs and explanations that actually benefited from natural language reasoning.

The registry document feature followed the same idea. Extraction, judgment, and explanation were separated, and the final risk judgment was handled with Python rules rather than delegated to the LLM.

In the **30 query presentation benchmark**, the checklist pipeline reached **96.9% recall with 0 recorded violations**.

`Python` `FastAPI` `Azure OpenAI` `Azure AI Search` `Document Intelligence` `RAG`

### [회랑 (Mind Palace)](https://github.com/liminal-cipher/mind-palace-graphrag)

A 3D spatial learning service built around **GraphRAG**. It turns uploaded study materials into a mind palace viewed in first person and uses the resulting knowledge structure for search and learning interactions.

My main focus was the backend system. I built the **GraphRAG backend and live orchestrator** connecting:

**upload → preprocessing → indexing → Palace generation → RAG serving**

GraphRAG indexing can take minutes, so I treated it as a stateful job rather than a normal API request. Job state was persisted in **Azure Cosmos DB**, while generated artifacts were stored in **Azure Blob Storage**. Heavy stages ran in separate subprocesses, which kept expensive indexing work isolated from the main server process. Persisted job state also survived application restarts.

I ran GraphRAG indexing experiments and model sweeps, added token and USD cost tracking across the pipeline, worked on RAG quality improvements, and maintained reproducible golden snapshots.

The final Korean history golden snapshot contained **357 entities**, and cached golden builds were verified to reproduce exactly at the byte level.

This project changed how I think about AI systems. Once a model becomes part of a product with multiple stages, state, latency, reproducibility, failure handling, and cost become part of the engineering problem too.

`Python` `FastAPI` `Microsoft GraphRAG` `Azure OpenAI` `Cosmos DB` `Blob Storage` `LLMOps`

## 🧪 Side Projects

### [Tri-Lens News](https://github.com/liminal-cipher/tri-lens-news)

A personal AI news pipeline that sends **two news items and one paper every morning**.

Each item is explained through three lenses: **Everyone**, **Developers**, and **Researchers**. They are not separate audiences. The idea is for one reader to move through them in order, starting with plain context, then implementation details, then open research questions.

The pipeline runs on **GitHub Actions**, uses Gemini for selection and interpretation, checks output constraints with deterministic rules, and automatically regenerates an interpretation once if it violates them. Delivered digests are committed back to the repository as Markdown.

`Python` `Gemini API` `GitHub Actions` `Prompt Engineering`

### [We Are Checking](https://github.com/liminal-cipher/we-are-checking) *(In Progress)*

A personal machine learning project for predicting whether each Formula 1 driver will finish in the top 10.

The project is built around a stricter question than simply getting a good score: **does a probability recorded before the race remain trustworthy after the race is over?**

So far, I have built the historical data pipeline, leakage checks, temporal evaluation, simple baselines, and the first feature experiments.

An initial test found that adding recent five race form did not improve accuracy over starting grid position alone. I have since moved model selection to **expanding window walk forward validation** so future experiments do not rely repeatedly on the same historical holdout.

The next major step is prospective evaluation: committing probabilities before each race and tracking their calibration against actual results across the season.

`Python` `pandas` `scikit-learn` `Machine Learning` `Model Evaluation`

## 🔍 What I Care About

* **Machine learning:** model comparison, evaluation, data quality, and controlled experiments
* **Applied AI systems:** turning ML and LLM components into usable services
* **RAG and GraphRAG:** retrieval architecture, grounding, and provenance
* **LLMOps:** orchestration, observability, reproducibility, latency, and cost
* **Reliable AI design:** deciding when a probabilistic model helps and when deterministic logic is safer

I like models. I probably like figuring out how they fit into a system just as much.

## 🛠️ Core Stack

**AI / ML**

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)

**Backend**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)

**Cloud / Data**

![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-4479A1?style=for-the-badge)

**Also worked with:** Azure OpenAI · Azure AI Search · Cosmos DB · Blob Storage · Document Intelligence · Microsoft GraphRAG

## ☕ About Me

If you've made it this far and you're curious about the person behind the projects, I've always been fascinated by **liminal spaces**, that strange, quiet feeling of being somewhere in between.

That's where the username came from. It also feels oddly fitting for someone whose background sits somewhere between **business and engineering**.

Outside of code, I'm mostly powered by **music and coffee**. My playlists change more often than my tech stack.

## 💬 Let's Chat

I'm fairly introverted, but I genuinely enjoy talking to people over shared interests, whether that's RAG architecture, an annoying FastAPI edge case, ML experiments, AI system design decisions, or a playlist you've had on repeat.

Feel free to open a **Discussion** or drop an **Issue** in one of my repos.

**Current status:** 🧠 Looking for my next role in AI/ML Engineering