# Auto-Researcher-The-AI-Powered-Research-Proposal-Coordinator

Overview
Writing a comprehensive research proposal—specifically identifying a genuine "Research Gap" and formulating a methodology—is a daunting task that typically takes researchers weeks or even months. Auto-Researcher is a multi-agent AI system designed to compress this timeline into minutes. By leveraging the Google Agent Development Kit (ADK) and Gemini 2.5 pro , this project simulates a full academic committee where distinct AI agents collaborate to perform literature reviews, critique existing work, identify gaps, and propose novel methodologies.

The Problem
Traditional LLMs often struggle with long-form research tasks. If asked to "write a research proposal," a single model often hallucinates citations, misses critical logical steps, or produces generic content. It lacks the "critical thinking" required to separate a literature review from a problem statement.

The Solution: A Multi-Agent Coordinator
Instead of relying on a single prompt, this project implements a "Coordinator of Agents" architecture. Each agent has a specialized persona and a specific job, mimicking a real-world research team. They communicate sequentially, passing context and data to one another to build a coherent final output.

Architecture & Agents
The system is built using Google ADK's SequentialAgent and InMemorySessionService. The workflow consists of 5 specialized agents:

The Coordinator Agent (Manager): Acts as the interface with the user. It understands the research topic and orchestrates the pipeline.

The Researcher Agent (Data Gatherer): Equipped with the Google Search Tool, this agent browses the live internet to fetch real-world, up-to-date research papers and articles. It ensures the data is current, solving the "knowledge cutoff" problem of static models.

The Reviewer Agent (Academic Writer): Takes the raw data and synthesizes it into a formal Literature Review, highlighting current trends.

The Analyst Agent (The "Brain"): This is the most critical agent. It analyzes the review to find what is missing. It explicitly identifies the Research Gap—the boundary between what is known and what needs to be discovered.

The Methodology Agent (Scientist): Based only on the identified gap, this agent proposes a scientific Methodology (e.g., specific algorithms, data collection methods) to solve the problem.

The Aggregator Agent: Compiles the outputs from all previous agents into a structured, cohesive final proposal.

Key Features
Agent-to-Agent (A2A) Communication: Utilizing ADK's context passing, agents share outputs seamlessly. The Analyst doesn't need to search; it relies on the Reviewer's output, ensuring logical consistency.

Stateful Memory: The system uses InMemorySessionService to maintain context. Users can ask follow-up questions (e.g., "Explain the methodology again") without restarting the research process.

Observability & Logging: A custom logging system captures the full execution trace (thoughts, tool inputs, and outputs) into a structured JSON file. This allows for detailed debugging and performance evaluation.

Tool Integration: Integration of GoogleSearchTool allows the agent to access real-time information.

Technology Stack
Framework: Google Agent Development Kit (ADK)
Model: Gemini 2.5 pro
Tools: Google Search API
Language: Python
