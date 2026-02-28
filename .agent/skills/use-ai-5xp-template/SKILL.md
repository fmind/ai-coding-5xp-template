---
name: use-ai-5xp-template
description: Apply the AI Coding 5xP Template framework to the project.
---

# Use AI 5xP Template

This skill helps AI Coding agents quickly initialize and adopt the [5xP Context Framework](https://github.com/fmind/ai-coding-5xp-template).

## Instructions

1. **Determine Template Type**: Ask the user whether the project needs the `simple` (flat context) or `complex` (nested context) 5xP structure.
2. **Copy Structure**: Copy the root `AGENTS.md` and the appropriate `context/` directory from this template to the target project.
3. **Customize Context**: Prompt the user to fill out or automatically generate the initial boilerplate for `PRODUCT.md`, `PLATFORM.md`, `PROCESS.md`, `PROFILE.md`, and `PRINCIPLES.md` based on their specific project needs.

## Suggested Additional Skills

To further enhance an agentic workflow, consider adding these skills to your `.agent/skills/` directory.

Here are 3 examples of generic skills you could add:

- **`write-documentation`**: A skill that instructs the agent on how to write clear, concise, and well-structured markdown documentation for your project.
- **`create-bash-script`**: A skill that helps the agent write, test, and document Bash scripts following best practices for error handling.
- **`refactor-code`**: A skill that provides guidelines for the agent to refactor code into clean, modular, and testable components.
