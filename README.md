# MCP Chatbot with Multi-Server Integration

![Python](https://img.shields.io/badge/python-3.11+-blue.svg)
![MCP](https://img.shields.io/badge/MCP-enabled-green.svg)
![LangChain](https://img.shields.io/badge/LangChain-integrated-orange.svg)
![Groq](https://img.shields.io/badge/Groq-LLM-red.svg)

An interactive chatbot powered by the **Model Context Protocol (MCP)** that integrates multiple specialized servers for enhanced functionality. Built with LangChain, Groq LLM, and MCP Agent for conversational AI with tool-calling capabilities.

## Features

- 🤖 **Conversational AI** with memory-enabled chat history
- 🔧 **Multi-Tool Integration** via MCP servers:
  - **Playwright**: Browser automation and web interaction
  - **Airbnb**: Search and retrieve accommodation listings
  - **DuckDuckGo Search**: Web search capabilities
- 📝 **Logging**: Comprehensive logging for debugging and monitoring
- 💬 **Interactive CLI**: Simple command-line interface with conversation management
- 🧠 **Memory**: Persistent conversation history within sessions

## Prerequisites

- Python 3.11+
- Node.js and npm (for MCP server dependencies)
- Groq API key

## Installation

1. **Clone the repository**:
   ```bash
   git clone <repository-url>
   cd chatbot_model_context_protocol
   ```

2. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   # or using uv
   uv sync
   ```

3. **Set up environment variables**:
   Create a `.env` file in the project root:
   ```env
   GROQ_API_KEY=your_groq_api_key_here
   ```

## Configuration

### MCP Servers

The chatbot uses three MCP servers defined in `mcp_servers.json`:

- **Playwright**: Browser automation for web scraping and interaction
- **Airbnb**: Search for accommodations with filters
- **DuckDuckGo Search**: General web search capabilities

You can modify `mcp_servers.json` to add or remove servers as needed.

### Logging

Logs are saved to `logs/mcpchatbot.log`. The logger configuration can be adjusted in `logger.py`.

## Usage

Run the chatbot:

```bash
python app.py
```

### Commands

- **Type your query**: Ask questions or give instructions
- **`clear` or `cls`**: Clear conversation history
- **`exit`, `quit`, or `q`**: Exit the chatbot

### Example Queries

```
You: Search for hotels in New York for March 1, 2026
You: Find information about the Eiffel Tower
You: Open a browser and navigate to example.com
```

## Project Structure

```
chatbot_model_context_protocol/
├── app.py                 # Main chatbot application
├── logger.py              # Logging configuration
├── mcp_servers.json       # MCP server definitions
├── .env                   # Environment variables (not in git)
├── requirements.txt       # Python dependencies
├── pyproject.toml         # Project metadata
├── uv.lock                # Dependency lock file
└── logs/                  # Log files (not in git)
```

## Dependencies

- `langchain-groq`: Groq LLM integration
- `mcp-use`: MCP Agent and Client
- `python-dotenv`: Environment variable management
- `asyncio`: Asynchronous execution

## License

MIT

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.