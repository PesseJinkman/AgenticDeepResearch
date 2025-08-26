# Agentic Deep Research

AgenticDeepResearch is a **multi-agent research framework** designed for orchestrating autonomous research agents with flexible supervision, scoped reasoning, and prompt-driven workflows. It supports modular agents, state management, and multi-agent supervision for complex research tasks.

---

## Features

- **Research Agents**: Modular agent implementations for different research tasks (`research_agent.py`, `research_agent_scope.py`, `research_agent_full.py`, `research_agent_mcp.py`).
- **Multi-Agent Supervision**: Supervisor to coordinate multiple agents (`multi_agent_supervisor.py`, `state_multi_agent_supervisor.py`).
- **Scoped Reasoning**: Fine-grained control of research scope and state tracking (`state_scope.py`, `state_research.py`).
- **Prompt Management**: Centralized prompts for guiding agents (`prompts.py`).
- **Utility Functions**: Reusable helper functions (`utils.py`).
- **Extensible**: Easy to add new agents or supervisory mechanisms.

---

## Project Structure

```
AgenticDeepResearch/
│── research_agent.py             # Core research agent
│── research_agent_scope.py       # Scoped research agent
│── research_agent_full.py        # Full research pipeline agent
│── research_agent_mcp.py         # MCP-integrated agent
│── multi_agent_supervisor.py     # Supervisor orchestrating multiple agents
│── state_multi_agent_supervisor.py # Supervisor state management
│── state_research.py             # Research state management
│── state_scope.py                # Scope state tracking
│── prompts.py                    # Prompt templates
│── utils.py                      # Utility functions
│── files/                        # Supporting data/files
│── __init__.py                   # Package initialization
```

---

## Installation

```bash
git clone https://github.com/yourusername/AgenticDeepResearch.git
cd AgenticDeepResearch
pip install -r requirements.txt
```

*(If no `requirements.txt` exists, list dependencies manually here — e.g. `openai`, `langchain`, `pydantic`, etc.)*

---

## Usage

### Example: Running a Research Agent
```python
from AgenticDeepResearch.research_agent import ResearchAgent

agent = ResearchAgent()
result = agent.run("What are the latest advances in quantum computing?")
print(result)
```

### Example: Using Multi-Agent Supervisor
```python
from AgenticDeepResearch.multi_agent_supervisor import MultiAgentSupervisor

supervisor = MultiAgentSupervisor()
results = supervisor.coordinate("Summarize breakthroughs in AI safety")
print(results)
```

---

## Roadmap

- Integrate vector databases for long-term memory.
- Expand supervisor policies (hierarchical, consensus-based).
- Add benchmarking tools for agent performance.
- Support for external APIs (arXiv, Semantic Scholar, etc.).

---

## Contributing

Contributions are welcome! Open an issue or submit a pull request.

---

