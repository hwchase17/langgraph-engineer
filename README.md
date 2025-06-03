# LangGraph Engineer

[![LangGraph](https://img.shields.io/badge/Built%20with-LangGraph-blue)](https://github.com/langchain-ai/langgraph)
[![Python 3.11+](https://img.shields.io/badge/python-3.11+-blue.svg)](https://www.python.org/downloads/)

An intelligent LangGraph application builder that helps you bootstrap LangGraph applications through interactive conversation. This alpha agent focuses on creating the correct graph topology (nodes and edges) while leaving the implementation details for you to customize.

## 🚀 Quick Start

**Try the deployed version:** [LangGraph Engineer Demo](https://smith.langchain.com/studio/thread?baseUrl=https://langgraph-engineer-23dacb3822e3589d80ff57de9ee94e1c.default.us.langgraph.app)

![](static/agent_ui.png)

## 📋 Table of Contents

- [Features](#features)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Project Structure](#project-structure)
- [Development](#development)
- [Deployment](#deployment)
- [Contributing](#contributing)
- [Troubleshooting](#troubleshooting)
- [Future Roadmap](#future-roadmap)

## ✨ Features

- **Interactive Requirements Gathering**: Conversational interface to understand your graph topology needs
- **Intelligent Code Generation**: Creates LangGraph applications using proven patterns from unit test examples
- **Multi-Model Support**: Compatible with both OpenAI and Anthropic models
- **Automated Validation**: Built-in programmatic checks and LLM-based critique system
- **Iterative Refinement**: Continuous improvement through feedback loops
- **Cloud-Ready**: Deployable to LangGraph Cloud with minimal configuration

## 🛠 Installation

### Prerequisites

- Python 3.11 or higher
- API keys for OpenAI and/or Anthropic (at least one required)
- Git (for cloning the repository)

### Local Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/langgraph-engineer.git
   cd langgraph-engineer
   ```

2. **Install dependencies:**
   ```bash
   pip install -e .
   ```

3. **Set up environment variables:**
   ```bash
   cp .env.example .env
   # Edit .env with your API keys
   ```

### Using LangGraph Studio (Recommended for Development)

1. Install [LangGraph Studio](https://github.com/langchain-ai/langgraph-studio)
2. Open the project directory in LangGraph Studio
3. Configure your API keys in the studio interface
4. Run the agent directly from the studio

## ⚙️ Configuration

### Environment Variables

Create a `.env` file in the project root with the following variables:

```env
# At least one of these is required
OPENAI_API_KEY=your_openai_api_key_here
ANTHROPIC_API_KEY=your_anthropic_api_key_here
```

### Model Configuration

The agent supports both OpenAI and Anthropic models. Model selection is handled automatically based on available API keys, with fallback logic built into the system.

## 🎯 Usage

### Basic Usage

1. **Start a conversation** with the agent about your LangGraph application needs
2. **Describe your requirements** - the agent will ask clarifying questions about:
   - Graph topology (nodes and edges)
   - Data flow requirements
   - Specific functionality needs
3. **Review the generated code** - the agent will provide a complete LangGraph application structure
4. **Iterate if needed** - provide feedback for refinements

### Example Interaction

```
User: "I want to build a customer support chatbot with sentiment analysis"

Agent: "I'll help you build that! Let me ask a few questions to understand your graph topology:
1. Do you want separate nodes for sentiment analysis and response generation?
2. Should there be a routing mechanism based on sentiment scores?
3. Do you need any human handoff capabilities?"

[After gathering requirements, the agent generates a complete LangGraph application]
```

### Running Locally

```bash
# Using LangGraph Studio (recommended)
langgraph-studio

# Or run directly with Python
python -m langgraph_engineer
```

## 🔄 How It Works

The LangGraph Engineer follows a structured 4-step workflow:

### 1. 📝 Requirements Gathering
- Interactive conversation to understand your needs
- Focuses on graph topology (nodes, edges, data flow)
- Asks clarifying questions to ensure complete understanding

### 2. ✍️ Draft Generation
- Creates LangGraph application code using proven patterns
- References unit test examples for best practices
- Generates complete graph structure with proper state management

### 3. ✅ Programmatic Validation
- Runs automated checks on generated code
- Validates format, structure, and basic syntax
- Returns to step 2 if validation fails

### 4. 🔍 LLM Critique
- AI-powered review of the generated solution
- Checks for best practices and potential improvements
- Iterates back to step 2 if critique suggests changes

## 📁 Project Structure

```
langgraph-engineer/
├── src/langgraph_engineer/
│   ├── agent.py              # Main LangGraph workflow definition
│   ├── state.py              # State management classes
│   ├── gather_requirements.py # Requirements gathering logic
│   ├── draft.py              # Code generation functionality
│   ├── critique.py           # Solution review and feedback
│   ├── check.py              # Validation and checks
│   ├── model.py              # Model selection and configuration
│   └── loader.py             # GitHub file loading utilities
├── static/
│   └── agent_ui.png          # UI screenshot
├── pyproject.toml            # Project configuration
├── langgraph.json            # LangGraph-specific settings
├── .env.example              # Environment variables template
└── README.md                 # This file
```

## 🚀 Deployment

### LangGraph Cloud

Deploy to [LangGraph Cloud](https://langchain-ai.github.io/langgraph/cloud/#overview) for production use:

1. Configure your `langgraph.json` file
2. Set up environment variables in the cloud console
3. Deploy using the LangGraph CLI or web interface

### Local Development

Use [LangGraph Studio](https://github.com/langchain-ai/langgraph-studio) for the best local development experience with visual graph debugging and real-time testing.

## 🤝 Contributing

We welcome contributions! Please see our contributing guidelines for details on how to:
- Report bugs
- Suggest enhancements
- Submit pull requests
- Follow our coding standards

## 🔧 Troubleshooting

### Common Issues

**API Key Errors:**
- Ensure at least one API key (OpenAI or Anthropic) is properly configured
- Check that your API keys have sufficient credits/quota

**Import Errors:**
- Verify Python 3.11+ is installed
- Ensure all dependencies are installed: `pip install -e .`

**Graph Execution Issues:**
- Check the LangGraph Studio console for detailed error messages
- Verify your graph topology is valid

For more help, please open an issue on GitHub with detailed error information.

## 🗺 Future Roadmap

