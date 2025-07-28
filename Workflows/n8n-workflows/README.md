# N8N Workflow Powerhouse: AI, Automation & Agentic Examples

Welcome to the N8N Workflow Powerhouse! This repository is a public collection of diverse and powerful n8n workflows designed to showcase a wide range of automation possibilities, with a strong focus on **AI-driven tasks, agentic systems, and practical integrations.**

Whether you're new to n8n, an experienced automator, or an AI enthusiast, you'll find valuable examples, templates, and inspiration here. Our goal is to help you learn, build, and supercharge your own n8n projects!

## 🚀 What's Inside?

This repository contains:

1.  **A Rich Collection of `.json` Workflow Files:**
    *   Dozens of ready-to-import n8n workflows covering use cases like:
        *   Advanced AI Document Parsing (LlamaParse, Invoices)
        *   AI Agent Chatbots with Long-Term Memory & Tool Usage (OpenAI, DeepSeek, Ollama, Google Gemini)
        *   YouTube Content Summarization, Transcription & Analysis
        *   Automated Multi-Platform Social Media Content Creation & Publishing
        *   RAG (Retrieval-Augmented Generation) Chatbots for Your Documents
        *   WordPress & Ghost Blog Content Automation from PDFs & Perplexity Research
        *   Local & Private AI Assistants with Ollama (including dynamic LLM routing)
        *   Web Scraping (Jina.ai, Tavily) & Data Aggregation
        *   Database Interaction (Postgres/Supabase) & Chart Generation (QuickCharts)
        *   Practical Utilities (n8n Workflow Backups, RSS Feed Monitoring)
        *   And much more!

2.  **`0. workflows.diy - n8n - public repo.md`:**
    *   This special markdown file contains the **aggregated raw JSON of ALL the workflows** in this repository. It's designed to be a powerful dataset for analysis and learning, especially when used with Large Language Models (LLMs) that have large context windows.

3.  **`1. Workflow Titles and Descriptions.md`:**
    *   A human-readable markdown table listing every workflow with a brief description. This helps you quickly find workflows relevant to your interests and provides excellent context for LLM analysis.

## 💡 Why This Repository? / Use Cases

This collection is designed to:

*   **Learn n8n Best Practices:** See real-world examples of how to structure complex workflows.
*   **Grab Ready-to-Use Templates:** Kickstart your projects by adapting these workflows to your specific needs.
*   **Explore Advanced AI & Agentic Systems:** Dive into how AI agents, various LLMs, RAG, and tool usage can be implemented in n8n.
*   **Understand Complex Integrations:** See how n8n can connect a multitude of services like Google Drive, Gmail, Telegram, WordPress, OpenAI, Ollama, and more.
*   **Demystify Local LLMs:** Explore workflows specifically designed for private, self-hosted AI using Ollama.

## 🧠 Supercharge Your Learning & Creation with LLMs (like Google Gemini!)

The `.md` files in this repository are not just for reading – they are powerful tools when combined with Large Language Models (LLMs) that can process large amounts of text (large context windows), such as **Google Gemini 2.5 Pro**.

### The Power of Aggregated JSON (`0. workflows.diy - n8n - public repo.md`)

This file contains the *entire JSON structure of every workflow*. By providing this to an LLM, you can:

*   **Deeply Understand n8n Workflows:**
    *   Ask the LLM: *"Based on this aggregated JSON, what are the common patterns for handling errors in these n8n workflows?"*
    *   *"Explain the structure of an n8n AI Agent node using examples from this data."*
*   **Get Explanations for Specific Workflows:**
    *   *"Explain the 'Advanced AI Powered Document Parsing & Text Extraction with Llama Parse.json' workflow from the provided aggregated JSON. What are its key steps and technologies?"*
*   **Recreate or Generate New Workflows:**
    *   Describe a new workflow you want to build and ask the LLM to draft the JSON for it, using the patterns it learned from the examples.
    *   *"Using the patterns in the provided n8n workflow JSON, can you generate a new workflow that triggers on a new GitHub issue, uses an AI agent to classify its sentiment, and then posts a summary to a Slack channel?"*
*   **Learn n8n Node Configuration:**
    *   *"What are the typical parameters for a Google Sheets node when reading data, based on these examples?"*
*   **Create Training Materials or Documentation:**
    *   *"Generate a tutorial on how to build an AI chatbot with long-term memory in n8n, using the examples from the `AI Agent Chatbot + LONG TERM Memory + Note Storage + Telegram.json` workflow found in the aggregated JSON."*

### Using Descriptive Summaries (`1. Workflow Titles and Descriptions.md`)

This file provides a quick overview and valuable context:

*   **Quick Discovery:** Easily scan the table to find workflows that interest you.
*   **Context for LLMs:** When used alongside `0. workflows.diy - n8n - public repo.md`, this file helps the LLM understand the *purpose* of each workflow, leading to more relevant and accurate explanations or generations.
    *   For example: *"Using both the aggregated JSON and the workflow descriptions, tell me more about the workflows related to 'YouTube Video Summarization'."*

## 📋 How to Use These Workflows

### Importing `.json` Workflow Files into n8n:

1.  **Open the `.json` file** from this repository (e.g., in a text editor or directly from GitHub).
2.  **Select and Copy** the entire JSON content (Ctrl+A or Cmd+A, then Ctrl+C or Cmd+C).
3.  **In your n8n instance,** go to your workflows list or open an empty workflow.
4.  **Click on an empty spot on the canvas.**
5.  **Paste** the copied JSON (Ctrl+V or Cmd+V).
6.  The workflow should appear on your canvas!

### ❗ Crucial: Configuration is Key!

*   **Placeholders:** Most workflows will contain **PLACEHOLDER VALUES** for API keys, URLs, chat IDs, Google Doc/Sheet IDs, etc. You **MUST** replace these with your own valid information for the workflows to function. Look for values like `"[YOUR_..._HERE]"` or example IDs.
*   **Credentials:**
    *   For nodes that interact with external services (e.g., OpenAI, Google Sheets, Gmail, Telegram, WordPress, Ollama API base URL), you will need to **select or create your own credentials** within the n8n interface for those nodes.
    *   The JSON files reference credential *types*, but not your actual secret keys.
*   **Test Thoroughly:** Always test a workflow after importing and configuring it, especially before using it in a production environment.

## 🛠️ Prerequisites & General Dependencies

To use these workflows effectively, you'll generally need:

*   An **n8n instance** (many work on n8n.cloud, but some, especially those using local Ollama or specific file paths, are best suited for self-hosted instances).
*   **Credentials** for the various services used, such as:
    *   OpenAI API Key
    *   Google Cloud API Key (for Gemini, YouTube Data API)
    *   Google OAuth Credentials (for Drive, Sheets, Gmail)
    *   Telegram Bot Token & Chat ID
    *   WordPress Admin API Credentials
    *   Ghost Admin API Key
    *   Perplexity API Key
    *   Tavily API Key
    *   Ollama (if running local LLMs, ensure Ollama is installed and models are pulled)
    *   Credentials for any other specific services mentioned in individual workflows.
*   **n8n Community Nodes:** Some workflows might use community nodes (e.g., `youtube-transcript`, `n8n-nodes-mcp`). You may need to install these in your n8n instance. Often, for packages like `youtube-transcript`, you might need to install it globally on your n8n server environment (`npm install -g youtube-transcript`) if a Code node uses it directly.
*   **Understanding of the services:** Familiarity with the APIs and services being automated will help in troubleshooting and customization.

## ✨ Workflow Highlights

This repository covers a vast range of automation tasks. Some exciting areas include:

*   **Advanced Document Processing:** Go beyond simple text extraction with LlamaParse and AI-driven structuring.
*   **Sophisticated AI Agents:** Explore multi-tool agents, long-term memory, and even dynamic LLM routing with local models.
*   **Content Creation Factories:** Automate social media and blog content from start to finish.
*   **Private AI with Ollama:** Run powerful AI assistants and tools entirely on your own hardware.

*(You can find a full list with brief descriptions in the `1. Workflow Titles and Descriptions.md` file!)*

## 📜 Disclaimer

*   These workflows are provided as-is for educational and illustrative purposes.
*   **Use them at your own risk.** Always test thoroughly in a safe environment before deploying to production or connecting to sensitive systems.
*   Be mindful of API costs, rate limits, and the terms of service for any external APIs or services used.
*   Ensure responsible use, especially for workflows involving web scraping or automated content posting.

## 🤝 Contributing & Feedback

If you find issues, have suggestions for improvements, or want to contribute your own amazing n8n workflows, please feel free to open an Issue or Pull Request on this GitHub repository (if applicable).

## 📄 License
This project is licensed under the MIT License.

---

Happy Automating!