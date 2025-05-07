# 🤖 Pehla AI Agent Banao `openai-agents` SDK ke sath – Step-by-Step Guide

Is README file mein aap seekhoge ke kis tarah aap OpenAI Agents SDK ka use kar ke apna pehla smart AI agent bana sakte ho. Har step ko asaan aur detail mein samjhaya gaya hai.

---

## 📦 Step 1: SDK Install Karo

Sabse pehle humein `openai-agents` package install karna hoga:

```python
!pip install openai-agents
```

🔍 Ye command:

* `openai-agents` SDK ko PyPI se install karta hai.
* Zaroori dependencies ko download karta hai.
* Aapko `Agent` aur `Runner` classes available karta hai jinki madad se aap agents bana aur run kar sakte ho.

> 💡 Tip: Google Colab use karna best hai, ya koi bhi Python 3.8+ environment.

---

## 🔐 Step 2: OpenAI API Key Set Karo

Agent ko OpenAI ke server se baat karwani hoti hai, is liye humein apni **API Key** set karni hoti hai.

```python
import os

# Yahan apni real OpenAI API key paste karein
os.environ["OPENAI_API_KEY"] = "sk-..."  
```

🧠 **Yahan kya ho raha hai?**

* `os.environ["OPENAI_API_KEY"]` ka matlab hai: hum environment variable set kar rahe hain jise SDK internally use karega.
* Ye key server ke sath har request mein lagti hai taake authorized access mile.

> ⚠️ Apni key kabhi public mat karo. Production mein `.env` file use karo.

---

## 🧠 Step 3: Agent Banao aur Run Karo

Ab hum apna pehla agent banayenge jo user ke input ka smart jawab de sakta hai.

```python
from agents import Agent, Runner

# Agent banayein
agent = Agent(
    name="HelperAgent",
    instructions="Tum ek helpful aur polite assistant ho."
)

# Agent ko kisi prompt ke sath run karein
result = Runner.run_sync(agent, "Mujhe aik achi Urdu shayari sunao.")
```

### 🔍 Samajhne Wali Baat:

#### ➤ `Agent(...)`:

* Yahan hum ek naya agent define kar rahe hain.
* `name`: agent ka naam (jaise "HelperAgent").
* `instructions`: yeh agent ki **soch aur behavior** set karta hai.

  * Jaise `"Tum ek helpful aur polite assistant ho."` ka matlab agent hamesha madadgar aur tameezdaar rahega.

#### ➤ `Runner.run_sync(...)`:

* Yeh agent ko ek prompt ke sath run karta hai.
* Prompt user ka input hota hai.
* Return hone wala `result` object agent ka detailed response hold karta hai.

---

## 💡 Output Ka Example

```plaintext
Phoolon ki tarah muskuraana zindagi,
Gham mein bhi khush rehna zindagi.
```

Yeh agent ka polite aur creative jawab hai, jo usko diye gaye instructions ke mutabiq diya gaya hai.

---

## 📥 Final Output Access Karna

```python
print(result.final_output)
```

* `result.final_output` mein agent ka final reply hota hai.
* Aap isay print kar sakte ho, store kar sakte ho, ya kisi aur jagah use kar sakte ho.

---

## 🧪 Full Example Code Ek Sath:

```python
!pip install openai-agents

import os
os.environ["OPENAI_API_KEY"] = "sk-..."  # Apni asli key lagayen

from agents import Agent, Runner

agent = Agent(
    name="HelperAgent",
    instructions="Tum ek helpful aur polite assistant ho."
)

result = Runner.run_sync(agent, "Mujhe aik achi Urdu shayari sunao.")
print(result.final_output)
```

---

## 🛠 Aage Ka Plan (Coming Soon)

* Async agents (jo background mein kaam karen)
* Multiple agents mil ke kaam karen
* Custom tools aur memory ka istemal
* Logs aur debugging

---

## 🤝 Contribute Karna Chahte Ho?

Agar aap is tutorial ko improve karna chahte ho ya naye ideas dena chahte ho, toh zaroor fork karo aur pull request bhejo.

---

## 📜 License

Ye tutorial OpenAI SDK ke upar based hai.OpenAI ki official documentation aur terms padhein Zaror parhen.

