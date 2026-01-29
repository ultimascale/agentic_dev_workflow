# Workflow

## General

- **[Best Practices & Clean Code Guidelines](./development_manager/20260121_best_practices/best_practices.md)** (MUST READ)
- User-in-the-loop approach (AI asks for all major decisions, especially for tech stack / architecture options)
- Component-driven workflow (with Storybook)
- Mission control initialization
    - Create .agent/rules dir w/ rules.md

## Phases

- Product Owner
    - Define product vision
    - Define product scope
    - Define product timeline
- Solutions architect
    - Define tech stack (or just changes to it)
    - Define feature architecture
    - Decide on the file structure, libraries, and technologies to use.
    - Create an implementation plan (step-by-step).
    - Output a "Technical Design Document".
- Ideation
    - Create user personas 
    - First designs: Nano Banana
        - **Goal:** Generate a visual north star
    - Uizard? Visily?
- Design
    - Hand over to Figma with plugins:
        - Nano Banana 
        - Relume (Sitemaps / Wireframes)
        - Magician (Icons / Copy)
    - **Goal**: Generate a design system (Colors, Typography, Components)
    - Can later be read using Figma MCP by AI agents to implement designs
- Prototyping
    - Create a click prototype 
- Data architecture
    - Act as a data modeler
    - e.g. create database (Supabase) schema (can be interacted upon with Supabase MCP by AI agents)
- Senior Developer
    - Doing the actual coding
    - Create app structure using output from solutions architect
    - Implement design system
    - Implement data architecture
    - Create a commit to the dev branch
    - Create a pull request to the staging branch
- QA
    - Check the pull request from the Senior Developer
    - Verify that the app from Senior Developer works as expected
    - Code review as gate
    - "Ruthless reviewer" AI agent
    - "Janitor" AI agent periodically cleans repo
    - Autonomous testing
        - Playwright?
    - Security audits
        - Scan code for vulnerabilities
        - Dependabot?
        - Snyk?
    - Output a review summary
    - If everything is fine, merge the pull request to the staging branch
    - If not, ask Senior Developer to fix the issues
- Ops
    - PostHog (User behavior analytics)
    - Sentry
