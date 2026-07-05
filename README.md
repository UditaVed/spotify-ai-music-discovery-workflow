# 🛠️ Spotify AI-Powered Review Discovery Engine & Music Discovery MVP

This repository contains the complete dataset pipelines, automation workflows, and configuration blueprints for an AI-native music discovery solution built for the Spotify Growth Team. 

The project solves a major product paradox: despite Spotify possessing highly advanced recommendation algorithms, a significant percentage of listening remains bounded within safe, repetitive user "comfort loops." By combining multi-channel web scraping with an advanced Large Language Model (LLM) orchestration engine, this system shifts recommendations away from rigid, popularity-biased history matrices toward **Natural Language Semantic Intent Parsing**.

## 🚀 Live Production MVP Link
*   **Interact with the Live MVP App here:** https://udify.app/chat/7mfomsHNT3hG2BRA

---

## 📂 Repository Contents

```text
├── data/
│   ├── dataset_reddit-scraper-lite_2026-06-25_13-40-05-166_2.csv          # Deep user behavior & rants on taste narrowing
│   ├── dataset_appstore-reviews-scraper_2026-07-02_10-18-22-574_2.csv    # iOS mobile friction & choice fatigue metrics
│   ├── dataset_google-play-scraper_2026-07-04_15-42-16-779_2.csv          # Android monetization & app performance data
│   ├── dataset_google-search-scraper_2026-07-04_16-26-40-734_2.csv        # Community Forum technical bug crawls
│   └── spotify_master_feedback_compiled.txt                              # Cleaned, consolidated RAG context file
└── workflow/
    └── Knowledge Retrieval_ A Smart Chatbot.yml                          # Production Dify Advanced-Chat Workflow DSL


    ==================================================================================
[WORKFLOW ARCHITECTURE] AI-NATIVE DISCOVERY ENGINE & MVP DEPLOYMENT
   =============================================================================

1. DATA INGESTION ENGINE (THE REVIEW DISCOVERY VECTOR)
   - Core Mechanism: Extracted 212 multi-channel rows across Reddit, mobile stores, and official forums[cite: 1]. Normalized text compiled into a zero-noise RAG context file (spotify_master_feedback_compiled.txt)[cite: 1].
   - Product Value: Eliminates internal assumptions. Grounds the AI model in real-world user frustration loops (e.g., choice paralysis, algorithmic over-pivoting, forced shuffles)[cite: 1].

2. RETRIEVAL-AUGMENTED GENERATION (🌟 KNOWLEDGE RETRIEVAL NODE)
   - Core Mechanism: Dify Advanced-Chat graph mapping user queries directly to the semantic text-chunk vector database via a dedicated retrieval node[cite: 2].
   - Product Value: Bypasses static item-ID limitations. Feeds unmapped qualitative user intent directly into the context window[cite: 1, 2].

3. LLM ORCHESTRATION LAYER (ANTI-POPULARITY FILTER)
   - Core Mechanism: gpt-4.1 engine operating under strict system prompt constraints[cite: 2].
   - Product Value: Enforces immediate anti-popularity bias. Instructed to ignore mainstream chart data and prioritize long-tail discovery scores[cite: 2].

4. PRODUCTION UX INTERFACE (LIVE MVP WEB APP)
   - Core App URL: https://udify.app/chat/7mfomsHNT3hG2BRA
   - Product Value: Interactive chat-flow workspace featuring dynamic conversation starters, natural language guardrails, and persistent history tracking[cite: 2]. Gives users real-time control to shape recommendation trajectories.
==================================================================================
