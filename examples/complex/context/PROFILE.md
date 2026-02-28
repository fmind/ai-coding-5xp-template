# Profile Context

**Persona**: Lead Full-Stack E-commerce Engineer.

## Persona & Background

- **Professional background**: Staff-level engineer leading a globally distributed e-commerce team.
- **Project role**: Architect and core contributor for the ActiveGear platform.
- **Industry context**: High-traffic B2C sports retail platform handling flash sales and real-time inventory sync.

## Technical Expertise

- **Strong areas**: Frontend performance (Next.js, React), backend architecture (Python Django, PostgreSQL), distributed systems.
- **Weak areas**: Intricate CSS animations, complex ML product recommendation algorithms.
- **Learning goals**: Enhancing Rust knowledge for background inventory workers; exploring edge computing.

## Communication Preferences

- **Decision making**: Lay out the top two options with distinct architectural trade-offs. I'll make the final call.
- **Tone & voice**: Extremely direct, zero fluff. No apologies when throwing errors. Do not explain basic concepts.
- **Answer format**: Start with the root cause and the fix immediately, followed by the code snippet.

## Development Philosophy

- **Trade-offs**: Fast page loads and immediate time-to-interactive over complex client-side state. Strict typing everywhere.
- **Core principles**: "Explicit over implicit." No magic frameworks. Predictable, deterministic behavior during checkout.
- **Risk tolerance**: Absolute zero risk for the core payment flow; moderate for frontend UI features behind feature flags.

## AI Interaction Rules

- **Autonomy**: Do not write the full implementation immediately if it touches >3 files. Give me a design doc first.
- **Verification**: If you add a database migration, also write the corresponding revert script.
- **Focus**: Stay exactly on topic. No unsolicited "best practice" advice unless explicitly requested.
