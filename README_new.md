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

## How to run

[Try out the deployed version](https://smith.langchain.com/studio/thread?baseUrl=https://langgraph-engineer-23dacb3822e3589d80ff57de9ee94e1c.default.us.langgraph.app)

You can run this code locally with [LangGraph Studio](https://github.com/langchain-ai/langgraph-studio)

You can deploy the code yourself to [LangGraph Cloud](https://langchain-ai.github.io/langgraph/cloud/#overview)


## Future direction:

 - Run more programatic checks (linting, checking imports)
 - Try to run the generated code
 - Attempt to generate code for the nodes and edges
