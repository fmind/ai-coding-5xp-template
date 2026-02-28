# Coding Standards

**Repository**: `activegear-core`
**Language**: Python 3.12+ (Backend) / TypeScript 5+ (Frontend)

## General Principles

- **Readability**: Code is read vastly more often than it is written. Optimize for the reader.
- **Fail Fast**: Catch errors at compile/type-check time rather than runtime.
- **YAGNI**: "You aren't gonna need it." Do not over-engineer solutions for hypothetical future requirements.
- **DRY**: "Don't repeat yourself." Extract common logic into reusable components or functions.

## Type Safety

- **Strict Typing for Currency**: All monetary values must be represented using the `Decimal` type on the backend or specialized currency libraries. Never use floats for prices.
- **No `Any`**: The use of `any` in TypeScript or `Any` in Python is strictly prohibited unless explicitly approved in code review.
- **Domain Modeling**: Favor strong domain models (e.g., `UserId`, `OrderId`) over primitive obsession (e.g., passing raw strings everywhere).

## Error Handling

- **Explicit Returns**: Functions should return specific `Result` or `Either` types rather than throwing exceptions whenever possible.
- **Unified Format**: All API error responses must adhere to the `Problem Details for HTTP APIs (RFC 7807)` standard.
- **Logging context**: Always include relevant context (e.g., `cart_id`, `user_id`) when logging errors, but never log PII (Personally Identifiable Information).

## State Management (Frontend)

- **Cart State**: Shopping cart state is highly volatile. Synchronize it with the backend aggressively, but optimistically update the client UI for a snappy feel.
- **Server State vs. Client State**: Prefer storing data on the server (using libraries like React Query or SWR for caching) rather than keeping a massive Redux store.

## Database Access

- **ORM Usage**: Use the ORM for simple CRUD operations, but drop down to raw SQL (via safe query builders) for complex reporting queries to prevent N+1 issues.
- **Migrations**: Database migrations must be forward-only and non-destructive. If a column needs renaming, add the new one, copy data, and deprecate the old one.
