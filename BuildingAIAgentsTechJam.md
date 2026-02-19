# 🚀 Building AI Agents - Pre Tech-Jam Setup Guide

This document rovides a clear, technical roadmap for setting up the **Cloud-Only AI Stack** for the **Building AI Agents Tech-Jam**.

To maximize our time during the **12-hour Tech Jam**, every participant must complete the following account setups. This ensures you have the necessary "Keys" to power your AI Agents.

**Estimated Time:** 15–20 Minutes
**Requirements:** A web browser (Chrome or Edge recommended) and a stable internet connection. **No installation is required.**

---

## 1. Flowise Cloud (The Command Center)

This is where we will build our AI workflows and the **Pharma-IQ** agent.

1. Go to [flowiseai.com](https://flowiseai.com).
2. Click on **"Get Started with Cloud"**.
3. Register for a free account.
4. 
**Verification:** Once logged in, you should see an empty dashboard with a side menu (Chatflows, Marketplaces, Credentials, etc.).

---

## 2. Groq (The Brain / LLM)

Groq provides the high-speed Large Language Models (LLMs) that act as the "reasoning engine" for our agents.

1. Go to [console.groq.com](https://console.groq.com).
2. Sign up using your work or personal email.
3. Navigate to **Settings** → **API Keys** in the sidebar.
4. Click **"Create API Key"**.
5. **Important:** Name it "Pharma-IQ-Key" and **copy the key immediately**. Store it in a notepad; you won't be able to see it again once you close the window.

---

## 3. Google AI Studio (The Knowledge / Embeddings)

We use Google’s Gemini to convert Pfizer documents into a format the AI can "read" and search.

1. Go to [aistudio.google.com](https://aistudio.google.com).
2. Sign in with a Google account.
3. On the left sidebar, click **"Get API key"**.
4. Click **"Create API key in new project"**.
5. **Copy the key** and save it. We will use the `gemini-embedding-001` model during Session 3.

---

## 4. Web Search Tools (The Hands / Real-Time Data)

To give our agents the ability to research live medical data, we will set up **both** SerpAPI and Tavily to ensure redundancy and higher search limits.

### Option A: Tavily (Recommended)

Tavily is optimized for AI agents and offers 1,000 free searches per month.

1. Go to [tavily.com](https://tavily.com).
2. Sign up for the **Free Tier**.
3. Copy your **API Key** from the dashboard.

### Option B: SerpAPI (Secondary)

SerpAPI is a powerful alternative that mimics Google Search.

1. Go to [serpapi.com](https://serpapi.com).
2. Register for a free account (provides 100 searches/month).
3. Navigate to your **Dashboard** and copy the **Private API Key**.

---

## 🛡️ Setup Checklist Summary

Before arriving at Session 1, ensure you have the following keys saved in a secure document:

| Service | Purpose | Node in Flowise |
| --- | --- | --- |
| **Flowise Cloud** | Application Platform | N/A |
| **Groq API Key** | Thinking & Reasoning | <br>`ChatGroq` 

 |
| **Google AI Key** | Document Reading (RAG) | `Google Gemini Embeddings` |
| **Tavily/Serp Key** | Live Medical Research | <br>`Tavily Search` / `SerpAPI` 

 
