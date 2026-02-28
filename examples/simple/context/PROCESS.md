# Process Context

**Workflow**: Fast iteration, directly inside the `main` branch. No PR reviews required for this solo project.

## UI / UX Guidelines

- **Styling approach**: Tailwind CSS (via CDN or simple PostCSS config)
- **Component library**: None, custom utility classes
- **Design tokens**: Dark mode by default, high contrast text
- **Accessibility (a11y)**: ARIA labels on interactive elements
- **Responsiveness**: Mobile-first layout, functional on varying screen sizes

## Quality Assurance

- **Testing approach**: Manual testing across viewports
- **Coverage goals**: N/A
- **Linting strategy**: Run Prettier before committing
- **Type safety**: Vanilla JS (Dynamic typing)

## Development Workflow

- **Commit rules**: Write clear, descriptive commit messages
- **Issue tracking**: None
- **Version control**: Trunk-based development straight to `main`
- **Code review**: Self-review only

## Code Standards & Conventions

- **Code formatting**: Prettier (default settings)
- **Directory structure**: Flat structure (`index.html`, `styles.css`, `script.js`)
- **Documentation**: Inline comments for complex logic
- **Naming conventions**: camelCase for JS variables, kebab-case for CSS classes
