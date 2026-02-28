# AI Coding 5xP Template

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](http://makeapullrequest.com)

**[The 5xP Framework: Steering AI Coding Agents from Chaos to Success](https://medium.com/@fmind/the-5xp-framework-steering-ai-coding-agents-from-chaos-to-success-83fbdb318b2b)**

Welcome to the **AI Coding 5xP Template**! This repository is a boilerplate and reference guide demonstrating the **5xP Context Framework**—a brutally simple and highly maintainable directory structure designed to keep AI coding agents (like Gemini, Copilot, Cline, or Antigravity) perfectly aligned with your architectural goals.

If you are tired of rewriting the same context prompts over and over, or struggling with your agent hallucinating tools you don't use, this framework is your solution.

---

## What is Context Engineering?

AI Coding Agents are incredibly powerful at parsing documentation and writing logic, but they lack _common sense_. They don't inherently know who they are working for, the exact tools you prefer, or your specific business constraints.

**Context Engineering** is the practice of systematically providing AI agents with the foundational knowledge they need to make the right decisions autonomously. Instead of managing the AI micro-step by micro-step, you provide a solid environment (context), and the AI builds within those boundaries.

## The 5xP Framework Explained

The 5xP Framework organizes your project context into 5 "pillars" using flat, readable Markdown files to give the AI the exact context it needs on day one.

1. **Profile**: Who is directing the AI? (Persona, your skill level, and communication preferences).
2. **Product**: What are we building and why? (Target audience, value proposition, business logic, and success criteria). Note: Specific features are intentionally omitted and should be developed conversationally with the AI.
3. **Platform**: What is the technical stack? (Languages, frameworks, databases, and infrastructure requirements).
4. **Process**: How do we work? (Development workflows, testing standards, UX guidelines, and CI/CD).
5. **Principle**: The core tenets and strict rules the AI must follow. These are embedded directly in the master prompt for maximum visibility.

---

## Repository Structure

The core mechanism of the 5xP framework relies on the `AGENTS.md` file at the root of your project, which acts as the **Master Prompt**. This file lists your core principles and links to the context files in the `context/` directory. By doing so, the AI agent can lazy-load exactly the information it needs, when it needs it.

```text
├── src/
├── tests/
├── context/               <-- The 5xP Context Files
│   ├── PROFILE.md
│   ├── PRODUCT.md
│   ├── PLATFORM.md
│   └── PROCESS.md
└── AGENTS.md              <-- The Master Prompt (Principle)
```

_(Note: For larger, more complex scale projects, the context files can be split into subdirectories like `context/product/`, `context/platform/`, etc.)_

---

## Examples

We provide multiple examples to demonstrate how the framework scales from a simple weekend project to a massive enterprise application.

### [Simple Example](examples/simple/)

Ideal for lightweight projects, personal portfolios, or freelance gigs. Includes a single flat `context/` folder.
Check out [`examples/simple/`](examples/simple/) for a dummy Personal Frontend Portfolio project.

### [Complex Example](examples/complex/)

Ideal for large, nested projects like enterprise applications or product suites. Includes nested context folders (`context/product/`, `context/platform/`, `context/process/`).
Check out [`examples/complex/`](examples/complex/) for a full fictional open-source e-commerce platform called **ActiveGear**.

---

## Getting Started

This repository is designed as a **GitHub Template**. Implementing the 5xP framework in your project is straightforward:

1. Click the **[Use this template](https://github.com/fmind/ai-coding-5xp-template/generate)** button at the top of the repository, or clone it directly.
2. Review the [`examples/`](examples/) directory to see which structure fits your use case best (Simple vs. Complex).
3. Copy the root `AGENTS.md` and `context/` structure from your chosen example into your project's root directory.
4. **Customize** the files to match your exact project rules, persona, and stack.
5. Point your AI Coding Agent to read `AGENTS.md` at the start of your sessions.

---

## Contributing

**Contributions are absolutely welcome!** The goal of this repository is to reach a wide audience and standardize the best practices of Context Engineering for AI Coding Agents.

If you have ideas to improve the framework, add new examples, or refine the existing context templates, please get involved:

1. **Open an Issue**: Share your ideas, report bugs, or discuss new context engineering patterns.
2. **Submit a Pull Request**: Feel free to submit PRs for typos, template improvements, or new examples.
3. **Share Your Experience**: Let us know how the 5xP framework has improved your AI coding workflows!

## License

This project is licensed under the [MIT License](LICENSE).
