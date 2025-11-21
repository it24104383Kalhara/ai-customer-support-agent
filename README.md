# 📧 Intelligent Customer Support AI Agent

<div align="center">

*An autonomous AI agent that acts as a 24/7 first-line support representative, intelligently triaging incoming emails based on sentiment and intent.*

![Workflow Screenshot](https://via.placeholder.com/800x400.png?text=AI+Agent+Workflow+Screenshot)
*(Replace with actual workflow screenshot)*

[![n8n](https://img.shields.io/badge/n8n-%2352B415.svg?style=for-the-badge&logo=n8n&logoColor=white)](https://n8n.io/)
[![OpenAI](https://img.shields.io/badge/OpenAI-%23412991.svg?style=for-the-badge&logo=openai&logoColor=white)](https://openai.com/)
[![Trello](https://img.shields.io/badge/Trello-%23026AA7.svg?style=for-the-badge&logo=trello&logoColor=white)](https://trello.com/)
[![Google Sheets](https://img.shields.io/badge/Google%20Sheets-%2334A853.svg?style=for-the-badge&logo=google-sheets&logoColor=white)](https://workspace.google.com/)

</div>

## ✨ Key Features

<div align="center">

| 🧠 Intelligence | 🚦 Routing | 🛡️ Reliability |
|:---:|:---:|:---|
| **Smart Sentiment Analysis**<br>Detects angry/urgent customers vs calm inquiries | **Intelligent Categorization**<br>Routes emails to appropriate channels | **Robust Error Handling**<br>Custom Python logic for reliable JSON parsing |
| **Context-Aware Responses**<br>Generates relevant email replies | **Multi-Channel Integration**<br>Trello, Sheets, Gmail | **24/7 Operation**<br>Always-on customer support |

</div>

### 🎯 Email Classification Categories

| Category | Emoji | Action Taken |
|----------|-------|--------------|
| **Urgent Complaints** | 🚨 | Creates high-priority Trello card |
| **Sales Leads** | 💼 | Logs opportunity in Google Sheets (CRM) |
| **General Questions** | ❓ | Sends automated, context-aware email reply |
| **Spam** | 🚫 | Automatically filtered and ignored |

## 🛠️ Tech Stack

<div align="center">

| Layer | Technology |
|-------|------------|
| **Workflow Engine** | n8n (Self-hosted) |
| **AI Model** | OpenAI GPT-4o-mini |
| **Email Integration** | Gmail API (OAuth2) |
| **Project Management** | Trello API |
| **CRM Integration** | Google Sheets API |
| **Error Handling** | Custom Python Script |

</div>

## ⚙️ How It Works

### 🔄 Workflow Process

| Step | Description | Output |
|------|-------------|---------|
| **1. 📧 Trigger** | Monitor Gmail for new emails | Email data |
| **2. 🤖 Analysis** | OpenAI classifies sentiment & intent | JSON response |
| **3. 🔍 Parsing** | Python sanitizes JSON data | Clean data |
| **4. 🔄 Routing** | Switch node routes by category | Path selection |
| **5. 🎯 Action** | Execute platform-specific action | Final result |


### 📋 Step-by-Step Breakdown

1. **📧 Trigger**
   - Monitors dedicated Gmail inbox for new, unread messages
   - Captures full email body and metadata

2. **🧠 Analyze**
   - Sends email content to OpenAI with strict system prompt
   - Classifies into one of 4 categories
   - Generates one-sentence summary

3. **⚡ Parse**
   - Custom Python code sanitizes JSON response
   - Ensures data integrity and proper formatting

4. **🔄 Route**
   - Switch node directs data based on category
   - Implements fallback for edge cases

5. **🎯 Action**
   - Executes final API calls
   - Creates Trello cards, spreadsheet rows, or sends emails

## 🚀 Quick Start

### 📥 Installation

   ```bash
   # Download and import the workflow file
   My_AI_Agent.json → n8n Editor
   ```
## 🔐 Configure Credentials

### 📧 Gmail Setup
```bash
1. Go to n8n Credentials
2. Select "Gmail OAuth API"
3. Click "Connect OAuth API"
4. Follow Google authentication flow
5. Grant necessary permissions
```
### 🤖 OpenAI Configuration
```bash
1. Navigate to n8n Credentials
2. Choose "OpenAI API"
3. Add your API Key:
   - Get key from https://platform.openai.com
   - Paste in API Key field
4. Save credentials
```
### 📋 Trello Setup
```bash
1. Get Trello API Key:
   - Visit https://trello.com/power-ups/admin
   - Generate new API Key
2. Get Trello Token:
   - Visit: https://trello.com/1/authorize?expiration=never&scope=read,write,account&response_type=token&name=n8n&key=YOUR_API_KEY
   - Replace YOUR_API_KEY with actual key
3. Add both to n8n Trello credentials
```
### 📊 Google Sheets Configuration
```bash
1. Select "Google Sheets OAuth API"
2. Click "Connect OAuth API"
3. Authenticate with Google account
4. Grant spreadsheet permissions
5. Save credentials
```
## ⚡ Activate

### 🟢 Enable Workflow
```bash
1. Open workflow in n8n editor
2. Click "Toggle Active" switch
3. Confirm activation
4. Verify workflow shows "Active" status
```

### 🧪 Test Functionality
```bash
# Test Email Categories:
📧 Send test urgent email → Check Trello card creation
📧 Send sales inquiry → Verify Google Sheets entry
📧 Send general question → Confirm auto-reply
📧 Send spam email → Ensure proper filtering
```

### 📈 Monitor Executions
```bash
1. Check "Executions" tab
2. Monitor for any errors
3. Verify response times
4. Review classification accuracy
```
***Built by K.Vinod Kalhara***