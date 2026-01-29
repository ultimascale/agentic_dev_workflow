# Agentic Dev Workflow

## Overview
This repository serves as a showcase and framework for a **Multi-Agent Development Workflow**. It utilizes a team of specialized AI agents, each with distinct personae, responsibilities, and dedicated memory, to simulate a professional software development lifecycle.

The primary goal is to demonstrate how multiple autonomous agents can collaborate effectively to plan, design, implement, and verify complex technical tasks.

## The Team
Our development team consists of 10 specialized roles:

| Member | Role | Responsibilities |
| :--- | :--- | :--- |
| **Paula** | Product Owner | Product vision, scope, timeline, and requirements management. |
| **Ian** | Ideation Specialist | Early concepts, user personas, and visual inspiration. |
| **Dani** | Designer | Design system maintenance, UI components, and aesthetic consistency. |
| **Pip** | Prototyper | Validation of user flows through interactive prototypes. |
| **Dex** | Data Architect | Database schema, data modeling, and API contract design. |
| **Alex** | Solutions Architect | Technical architecture, stack decisions, and implementation planning. |
| **Leo** | Senior Developer | Core coding, logic implementation, and system structure. |
| **Sara** | QA Engineer | Code reviews, testing, security audits, and verification. |
| **Oscar** | DevOps Engineer | CI/CD, infrastructure, deployments, and monitoring. |
| **Marcus** | Development Manager | Team coordination, process oversight, and reporting. |

## How It Works
The workflow is driven by structured interaction and persistent state:

1.  **Specialized Rules**: Each agent operates under a specific set of rules (located in `.agent/rules/`) that define their character and boundaries.
2.  **Persistent Memory**: Agents maintain context across interactions via memory files in `.agent/memory/`.
3.  **Command-Driven Interaction**: Handoffs and role activations are managed via slash commands (e.g., `/dev`, `/architect`, `/team`).
4.  **Structured Documentation**: All significant work is documented in role-specific folders within the `doc/` directory, following a standardized naming convention (`YYYYMMDD_task_name`).

## Development Standards
- **Git Flow**: All active development occurs on the `dev` branch.
- **Verification**: Every change must be verified by the appropriate specialist (e.g., QA review).
- **Aesthetics**: UI-related work prioritizes premium, modern design principles.

## 🚀 Usage / Getting Started

**Prerequisite**: Ensure you have the agentic workflow environment set up.

1.  **Checkout**: Clone this repository to your local machine.
2.  **Define Vision**: To start a new project or feature, use the following slash command to introduce yourself to the Team Lead:
    ```
    @[/team] "I want to build a..." (Describe your project vision)
    ```
3.  **Kickoff**: Marcus (Development Manager) will acknowledge your request, notify the team, and create a `vision.md` file in the root directory to formally document your goals.

---
*This project is managed by the Development Manager (Marcus).*
