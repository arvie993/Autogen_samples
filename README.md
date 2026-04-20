# AutoGen Samples

A comprehensive learning progression through Microsoft's [AutoGen](https://github.com/microsoft/autogen) multi-agent framework — from simple chat agents to distributed systems communicating over gRPC.

## Labs

| Lab | Topic | Description |
|-----|-------|-------------|
| [Lab 1](1_lab1_autogen_agentchat.ipynb) | AgentChat Basics | Models, messages, and agents — build an airline assistant with SQLite tools |
| [Lab 2](2_lab2_autogen_agentchat.ipynb) | AgentChat Advanced | Multi-modal messages, structured outputs (Pydantic), LangChain tools, agent teams |
| [Lab 3](3_lab3_autogen_core.ipynb) | AutoGen Core | Lower-level runtime with `RoutedAgent`, `@message_handler`, and local `SingleThreadedAgentRuntime` |
| [Lab 4](4_lab4_autogen_distributed.ipynb) | Distributed Agents | gRPC-based distributed runtime across processes/machines with LangChain tool integration |

## Multi-Agent Idea Generation System

The Python modules implement a distributed idea generation system where agents brainstorm business ideas and refine each other's work:

- **agent.py** — A creative entrepreneur agent that generates Agentic AI business ideas, with a chance of bouncing ideas off peers
- **creator.py** — Dynamically generates new agent personalities from a template and registers them at runtime
- **messages.py** — Message dataclass and agent routing utilities
- **world.py** — Orchestrates 20+ agents in a distributed gRPC runtime

## Tech Stack

- **AutoGen Core / AgentChat / Extensions** — Agent framework, runtimes, message routing
- **OpenAI GPT-4o-mini** — Primary LLM
- **gRPC** — Distributed agent communication
- **LangChain** — Tool integration
- **Pydantic** — Structured outputs
- **SQLite** — Local data storage

## Setup

```bash
pip install autogen-agentchat autogen-ext[openai,docker,langchain] langchain-community
```

Create a `.env` file with your API keys:

```
OPENAI_API_KEY=your-key-here
```

## License

See the root repository for license details.
