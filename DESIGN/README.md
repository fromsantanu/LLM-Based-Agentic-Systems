# What are Agentic Design Patterns

In the context of **agentic systems** (LLMs, LangChain, LangGraph, n8n, etc.), “design patterns” are reusable ways of structuring agents, workflows, and interactions so they can reliably handle complex tasks.

Here’s a list of **20 commonly used agentic design patterns**:

---

## [**Core Agent Patterns**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/edit/main/DESIGN/p01.md)

1. **Single-Agent Pattern** – One agent handles all tasks (simple Q\&A or retrieval).
2. **Multi-Agent Collaboration** – Multiple agents with specialized roles (e.g., doctor agent + diagnostic agent).
3. **Orchestrator-Worker Pattern** – One orchestrator delegates subtasks to worker agents.
4. **Hierarchical Agent Pattern** – Agents organized in a tree (manager → sub-agents).
5. **Supervisor Pattern** – A monitoring agent oversees outputs and enforces rules.

---

## [**Memory & Context Patterns**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/edit/main/DESIGN/p02.md)

6. **Conversation Memory Pattern** – Agent maintains past dialogue for context.
7. **Scratchpad / Chain-of-Thought Pattern** – Use intermediate reasoning steps before final output.
8. **Long-Term Knowledge Store Pattern** – Agents store facts in vector DBs and recall later.
9. **Role-Play Pattern** – Assign agent a persona/expertise to shape responses.
10. **Stateful Agent Pattern** – Agent carries structured state across steps (diagnosis → treatment → monitoring).

---

## [**Task Execution Patterns**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/edit/main/DESIGN/p03.md)

11. **ReAct (Reason + Act) Pattern** – Agent alternates between reasoning and taking actions/tools.
12. **Plan-and-Execute Pattern** – Agent first drafts a plan, then executes step-by-step.
13. **Toolformer Pattern** – Agent learns when and how to call external APIs/tools.
14. **Reflection / Self-Critique Pattern** – Agent critiques or refines its own answers.
15. **Simulation Pattern** – Run multiple “what-if” scenarios with agents (common in research).

---

## [**Interaction & Workflow Patterns**](https://github.com/fromsantanu/LLM-Based-Agentic-Systems/edit/main/DESIGN/p04.md)

16. **Human-in-the-Loop Pattern** – Agent pauses to ask user for approval or guidance.
17. **Parallel Agent Pattern** – Multiple agents work concurrently on subtasks, results are merged.
18. **Round-Table Debate Pattern** – Several agents argue, and a judge agent decides best answer.
19. **Routing Pattern** – Router agent selects the right expert agent or workflow path.
20. **Recovery / Fallback Pattern** – If one agent fails, another handles exceptions or retries.

---

✅ These patterns are **combinable**—for example, a **Hierarchical + ReAct + Human-in-the-Loop** setup is common in **healthcare assistant workflows** like the one you’re planning.
