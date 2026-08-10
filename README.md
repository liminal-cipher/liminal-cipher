<p align="center">
<img src="avatar.png" width="150" />
</p>

# Hey, I'm liminal-cipher. 👋
I'm a grad with a major in **Technological Systems Management** and a minor in **Computer Science**. I recently wrapped up the **Microsoft AI School (9th cohort, 2025.12 – 2026.06)** and am actively looking for my next role in **AI/ML Engineering**.

### 💻 What I've Built

Six months. Three projects. An unhealthy number of Azure deployments.

**E-Nudge** 🥇
An AI-powered *nudge* moderation service that warns writers before they post something harmful, instead of silently deleting it after. Took **1st place** in our cohort evaluation. I served as Team Lead and Dev Lead, owning the decision engine, the nudge UX, and FastAPI serving on Azure App Service. The finding I'm proudest of came from the team's controlled experiment: nine algorithms all plateaued around 52%, and mixing in pseudo-labelled data made a fine-tuned KcELECTRA *worse*. The ceiling was label quality, not model capacity.

**이사이상무**
A RAG-powered moving assistant that generates personalised legal checklists, with a citeable statute or agency link for every item. Built on a 3-index Azure AI Search architecture (law 1,635 / guide 340 / mapping 122 chunks) with GPT-4o. I led the team and designed the index schema, splitting one combined index into three because prose you search and values you quote verbatim behave differently.

**회랑**
A first-person 3D mind palace app that uses GraphRAG to index uploaded study materials, then powers an in-palace query engine, quiz, and learning chatbot. I built the indexing pipeline and the live orchestrator, plus the state layer on Cosmos DB and Blob so a multi-minute index survives a restart. Golden snapshots reproduce byte-identical, and the indexing model was chosen by sweeping four candidates.

### 🔍 Currently

 * **Building:** *오늘도 안녕*, a stroke early-check service for older adults, for the 8th K-Digital Training Hackathon. The system rings first so nobody has to place a call, then measures face, arm and voice against that person's own baseline rather than a population average. Preliminary results are pending.
 * **Exploring:** NLP, ML, Computer Vision, Responsible AI, and everything MLOps-adjacent.
 * **Shipping on the side:** Utility mobile apps in **React Native** and **Firebase**. If I run into a problem in my day-to-day, I'll probably build an app for it before I think to Google it.

### 🛠️ Tech Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=for-the-badge&logo=scikit-learn&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![Azure](https://img.shields.io/badge/Azure-0078D4?style=for-the-badge&logo=microsoftazure&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![React Native](https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Firebase](https://img.shields.io/badge/Firebase-039BE5?style=for-the-badge&logo=Firebase&logoColor=white)

### ☕ About Me

 * **Vibe:** I've always been fascinated by **liminal spaces**: that strange, quiet feeling of being in between places. Feels fitting for someone pivoting from systems management into ML.
 * **Fuel:** Basically powered by **music and coffee**. My personality tends to come in phases. I'll spend months obsessing over a specific artist or drinking nothing but iced americanos, then wake up one day and decide it's a latte-and-lofi kind of month.

**Current Status**: 🎧 Looping LANY | 🧊 Iced latte in hand | 🧠 Actively looking for my next role

### 💬 Let's Chat

I'm an introvert, but I genuinely love connecting with people over shared interests: NLP, a weird edge case in FastAPI, or a playlist you've been looping. Feel free to open a **Discussion** or drop an **Issue** in one of my repos. I'm always around GitHub.