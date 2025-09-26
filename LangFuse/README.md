# **LangFuse Tutorial Topics for Agentic AI Applications**

## 1. [**Getting Started with LangFuse**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/LangFuse/p01.md.md)

* Introduction: What is LangFuse and why it matters in Agentic AI
* Installing & setting up LangFuse (cloud and self-hosted options)
* Core concepts: Traces, Spans, Metrics, Evaluations, Feedback
* Connecting LangFuse with LangChain / LangGraph

---

## 2. [**Instrumentation Basics**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/LangFuse/p02.md.md)

* Logging LLM calls with LangFuse
* Capturing inputs, outputs, and intermediate reasoning steps
* Adding metadata (user ID, session, application state)
* Visualizing traces in the LangFuse dashboard

---

## 3. [**Agentic AI Context**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/LangFuse/p03.md.md)

* Role of observability in Agentic AI workflows
* Tracing hierarchical agents (Coordinator → Sub-agents → Tools)
* Recording multi-step reasoning (e.g., triage → diagnosis → plan generation)
* Debugging failures and edge cases in autonomous workflows

---

## 4. [**Integrating LangFuse with Frameworks**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/LangFuse/p04.md.md)

* LangChain integration (`@traceable` decorator, callbacks)
* LangGraph integration (capturing state transitions)
* Direct Python SDK instrumentation (for custom agents)
* Using LangFuse with FastAPI / Streamlit for interactive apps

---

## 5. [**Evaluation & Quality Monitoring**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/LangFuse/p05.md.md)

* Human-in-the-loop feedback collection in LangFuse
* Automatic evaluations (factuality, relevance, coherence)
* Tracking hallucinations and failure modes
* Setting up evaluation pipelines with custom scoring functions

---

## 6. [**Analytics & Metrics**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/LangFuse/p06.md.md)

* Understanding latency, token usage, and cost monitoring
* Aggregating metrics per agent or workflow
* Measuring agent success rates (task completion, handoffs)
* Setting up dashboards and alerts

---

## 7. [**Debugging & Iteration**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/LangFuse/p07.md.md)

* Identifying bottlenecks in reasoning
* Debugging failed tool calls or API integrations
* Replaying past traces for iterative improvement
* Versioning and comparing multiple agent strategies

---

## 8. [**Advanced Patterns**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/LangFuse/p08.md.md)

* Observability for RAG pipelines (document retrieval + grounding)
* Tracking autonomous decision-making with guardrails
* Capturing multi-modal agent interactions (text, image, speech)
* Privacy and data governance in logging sensitive data

---

## 9. [**Deployment & Scaling**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/LangFuse/p09.md.md)

* Configuring LangFuse for production environments
* Setting up monitoring for high-volume agent traffic
* Best practices for scalable observability
* Integrating with external APM/monitoring tools (Prometheus, Grafana)

---

## 10. [**Case Studies & Hands-On Projects**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/blob/main/LangFuse/p10.md.md)

* Tracing a healthcare triage agent
* Debugging a multi-step research assistant
* Monitoring a customer support automation system
* Setting up continuous evaluation for an educational tutor agent

---

