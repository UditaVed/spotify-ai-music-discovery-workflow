# 🛠️ Spotify AI-Powered Review Discovery Engine & Music Discovery MVP

This repository contains the complete dataset pipelines, automation workflows, and configuration blueprints for an AI-native music discovery solution built for the Spotify Growth Team.

The project solves a major product paradox: despite Spotify possessing highly advanced recommendation algorithms, a significant percentage of listening remains bounded within safe, repetitive user "comfort loops." By combining multi-channel web scraping with an advanced Large Language Model (LLM) orchestration engine, this system shifts recommendations away from rigid, popularity-biased history matrices toward **Natural Language Semantic Intent Parsing**.

## 🚀 Live Production MVP

**Interact with the Live MVP App:**  
https://udify.app/chat/7mfomsHNT3hG2BRA

---

## 📂 Repository Contents

```text
.
├── data/
│   ├── dataset_reddit-scraper-lite_2026-06-25_13-40-05-166_2.csv
│   │   # Deep user behavior & rants on taste narrowing
│   ├── dataset_appstore-reviews-scraper_2026-07-02_10-18-22-574_2.csv
│   │   # iOS mobile friction & choice fatigue metrics
│   ├── dataset_google-play-scraper_2026-07-04_15-42-16-779_2.csv
│   │   # Android monetization & app performance data
│   ├── dataset_google-search-scraper_2026-07-04_16-26-40-734_2.csv
│   │   # Community Forum technical bug crawls
│   └── spotify_master_feedback_compiled.txt
│       # Cleaned, consolidated RAG context file
│
└── workflow/
    └── Knowledge Retrieval_ A Smart Chatbot.yml
        # Production Dify Advanced-Chat Workflow DSL
```

---

## 🏗️ Workflow Architecture: AI-Native Discovery Engine & MVP Deployment

### 1. Data Ingestion Engine (The Review Discovery Vector)

**Core Mechanism**

- Extracted **212** multi-channel review rows across Reddit, mobile app stores, and official Spotify forums.
- Normalized and consolidated all text into a zero-noise Retrieval-Augmented Generation (RAG) context file:
  - `spotify_master_feedback_compiled.txt`

**Product Value**

- Eliminates internal assumptions.
- Grounds the AI model in real-world user frustration loops, including:
  - Choice paralysis
  - Algorithmic over-personalization
  - Repetitive recommendations
  - Forced shuffle complaints

---

### 2. Retrieval-Augmented Generation (🌟 Knowledge Retrieval Node)

**Core Mechanism**

- Uses a Dify Advanced-Chat workflow that maps natural-language queries directly into a semantic vector knowledge base through a dedicated retrieval node.

**Product Value**

- Bypasses static item-ID limitations.
- Injects qualitative user intent directly into the LLM context window.

---

### 3. LLM Orchestration Layer (Anti-Popularity Filter)

**Core Mechanism**

- Powered by `gpt-4.1`.
- Operates under strict system prompt constraints designed for music discovery.

**Product Value**

- Enforces an anti-popularity bias.
- Explicitly deprioritizes mainstream chart hits.
- Prioritizes long-tail artists, hidden gems, and semantically relevant recommendations.

---

### 4. Production UX Interface (Live MVP Web App)

**Live Application**

https://udify.app/chat/7mfomsHNT3hG2BRA

**Product Value**

Provides an interactive conversational interface featuring:

- Dynamic conversation starters
- Natural language recommendation refinement
- Persistent conversation history
- Real-time control over recommendation trajectories
- AI-guided music discovery beyond traditional collaborative filtering

---

# 💻 Deployment Runbook: Replicating on Dify

Follow the steps below to recreate the complete AI-powered music discovery workflow.

## Step A: Initialize the Application Workflow

1. Log in to your **Dify.ai** account.
2. Navigate to **Studio**.
3. Click **Create from Blank**.
4. Select **Import DSL File**.
5. Upload:

   ```text
   workflow/Knowledge Retrieval_ A Smart Chatbot.yml
   ```

This automatically recreates the complete Advanced Chat workflow, including all nodes, connections, and configurations.

---

## Step B: Create and Bind the Knowledge Base

1. Navigate to the **Knowledge** tab.
2. Click **Create Knowledge**.
3. Upload:

   ```text
   data/spotify_master_feedback_compiled.txt
   ```

4. Select **High Quality** indexing.
5. Allow Dify to complete document segmentation and embedding generation.
6. Save the knowledge base.

---

## Step C: Link the Knowledge Base & Deploy

1. Re-open the imported workflow in **App Studio**.
2. Select the **🌟 Knowledge Retrieval** node.
3. Attach the knowledge base created in Step B.
4. Verify that the retrieval output variable

   ```text
   {{#1711528915811.result#}}
   ```

   is correctly mapped into the primary LLM context input.

5. Click **Publish**.
6. Select **Run as Web App**.

Dify will generate a public deployment URL for your AI-powered music discovery application.

---

# 🛠️ Infrastructure Dependencies

| Layer | Technology |
|--------|------------|
| **Data Collection** | Apify Cloud Platform |
| **Data Processing** | Python 3.11, Pandas |
| **Knowledge Base** | Dify Knowledge Index (High Quality Embeddings) |
| **Workflow Engine** | Dify Advanced Chat Workflow (v0.6.0) |
| **LLM Provider** | OpenAI GPT-4 API |
| **Integration** | `langgenius/openai` Plugin |
| **Deployment** | Dify Web Application |

---

# 📌 Technology Stack

- **LLM:** OpenAI GPT-4
- **Workflow Orchestration:** Dify Advanced Chat
- **Knowledge Retrieval:** Retrieval-Augmented Generation (RAG)
- **Data Sources:** Reddit, Google Play Store, Apple App Store, Spotify Community Forums
- **Data Processing:** Python, Pandas
- **Vector Knowledge Base:** Dify Knowledge
- **Deployment:** Dify Web App
