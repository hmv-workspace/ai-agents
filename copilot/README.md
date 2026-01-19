# GitHub Copilot Custom Agents

A collection of specialized AI agents for GitHub Copilot designed to enhance your development workflow with expert assistance in coding and software architecture.

## 🤖 Agents

### Architect-Assistant (`.github/agents/architect.assistant.md`)
Focus: architecture decisions and lightweight documentation.

Responsibilities:
- Clarify requirements and constraints (ask questions when unclear)
- Break down architecture work into manageable plans
- Document and track progress in:
  - `.github/requirements.md` (owned by Architect-Assistant)
  - `.github/architecture.md` (owned by Architect-Assistant)

Hard constraints:
- Does **not** change code
- Does **not** create other docs unless explicitly instructed
- Avoids assumptions (especially on performance/security/maintainability) without confirmation

### Developer-Assistant (`.github/agents/developer.assistant.md`)
Focus: implementation help under developer control.

Responsibilities:
- Code suggestions, debugging help, reviews, small incremental changes
- Validate changes step-by-step (developer runs/tests)
- Document and track progress in:
  - `.github/implementation.md` (owned by Developer-Assistant)
  - `.github/deployment.md` (owned by Developer-Assistant)

Hard constraints:
- Does **not** change architecture/design without explicit direction
- Does **not** create other docs unless explicitly instructed
- Avoids assumptions; asks clarifying questions when requirements are unclear

## Handoffs (when to switch agents)
- Use **Architect-Assistant** when you need design decisions, requirements clarification, or architecture documentation.
- Use **Developer-Assistant** when you need coding help, fixes, tests, or deployment/implementation documentation updates.
- Developer-Assistant can hand off to Architect-Assistant for “Architecture Review / Validation Review / Stakeholder Review”.

## Model
Both agents are intended to be used with **GPT-5.2**.

### Installation

1. Clone this repository:
```bash
git clone https://github.com/yourusername/copilot-custom-agents.git
cd copilot-custom-agents
```

2. Create the agents directory structure in your VS Code project:
```bash
cd your-project-folder
mkdir -p .github/agents
```

3. Copy the agent files to the agents directory:
```bash
cp path/to/copilot-custom-agents/architect.assistant.md .github/agents/
cp path/to/copilot-custom-agents/developer.assistant.md .github/agents/
```

Your project structure should look like this:
```
your-project/
├── .github/
│   └── agents/
│       ├── code.agent.md
│       └── architect.agent.md
├── src/
└── ...
```

4. Restart VS Code to ensure GitHub Copilot recognizes the custom agents

## 📖 Usage

### Using the Developer Assistant
Invoke the developer when you need assistance with implementation details, code quality, or debugging. The agent will provide contextual suggestions based on your current code.

### Using the Architect Assistant
Engage the architect when making design decisions, planning system architecture, or evaluating technical approaches. It helps ensure your solutions are scalable and maintainable.

## 📝 Examples

Include specific examples of how these agents have helped in real scenarios:
- Refactoring legacy code with the Developer Assistant
- Designing microservices architecture with the Architect Assistant
- Optimizing database queries and API endpoints

## 🙏 Acknowledgments

- GitHub Copilot team for the amazing AI coding assistant
- The developer community for feedback and suggestions

---

**Note**: These agents are designed to augment your development process, not replace human judgment and expertise. Always review and validate AI-generated suggestions.
