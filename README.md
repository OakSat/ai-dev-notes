# 🧠 AI/LLM Cheat Sheet for Developers

Welcome to your all-in-one cheat sheet for working with modern AI tools and Large Language Models (LLMs). Whether you're building automations, writing prompts, or just trying to make sense of all these buzzwords — this guide is for you.

---

## 📦 Foundational Concepts

### 🤖 LLM (Large Language Model)

A language model trained on massive text corpora to understand and generate human-like language.

Examples: GPT-4, LLaMA 3, Claude, Mistral

Use cases:

* Text generation
* Summarization
* Classification
* Code completion

### 🔤 Tokens

LLMs work on **tokens**, which are word pieces (not full words).

* "ChatGPT is awesome" → 4 tokens
* Different models have **token limits** (e.g., 4096, 8192, or 100k+ tokens)
* Token count = input + output → affects cost and context

### ⚙️ Foundation Model

The base model (e.g., GPT-4, LLaMA) trained on general data. Think of it like a pre-trained brain.

You can:

* Use it as-is (zero-shot)
* Prompt it smartly (prompt engineering)
* Fine-tune (custom training)

---

## 🧱 Prompt Engineering (Basics)

* **Zero-shot**: Asking without any example.
* **Few-shot**: Giving examples in the prompt.
* **Chain of Thought (CoT)**: Ask the model to think step by step.
* **Role prompting**: "Act as a cybersecurity analyst..."
* **System messages**: Instructive context for chat-based LLMs

Pro tip: Be specific. Ambiguous prompts = weird answers.

---

## 🔧 Tools & Frameworks

### 🐍 Ollama

A lightweight tool to **run open-source LLMs locally** via Docker or CLI.

* Great for privacy & offline use
* Supports LLaMA 3, Mistral, Gemma, and more
* Simple API: `ollama run llama3 "What's the capital of France?"`

Use it when:

* You want to avoid cloud LLM costs
* You need full control

### 🔗 LangChain

A Python/JS framework to build LLM-powered apps.

* Chains = sequences of calls (e.g., prompt → LLM → tool)
* Supports memory, tools, agents, vector DBs
* Often used with RAG or agents

Use when building:

* Chatbots
* Search tools
* Complex LLM workflows

---

## 🧠 Smart Enhancers

### 📚 RAG (Retrieval-Augmented Generation)

Let the LLM "consult a library" before answering.

* Combines search (from vector DB) + generation
* Keeps answers grounded in *your* data

Use when:

* The model doesn’t know your custom knowledge
* You want up-to-date or domain-specific responses

### 🕵️ LLM Agents

These are goal-oriented LLMs that:

* Plan
* Use tools (like APIs)
* Iterate toward a result

Popular frameworks: LangChain Agents, Autogen, CrewAI

Use when:

* You need the model to take actions (e.g., browse, call APIs)
* Tasks involve multiple steps or reasoning

Avoid when:

* A single prompt is enough — simple > complex!

---

## 🧬 Model Customization

### 🧪 Fine-Tuning

Custom training on your own data to make the model:

* Better at a task (e.g., medical diagnosis)
* Match a tone/style

Requires:

* Labeled examples
* Time + compute + patience

As a dev, use it **only if**:

* Prompting/RAG isn't enough
* You have domain-specific data

### 🧠 MCP (Multi-Context Prompting)

Inject **multiple perspectives** or **context sets** into a single LLM session.

* Think: one LLM sees multiple documents or scenarios

Use when:

* You want richer output with layered context
* You're working with conflicting or varied info

---

## 🎓 Bonus Buzzwords

* **Vibe Coding**: Coding alongside an LLM by just describing what you need. Less structured, more exploratory.
* **Tokenizers**: Tools that break text into tokens. Different models = different tokenizers.
* **Embedding models**: Convert text into vectors for similarity search (used in RAG)
* **Vector DBs**: Store embeddings for fast retrieval (e.g., Chroma, Pinecone, Weaviate)
* **Open-source models**: Mistral, Gemma, LLaMA — can be run locally!

---

## 📘 TL;DR (Too Long; Do Run)

* Want quick answers? Use prompts.
* Want accurate answers from private data? Use RAG.
* Want to automate decisions or tool use? Try LLM agents.
* Want to own the model? Use Ollama.
* Want to build smart pipelines? Use LangChain.
* Want to *really* teach the model? Fine-tune it.

---

## 🧩 Contributions Welcome

Have a better way to explain "token limits" or a cool Ollama tip? PRs are open!

---

## 🧑‍💻 About the Author

Created by [Alon Shabat](https://alonshabat.com).

---

License: MIT
