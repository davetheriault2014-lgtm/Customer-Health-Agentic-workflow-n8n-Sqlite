# Customer-Health-Agentic-workflow-n8n-Sqlite
Automated Customer Success AI agent built in n8n and Groq to monitor MAU % utilization and flag churn risks.
# Customer Success MAU % Utilization & Churn Risk Agent

An automated AI agent built in **n8n** and powered by **Groq (`llama-3.1-8b-instant`)** that ingests customer usage data, evaluates Monthly Active User (MAU) utilization thresholds, and routes at-risk accounts for immediate Customer Success outreach.

## Workflow Architecture
![Workflow Diagram](workflow-diagram.png)

## Business Problem & Solution
Customer Success teams often lose valuable time manually reviewing usage spreadsheets to spot declining adoption. This workflow automates account health triage:
1. **Data Ingestion:** Reads customer CSV reports and parses account-level MAU metrics.
2. **AI Health Evaluation:** Uses an LLM chain with custom CS threshold rules to classify accounts into *Healthy*, *Moderate Adoption*, or *High Churn Risk*.
3. **Automated Routing:** Uses conditional logic (`If` node) to isolate *High Churn Risk* accounts and trigger targeted retention actions.

## How to Run This Workflow
1. Download the `.json` workflow file from this repository.
2. Open your local or cloud **n8n** instance and create a new workflow.
3. Click the **`...`** menu in the top right > **Import from File**, and select the `.json` file.
4. Add your free **Groq API** credential to the Groq Chat Model node and execute.
