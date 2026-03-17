# Data-cleaning-Automation-n8n-Agentic-AI
n8n workflow that automatically cleans movie data from email attachments. Extracts XLSX files, splits combined ID/name columns, trims fields, and emails back formatted results. Built for Gmail integration with OAuth2. Perfect for automating repetitive data processing tasks.
# 🎬 n8n Movie Data Cleaning Automation

An automated n8n workflow that processes movie data from email attachments, cleans and formats the data, and sends back the cleaned version via email.

## ✨ Features

- 📧 Email Trigger: Automatically detects incoming emails with movie data attachments
- 📊 Data Extraction: Reads XLSX files from email attachments
- 🧹 Data Cleaning: 
  - Splits combined movie ID and name columns at first colon
  - Trims whitespace from all fields
  - Standardizes formatting
- 📁 File Conversion: Converts cleaned data to XLSX format
- 📨 Auto-Reply: Sends cleaned data back to original sender

## 🖼️ Workflow Screenshots

### 1. Complete Workflow Structure
![Workflow Overview](screenshots/workflow-overview.png)
*The full automation workflow showing all connected nodes*

### 2. Gmail Send Configuration
![Gmail Send Node](screenshots/gmail-send.png)
*Configuration of the final Gmail node with attachment settings*

### 3. Successful Execution Result
![Gmail Output](screenshots/gmail-output.png)
*The cleaned data successfully received in Gmail inbox*

## 📝 How It Works

```mermaid
graph LR
    A[Email with Attachment] --> B[Gmail Trigger]
    B --> C[Extract from File]
    C --> D[Code: Clean Data]
    D --> E[Convert to XLSX]
    E --> F[Gmail: Send Reply]
    F --> G[Cleaned Data to Sender]
