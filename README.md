# research_agent
Project Overview

The Research Agent is an AI-powered assistant developed for the IBM Hackathon 2025 to streamline academic and scientific research tasks. Built and deployed on IBM Watsonx AI Studio using IBM Cloud Lite services, it leverages IBM Granite and Retrieval-Augmented Generation (RAG) to assist researchers, students, and R&D professionals. The agent performs semantic searches across academic literature, summarizes papers, recommends resources and collaborators, and generates structured reports, enhancing efficiency and innovation in research workflows.

Dataset

The project uses a simulated dataset of academic paper metadata (e.g., titles, abstracts, authors, URLs) stored as documents.csv for hackathon purposes, mimicking sources like arXiv or PubMed. For production, the agent can integrate with real-time APIs (e.g., arXiv, PubMed) to retrieve up-to-date literature, managed via IBM Cloud Object Storage and a vector index for RAG.

Requirements
IBM Cloud Account: Access to Watsonx AI Studio and Cloud Lite services.
IBM Watsonx AI Studio: Environment for building and deploying the agent.
IBM Granite Model: Foundation model for NLP and RAG tasks.
Cloud Object Storage: Lite plan for storing datasets and vector indices.
ibm-watsonx-ai: For integration with Watsonx AI and Granite.
pandas: For data manipulation of metadata.
requests: For optional API calls in production.
Hardware: Standard laptop/desktop for local testing; IBM Cloud for deployment.

Installation
Clone the repository from GitHub.

Configure IBM Cloud credentials:
Obtain an IBM Cloud API key and project ID from IBM Cloud.
Set up credentials in Watsonx AI Studio for secure access.

Prepare the dataset:
Place documents.csv in the project directory or configure API access (e.g., arXiv) for production.

Set up IBM Watsonx AI Studio:
Log in to IBM Cloud and navigate to Watsonx AI Studio.
Create a new project and associate a Cloud Object Storage instance (Lite plan).
Upload the dataset to Cloud Object Storage and create a vector index for RAG.
Deployment on IBM Watsonx AI Studio

Create the Agent:
In Watsonx AI Studio, select "Build AI agent to automate tasks."
Choose the IBM Granite model from the foundation models list.
Configure a new vector index in the knowledge section, linking to the dataset in Cloud Object Storage.
Add tools (e.g., RAG for document retrieval) and define agent behavior (e.g., semantic search, summarization).
Save the agent configuration.

Deploy the Agent:
Create a new deployment space in Watsonx AI Studio.
If a previous deployment space exists, delete it via the "View all deployment spaces" option and confirm deletion.
Deploy the agent and monitor the status until the "space is ready" pop-up appears.
Access the deployed agent via the provided API endpoint or Watsonx interface.

Access the Agent:
Interact with the agent through the Watsonx AI Studio interface or API.
Test functionality using sample queries (e.g., “machine learning trends”).

Usage
Agent Interaction:
Greeting: The agent responds with, "Hi, I am the Research Agent powered by IBM Watsonx.ai. How can I assist with your research today?"
Query Input: Enter a research topic (e.g., “machine learning trends”) or specific paper details.

Outputs:
Semantic Search: Retrieves 3–5 relevant papers with titles, authors, and URLs.
Summarization: Generates 100–150-word summaries with APA citations.
Recommendations: Suggests research gaps and collaborators based on document analysis.
Reports: Produces downloadable reports or draft sections (e.g., literature review).

Features:
Supports multilingual queries (e.g., English, Hindi) using IBM Granite.
Provides follow-up prompts, e.g., “Would you like a summary of a specific paper or recommendations for collaborators?”
Handles batch analysis of uploaded metadata for bulk summarization.

Agent Instructions
Greeting: Respond with, "Hi, I am the Research Agent powered by IBM Watsonx.ai. How can I assist with your research today?"
Query Handling: Use IBM Granite’s NLP to parse queries and RAG to retrieve relevant documents from the vector index.

Functions:
Perform semantic searches and rank results by relevance.
Summarize papers or topics with citations in APA format.
Recommend research gaps and collaborators based on document analysis.
Generate structured reports or draft sections for download.
Style: Maintain a professional, academic tone with concise, accurate responses.
Multilingual: Support queries in multiple languages using Granite’s translation capabilities.
Error Handling: If a query is unclear, respond with, “Could you clarify your research topic or specify the type of assistance needed?” and suggest options.

Results
Deployed Agent: Hosted on IBM Watsonx AI Studio, accessible via API or interface.

Outputs:
Semantic search results for user queries.
Summaries of papers or topics (100–150 words).
Recommendations for research gaps and collaborators.
Performance: Accurate retrieval and summarization using IBM Granite’s RAG capabilities.

Future Scope
Integrate real-time APIs (e.g., arXiv, PubMed, IEEE Xplore) for broader data access.
Add voice input support using IBM Watson Speech-to-Text.
Enhance multilingual capabilities for regional languages (e.g., Tamil, Bengali).
Implement real-time collaboration features with platforms like ResearchGate.
Develop AI-assisted paper drafting for publication submissions.
Scale to handle larger datasets and complex research queries.

References
Dua, D., & Graff, C. (2017). UCI Machine Learning Repository. https://archive.ics.uci.edu
IBM Watsonx AI Documentation. https://cloud.ibm.com/docs/watsonx-ai
IBM Granite Model Overview. https://www.ibm.com/granite
Pedregosa, F., et al. (2011). Scikit-learn: Machine Learning in Python. Journal of Machine Learning Research, 12, 2825-2830.

Contributing
Contributions are welcome! Submit a pull request or open an issue on the GitHub repository for suggestions or improvements.
