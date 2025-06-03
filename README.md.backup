# LangGraph Engineer

[Try out the deployed version](https://smith.langchain.com/studio/thread?baseUrl=https://langgraph-engineer-23dacb3822e3589d80ff57de9ee94e1c.default.us.langgraph.app)

![](static/agent_ui.png)

This is an alpha version of an agent that can help bootstrap [LangGraph](https://github.com/langchain-ai/langgraph) applications. It will focus on creating the correct nodes and edges, but will not attempt to write the logic to fill in the nodes and edges - rather will leave that for you.

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