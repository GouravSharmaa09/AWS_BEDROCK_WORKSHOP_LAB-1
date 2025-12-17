# 🤖 AWS Bedrock Restaurant AI Agent

A sophisticated AI-powered Restaurant Concierge built using **Amazon Bedrock (Claude 3 Sonnet)**. This agent can process multiple unstructured documents (DOCX, TXT) to provide accurate information about menus, booking policies, and restaurant schedules.

## 🌟 Features
- **Local RAG (Retrieval-Augmented Generation):** Bypasses complex cloud setups to inject local data directly into the AI context.
- **Custom DOCX Parser:** A zero-dependency Python solution to extract clean text from Microsoft Word documents.
- **Direct AWS Integration:** Uses `boto3` for high-performance communication with Claude 3.
- **Smart Context Handling:** Efficiently manages 170k+ characters of restaurant data.

## 🛠️ Tech Stack
- **AI Model:** Anthropic Claude 3 Sonnet (via Amazon Bedrock)
- **Language:** Python 3.10+
- **AWS Services:** Bedrock Runtime, IAM
- **Libraries:** Boto3, Zipfile, XML.etree

## 🚀 How to Run
1. Clone this repository.
2. Install dependencies: `pip install boto3`.
3. Open `restaurant-assistant.ipynb` in VS Code.
4. Replace the AWS Credentials placeholders with your temporary session keys.
5. Update the `DATA_PATH` to point to your `prereqs` folder.
6. Run all cells.

## 🏗️ Architecture
Instead of waiting for slow Vector Database provisioning, this project implements a **Direct Prompt Injection** strategy. It reads local files, cleans the text, and structures it into a high-density "Knowledge Database" within the System Prompt.