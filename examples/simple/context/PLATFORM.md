# Platform Context

**Stack Description**: A lightweight static site setup leveraging simple, universal web standards. NO complex frameworks unless strictly necessary.

## Core Technology Stack

- **Languages**: HTML5, CSS3, Vanilla JavaScript (ES6+)
- **Tooling**: npm (for basic scripts)
- **Backend**: None (pure client-side)
- **Frontend**: Native DOM APIs
- **Database & Storage**: LocalStorage for temporary client state

## Architecture & Patterns

- **Data flow**: Synchronous interactions, mostly semantic HTML rendering
- **Design patterns**: Procedural script execution, modular JS files where reasonable
- **State management**: Minimal client-state (e.g., toggles)
- **System architecture**: Static Site
- **Service communication**: Basic Fetch API for external JSON data if needed

## Infrastructure & Deployment

- **Containerization**: None
- **Environment**: GitHub Pages
- **Secret management**: None required
- **CI/CD pipelines**: GitHub Actions (deploy to gh-pages branch on `main` push)
- **Observability**: Cloudflare analytics

## Third-Party Integrations

- **Payments**: None
- **Authentication**: None
- **AI / LLM Providers**: None
- **Communication**: Basic `mailto:` links or simple Google Forms embedding
