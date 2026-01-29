# Multi-Agent Workflow Implementation Plan

We will implement a multi-agent system where different "personae" handle specific parts of the `dev_workflow.md`. Each agent will have a dedicated slash command, specialized rules, and persistent memory.

## Development Team Personae

| Name | Role | Slash Command | Responsibilities |
| :--- | :--- | :--- | :--- |
| **Paula** | Product Owner | `/po` | Product vision, scope, timeline, requirements. |
| **Ian** | Ideation Specialist | `/ideation` | User personas, visual north star, early concepts. |
| **Dani** | Designer | `/design` | Design system, Figma sync, components, UI logic. |
| **Pip** | Prototyper | `/prototype` | Interactive prototypes, user flow validation. |
| **Dex** | Data Architect | `/data` | Database schema, data modeling, API contracts. |
| **Alex** | Solutions Architect | `/architect` | Technical design, stack decisions, implementation plans. |
| **Leo** | Senior Developer | `/dev` | Core coding, structure, logic implementation. |
| **Sara** | QA Engineer | `/qa` | Code review, testing, verification, security audits. |
| **Oscar** | DevOps Engineer | `/ops` | Deployments, infrastructure, monitoring, CI/CD. |
| **Marcus** | Development Manager (Team Lead) | `/team` | Project coordination, team management, process oversight, handoffs. |

## Implementation Details

### Configuration & Rules
- `.agent/rules/rules.md`: Core identity reporting and memory access rules.
- Agent-specific rule files (e.g., `po.md`, `dev.md`) defining their boundaries.

### Workflows (Slash Commands)
- A `.md` workflow file for each command in `.agent/workflows/`.
- Commands: `/po`, `/ideation`, `/design`, `/prototype`, `/data`, `/architect`, `/dev`, `/qa`, `/team`, `/ops`.

### Memory System
- `.agent/memory/`: Persistent memory files for each agent to record context and instructions.

### Artifacts & Documentation
- Every agent has a personalized documentation folder in `doc/[name]/`.
- All implementation plans, technical designs, persona descriptions, and other artifacts are saved in the agent's folder.
- **Development Manager** documentation is stored in `doc/manager/`.

## Identity & Communication Protocol
- **Prefix**: Every agent starts with: `"Hello, I am [Name], your [Role]."`
- **Memory**: Agents check `.agent/memory/[name].md` at the start of any conversation.
- **Documentation**: Agents save work to `doc/[name]/`.
- **Independence**: Agents stay "in character" and defer to the appropriate specialist for out-of-scope tasks.
