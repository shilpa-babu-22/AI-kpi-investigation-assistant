# AI-KPI-Investigator

An AI-powered business intelligence assistant that investigates KPI changes, identifies likely root causes and provides evidence-backed insights and recommendations.

## Problem Statement

Business users can monitor KPIs and trends through tools such as Power BI, but understanding **why a KPI changed** often requires manually analyzing data, comparing historical trends, and searching through business documentation.

This investigation can be time-consuming, especially when the information required to explain a KPI change is distributed across multiple data sources.

## Solution

The **AI-KPI-Investigator** aims to automate this investigation process by combining structured business data with relevant business knowledge.

The system will:

* Analyze KPI values, changes, and historical trends.
* Detect and investigate significant KPI changes.
* Retrieve relevant information from business documents and knowledge sources using RAG.
* Use an AI agent to determine which information and analysis are relevant to the investigation.
* Orchestrate the investigation workflow using LangGraph.
* Correlate KPI patterns with business data and retrieved contextual knowledge to identify likely root causes.
* Provide evidence supporting the identified causes.
* Generate clear explanations and actionable recommendations for business users.

## Example Investigation Flow

```text
Business User
      |
      v
"KPI X decreased by 18%. Why?"
      |
      v
AI Investigation Agent
      |
      v
Analyze KPI + Historical Trends
      |
      +------------------+
      |                  |
      v                  v
Structured Data       RAG
                      |
                      v
                Business Documents
      |                  |
      +--------+---------+
               |
               v
       Root Cause Analysis
               |
               v
     Evidence + Explanation
               |
               v
       Recommendation
```

## Planned Architecture

```text
                 Power BI / KPI Data
                         |
                         v
                AI Investigation Agent
                         |
                         v
                     LangGraph
                         |
              +----------+----------+
              |                     |
              v                     v
       Structured Data           RAG
              |                     |
              |              Business Documents
              |                     |
              +----------+----------+
                         |
                         v
                 Root Cause Analysis
                         |
                         v
              Evidence-backed Insights
                         |
                         v
                  Recommendations
                         |
                         v
                    Streamlit UI
```

## Planned Technology Stack

* **Python** — Core application development
* **LangChain** — LLM and retrieval components
* **LangGraph** — Agent workflow orchestration
* **Large Language Model (LLM)** — Reasoning and natural-language generation
* **RAG** — Retrieval of relevant business knowledge
* **SQL / Structured Data** — KPI and business data analysis
* **Power BI** — Business intelligence and KPI visualization
* **Streamlit** — Interactive user interface

## Project Goals

* **Automate KPI investigation** by analyzing KPI changes, trends, and relevant business data.

* **Combine structured and unstructured information** from business data, historical trends, and business documentation.

* **Identify likely root causes** by correlating KPI patterns with relevant data and contextual business knowledge.

* **Provide evidence-backed insights** by showing the information supporting the AI-generated conclusions.

* **Generate actionable recommendations** to help business users understand potential causes and determine appropriate next steps.

* **Demonstrate a practical GenAI solution** using RAG, AI agents, and LangGraph to address a real-world business intelligence problem.

* **Provide a simple business-user interface** that allows users to investigate KPI changes without manually performing the entire analysis.
