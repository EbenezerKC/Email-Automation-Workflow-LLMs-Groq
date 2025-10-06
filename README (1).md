
# Project Title

SmartMail AI Automation Workflow – Intelligent Email Categorization using LLMs and n8n.

## Project Overview

The SmartMail AI Automation Workflow is an intelligent automation system built using n8n and Large Language Models (LLMs) to streamline the management of incoming emails.

The solution automatically receives, processes, and categorizes Gmail messages in real time using LLM-based content analysis — enhancing productivity, prioritization, and automated decision-making in email workflows.

## Project Architecture & Workflow Design

The automation flow is designed to perform end-to-end email intelligence in four main stages:

1. Trigger – Gmail Node

The workflow begins with a Gmail Trigger node, which monitors the inbox for any new incoming messages.

Once a new email is detected, key metadata (sender, subject, snippet, and message ID) is extracted.

2. Message Retrieval

A secondary Gmail Get Message node retrieves the full email body (HTML and text) using the unique Gmail message ID.

This ensures that the entire email content is available for intelligent processing.

3. LLM Categorization & Data Parsing

A Function (or LLM Parse) node processes the full message and uses natural language understanding to categorize the email into pre-defined categories such as:

Notification

Career

Financial

Meeting/Calendar

Personal

Promotion

Action Required

Work

Other

The system then maps each category to a corresponding Gmail Label ID, ensuring seamless integration with the Gmail labeling system.

4. Dynamic Label Application & Smart Summary Generation

Using a JavaScript Function node, the workflow:

Combines the LLM category with the Gmail Label ID dynamically.

Generates a structured summary message that includes the category emoji, label ID, and concise email snippet.

The message is then output for labeling, notifications, or further downstream actions (e.g., Slack alerts or Google Sheets logging).

## Core Technologies & Tools Used
Technology	Description
n8n	Low-code automation platform used to design and orchestrate the workflow
LLMs (Large Language Models)	Used for semantic understanding and categorization of email content
Gmail API Integration	Enables real-time email fetching, parsing, and labeling
JavaScript Function Nodes	Handles logic for dynamic mapping, parsing, and message generation
HTML & JSON Email Representation	Enables clean rendering and flexible data transformation

## Key Features & Functionalities

✅ Automated Email Categorization:
Each incoming email is analyzed by an LLM to determine its contextual category.

✅ Real-Time Gmail Labeling:
Automatically applies the correct Gmail label using label IDs for instant inbox organization.

✅ LLM-Driven Content Parsing:
Parses HTML email messages to extract meaningful content for decision-making.

✅ Dynamic Message Summaries:
Creates short, intelligent summaries (snippets) of each email for quick insight.

✅ Scalable and Extensible Design:
Built modularly — new categories, nodes, or integrations (e.g., Slack, Notion, or Sheets) can be added easily.

## Impact & Value

Reduced Inbox Clutter: Automates sorting and labeling of emails, reducing manual effort.

Enhanced Decision Speed: Enables faster prioritization of important emails like “Action Required” or “Financial”.

Showcases Intelligent Automation: Demonstrates how LLMs + n8n + Gmail API can create real-world AI-powered business productivity tools.

Scalable Use Case: Can be extended to enterprise email systems, customer support inboxes, or ticketing systems.

## My Role & Contributions

As a Cloud & DevOps Engineer, I:

Designed and implemented the end-to-end automation flow using n8n.

Integrated Gmail API nodes for real-time triggers and message retrieval.

Developed custom JavaScript logic for intelligent message parsing and dynamic label mapping.

Embedded LLM reasoning capabilities for semantic email classification.

Documented and tested the entire workflow for performance and scalability.

Groq API – for high-speed inference and efficient LLM integration

## Outcome

The SmartMail AI Automation Workflow successfully automates the email triage process, combining cloud automation, LLM intelligence, and no-code orchestration.

This project demonstrates how modern AI-driven automations can empower professionals and organizations to focus on meaningful work — while intelligent systems handle repetitive communication tasks.


## Workflow

# Intelligent Email Automation Workflow (n8n + LLMs + Groq)

## 📘 Overview
This workflow automatically reads incoming Gmail messages, categorizes them using a Large Language Model (LLM), and labels them accordingly in real time.

## ⚙️ Tools Used
- n8n (Open-source automation)
- Groq API for LLM processing
- Gmail Node
- Function Node (for categorization logic)

## 🧠 Workflow Structure
1. *Trigger Node:* Gmail Trigger (new email)
2. *Processing Node:* Send email content to Groq API
3. *Decision Node:* LLM classifies emails (e.g., Work, Personal, Marketing)
4. *Action Node:* Gmail Node applies label

## 💾 Files
- email_automation.json: Exported n8n workflow file
- README.md: Project documentation

## 🚀 How to Import
1. Open n8n.
2. Click *Import from File*.
3. Choose email_automation.json.
4. Update your API credentials.
5. Activate the workflow.


## Check the json file to see the n8n workflow