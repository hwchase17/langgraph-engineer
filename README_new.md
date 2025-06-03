# LangGraph Engineer

**An AI-powered agent that helps you bootstrap LangGraph applications with intelligent workflow design**

[Try out the deployed version](https://smith.langchain.com/studio/thread?baseUrl=https://langgraph-engineer-23dacb3822e3589d80ff57de9ee94e1c.default.us.langgraph.app)

![](static/agent_ui.png)

## What is LangGraph Engineer?

LangGraph Engineer is an intelligent AI agent designed to accelerate the development of [LangGraph](https://github.com/langchain-ai/langgraph) applications by automating the initial scaffolding and workflow design process. Instead of starting from scratch, developers can describe their requirements in natural language and receive a well-structured LangGraph application foundation.

### Key Value Propositions

- **🚀 Rapid Prototyping**: Transform ideas into working LangGraph structures in minutes, not hours
- **🎯 Intelligent Design**: Leverages AI to create optimal node and edge configurations based on your specific requirements
- **🔄 Iterative Refinement**: Built-in validation and critique system ensures high-quality output through multiple review cycles
- **📚 Best Practices**: Generates code following LangGraph conventions and patterns
- **⚡ Developer Focused**: Handles the boilerplate so you can focus on implementing your unique business logic

### What Problems Does It Solve?

- **Learning Curve**: Reduces the barrier to entry for developers new to LangGraph
- **Architecture Decisions**: Eliminates guesswork in designing optimal workflow structures
- **Time to Market**: Significantly reduces initial development time for LangGraph projects
- **Consistency**: Ensures applications follow established patterns and best practices

> **Note**: This is an alpha version that focuses on creating the correct nodes and edges structure. It intentionally leaves the implementation of node logic to you, providing a solid foundation while preserving your creative control over the business logic.

## Agent Details

The agent consists of a few steps:

1. Converse with the user to gather all requirements
2. Write a draft
3. Run programatic checks against the generated draft (right now just checking that the response has the right format). If it fails, then go back to step 2. If it passes, then continue to step 4.
4. Run an LLM critique against the generated draft. If it fails, go back to step 2. If it passes, the continue to the end.

## 🚀 Installation & Setup

### Prerequisites

Before getting started, ensure you have the following installed on your system:

- **Python 3.11+** (Required - specified in langgraph.json)
- **pip** (Python package manager)
- **Git** (for cloning the repository)

### API Keys Required

You'll need API keys from the following services:

- **Anthropic API Key** - For Claude models ([Get your key](https://console.anthropic.com/))
- **OpenAI API Key** - For GPT models ([Get your key](https://platform.openai.com/api-keys))
- **Tavily API Key** - For web search capabilities ([Get your key](https://tavily.com/))

### Local Development Setup

#### 1. Clone the Repository

```bash
git clone <repository-url>
cd langgraph-engineer
```

#### 2. Create a Virtual Environment (Recommended)

```bash
# Create virtual environment
python -m venv venv

# Activate virtual environment
# On macOS/Linux:
source venv/bin/activate
# On Windows:
venv\Scripts\activate
```

#### 3. Install Dependencies

```bash
# Install the package and its dependencies
pip install -e .
```

This will install the following core dependencies:
- `langgraph` - Core LangGraph framework
- `langchain_anthropic` - Anthropic model integration
- `langchain_core` - Core LangChain functionality
- `langchain_openai` - OpenAI model integration

#### 4. Environment Configuration

Create a `.env` file in the root directory by copying the example:

```bash
cp .env.example .env
```

Edit the `.env` file and add your API keys:

```env
ANTHROPIC_API_KEY=your_anthropic_api_key_here
TAVILY_API_KEY=your_tavily_api_key_here
OPENAI_API_KEY=your_openai_api_key_here
```

#### 5. Verify Installation

Test that everything is working correctly:

```bash
python -c "import langgraph_engineer; print('Installation successful!')"
```

### Running Options

#### Option 1: LangGraph Studio (Recommended for Development)

1. Install LangGraph Studio following the [official guide](https://github.com/langchain-ai/langgraph-studio)
2. Open the project directory in LangGraph Studio
3. The studio will automatically detect the `langgraph.json` configuration
4. Start developing and testing your agent interactively

#### Option 2: Deploy to LangGraph Cloud

1. Follow the [LangGraph Cloud deployment guide](https://langchain-ai.github.io/langgraph/cloud/#overview)
2. The `langgraph.json` file contains all necessary configuration
3. Ensure your environment variables are properly set in your deployment environment

#### Option 3: Try the Deployed Version

For quick testing without local setup:
[Try out the deployed version](https://smith.langchain.com/studio/thread?baseUrl=https://langgraph-engineer-23dacb3822e3589d80ff57de9ee94e1c.default.us.langgraph.app)

### Troubleshooting

#### Common Issues

**Python Version Error**
- Ensure you're using Python 3.11 or higher: `python --version`
- If using multiple Python versions, try `python3.11` explicitly

**API Key Issues**
- Verify your API keys are correctly set in the `.env` file
- Check that there are no extra spaces or quotes around the keys
- Ensure your API keys have the necessary permissions and credits

**Import Errors**
- Make sure you've activated your virtual environment
- Try reinstalling dependencies: `pip install -e . --force-reinstall`
- Check that all required packages are installed: `pip list`

**LangGraph Studio Issues**
- Ensure LangGraph Studio is properly installed and updated
- Check that the `langgraph.json` file is in the root directory
- Verify that your environment variables are accessible to the studio

#### Getting Help

If you encounter issues not covered here:
1. Check the [LangGraph documentation](https://langchain-ai.github.io/langgraph/)
2. Review the project's issue tracker
3. Ensure all prerequisites are met and API keys are valid

## How to run

[Try out the deployed version](https://smith.langchain.com/studio/thread?baseUrl=https://langgraph-engineer-23dacb3822e3589d80ff57de9ee94e1c.default.us.langgraph.app)

You can run this code locally with [LangGraph Studio](https://github.com/langchain-ai/langgraph-studio)

You can deploy the code yourself to [LangGraph Cloud](https://langchain-ai.github.io/langgraph/cloud/#overview)


## Future direction:

 - Run more programatic checks (linting, checking imports)
 - Try to run the generated code
 - Attempt to generate code for the nodes and edges


## Key Capabilities and Features

LangGraph Engineer provides comprehensive capabilities for streamlining LangGraph application development:

### Core Features

- Intelligent Requirements Gathering: Interactive conversational interface
- Automated Code Generation: Well-structured LangGraph applications  
- Built-in Validation: Programmatic checks for code format
- AI-Powered Code Review: LLM-based critique system
- Iterative Refinement: Continuous improvement loops
- Multi-Model Support: OpenAI and Anthropic model support
- Best Practices: LangGraph conventions and patterns

### Technical Capabilities

- State Management: Generates MessagesState and TypedDict structures
- Graph Topology: Complex workflows with conditional routing
- Error Handling: Robust validation and recovery mechanisms
- Code Formatting: Python and LangGraph best practices
- Documentation Integration: Uses official LangGraph test files

USAGE_DOCS'