# mcp_gemini
Example of MCP server and client using Gemini

## Background

`mcp_gemini` demonstrates how to build an AI-powered research assistant using the [MCP](https://github.com/stanford-crfm/mcp) (Modular Command Protocol) framework and Google Gemini LLM. The project includes:
- An MCP server (`research_server.py`) that provides tools for searching and extracting information from arXiv papers.
- An MCP client (`mcp_client.py`) that connects to the server and uses Gemini 2.0 Flash for conversational AI, including tool/function calling.

## Prerequisites

- Python 3.11 or newer
- [uv](https://github.com/astral-sh/uv) (for running the server)
- A Google Gemini API key (set as `GEMINI_API_KEY` in your environment)

## Installation

1. **Clone the repository:**
   ```sh
   git clone https://github.com/yourusername/mcp_gemini.git
   cd mcp_gemini
   ```

2. **Install dependencies:**
   ```sh
   uv pip install -r pyproject.toml
   ```

3. **Set up environment variables:**
   - Create a `.env` file or export your Gemini API key:
     ```sh
     export GEMINI_API_KEY=your-gemini-api-key
     ```

## How to Run

1. **Start the MCP server (optional, the client can also auto-start it):**
   ```sh
   uv run research_server.py
   ```

2. **Run the MCP client:**
   ```sh
   uv run mcp_client.py
   ```

   The client will connect to the server, list available tools, and start an interactive chat loop. Type your queries (e.g., "Find papers about quantum computing") and the Gemini LLM will use the server's tools as needed.

3. **Exit:**
   Type `quit` in the chat to exit.

## Notes

   MCP support in Gemini SDK 1.16.1 is experimental, and the API is subject to change in future versions.

---
