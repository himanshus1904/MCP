# MCP

![Model Context Protocol (MCP)](https://microsoft.github.io/genaiscript/_astro/mcp.CBnQ_GM8_1eWG7e.webp )

# Content
1. Introduction
2. How it works?
3. Real-World Use Cases
4. Why should you care?

# Introduction


In late November 2024, Anthropic introduced the **Model Context Protocol (MCP)** – an open standard for connecting AI models (like LLMs) to external data sources and tools.

MCP is designed to break AI systems out of isolation by giving them a standardized way to access relevant context and perform actions on other systems. 

Think of MCP like a USB-C port for AI applications. Just as USB-C provides a standardized way to connect your devices to various peripherals and accessories, MCP provides a standardized way to connect AI models to different data sources and tools.
<!-- ![Model Context Protocol (MCP)](https://norahsakal.com/assets/images/mcp_overview-641a298352ff835488af36be3d8eee52.png) -->
<img src="https://norahsakal.com/assets/images/mcp_overview-641a298352ff835488af36be3d8eee52.png" alt="MCP Architecture" width="600"/>

<br></br>
# How it works
How MCP works: A technical breakdown
At its core, MCP follows a client–server architecture to link AI models with external resources. There are three main components in this design: 
1. a Host, 
2. one or more Clients, and 
3. one or more Servers

**MCP Host**: The host is the AI-powered application or agent environment (for example, the Claude desktop app, an IDE plugin, or any custom LLM-based app). The host is what the end-user interacts with, and it can connect to multiple MCP servers at once (e.g. one server for email, one for a database).  

**MCP Client**: The client is an intermediary that the host uses to manage each server connection. Each MCP client handles the communication to one MCP server, keeping them sandboxed for security. The host spawns a client for each server it needs to use, maintaining a one-to-one link.  

**MCP Server**: The server is a program (usually external to the model) that implements the MCP standard and provides a specific set of capabilities – typically a collection of tools, access to data resources, and predefined prompts related to some domain. An MCP server might interface with a database, a cloud service, or any data source; Anthropic and the community have released servers for Google Drive, Slack, GitHub, databases like Postgres/SQLite, web browsers (via Puppeteer), and more.

![MCP Architecture](https://portkey.ai/blog/content/images/size/w2000/2024/12/whatismcp.png)
<br></br>
# Real-World Use Cases

Applications and Use Cases of MCP

###  **Enterprise Data Assistants**: 
    MCP enhances AI-powered chatbots that access internal company data for:

    a) Querying employee HR records
    b) Checking project details from management tools
    c) Pulling documents from Google Drive or Slack

    This improves customer support bots, HR assistants, and other enterprise AI agents by ensuring access to updated internal knowledge bases.

### Software Development and Coding Agents: 
    Coding assistants (like GitHub Copilot, Sourcegraph's Cody, etc.) leverage MCP to:

    a) Fetch code context, documentation, or commit logs
    b) Execute build/test commands directly via MCP connectors

    For instance, an IDE with MCP integration can fetch relevant files, improving code suggestions with greater project awareness.

### Multi-Modal and Data Analysis Tools: 
    MCP allows AI to connect with data sources beyond text. Examples include:

    a) Fetching charts from spreadsheets
    b) Retrieving metrics from Cloudflare or Sentry for DevOps monitoring

    This simplifies integrating AI into finance, healthcare, and education domains via a common protocol layer.



<br></br>
# Why should you care?

1. **Universal Data Access**

Traditionally, connecting AI models to various data sources required custom code for each dataset—a time-consuming and error-prone process. MCP eliminates this hurdle by providing a standardized protocol, allowing AI systems to seamlessly access any data source.

2. **Enhanced Performance and Efficiency**

By streamlining data access, MCP significantly boosts AI performance. Direct connections to data sources enable faster and more accurate responses, making AI applications more efficient.

3. **Broad Applicability**

Unlike previous solutions limited to specific applications, MCP is designed to work across all AI systems and data sources. This universality makes it a versatile tool for various AI applications, from coding platforms to data analysis tools.

4. **Facilitating Agentic AI**

MCP supports the development of AI agents capable of performing tasks on behalf of users by maintaining context across different tools and datasets. This capability is crucial for creating more autonomous and intelligent AI systems.

# References

1. https://modelcontextprotocol.io/introduction
2. https://www.anthropic.com/news/model-context-protocol
3. https://wandb.ai/onlineinference/mcp/reports/The-Model-Context-Protocol-MCP-by-Anthropic-Origins-functionality-and-impact--VmlldzoxMTY5NDI4MQ