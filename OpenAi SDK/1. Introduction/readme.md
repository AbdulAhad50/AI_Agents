### ✅ `OpenAi SDK For Agents` (Introduction)

````markdown
# 🤖 OpenAI Agents SDK – Agentic AI App Starter

This project demonstrates how to build intelligent agent-based applications using the **OpenAI Agents SDK** — a lightweight, Python-first framework to develop agentic workflows using LLMs.

---

## 🚀 What is the OpenAI Agents SDK?

The **Agents SDK** enables you to create LLM-based agents that can:
- Perform tasks based on instructions.
- Use tools (Python functions) to interact with data or APIs.
- Delegate subtasks to other agents using handoffs.
- Validate input and behavior through guardrails.
- Visualize workflows using built-in tracing.

> ✅ It's a production-ready upgrade of OpenAI's experimental **Swarm** framework.

---

## ✨ Key Features

- 🔁 **Agent Loop** – Built-in loop to run tools and return results to the LLM until the task is complete.
- 🐍 **Python-first** – Use native Python to orchestrate agents and tools.
- 🤝 **Handoffs** – Delegate specific tasks to other agents.
- ✅ **Guardrails** – Validate and secure input before agents act.
- 🧰 **Function Tools** – Any Python function can be converted into a tool with automatic schema validation (Pydantic).
- 🧠 **Tracing** – Debug, visualize, and monitor workflows.

---

## 📦 Installation

Make sure you have Python 3.8+ installed.

```bash
pip install openai-agents
````

Set your OpenAI API key before running the app:

```bash
export OPENAI_API_KEY=sk-...your_api_key_here...
```

(Optional) Enable tracing to visualize agent behavior:

```bash
export AGENTS_TRACE=1
```

---

## 👋 Hello World Example

```python
from agents import Agent, Runner

agent = Agent(name="Assistant", instructions="You are a helpful assistant")

result = Runner.run_sync(agent, "Write a haiku about recursion in programming.")
print(result.final_output)
```

**Sample Output:**

```
# Code within the code,
# Functions calling themselves,
# Infinite loop's dance.
```

---

## 🧰 Add a Python Tool

Turn any Python function into a tool using the `@tool` decorator:

```python
from agents import tool

@tool
def add(a: int, b: int) -> int:
    """Add two numbers."""
    return a + b
```

You can now register this tool with your agent so it can call it when needed.

---

## 🧠 Core Concepts

| Primitive     | Description                                                      |
| ------------- | ---------------------------------------------------------------- |
| **Agent**     | An LLM with a name, tools, and instructions.                     |
| **Runner**    | Orchestrates agent loops, tools, and interactions.               |
| **Tool**      | Any Python function exposed to an agent as a callable operation. |
| **Handoff**   | Delegate task to another agent.                                  |
| **Guardrail** | Validates input or controls behavior before execution.           |
| **Tracing**   | Built-in debugger and visualizer for agentic flows.              |

---

## 📈 Tracing and Debugging

To enable tracing for debugging and monitoring:

```bash
export AGENTS_TRACE=1
```

You'll receive detailed logs of:

* Tool usage
* Agent thoughts
* Inputs/outputs
* Errors (if any)

---

## 📚 Learn More

* [OpenAI Agents SDK Docs](https://platform.openai.com/docs/agents)
* [Pydantic for Input Validation](https://docs.pydantic.dev/)
* [OpenAI Python Client](https://github.com/openai/openai-python)

---

## 🪪 License

Licensed under the [MIT License](LICENSE)

---

## 🙋‍♂️ Author

Built with ❤️ using the OpenAI Agents SDK. Contributions, feedback, and suggestions are welcome!
