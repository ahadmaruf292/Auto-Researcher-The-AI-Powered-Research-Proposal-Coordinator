# 🚀 Auto-Researcher: AI-Powered Research Proposal Committee

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![Google ADK](https://img.shields.io/badge/Built%20with-Google%20ADK-orange)
![Gemini](https://img.shields.io/badge/Model-Gemini%201.5%20Flash-purple)
![License](https://img.shields.io/badge/License-MIT-green)

**Auto-Researcher** is an autonomous multi-agent system designed to accelerate academic research. Instead of relying on a single LLM prompt, this project simulates a **Research Committee** where five specialized AI agents collaborate to search the web, review literature, identify research gaps, and propose scientific methodologies for PhD-level proposals.



---

## 🤖 How It Works (The Architecture)

This system leverages the **Google Agent Development Kit (ADK)** and **Sequential Agent Architecture**. The workflow is orchestrated as follows:

1.  **Coordinator Agent (The Manager):** Interacts with the user, understands the topic, and manages the workflow.
2.  **Researcher Agent (The Data Gatherer):** Uses **Google Search Tool** to scrape the live internet for real-time academic resources.
3.  **Reviewer Agent (The Academic Writer):** Synthesizes raw data into a structured **Literature Review**.
4.  **Analyst Agent (The Critical Thinker):** Analyzes the review to find what is *missing* and identifies a **Research Gap**.
5.  **Methodology Agent (The Scientist):** Proposes a scientific **Methodology** (algorithms, data collection) to address the gap.
6.  **Aggregator Agent:** Compiles all outputs into a final, cohesive Research Proposal.

---

## ✨ Key Features

* **Multi-Agent Collaboration:** Complex tasks broken down into specialized agents.
* **Agent-to-Agent (A2A) Communication:** Seamless context passing between agents.
* **Live Internet Access:** Real-time data fetching using Google Custom Search.
* **Stateful Memory:** `InMemorySessionService` allows for context-aware follow-up questions.
* **Observability & Logging:** Auto-generates detailed **JSON logs** for every session.
* **Cost Optimized:** Uses the efficient **Gemini 1.5 Flash** model.

---

## 🛠️ Installation & Setup

1.  **Clone the Repository:**
    ```bash
    git clone [https://github.com/your-username/auto-researcher.git](https://github.com/your-username/auto-researcher.git)
    cd auto-researcher
    ```
2.  **Install Dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
3.  **Set Up Environment Variables:** Create a `.env` file with your keys:
    ```env
    GOOGLE_API_KEY="your_gemini_api_key"
    GOOGLE_SEARCH_API_KEY="your_google_search_api_key"
    GOOGLE_CSE_ID="your_custom_search_engine_id"
    ```

---

## 🚀 Usage

Run the Jupyter Notebook `Research Proposal Assistant.ipynb`.

**Example Interaction:**
> **User:** "Create a research proposal on Deep Learning for Rice Variety Classification."
> **Final Output:** A complete proposal containing Literature Review, Research Gap, and Methodology.

---

## 📊 Observability

Logs are automatically saved as JSON files (e.g., `Research_Log_rice_v1_...json`) after each session, capturing the full execution trace for analysis.

---

**Built with ❤️ using Google ADK & Gemini.**
