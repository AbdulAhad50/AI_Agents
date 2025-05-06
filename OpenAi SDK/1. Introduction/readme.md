# 🧠 OpenAI Agents SDK – Roman Urdu Style Guide

## 📌 What is OpenAI Agents SDK?

**OpenAI Agents SDK** aik lightweight aur easy-to-use SDK hai jo aapko smart AI agents banane mein madad deta hai. Pehle is per OpenAI ne ek experimental project "Swarm" banaya tha — yeh usi ka production-ready version hai.

Is SDK ke zariye aap real-world applications ke liye powerful agents design kar sakte hain, bina kisi complex code ke.

---

## 🔑 Core Components (Primitives)

### 1. Agents

Yeh Large Language Models (LLMs) hote hain jo aap instructions aur tools ke sath configure karte ho.
**Example:** Aap bolte ho `Tum aik helpful assistant ho` aur agar zarurat ho to tools bhi dete ho.

### 2. Handoffs

Aik agent doosray agent ko task assign kar sakta hai.
**Example:** Agar aik agent ko technical kaam milta hai, woh doosray expert agent ko handoff kar dega.

### 3. Guardrails

Yeh input validation ke liye hote hain. Agar input invalid ya empty ho to agent kaam hi nahi karega.

---

## ⚙️ Built-in Features

* **Agent loop**: Tool ko call karo → result LLM ko do → repeat until done.
* **Python-first**: Python ke andar kaam karo, koi naye framework ya syntax seekhne ki zarurat nahi.
* **Multi-agent coordination (handoffs)**: Agents aapas mein tasks share kar sakte hain.
* **Guardrails**: Input validation aur error handling.
* **Function tools**: Kisi bhi Python function ko tool bana sakte ho.
* **Tracing**: Agent kya kar raha hai — visualize aur debug karo.

---

## 🚀 Installation

```bash
pip install openai-agents
```

---

## 👋 Hello World Example

```python
from agents import Agent, Runner

agent = Agent(
    name="Assistant",
    instructions="You are a helpful assistant"
)

result = Runner.run_sync(agent, "Write a haiku about recursion in programming.")
print(result.final_output)
```

🔁 **Output Example:**

```
Code within the code,
Functions calling themselves,
Infinite loop's dance.
```

---

## 🔐 API Key Setup

Before running the code, set your OpenAI API key in environment variables:

```bash
export OPENAI_API_KEY='YOUR_OPENAI_KEY'
```

---

## ✅ Summary

* Simple aur powerful SDK.
* Python ke sath direct integration.
* LLM agents, input guardrails, aur handoffs support karta hai.
* Real-world AI apps ke liye tayyar hai.

---

**Made for devs who think in Python, speak in logic, and build in AI.**


