# gmail-ai-workflow

Gmail Character Agent (n8n)

An AI-powered Gmail assistant built with n8n, LangChain Agent, and OpenAI (gpt-5-mini).

This workflow enables intelligent email summarization and sending using natural language via chat.

🚀 Overview

The Gmail Character Agent acts as an AI email assistant capable of:

📩 Summarizing emails

📤 Sending emails

🔁 Summarizing and sending email summaries

🤖 Determining user intent automatically

It uses a structured system prompt to ensure consistent execution reporting and controlled output formatting.

🏗 Workflow Architecture
Chat Trigger
     ↓
AI Agent (LangChain)
     ↓
OpenAI Chat Model (gpt-5-mini)
     ↓
Gmail Tool(s)
Core Components

Chat Trigger – Receives user messages

AI Agent – Determines intent and selects action

OpenAI Model – Processes reasoning and response generation

Gmail Tool – Fetches emails for summarization

🧠 Agent Capabilities

The agent is designed to perform exactly one of the following actions per request:

Summarize an email

Send an email

Summarize and send the summary

Output Rules

Always returns an execution report

Always returns Status: Success

No reasoning or extra commentary

No greetings

No empty responses

Example outputs:

Email summary: <summary content>

Status:
Success

or

Email was sent to example@email.com.

Status:
Success
📦 Requirements

n8n (latest version recommended)

OpenAI API Key

Gmail OAuth2 credentials

Gmail API enabled in Google Cloud Console

⚙️ Setup Instructions
1️⃣ Import Workflow

Copy the provided JSON file

In n8n → Import Workflow

Paste the JSON

2️⃣ Configure Credentials

Manually connect:

OpenAI API credentials

Gmail OAuth2 credentials

Attach them to:

OpenAI Chat Model

Gmail Tool nodes

3️⃣ Activate Workflow

Toggle workflow to Active

💬 Example Prompts

“Summarize my last two emails.”

“Send an email to john@example.com
 saying I will be late.”

“Summarize the last email and send the summary to my manager.”

“Summarize today’s unread emails.”

🔒 Security Notes

Credentials are not included in this repository.

Never commit API keys.

Use environment variables or secure credential storage.

Ensure least-privilege Gmail permissions.

🛠 Customization Ideas

You can enhance this workflow by:

Adding a Send Email Gmail node

Filtering unread emails only

Adding label-based filtering

Implementing email classification

Connecting Slack or Telegram notifications

Adding attachment summarization

📊 Metadata

Agent Type: LangChain Agent

Model: gpt-5-mini

Gmail Operation: getAll

Execution Mode: v1

Status: Inactive by default

📌 Future Improvements

Memory-based email context

Multi-step reasoning workflows

Calendar integration

Unified AI productivity assistant
